---
title: Creating Environments
description: Learn how to create environments and deploy applications.
---

# Overview

This guide walks you through the steps required to create a new environment and deploy applications in Environment Operations Center.

An environment is where a RadiantOne product lives. Each environment is completely isolated and contains endpoints to access different applications. Each instance of the Environment Operations Center has a predefined number of production and non-production environments that can be created for production, development, quality assurance, and staging purposes.

## Getting started

Before setting up your environment, you need the following:

- The version number that corresponds with your RadiantOne product (Identity Data Management, Identity Analytics, and/or Identity Data Platform).
- If you are deploying the Identity Data Management application, and want to initialize the product with configuration that has been exported from an existing environment, ensure you have the correct file type saved and ready to go since you need to select this file during creation of the new environment.

The new environment setup requires you to define the environment type, details, and provides an optional step to upload a configuration file from another environment.

## Creating environments

To create a new environment, select **New Environment** on the *Environments* home screen or from the *Overview* home screen.

This takes you to the *New Environment* page that contains all the input fields for the information required to create a new environment. The following sections outline more details about these fields.

### Define environment details

Start by filling out the **Environment Details** section.

#### Type

To set the **Type**, use the radio buttons to select either **NonProduction**, for development and testing, or **Production**, for production purposes.

#### Name

In the **Name** field, enter a unique name. The name can be up to 5 characters long.

#### Infrastructure

From the **Infrastructure** dropdown, select the infrastructure to deploy the environment on. Each infrastructure is tied to a cloud provider, for example an AWS-based or Azure-based infrastructure, and is configured by Radiant Logic during onboarding.

#### Description

Optionally, enter a description of the environment in the **Description** field. The description can be up to 255 characters long.

### Ephemeral environments

An ephemeral environment is a temporary environment that deletes itself at a time you set. When you turn on the **Ephemeral** toggle during environment creation, select the calendar icon to set the date and time when the environment expires. A message below the field confirms when the environment and its applications will be deleted. Environment Operations Center deletes the environment automatically when that time arrives, even if you forget to remove it, so unused environments do not continue to consume resources.

If you add an ephemeral environment to a promotion pipeline, it loses its ephemeral property and becomes a regular environment.

> Ephemeral environments are feature-flagged. If the feature is not enabled for your account, the option does not appear. Contact Radiant Logic to enable it.

### Deploy applications

In your environment, you can install one or more of the following RadiantLogic applications:

* **Identity Data Management** – This application streamlines identity data by eliminating silos and ensuring seamless synchronization across your organization. It serves as a scalable, unified source of truth, helping to manage and maintain accurate, up-to-date identity information.

* **Identity Analytics** – This application offers deep insights into potential gaps in your identity data, particularly in relation to access management workflows. It enhances visibility, enabling you to identify and address blind spots, while strengthening your organization’s overall identity security posture.

* **Identity Data Platform** (previously known as Identity Observability) – Provides observability services for your identity data including AI agents' data. You may request additional services such as extra storage, Portal API, and MCP features to be enabled for this application during application creation.

To deploy an application, select the checkbox adjacent to the application name. In the expanded view, fill out all required information.

Applications that are not part of your subscription are shown greyed out and labelled *Not in current subscription*, and you cannot select them. For example, Identity Data Platform is greyed out if it is not included in your subscription.

#### Application details

Under the **Application Details** section, provide the required details such as the application version, password, and application description. The **Nodes** row at the top of each application's section shows how many of that application's subscription nodes are already in use, for example *0 of 3 used*.

There are minor differences in the application details form for each application. For Identity Data Management deployment, you have the option to enable advanced setup if you wish to deploy the application using an existing configuration file. Note that this option is available only in Identity Data Management.

![image description](Media/iddm-details.png)

![image description](Media/ida-details.png)

For Identity Analytics and Identity Data Platform, the form also asks for a setup email address. Enter the address in **Setup Email Address** and repeat it in **Confirm Setup Email Address**, or select **Auto-fill** to populate both fields with the email address of the signed-in account.

#### Version

To set the application **Version**, select the version drop down to display all available versions. Select the value that corresponds with your organization's version of Environment Operations Center.

#### Password

Enter a password in the **Create Password** field, or select **Generate** to have a password automatically generated for you. The password must meet the following requirements:

- At least 16 characters
- Both lowercase and uppercase letters
- At least 1 number
- At least 1 special character, excluding `' " / \ € £ ; : & “ ” ‘ ’`

A strength bar below the field shows how strong the password is as you type.

To confirm your password, reenter it in the **Confirm Password** field. If you selected to have a password automatically generated, use the copy icon to the right of the field to copy it, then paste it into the confirmation field.

![image description](Media/password.png)

To reveal your original or confirmation password, select the eye icon (![image description](Media/eye-icon.png)) located within the text field you wish to view.

### Advanced setup

Each application's details end with an **Options** section that contains optional toggles. Identity Data Management and Identity Analytics include **Install Samples**, which imports sample data. Identity Data Management also includes **Advanced Setup**.

Advanced setup is not required. It can be used to restore an Identity Data Management application from an existing backup file. When creating a new application, choose the backup configuration (ZIP file) that was downloaded from the environment you want to restore.

#### Custom configuration

To import a configuration file, select the configuration ZIP file to upload. You can locate the file on your system and drag and drop it into the provided space. Alternatively, you can select **choose file** within the upload box to open your system's file manager and locate the file to upload.

While your file is uploading, an **Uploading** message displays in the file upload box, along with a progress bar. You can cancel the file upload while it is in progress by selecting the **X** located in the progress bar box.

Once your configuration file has successfully loaded, the file name displays in place of the file upload box. Select **Create** to create the new environment.

To delete the file and return to the file upload screen, select the trash can icon located in the same box as the successful file upload.

If the file upload is not successful, the configuration upload box displays with a red dashed outline and an error message appears just below. Review your file type to ensure you have selected the correct configuration file for upload and try again.

### Create the new environment

Once you have completed filling out the *Environment Details* and *Application Details* sections, click the **Create** button to create the new environment.

## New environment confirmation

After saving the New Environment details form, a confirmation message appears noting that your environment is being created and that the process can take up to twenty minutes.

![image description](Media/creating2.png)

Once the environment has been successfully created, the environment's status changes to "Operational".

If there is an error and the environment cannot be created, the environment status changes to "Creation Failed".

Select the ellipsis (**...**) in line with the environment to display a list of options. Options include:

- **Submit Again**: resubmit the same form without editing any of the fields.
- **View Logs**: troubleshoot where the error may have occurred while the form data was processing.
- **Delete**: if the environment hasn't been successfully created, delete the failed instance.

## Next steps

Learn how to view [application details](../applications/application-details.md), [update an application](../applications/update-an-application.md) and [delete an environment](delete-environment.md). 

