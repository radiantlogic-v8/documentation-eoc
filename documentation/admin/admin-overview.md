---
keywords:
title: Admin Overview
description: Learn more about the administrative functions that can be performed in the Environment Operations Center. This includes how you can access tabs to manage your account settings, Environment Operation Center users, environment alerts and integrations, and monitor cluster health.
---
# Admin Overview

This guide provides an overview of the *Admin* home screen and its features. From the *Admin* screen, you can access tabs to manage your account settings, Environment Operation Center users, environment alerts and integrations, and monitor cluster health.

All Env Ops Center users can access the *Admin* screen, but view and edit permissions differ depending on a user's assigned role. For details on role-based permissions, see the [role-based permissions](role-based-permission/role-based-permissions.md) guide.

## Getting started

To navigate to the *Admin* screen, select **Admin** (![image description](images/icon-admin.png)) located at the bottom of the left navigation.

![image description](images/admin.png)

![image description](images/admin2.png)

## Top navigation

A navigation bar is located at the top of the *Admin* home screen and is visible from all tabs in the *Admin* view. The top navigation allows you to access several account and user management tools through the following tabs:

- Users
- Integration
- Events
- Tasks
- Authentication
- Settings

![image description](images/top-nav.png)

### Users

The *Users* tab allows you to manage all users within your Environment Operation Center instance. From here you can view a user's name, email address, and status.

For details on managing Environment Operation Center users, including their roles and permissions, see the [user management](user-management/create-user.md) guide.

![image description](images/users-tab.png)

### Integration

From the *Integrations* page you can manage your connections to external applications to send alerts from Environment Operations Center. The *Integrations* tab displays the integration "Label", indicating the integrations purpose, and the "Integration", indicating the external application the integration is connected to.

For details on managing integrations, see the [managing integrations](integrations/manage-integrations.md) guide.

![image description](images/integration-tab.png)

### Event

The *Event* page provides an overview of all create, update, and delete activities performed for all environments, including the action, environment, date and time stamp of the activity, and the user who performed the activity.

![image description](images/activity-log-tab.png)

### Tasks

From the *Tasks* page, you can view information on the following EOC tasks.

- Create application
- Delete application
- Restart application
- Scale application
- Start application
- Stop application
- Update application
- Create backup
- Update backup settings
- Create environment
- Delete environment
- Enable endpoint
- Disable endpoint

Information on these tasks includes the environment and application the tasks was performed on, the task's start and end times, and the task's status. The search bar in the upper-left corner allows you to display tasks for specified environments. 

![image description](images/tasks.png)

### Authentication

The *Authentication* page provies an overview of all authentication providers. To add an authentication provider, click **New Provider**. 

![image description](images/authentication.png)

### Settings

The **Settings** page provides options to setup release channels and automatic/manual update checks for the channel. It also allows you to configure a OIDC provider and enable multi-factor authentication. 

![image description](images/settings-tab.png)

## Next steps

After reading this guide you should be able to navigate the *Admin* home screen and understand its main features including the top navigation. For details on updating your account settings, review the [account settings](account-settings/update-account.md) guide. To learn how to create a new user, review the [create a new user](user-management/create-user.md) guide.
