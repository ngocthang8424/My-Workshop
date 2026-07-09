---
title: "Week 6 Worklog"
date: 2026-05-27
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Week 6 Objectives
* Organize AWS resources effectively using Tags and Resource Groups.
* Apply access control with IAM policies and Resource Tag conditions.
* Manage remote servers securely using AWS Systems Manager Session Manager.
* Automate infrastructure deployment using AWS CloudFormation.

### Tasks carried out this week
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | Resource Organization with Tags and Resource Groups:<br>- Standardize a tag set (Environment, Owner, Project, CostCenter).<br>- Apply tags to EC2, EBS, S3, and IAM roles.<br>- Create Resource Groups to organize tagged resources. | 22/05/2026 | 22/05/2026 | AWS Tagging Best Practices |
| 3 | Access Control with IAM and Resource Tags:<br>- Create IAM policies with `aws:ResourceTag` conditions.<br>- Test permissions by tags (allow/deny by environment or project).<br>- Validate least-privilege access behavior. | 23/05/2026 | 23/05/2026 | IAM Policy Elements Reference |
| 4 | Systems Management with AWS Session Manager:<br>- Enable SSM Agent and IAM instance profile.<br>- Configure Session Manager preferences and logging.<br>- Start secure management sessions without SSH keys or public RDP. | 24/05/2026 | 24/05/2026 | AWS Systems Manager User Guide |
| 5 | Remote Server Access with Session Manager:<br>- Access Linux/Windows instances through Session Manager.<br>- Run basic operational commands and verify session history.<br>- Compare security posture with traditional SSH/RDP access. | 25/05/2026 | 25/05/2026 | Session Manager Documentation |
| 6 | Infrastructure as Code with AWS CloudFormation:<br>- Write templates for VPC, subnet, security group, and EC2.<br>- Deploy stack, monitor events, and handle rollback on failure.<br>- Use Change Sets to control stack updates. | 26/05/2026 | 27/05/2026 | AWS CloudFormation User Guide |

### Week 6 Achievements

**Knowledge**
* Understood how to design a consistent tagging strategy for governance, cost tracking, and operations.
* Learned IAM policy control using tag-based conditions to enforce contextual access.
* Understood server access without exposing public SSH/RDP ports through Session Manager.
* Learned CloudFormation stack lifecycle: create, update, rollback, and change management.

**Hands-on skills**
* **Tagging & Grouping:** Designed and applied a standard tag model; created Resource Groups for faster filtering and management.
* **IAM:** Wrote and tested policies with `Condition` blocks based on `aws:ResourceTag`.
* **Session Manager:** Configured secure remote access for EC2 with session visibility and control.
* **CloudFormation:** Built and operated infrastructure stacks from templates and troubleshot deployment events.

**Problem solving**
* Resolved Session Manager access failures caused by missing IAM roles or inactive SSM Agent.
* Fixed policy mismatches by reviewing tag conditions and resource scope.
* Performed rollback and template corrections when CloudFormation stack updates failed due to dependency/configuration errors.
