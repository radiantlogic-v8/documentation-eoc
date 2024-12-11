---
keywords:
title: Environments Overview
description: Learn how to navigate the Environments page and view environment details in Environment Operations Center, and understand the topics accessible in the options menu.
---
# Environments overview

This guide provides an overview of the *Environments* home screen and its features. To navigate to the *Environments* home screen, select **Environments** in the left navigation.

![image description](Media/select-envs.png)

The *Environments* home screen provides an overview of all your organization's available environments. Each environment provides information about installed application(s).

Two environment display views are available, either list- or grid-view. In the list-view, environments are organized by row with the associated environment details contained in the row.

![image description](Media/envs-list-view.png)

In the grid-view, environments are organized in a card format with associated details for an environment contained within the card.

![image description](Media/envs-grid-view.png)

Each environment has its own **Options** menu (**...**) that allows you to either add an application or delete the environment. 

In the list-view, the options menu is located at the end of an environment row.

![image description](Media/options-list.png)

In the grid-view, the options menu is located in the upper corner of an environment card.

![image description](Media/options-grid.png)

A **Search** bar at the top of the *Environments* screen can be used to filter the listed environments. Enter an environment name, specific characters, or words in the space provided to quickly filter through the environments.

![image description](Media/search-to-filter.png)

A refresh button is located in the upper right corner of the *Environments* screen. Select the refresh icon to pull up to date information about the environments.

![image description](Media/refresh-envs.png)


### New environment

The **New Environment** button allows you to quickly start creating a new environment from the home screen. For details on how to create a new environment, review the guide on [creating a new environment](create-environments.md).

### Applications

In your environment, you can install one or both of the following RadiantLogic applications:

* **Identity Data Management** – This application streamlines identity data by eliminating silos and ensuring seamless synchronization across your organization. It serves as a scalable, unified source of truth, helping to manage and maintain accurate, up-to-date identity information.

* **Identity Data Analytics** – This application offers deep insights into potential gaps in your identity data, particularly in relation to access management workflows. It enhances visibility, enabling you to identify and address blind spots, while strengthening your organization’s overall identity security posture.

Refer to the [applications-overview](../applications/applications-overview.md) guide for additional details on the installation steps. 


## Access permissions

Depending on your [role](../../role-based-permission/role-based-permissions.md), your administrator may set your access permissions to read-only for certain environments. If you have read-only access:

- You will not be able to create new environments and the **New Environment** button will be deactivated.
- Certain environments will be hidden if you have not been assigned either read-only or editing permissions.
- You will not be able to edit or update the environments that you have read-only access to and the **Options** menu (**...**) will no longer be visible next to the environment. You can still view the details for these environments by selecting the environment name to navigate to their respective "Overview" screens.
- An administrator can assign editing permission to you for specific environments. This allows you to edit, update, or delete the environments they have specified, while others remain hidden or read-only.

## Next steps

After reading this guide you should have an understanding of how to navigate the *Environments* home screen and its main features. To begin setting up a new environment, review the documentation on [creating a new environment](create-environments.md).
