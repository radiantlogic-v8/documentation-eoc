---
title: Role-based Permissions
description: Learn about the default roles in Environment Operations Center - Tenant Admin, Tenant Admin Read-Only, Tenant User, Environment Creator, Environment Admin, and Environment User - and about custom roles.
---
# Role-based permissions

The operations a user can perform and what they can view in Environment Operations Center depend on their assigned role. Environment Operations Center includes six default roles: Tenant Admin, Tenant Admin Read-Only, Tenant User, Environment Creator, Environment Admin, and Environment User. Tenant admins can also create custom roles on the **Roles** tab of the *Admin* screen. This guide outlines the permissions for each default role.

The following table summarizes the permissions for each default role:

| Role | Environments | Users |
| ---- | ------------ | ----- |
| [Tenant Admin](#tenant-administrator) | View and edit all environments | View and edit all users |
| [Tenant Admin Read-Only](#tenant-admin-read-only) | View all environments | View all users |
| [Environment Creator](#environment-creator) | View and edit assigned environments, and create new ones | View and edit their own details only |
| [Environment Admin](#environment-administrator) | View and edit assigned environments | View and edit their own details only |
| [Environment User](#environment-user) | View assigned environments | View and edit their own details only |
| [Tenant User](#tenant-user) | Minimal environment access | – |

## Tenant administrator

A Tenant Administrator is granted permission to access all possible operations and views for all of the organization's environments. A Tenant Administrator can view and edit all environments and users, and can edit their own user details.

From the Environment Operations Center home page, the Tenant Administrator can view and access operations for all of the organization's environments.

## Tenant Admin Read-Only

A Tenant Admin Read-Only user is granted permission to access all possible views for all of the organization's environments. A user with this role can view all environments and users, but can not edit any of those details.

From the Environment Operations Center home page, the Tenant Admin Read-Only user can view all of the organization's environments.

## Environment administrator

An Environment Administrator has access only to the environments they have been assigned to. Within those environments, an Environment Administrator can add applications and has read, write, and delete permissions.

An Environment Administrator cannot:

- Create new environments.
- Create Secure Data Connector groups or connectors.
- Use promotion pipelines or reporting, because both are tied to environments.

From the Environment Operations Center home page, the Environment Administrator can view and access operations only for the environments they have been assigned to.

## Environment creator

An Environment creator is granted permission to access all operations and views for the environments they have been assigned to. In addition to managing existing environments, they can also create and manage new environments. They cannot view or edit environments that have not been assigned to them. 

## Environment user

An Environment User has read-only access to the environments they have been assigned to and cannot create, delete, or perform other actions on them. Certain administrative functions are hidden, such as editing other users or updating environment authentication.

From the Environment Operations Center home page, the Environment User can view all of the environments they have been assigned to. An Environment User cannot perform operations on the environment and the  **Delete** button is disabled in the **Options** (**...**) drop down menu.

## Tenant User

A Tenant User is a standard user within the tenant with minimal environment access.

## Custom roles

In addition to the default roles, tenant admins can create custom roles with their own permissions. To create one, open the *Admin* screen, select the **Roles** tab, and select **New Role**. See the [admin overview](../admin/admin-overview.md#roles).

## Next steps

After reading this guide you should have an understanding of the different role assignments in Environment Operations Center and their permissions within the application. For details on user management, see the guides to [create a user](../admin/user-management/create-user.md) or [edit a user](../admin/user-management/edit-user.md).
