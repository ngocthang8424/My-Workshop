---
title: "Week 9 Worklog"
date: 2026-06-14
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

### Week 9 Objectives
* Set up a development environment with AWS Toolkit for VS Code.
* Learn identity federation and access patterns with AWS IAM Identity Center (AWS SSO).
* Design and document the capstone project architecture diagram.
* Continue implementing and iterating on the end-of-semester project.

### Tasks carried out this week
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | Development Environment with AWS Toolkit for VS Code:<br>- Install and configure AWS Toolkit in VS Code.<br>- Connect to AWS accounts/regions and explore resources from the IDE.<br>- Deploy and debug serverless or cloud resources from the editor. | 09/06/2026 | 09/06/2026 | AWS Toolkit for VS Code User Guide |
| 3 | Identity Federation with AWS Single Sign-On:<br>- Explore IAM Identity Center (SSO) for centralized user access.<br>- Configure permission sets and account assignments.<br>- Sign in via SSO and verify federated access to AWS resources. | 10/06/2026 | 10/06/2026 | AWS IAM Identity Center Documentation |
| 4 | Capstone project architecture diagram:<br>- Map frontend, backend, AI processing, storage, and monitoring layers.<br>- Define service boundaries, data flow, and security entry points.<br>- Produce the architecture diagram for the AI Upscaler project. | 11/06/2026 | 11/06/2026 | â€” |
| 5 | Continue end-of-semester project:<br>- Implement core components aligned with the architecture diagram.<br>- Integrate authentication, API, and storage services.<br>- Validate deployment steps from prior weeks (VPC, IAM, monitoring). | 12/06/2026 | 12/06/2026 | â€” |
| 6 | Continue end-of-semester project:<br>- Advance AI processing and backend workflow implementation.<br>- Test end-to-end flows and refine service configuration.<br>- Track progress against capstone milestones. | 13/06/2026 | 14/06/2026 | â€” |

![Capstone project architecture â€“ AI Upscaler](/images/week9/project-architecture-ai-upscaler.png)
*Architecture diagram: WAF â†’ CloudFront â†’ Amplify (Next.js); Cognito â†’ ALB â†’ EC2 (FastAPI); AI layer (SQS, Rekognition, SageMaker, Lambda); S3, DynamoDB, ElastiCache; Secrets Manager and CloudWatch.*

### Week 9 Achievements

**Knowledge**
* Understood how AWS Toolkit streamlines cloud development inside VS Code.
* Learned SSO-based federation with IAM Identity Center for multi-account access control.
* Clarified capstone architecture layers: frontend, API, AI processing, storage, and observability.
* Mapped request flow from user through WAF/CloudFront to backend and AI pipeline services.

**Hands-on skills**
* **AWS Toolkit:** Connected VS Code to AWS, browsed resources, and used toolkit workflows for deploy/debug.
* **SSO / IAM Identity Center:** Configured permission sets and verified federated sign-in behavior.
* **Architecture design:** Drew the AI Upscaler diagram covering WAF, Amplify, Cognito, ALB, EC2, SageMaker, S3, DynamoDB, and CloudWatch.
* **Capstone:** Continued building project components according to the documented architecture.

**Problem solving**
* Resolved Toolkit credential or profile issues when switching accounts/regions in VS Code.
* Fixed SSO permission gaps by adjusting permission sets and account assignments.
* Aligned architecture decisions with bootcamp constraints (cost, quotas, and service familiarity).
* Broke implementation work into deployable slices matching the diagram layers.
