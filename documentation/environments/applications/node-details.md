---
keywords:
title: Update and monitor environment nodes
description: Learn how to adjust the number of nodes in a RadiantOne cluster and to monitor the status details of a specific node.
---
# Update and monitor environment nodes

A "node" refers to an individual service configured within a RadiantOne cluster. When multiple nodes are present, a load balancer automatically distributes workloads across them. Each customer’s tenant in the Environment Operations Center is allocated a specific number of nodes based on their license plan. The number of nodes can be scaled up or down within your environment, and the total number of nodes allowed is shared across all environments.

This guide describes how to adjust the number of nodes in an environment and to monitor the status details of a specific node. The *Overview* tab provides a high-level view of all FID node statuses for quick monitoring of cluster health. Each individual node has a detailed view that provides further information on the status and health of a given node.

## Adjust number of nodes

To set the number of FID nodes contained in an environment, select the  **Scale** option under *Application Details*.

![image description](images/select-scale.png)

In the *Adjust Application Scale* dialog, use the slider to increase or decrease the quantity. Alternatively, you can select either the minus (**-**) or plus (**+**) sign on either side of the slider to increase or decrease the number of nodes to display.

By default the scale reflects the number of nodes at the current state. Adjust the scale to required number of nodes.

![image description](images/adjust-scale.png)

Click **UPDATE** to confirm your selection.

![image description](images/scale-confirmation.png)

A message indicates that application scaling is in process. After the process completes, the number of nodes in the application changes to match your selection.

![image description](images/increased-nodes-new.png)

## View node details

There are two ways to access the status details for a specific node: select the node name to open node details or select the **Options**(**...**) menu.

![image details](images/select-node-name.png)

### FID node details

The FID node details dialog provides the following information for the selected node:

| Node Details | Definition |
| ------------ | ---------- |
| Name | The name assigned to the specific FID node. |
| Status | Indicates if the node is operational, experiencing a partial outage, or experiencing a full outage. Displays as "Healthy", "Warning", or "Outage". |
| Cloud ID | The unique ID of the node within the cluster of an environment. |
| Version | The environment version number. |
| Health | The status of the CPU and quantity used of memory and disk space. |
| Disk Latency | The node performance. |
| Up Time | How long the application has been running. |
| Services | Lists the internal ports and their statuses. |

![image description](images/node-details.png)

## View node logs

Each node has associated log files that contain further information about the node's health and status alerts. The log files for a specific node can be accessed from the node details dialog or from the **Options** (**...**) drop-down of a node.

To access log files from a node's details dialog, select **View Logs** in the dialog.

Select **Close** to exit the node details dialog.

![image description](images/details-view-logs.png)

Alternatively, the log files of a node can be accessed by selecting **View Logs** from the associated **Options** (**menu**).

![image description](images/options-view-logs.png)

## Next steps

After reviewing this guide, you should have an understanding of how to review the status and health of specific FID nodes. For information on reviewing environment logs, see [application logs](logging/application-logs.md).
