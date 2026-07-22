---
keywords:
title: Account Settings
description: Learn how to view and update your account settings and manage your API tokens. Users can generate API tokens for applications that are required to connect to Environment Operations Center without logging in.
---
# Account Settings

This guide provides an overview of how to update your account settings and manage your API tokens. Users can generate API tokens for applications that are required to connect to Environment Operations Center without logging in.

## Getting started

From any section or tab in Environment Operations Center, your account avatar will be visible in the upper right corner of the screen. To access your account settings, select the avatar icon to expand the account dropdown menu. From the dropdown menu, select **Account Settings** to open the *Account Settings* screen.

![image description](images/account-settings.png)

## Account settings

From the *Account Settings* screen you can update your user details including your first name, last name, email address associated with the account, email address to receive notifications and your profile image.

### Update user details

To update your first or last name, enter your information in the spaces provided and select **Save** to update.

> [!note] Only administrators can update email addresses. Please contact your administrator if you need to change the email associated with your Environment Operations Center account.

To update your profile image, select "Edit Avatar" and select an image from you local file system to upload.

![image description](images/account-details.png)

## Manage API tokens

API tokens let applications connect to Environment Operations Center without signing in, and are available to every user, regardless of role, under Account Settings. You need a valid token to call Environment Operations Center endpoints; a request without one returns 401 Unauthorized. You can create up to five tokens in the Environment Operations Center. 

Each token is unique to the user who creates it and is scoped to that user's access. For example, an environment user's token returns data only for that user's assigned environments. Using a token beyond its scope returns an unauthorized error.

![The Account Token panel with the token counter, the New API Token form, and existing tokens](images/api-tokens.jpg)

### Create an API token

To create a new API token, set the API expiration by selecting one of the **Expires In** radio buttons. Then select **Generate** to generate a new API token. A unique API token will populate in the *API token* input field.

![image description](images/generate-token.png)

A unique API token will populate in the *API token* input field and the creation and expiration dates will display below the token. Copy the token immediately and store in a safe place.

> [!warning] Once you leave the page, you can no longer view or copy the API token. Ensure you copy the token before saving.

![image description](images/created-copy.png)

You will receive a warning when your API token is close to expiring. A warning is displayed in your *Account Settings* next to the *Expiration Date* dropdown.
> [!warning] API token expiry cannot be extended. Once a token has expired, a new token must be generated.

The token list shows each token you have created, along with:

- **Status** — **Active** or **Expired**.
- **Creation date** and **expiration date**.
- **Last used** — when the token was most recently used.

### Delete an API token

Only one API token can be created at a time. If you need to create a new API token but one already exists, you must first delete the current token.

You can delete the API token by selecting the trash bin icon (![image description](images/icon-delete.png)) located next to the *API Token* input field.

> [!warning] Deleting an API token is a permanent action and cannot be undone.

![image description](images/delete-token.png)

A confirmation message will appear to verify that you would like to delete the API token and reminding you that a new API token will need to be generated for future calls. Select **Confirm** to delete the token.

If the token is successfully deleted you will receive a confirmation message and the *API token* field will be empty. You can proceed to generate a new token or exit out of *Account Settings* without generating a new token by selecting **Save**.

## Next steps

After reading this guide you should have an understanding of how to update your account settings and manage your API tokens. For details on managing Environment Operations Center users, see the [create a new user](../../admin/user-management/create-user.md) or [edit an existing user](../../admin/user-management/edit-user.md) guides.
