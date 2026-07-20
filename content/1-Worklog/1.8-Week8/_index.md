---
title: "Week 8 Worklog"
date: 2026-06-08
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Week 8 Objectives
* Monitor VPC network traffic using VPC Flow Logs and analyze flow records.
* Delegate billing console access safely for cost visibility and shared account management.
* Manage AWS service limits and quotas through Service Quotas.
* Track and analyze spend with Cost and Usage Management tools.
* Automate EBS snapshots with the Data Lifecycle Manager (DLM).
* Detect unusual backup activity with anomaly detection for EBS backups.
* Continue developing the internship project.

### Tasks carried out this week
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | Network Monitoring with VPC Flow Logs:<br>- Enable VPC Flow Logs on a VPC or subnet.<br>- Send logs to CloudWatch Logs or S3 and review accepted/rejected traffic.<br>- Use flow records to troubleshoot connectivity and security group rules. | 03/06/2026 | 03/06/2026 | Amazon VPC Flow Logs User Guide |
| 3 | Billing Console Delegation:<br>- Configure IAM policies for billing and cost management access.<br>- Delegate billing console visibility to a trusted user or role.<br>- Verify least-privilege access to invoices, budgets, and payment methods. | 04/06/2026 | 04/06/2026 | AWS Billing and Cost Management |
| 4 | Managing Quotas with Service Quotas:<br>- View default and applied quotas for key services (EC2, VPC, Lambda, â€¦).<br>- Request quota increases where needed for project workloads.<br>- Monitor quota utilization to avoid deployment failures. | 05/06/2026 | 05/06/2026 | AWS Service Quotas User Guide |
| 5 | Cost and Usage Management:<br>- Explore Cost Explorer and cost allocation tags.<br>- Review usage reports and identify top cost drivers.<br>- Align spending visibility with budgets and optimization goals. | 06/06/2026 | 06/06/2026 | AWS Cost Management Documentation |
| 6 | EBS backup automation and project progress:<br>- Create DLM lifecycle policies for automated EBS snapshots.<br>- Configure anomaly detection for EBS backup patterns.<br>- Continue building and iterating on the internship project. | 07/06/2026 | 08/06/2026 | Amazon EBS / Data Lifecycle Manager |

### Week 8 Achievements

**Knowledge**
* Understood how VPC Flow Logs capture IP traffic and support network troubleshooting.
* Learned billing delegation patterns and IAM boundaries for financial console access.
* Understood Service Quotas as the central place to view limits and request increases.
* Reinforced cost visibility practices with usage reports, tags, and Cost Explorer.
* Learned EBS snapshot automation with DLM and backup anomaly detection concepts.

**Hands-on skills**
* **VPC Flow Logs:** Enabled flow logging, inspected records, and correlated traffic with security groups and NACLs.
* **Billing delegation:** Applied IAM policies for controlled billing console access.
* **Service Quotas:** Checked quotas, submitted increase requests, and planned capacity around limits.
* **Cost management:** Analyzed usage and cost trends to support budget-aware decisions.
* **EBS backups:** Built DLM policies and reviewed anomaly signals for backup activity.
* **Internship project:** Advanced project implementation using monitoring, cost, and backup practices from the week.

**Problem solving**
* Resolved missing or empty flow logs by checking IAM roles, log destinations, and aggregation intervals.
* Fixed billing access issues caused by incomplete IAM permissions or missing billing activation.
* Handled quota-related deploy failures by identifying the limiting service and requesting adjustments.
* Tuned DLM schedules and retention rules to balance recovery needs with storage cost.
