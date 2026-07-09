---
title: "Week 7 Worklog"
date: 2026-06-02
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Week 7 Objectives
* Learn infrastructure as code using the AWS Cloud Development Kit (CDK).
* Apply CDK constructs, stacks, and deployment workflows from essentials through advanced patterns.
* Complete hands-on labs from the Infrastructure as Code Workshop Series.
* Optimize EC2 workloads using right-sizing and resource utilization analysis.
* Kick off the end-of-semester capstone project (goals, architecture, and AWS services scope).

### Tasks carried out this week
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | AWS CDK Essentials:<br>- Install and configure AWS CDK CLI and bootstrap the environment.<br>- Define an app with stacks and deploy a simple resource (e.g. S3, Lambda).<br>- Understand synthesis (`cdk synth`) and deployment (`cdk deploy`). | 28/05/2026 | 28/05/2026 | AWS CDK Developer Guide |
| 3 | AWS CDK Advanced:<br>- Work with L2/L3 constructs, parameters, and environment context.<br>- Organize multi-stack apps and cross-stack references.<br>- Use aspects, tagging, and deployment best practices. | 29/05/2026 | 29/05/2026 | AWS CDK Advanced Workshop |
| 4 | Infrastructure as Code Workshop Series:<br>- Compare IaC approaches (CloudFormation, CDK, Terraform concepts).<br>- Build and update infrastructure through repeatable pipelines.<br>- Review drift, change sets, and safe update patterns. | 30/05/2026 | 30/05/2026 | AWS IaC Workshop Series |
| 5 | Right-Sizing with EC2 Resource Optimization:<br>- Analyze CPU, memory, and network metrics for EC2 instances.<br>- Identify over-provisioned instances and candidate instance families.<br>- Document cost/performance trade-offs from right-sizing recommendations. | 31/05/2026 | 31/05/2026 | AWS Compute Optimizer / EC2 Right-Sizing |
| 6 | End-of-semester project kickoff:<br>- Define project goals, architecture diagram, and AWS services to use. | 01/06/2026 | 02/06/2026 | â€” |

### Week 7 Achievements

**Knowledge**
* Understood the CDK model: app, stack, construct, and how it maps to CloudFormation.
* Learned advanced CDK patterns for modular infrastructure and environment-specific configuration.
* Reinforced IaC principles: versioned templates, repeatable deploys, and controlled change management.
* Understood EC2 right-sizing signals and how optimization supports cost and performance goals.
* Aligned capstone scope with skills from prior weeks (networking, security, automation, monitoring).

**Hands-on skills**
* **CDK Essentials:** Bootstrapped an account/region, synthesized templates, and deployed a first CDK stack.
* **CDK Advanced:** Structured multi-stack apps, used constructs/parameters, and applied deployment conventions.
* **IaC workshops:** Practiced end-to-end define â†’ deploy â†’ update workflows with rollback awareness.
* **EC2 optimization:** Used metrics and recommendations to evaluate instance sizing and utilization.
* **Capstone:** Defined project goals, architecture, and AWS services for the final deliverable.

**Problem solving**
* Resolved CDK bootstrap or IAM permission errors during first-time deploy.
* Fixed synthesis/deploy failures from construct props, asset paths, or region/account mismatches.
* Interpreted noisy or insufficient CloudWatch metrics when evaluating right-sizing candidates.
* Outlined capstone scope into clear milestones and a minimal viable architecture.
