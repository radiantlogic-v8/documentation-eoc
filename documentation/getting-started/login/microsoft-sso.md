---
keywords:
title: Microsoft SSO
description: This Guide provides the information about configuring the SSO for Microsoft in Microsoft and setting up Microsoft SSO authentication in the Environment Operations Center. 
---

# Microsoft SSO

This guide explains how to configure Microsoft Single Sign-On (SSO) using Microsoft Entra ID. By default, Radiant Logic offers a “Sign in with Microsoft” option. If you choose this method, when you click the Sign in with Microsoft button, you’ll be prompted to grant admin approval for the Environment Operations Center (EOC). Once an administrator authorizes access, you can log in using the Microsoft sign-in option.

![menu](images/approval-request.png)

Alternatively, if you prefer to configure Microsoft authentication on your own, follow the steps listed in this guide. 



## Registering your application in Entra ID 

This section describes how to establish your application as a recognized entity in Azure AD to facilitate secure interactions. 
1. Using an administrative account, log into the Entra ID (previously known as Azure AD) portal.
2. In the navigation pane on the left, select **App registrations**.
    ![menu](images/app-registrations.png)
3. At the top of the page, click **New Registration**.
4. Enter a descriptive name that helps identify the application within your organization.
    ![form](images/register-application.png)
5. In the Supported Account Types section, select one of the following options.
    - **Single Tenant:** limits access to users within the organization.
    - **Multitenant:** allows users from any Azure AD directory to access the application.
6. From the Select A Platform drop-down menu, select **Web**.
7. Next to the Select A Platform menu, specify a URI to which Azure AD will send authentication responses.
8. Click **Register**.
9. Make note of the Application ID for future reference.

## Creating a secret for authentication

This section describes how to generate a secret key that your application uses to authenticate itself with Azure AD.

1. In the Azure AD portal, navigate to **Manage > Certificates & Secrets**.
    ![menu](images/certificates-secrets.png)
2. On the Client Secret tab, click **New Client Secret**. An "Add a Client Secret" window displays.
    ![form](images/add-client-secret.png)
3. Provide a meaningful description for the secret, i.e. "Production Key 2024".
4. Select an option from the **Expires** drop-down menu.
5. Note the value displayed on the Client Secrets tab.
    ![result](images/client-secrets.png)

## Assigning API permissions

This section describes how to specify which resources your application can access and which actions it can perform in Azure AD.

1. In the Azure AD Portal, navigate to **Manage > API Permissions**.
    ![menu](images/api-permissions.png)
2. Click **Add a Permission**.
3. Select an API and click **Delegated Permissions**.
    ![form](images/request-api-permissions.png)
4. Add permissions as needed.
    > [!warning] These permissions must align with the functionality your application requires.
5. To apply these permissions across all users in your directory, click **Grant admin consent for [your directory]"**.
6. Click **Yes**.
    ![result](images/configured-permissions.png)

## Testing your implementation

The section describes how to integrate and verify that SSO via Azure AD is functioning correctly in your application.

