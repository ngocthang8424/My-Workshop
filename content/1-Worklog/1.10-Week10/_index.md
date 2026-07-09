---
title: "Week 10 Worklog"
date: 2026-06-20
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Week 10 Objectives
* Manage permissions with IAM permission boundaries to limit maximum grantable access.
* Apply access control using IAM policies and condition keys for context-aware authorization.
* Map IAM roles and policies to the capstone architecture (Cognito, EC2, Lambda, S3, and related services).
* Continue implementing the end-of-semester project with least-privilege security aligned to the architecture diagram.

### Tasks carried out this week
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | Permission Management with IAM Permission Boundaries:<br>- Create and attach permission boundaries to IAM users or roles.<br>- Understand how boundaries cap effective permissions alongside identity policies.<br>- Test allowed and denied actions within boundary limits. | 15/06/2026 | 15/06/2026 | IAM Permissions Boundaries Guide |
| 3 | Access Control with IAM Policies and Conditions:<br>- Write policies with `Condition` blocks (tags, source IP, MFA, resource ARN, …).<br>- Combine allow/deny rules for environment- or project-scoped access.<br>- Validate least-privilege behavior with policy simulator or test principals. | 16/06/2026 | 16/06/2026 | IAM Policy Elements Reference |
| 4 | Apply architecture to project – IAM layer:<br>- Define roles for EC2 (FastAPI), Lambda, SageMaker, and service-linked access per the AI Upscaler diagram.<br>- Scope S3, DynamoDB, SQS, and Secrets Manager permissions to required actions only.<br>- Align Cognito identity pool / authenticated role with backend API access. | 17/06/2026 | 17/06/2026 | — |
| 5 | Continue capstone – secure deployment:<br>- Attach permission boundaries and refined policies to project roles.<br>- Verify WAF → CloudFront → Amplify → Cognito → ALB → EC2 flow with correct IAM trust.<br>- Test API and storage access from application components. | 18/06/2026 | 18/06/2026 | — |
| 6 | Continue capstone – integration and review:<br>- Harden Lambda and AI pipeline roles (SQS, Rekognition, SageMaker) per architecture.<br>- Review CloudWatch and Secrets Manager access for observability and credentials.<br>- Document IAM decisions against the architecture diagram. | 19/06/2026 | 20/06/2026 | — |

### Week 10 Achievements

**Knowledge**
* Understood how permission boundaries set the upper limit of permissions for IAM identities.
* Learned to use IAM policy conditions for tag-based, resource-scoped, and contextual access control.
* Mapped IAM trust and permissions to each layer of the AI Upscaler architecture.
* Reinforced least-privilege design when connecting Cognito, compute, storage, and AI services.

**Hands-on skills**
* **Permission boundaries:** Created boundaries and verified effective permissions on test roles.
* **Policies & conditions:** Authored and tested policies with `Condition` blocks for realistic scenarios.
* **Architecture → IAM:** Applied the week 9 diagram to role design for EC2, Lambda, S3, DynamoDB, and Cognito.
* **Capstone:** Deployed and validated project components with boundary-aware, conditional IAM policies.

**Problem solving**
* Resolved overly permissive or blocked access by separating identity policy, boundary, and resource policy scope.
* Fixed condition mismatches (wrong key, tag name, or ARN pattern) causing unexpected deny results.
* Aligned multiple service roles in the AI pipeline without privilege creep across SageMaker, Lambda, and EC2.
