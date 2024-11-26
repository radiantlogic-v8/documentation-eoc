---
keywords:
title: Authentication
description: This guide provides information about configuring SSO with various OIDC providers in the Environment Operations Center. 
---


## Authentication (draft)
This guide provides information about configuring SSO with various OIDC providers in the Environment Operations Center. 

### **Prerequisites:**
2. **Admin Access** - You will need administrative privileges to configure SSO and authentication providers.
3. **SSO Provider Details** - Obtain the necessary OIDC details and credentials from your Identity Provider, such as Redirect URL, Authorization Endpoint URL, Token Endpoint URL

### **Steps to Configure SSO in EOC:**

#### **1. Navigate to the Admin screen**
   - In EOC, navigate to the **Admin** screen and click **Authentication**.

#### **2. Provide required details related to your OIDC provider**
  1. PROVIDER NAME
  * This is the name of your OpenID Connect provider. It can be any name you choose to identify the provider (e.g., "MyOIDCProvider").
  2. DISCOVERY URL
  * The discovery URL is the endpoint from which the OIDC provider's metadata is retrieved. This URL typically ends with /.well-known/openid-configuration (e.g., https://example.com/.well-known/openid-configuration). This URL provides essential information like the authorization and token endpoints, supported scopes, and other configuration details.
  3. REDIRECT URL
  * This is the URL to which the OIDC provider will redirect users to, after successful authentication. It must match one of the redirect URIs registered in the OIDC provider's settings (e.g., https://yourapp.com/callback).
  4. AUTHORIZATION ENDPOINT URL
  * This is the endpoint the client will use to initiate the OAuth2 authorization code flow. It typically looks like https://example.com/authorize.
  5. TOKEN ENDPOINT URL
  * This is the URL where the client can exchange the authorization code for an access token and ID token. It typically looks like https://example.com/token.
  6. CLIENT ID
  * This is the unique identifier assigned to your application by the OIDC provider when you register it. The provider will issue this ID to identify your application.
  7. CLIENT SECRET
  * This is the secret associated with your client ID. It is used to authenticate your application when exchanging authorization codes for tokens. Make sure to keep it secure.
  8. EMAIL SCOPE
  * The scope is a parameter that defines the level of access the application needs. For email-related information, the email scope is commonly used. It requests the OIDC provider to return the user's email address.

#### **7. Configure EOC MFA (Optional)**
   - **Attribute Mapping:** Depending on the SSO protocol, you may need to map user attributes from the IdP to EOC user attributes. For example, map the IdP's `email` attribute to EOC’s `email` field.
   - **Role Mapping (if applicable):** For systems that support role-based access, you may also need to map IdP roles to EOC roles, allowing users to access the correct resources after logging in.

#### **8. Save the Provider Configuration**
   - After entering all the details and verifying the settings, click on the **Save** or **Create** button to save your provider configuration.

#### **9. Enable SSO for Users**
   - Once the provider is created, you may need to enable it for specific users or groups. This can be done through the **User Management** section in EOC.
   - Assign the provider to the appropriate user groups and specify the conditions for automatic login.


### **Conclusion**
By following the steps above, you can successfully set up and configure **SSO (Single Sign-On)** using **EOC's authentication provider** page. Once set up, this configuration will allow users to log into Environment Operations Center via your chosen OIDC provider. This removes the need to remember additional credentials for accessing EOC, improving security and user experience.

If you encounter any issues, it’s helpful to consult the official Radiant Logic documentation or reach out to support for troubleshooting assistance.

