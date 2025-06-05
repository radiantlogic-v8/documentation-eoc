---
keywords:
title: Overview
description: Overview of EOC
---
# Getting started

Environment Operations Center allows you to control your RadiantOne implementation in a cloud environment. It provides all of the required tools to:
 
1. Create and manage RadiantOne [environments](../environments/environment-overview/environments.md) where you can install and manage RadiantOne applications in your environments. 

2. [Securely connect with on-premises data ](../secure-data-connector/configure-sdc-service.md). Note that this feature is currently supported in Identity Data Management applications only.

3. Observe usage and issues with [reporting](../reporting/reporting-overview.md), [monitoring](../monitoring/monitoring-overview.md), [logging](../environments/applications/logging/application-logs.md), and [alerting](../environments/applications/alerting/alert-management-overview.md) dashboards.

4. [Administrate](../admin/admin-overview.md) account settings, users, environment alerts and integrations depending on the user role.  

5. Customize the homepage with widgets and relevant links.  

This guide provides an overview of the Environment Operations Center home screen and how to navigate the user interface of this screen.

## Overview
After logging in to the Environment Operations Center, the *Overview* screen appears. This is the Environment Operations Center home screen. It provides access to Radiant Logic quick links, application status and so on. You can customize the displayed layout of the screen. 

A navigation bar is located to the left and is visible from all screens within Environment Operation Center. You can access your account settings by selecting the avatar in the upper right corner, also visible from all screens in the application. If you are an admin, you can access admin settings by selecting the admin icon in the bottom left corner of the page. 

### Account settings

A user avatar is always located in the upper right corner of the Environment Operations Center user interface. Select the avatar to expand your account dropdown menu. 

![image description](Media/profile-icon.png)

The dropdown displays your name, email, and permissions associated with the account. From the dropdown menu you can navigate to your **Account Settings**, access the **Help** center, or **Logout** of Environment Operations Center.

For information on managing your account settings, see the [account settings](../account-settings/update-account.md) guide.


### Quick links

By default, the Quick Links section contains guides and resources to help you with your work in RadiantOne and Environment Operations Center. An admin can add or remove links to display relevant content in this section by using the **Add links** and **Manage links** options. 

![image description](Media/documentation-link.png)

### Application status 

The *Application Status* section on the *Overview* screen allows you to quickly preview your available environments and see the count of applications in various status — Operational, Offline, Critical, and Warning.

![image description](Media/env-section.png)

The **New Environment** button lets you create a new environment whereas the **Go to Environments** links takes you to the Environments page. 

### Subscriptions

The **Subscriptions** section shows the number of used nodes and available nodes in an application. 


### What's new

The **What's new** section shows Radiant Logic's latest infographics, webinars, press releases and live events. 

### Custom widgets

At the bottom right of the screen, you will see a customization icon as shown in the image below.

![image description](Media/custom-widget.png)

By clicking on it, you can change the layout of the home screen, add another widget to the screen or delete any existing widget. Once you perform any of these actions, click **Save** to save the changes in the layout or **Cancel** to cancel those changes. 

 ![image description](Media/customize.png)


### Left navigation

The left navigation contains links to various screens, providing access to the following Environment Operation Center features:

![image description](Media/left-nav.png)

- Overview: To navigate to the *Overview* screen, select either **Overview** or the Radiant Logic logo.

- Environments: The main *Environments* screen provides an overview of all the environments you have access to. Select **Environments** to navigate to the *Environments* overview. To learn more about the *Environments* section, see the [environments overview](../environments/environment-overview/environments.md) guide.

- Secure data connectors: You can manage connections to on-premise data connectors in the *Secure Data Connectors* section. Select **Secure Data Connectors** to navigate to the *Secure Data Connectors* screen. For details on managing data connections, see the [secure data connectors](../secure-data-connector/configure-sdc-service.md) guide. This feature is currently available only in the Identity Data Management application.

- Observe: The Observe section contains navigation items for [Reporting](../reporting/reporting-overview.md), [Monitoring](../monitoring/monitoring-overview.md), [Logging](../environments/applications/logging/application-logs.md), and [Alerting](../environments/applications/alerting/alert-management-overview.md) dashboards.

- Admin: From the *Admin* section you can perform various administrative actions in Environment Operations Center. Select **Admin** to navigate to the *Admin* home screen. For further details on operations available in the *Admin* section, see the [admin overview](../admin/admin-overview.md) guide.

### Scheduled maintenance notice

Periodically, you may see a scheduled maintenance notice at the top of the home screen. This serves to inform you about upcoming maintenance that could affect the applications in your Environment Operations Center. You may also receive email notifications ahead of the maintenance.

 ![image description](Media/schedule-maintenance-notice.png)

After you click on the "Know more" link and confirm you've read it by clicking on the "I acknowledge this notification" checkbox, the alert will be removed from the landing page.

You can also view additional information about maintenance schedules and updates by navigating to Admin > Settings > Scheduled Maintenance Settings page. 

 ![An image of schedule maintenance settings page](Media/schedule-maintenance-settings.png)

#### Configure email recipients list

By default, scheduled maintenance notification emails are sent to account administrators. You can customize this list by adding additional recipients by following these steps:

1. Create an [email integration](././admin/integrations/manage-integrations/#integration-type) and include all the desired recipient email addresses.

 ![An image of email integration page](Media/emailint.png) 
 
2. Go to Admin > Settings > Scheduled Maintenance Settings.

 ![An image of scheduled maintenance email settings](Media/emailsettings.png) 

4. Under the Notifications section, select the email integration you just created.

5. Save your changes. 

## Next steps

After reading this guide you should have an understanding of the *Overview* screen components and how to navigate the Environment Operations Center user interface. To learn about role-based permissions that different users have, see the [role-based permissions](../role-based-permission/role-based-permissions.md) guide. To learn how to create an environment, see the [create an environment](../environments/environment-overview/create-environments.md) guide.
