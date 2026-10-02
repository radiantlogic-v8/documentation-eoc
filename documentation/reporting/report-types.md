---
keywords:
title: Types of Reports
description: Learn about Access Reports available in Environment Operations Center that can be used to monitor activities and the overall health of your environments.
---
# Types of Reports

This guide outlines the types of reports available in Environment Operations Center for you to monitor activities and the overall health of your environments.

A report is generated from a dashboard. When you build a report, you select the dashboard to include, the period it covers, and the environment it applies to, and Environment Operations Center renders that dashboard as a PDF on the schedule you set. The report types available to you are therefore the dashboards available for your applications. For the steps to build one, see the [reporting overview](reporting-overview.md).

The same dashboards are also available to view directly, from the [Dashboards](../dashboards/dashboards-overview.md) screen and from the **Monitoring** tab of an application.

## Available dashboards

The dashboards offered depend on the application you select.

### Identity Data Management

| Dashboard | Description |
| --------- | ----------- |
| IDDM Dashboard | Health and activity metrics for a selected node, including CPU, memory, disk, and file descriptor usage, leader and ZooKeeper status, HDAP store count and size, up time, operation count, live connections, and peak values. |
| Audit Report | Client access activity drawn from the access logs, including operation counts by type, connections by host, and result codes. |

### Identity Analytics

| Dashboard | Description |
| --------- | ----------- |
| IDA Dashboard | Health and activity metrics for the Identity Analytics application. |

### Identity Data Platform

| Dashboard | Description |
| --------- | ----------- |
| IDO - Portal Dashboards | Activity and health for the Identity Data Platform portal. |
| IDO - Observations - Channels contention | Contention across observation channels. |
| IDO - Observations - Functional | Functional observation results. |
| IDO - Observations - Process | Observation processing activity. |
| IDO - Observations - Timings | Timing measurements for observations. |
| IDO - Alert center | Alerts raised by the Identity Data Platform application. |
| IDO - Graph Database | Health and activity of the graph database. |
| IDO - ID Sync Config | Identity synchronization configuration. |
| IDO - System | System health of the Identity Data Platform application. |
| IDO - Writeback service | Activity of the writeback service. |
| IDO Graph Pipeline Sink | Activity of the graph pipeline sink. |

> The dashboards available to you depend on the applications installed in the environment and on your subscription. If an application is not installed, its dashboards do not appear.

## Access reports

The **Audit Report** dashboard is built from the access logs. Information provided by these logs includes client requests to RadiantOne and the responses. The report outlines how long operations run and provides a summary of associated error codes.

### Operation types

The types of operations included in the access data are:

- connections:
- bind: LDAP bind (authentication) requests received by RadiantOne.
- search: Search (base search, one level search, sub-tree search) requests received by RadiantOne.
- add: Add entry requests received by RadiantOne.
- modify: Update entry requests received by RadiantOne.
- compare: Compare requests received by RadiantOne.
- delete: Delete requests received by RadiantOne.

### Standard report details

The access data covers the following details for all operation types:

- response time interval: how long the operation took to complete (in milliseconds)
- response time threshold: any operation that exceeds a specified response time.
- error codes: specified error codes to track
- date: 
- session ID
- connection ID
- operation ID

### Unique report details

Details that are unique to each operation type include:

| Operation | Details |
| --------- | ------- |
| Bind | Bind DN (user the operation was issued by). |
| Base Search | Base DN (entry that was searched for) and the filter. |
| One Level Search | Base DN (entry where the one level search started from) and the filter. |
| Sub Tree Search | Base DN (entry where the sub tree search started from) and the filter. |
| Add | The Entry (DN) to be added. |
| Modify | The object (entry to be modified) and the modification details. |
| Delete | The Entry (DN) to be deleted. |
| Compare | Information about the compare operation. |

## Next steps

You should now have an understanding of the types of reports available in Environment Operations Center and the activity data they provide. For further information on accessing reports, see the [reporting overview](reporting-overview.md) guide.
