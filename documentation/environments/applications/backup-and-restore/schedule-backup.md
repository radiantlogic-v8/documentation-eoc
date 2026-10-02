---
keywords:
title: Schedule Automatic Application Backups
description: Learn how to schedule automatic backups of applications in Environment Operations Center.
---

# Schedule automatic application backups

This guide explains how to schedule automatic backups for an application. For details on creating backups manually, see the [create a backup](create-backup.md) guide.

## Getting started

Select an application in your environment and open its **Backups** tab.

Select the gear icon (![image description](Media/gear-icon.png)) next to the *Scheduled* status to open the *Backup Settings* screen.

## Backup settings

The *Backup Settings* screen has three sections: **Automatic Backups**, **Data retention policy**, and **Schedule**.

### Automatic backups

To turn on scheduled backups, switch the **Enabled** toggle from **Inactive** to **Active**.

### Data retention policy

The data retention policy deletes backup runs older than the period you select. Select **10 Days**, **20 Days**, **30 Days**, or **60 Days** from the **Retention Period** dropdown. The default is 30 days.

### Schedule

Use the **Schedule** section to set when the backup runs:

- **Timezone** shows the time zone the schedule uses.
- **Backup Frequency**: select **Daily**, **Weekly**, or **Monthly**.
- **Every**: for daily backups, select how often the backup runs: every **2**, **4**, **8**, **12**, or **24 hours**.
- **Starting On**: for weekly and monthly backups, select the day the backup runs.
- **At**: select the time the backup starts.

Below the fields, Environment Operations Center summarizes the schedule in words, shows the date and time of the next backup, and shows the schedule as a cron expression. Check the summary, then select **Save** to save the schedule, or **Cancel** to discard your changes.

## Confirmation

After you save the backup settings, Environment Operations Center returns you to the *Backups* tab and shows a confirmation message. The *Scheduled* status now shows the frequency and time of the scheduled backup and when the next backup runs.

If Environment Operations Center cannot save the schedule, an error message appears. Close the message and try again.

## Next steps

You can now schedule automatic backups. To restore a new application from a backup, see [advanced setup](../applications-overview.md#advanced-setup). To restore an existing application from a backup, see [restore a backup](backup-restore-overview.md#restore-a-backup).
