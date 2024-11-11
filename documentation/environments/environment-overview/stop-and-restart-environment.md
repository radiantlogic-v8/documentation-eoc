---
keywords:
title: Stop and restart an Application
description: Learn how to stop and restart an application in Environment Operations Center.
---
# Stop an Application

This guide outlines the required steps to stop an application while on the *Environments* home screen in Environment Operations Center.

> [!note] Only non-production applications can be stopped by users. To stop a production application, please contact Radiant Logic.

## Select the application

From the *environment* home screen, locate the application you would like to stop from the list of applications. Go the specific application and, on the right top corner, click on the power icon.

![image description](Media/power-icon.png)

From the list of options elect **STOP** to stop the application.

> [!note] When an application is stopped, no data is lost. The application can be started back to the state before it was stopped.

![image description](Media/power-icon-stop.png)

A pop up appears asking to confirm Stopping the application, click **CONFIRM** to stop the application, or click **CANCEL** to cancel the operation.

![image description](Media/power-icon-stop-confirmation.png)

In the upper-right corner of the application overview page, a message indicates the application is being stopped.

![image description](Media/stopping-env-message.png)

![image description](Media/stopping-application.png)

When the application is successfully stopped, the status on the overview page changes to **OFFLINE**.

![image description](Media/offline.png)

![image description](Media/offline1.png)

![image description](Media/offline2.png)

## Start application

> [!note] Starting an application is only available when an application has been created and stopped.

To start the selected application, click the power icon in the upper-right corner of the *Overview* page.

![image description](Media/power-icon2.png)

From the options under power, click **Start**.

![image description](Media/start.png)

A message prompts you to confirm the **Start application**. Click **Confirm** to start the application, or to go back click **Cancel**.

![image description](Media/start-confirm.png)

A "Starting application" message displays on the application *Overview* page.

![image description](Media/starting-env.png)

![image description](Media/starting-env1.png)

![image description](Media/starting-env2.png)

> [!note] The process of starting an application may take up to 10 minutes.

## Confirmation

After a successful restart of the application, status of the application turns to **OPERATIONAL** on the application *Overview* page.

![image description](Media/operational-message.png)

![image description](Media/operational-message1.png)