1. In your application authentication settings, input the Application (Client) ID and the Client Secret.
2. Configure the authentication library or framework you are using (such as Microsoft's Identity platform libraries) to interact with Azure AD using these credentials.
3. Implement a login feature where users are redirected to Azure AD for authentication.
4. Verify that after successful authentication, Entra ID redirects users back to your application's specified redirect URI.
    > [!note] Your application should handle this response to authenticate the user internally.
5. After implementation, monitor the integration closely for any performance issues or errors.
6. Review logs and user feedback to identify and troubleshoot any potential problems in the SSO process. 

For the latest information on these steps, refer to [Microsoft's OIDC document](https://learn.microsoft.com/en-us/entra/identity-platform/v2-protocols-oidc). 

## Enable Microsoft SSO authentication in Environment Operations Center

After configuring OIDC with Microsoft Entra ID, you will need to enable this SSO option in Radiant Logic's Environment Operations Center by following these steps:
1. Click on the Admin option at the bottom of the left navigation bar.
2. Click Authentication and click New Provider.
3. In the OpenID Connector form, provide details for the OIDC Provider.

    i. Select Microsoft as the OIDC PROVIDER. Next, you will see that PROVIDER NAME, DISCOVERY URL, REDIRECT URL, AUTHORIZATION ENDPOINT URL, TOKEN ENDPOINT URL, and EMAIL SCOPE fields get auto-populated.

   ii. Enter the CLIENT ID and CLIENT SECRET that was generated in your Azure application.

   iii. Optionally, you can enable EOC MFA. If you enable EOC MFA, upon logging in, the user will be see a prompt to set up MFA with an authenticator app. Complete the prompt to enable MFA.

   ![form](images/OIDC-form.png)

## User-Side Configuration (External Organization)

When you add a user from an external organization to EOC — for example, adding `jane@contoso.com` while your EOC is registered under `radiantlogic.com`, additional configuration may be needed on the user's side.

The steps depend on the external organization's security posture. There are three scenarios, from simplest to most restrictive which are explained below.

### How It Works

When an external user clicks "Sign in with Microsoft" on EOC:

```
User clicks "Sign in with Microsoft"
    │
    ▼
Entra ID checks: Is this app known to the user's tenant?
    │
    ├── YES (Service Principal exists) → Sign in proceeds
    │
    └── NO (First-time access) → Consent required
            │
            ├── User consent allowed? → User approves → Service Principal created → Sign in proceeds
            │
            └── User consent blocked? → "Admin approval required" error
                    │
                    └── Admin must grant consent (see Scenario 2 or 3)
```

> **Key concept — Service Principal:** When an external user (or their admin) consents to your app, Entra ID creates a *Service Principal* in their tenant. Think of it as a local reference card for your app in their directory. It is what allows their admins to manage access, assign users, and apply their own security policies to your app. Without this Service Principal, the login cannot work.

### Scenario 1: Default Entra ID Settings (No Action Required)

This applies when the external organization uses default Entra ID settings and has not restricted user consent or cross-tenant access.

**What happens:**

1. You add the user's email (e.g., `jane@contoso.com`) in EOC.
2. The user clicks "Sign in with Microsoft" on EOC's login page.
3. Entra ID redirects them to their organization's sign-in page.
4. After authentication, Entra ID shows a **consent prompt**:
   > *"RadiantLogic EOC wants to: Sign you in and read your profile"*
5. The user clicks **Accept**.
6. A Service Principal is created in their tenant automatically.
7. The user is signed in to EOC.

**External admin action:** None required.

**Subsequent logins:** The user signs in directly and no consent prompt appears again.

> This scenario works when your app only requests basic permissions (`openid`, `profile`, `email`, `User.Read`) and the external org hasn't changed the default consent settings.


### Scenario 2: Admin Consent Required (Most Enterprises)

This scenario is applicable when the external organization has disabled user consent in their Entra ID. This is standard practice at most regulated enterprises and large organizations.

When the user attempts to login to EOC, instead of a consent prompt, the user gets an error:

`"AADSTS65001: The user or administrator has not consented to use the application. Need admin approval."`

To resolve this issue, follow these steps:

1. Share the Admin Consent URL.

You (the EOC admin) will need to provide the external org's IT admin with an **admin consent URL**. Construct it as follows:

```
https://login.microsoftonline.com/{external-org-domain}/adminconsent?client_id={your-app-client-id}
```

**Example:**
```
https://login.microsoftonline.com/contoso.com/adminconsent?client_id=a1b2c3d4-e5f6-7890-abcd-ef1234567890
```

Alternatively, if the admin knows their tenant ID:

```
https://login.microsoftonline.com/{external-org-tenantID}/adminconsent?client_id={your-app-client-id}
```

**Example:**

```
https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db47/adminconsent?client_id=a1b2c3d4-e5f6-7890-abcd-ef1234567890
```

2. After the exteranl IT team's admin approves the access using the Admin Consent URL, the application gets registered in their tenant. Following this, users from their tenant who are assigned to EOC can login in successfully.



