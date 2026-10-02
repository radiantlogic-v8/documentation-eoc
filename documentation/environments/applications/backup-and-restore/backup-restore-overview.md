---
keywords:
title: Backup Overview
description: Get a quick introduction to backing up applications in Environment Operations Center.
---
# Backup Overview

In Environment Operations Center, you create and restore backups of your applications' configuration. Backups are available for Identity Data Management and Identity Analytics applications. You manage backups from the *Backups* tab in each application's detailed view. This guide describes the *Backups* tab and its features.

## Getting started

To open the *Backups* tab for an application, select **Backups** in the top navigation of the application's detailed view.

The *Backups* tab lists all backups of the application, newest first.

## Review backups

The *Backups* tab lists each backup with its name, creation date, version, and size. Select a column heading to sort the list, and use the **Search for Backups** bar to find a backup by name. Use the controls below the list to set how many backups appear per page and to move between pages.

Next to the search bar, the *Scheduled* status shows whether automatic backups are enabled. When they are, it shows the frequency and time of the scheduled backup and when the next backup runs. When they are not, it reads *Scheduled: disabled*.

For more information on scheduling backups, see the [schedule backups](schedule-backup.md) guide.

## Manage backups

Select **Backup** to create a backup manually. Backup names can be up to 20 characters. To schedule automatic backups, select the gear icon next to the *Scheduled* status.

For details on creating backups manually, see the [create a backup](create-backup.md) guide. For details on scheduling automatic backups, see the [schedule a backup](schedule-backup.md) guide.

## Restore a backup

Each backup has an **Options** (**...**) menu with **Download**, **Restore**, and **Delete**.

To restore an existing Identity Data Management or Identity Analytics application from a backup, select **Restore** from the backup's **Options** (**...**) menu, then confirm in the dialog. After a few minutes, Environment Operations Center restores the application to the backed-up version.

**Delete** permanently deletes the backup.

**Download** saves the backup's configuration file to your computer. This option is available only for Identity Data Management applications.

To use a backup in a new Identity Data Management application, select **Download** from the backup's **Options** (**...**) menu. Then create a new Identity Data Management application and upload the downloaded file, as described in [custom configuration](../applications-overview.md#custom-configuration). If you restore the backup in a new environment, the application's [endpoint URLs](../endpoints-overview.md) differ from those of the original application.  

<!-- The workflow to restore a backup can also be initiated by selecting the **Restore** button. For more information on restoring backups, see the [restore a backup](restore-backup.md) guide.

![image description](images/restore-button.png) -->

## Read-only mode

If you have read-only access to the environment, you can still view the list of backups and the backup schedule, but you cannot create or modify backups.

The gear icon and the **Backup** button are deactivated, and the **Options** (**...**) menu for each backup is hidden.

## Next steps

You can now navigate the *Backups* tab and use its main features. To create a backup, see [create a backup](create-backup.md).
