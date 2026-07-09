---
title: "Week 5 Worklog"
date: 2026-05-21
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Week 5 Objectives
* Work with Amazon DynamoDB via Console, CloudShell, and AWS SDK.
* Deploy CloudFront with an S3 bucket origin and explore Lambda@Edge.
* Optimize EC2 costs using Lambda (tags, IAM role, function).
* Set up advanced monitoring with CloudWatch and Grafana.

### Tasks carried out this week
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | Work with Amazon DynamoDB:<br>- Manage using AWS Management Console<br>- Use AWS CloudShell *(not completed yet)*<br>- Begin with AWS SDK | 15/05/2026 | 16/05/2026 | Amazon DynamoDB Developer Guide |
| 3 | CloudFront with S3 bucket origin:<br>- Create distribution and attach S3 as origin<br>- Configure cache behavior and verify CloudFront access | 16/05/2026 | 17/05/2026 | CloudFront + S3 Origin Docs |
| 4 | Edge computing with CloudFront and Lambda@Edge:<br>- Completed CloudFront portion<br>- Lambda@Edge *(not completed yet)* | 17/05/2026 | 18/05/2026 | Lambda@Edge Developer Guide |
| 5 | Optimizing EC2 Costs with Lambda:<br>- Create Tag for Instance<br>- Create Role for Lambda<br>- Create Lambda Function | 18/05/2026 | 19/05/2026 | AWS Lambda + EC2 Cost Optimization |
| 6 | Advanced monitoring with CloudWatch and Grafana:<br>- Collect metrics/logs in CloudWatch<br>- Deploy Grafana, connect data sources, verify dashboards | 19/05/2026 | 21/05/2026 | CloudWatch + Grafana Docs |

![Figure 1 - Successful EC2 connection](/images/week5/week5-ec2-connection.png)
*Figure 1: Successful connection to an EC2 instance.*

![Figure 2 - Grafana interface](/images/week5/week5-grafana.png)
*Figure 2: Grafana interface.*

### Week 5 Achievements

**Knowledge**
* Learned DynamoDB management via Console and started AWS SDK integration.
* Understood CloudFront delivery from S3 origins and the role of Lambda@Edge at the edge.
* Learned how Lambda, EC2 tags, and CloudWatch/Grafana support cost and observability workflows.

**Hands-on skills**
* **DynamoDB:** Managed tables via Console; started SDK work (CloudShell still pending).
* **CDN:** Successfully deployed CloudFront with an S3 bucket origin.
* **Lambda:** Created instance tags, IAM role, and Lambda function for EC2 cost optimization lab.
* **Monitoring:** Connected to EC2 via SSH and accessed the Grafana UI after deployment.

**Problem solving**
* Tracked pending items (CloudShell, Lambda@Edge) for follow-up in later weeks.
* Resolved EC2/Grafana connectivity issues related to security groups, ports, and endpoint configuration.
