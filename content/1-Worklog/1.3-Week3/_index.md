---
title: "Week 3 Worklog"
date: 2026-05-07
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

### Week 3 Objectives
* Set up Hybrid DNS using Route 53 Resolver.
* Deploy and validate VPC Peering connectivity.
* Build centralized routing with AWS Transit Gateway.

### Tasks carried out this week
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | Set up Hybrid DNS with Route 53 Resolver:<br>- Connecting to RDGW<br>- Microsoft AD Deployment<br>- Setup DNS | 01/05/2026 | 02/05/2026 | Route 53 Resolver Docs |
| 3 | Setting up VPC Peering:<br>- Create Peering connection<br>- Configure route tables | 03/05/2026 | 04/05/2026 | AWS VPC Peering Guide |
| 4 | Validate inter-VPC connectivity:<br>- SSH to EC2 in VPC<br>- Ping tests across peered VPCs | 05/05/2026 | 05/05/2026 | EC2 Connectivity Guide |
| 5 | Set up AWS Transit Gateway:<br>- Create Transit Gateway<br>- Create Transit Gateway Attachments | 06/05/2026 | 06/05/2026 | AWS Transit Gateway Docs |
| 6 | Finalize centralized routing:<br>- Create Transit Gateway Route Tables<br>- Verify end-to-end routing | 07/05/2026 | 07/05/2026 | Transit Gateway Route Tables |

![Figure 1 - SSH connection to EC2 in my VPC](/images/week3/week3-ssh-ec2-vpc.png)
*Figure 1: SSH connection to EC2 in my VPC.*

![Figure 2 - CloudFormation template initialization](/images/week3/week3-cloudformation.png)
*Figure 2: CloudFormation template initialization.*

![Figure 3 - VPC Peering ping success](/images/week3/week3-vpc-peering-ping.png)
*Figure 3: VPC Peering ping success.*

### Week 3 Achievements

**Knowledge**
* Understood the Hybrid DNS flow with Route 53 Resolver, RDGW, and Microsoft AD integration.
* Learned the full VPC Peering setup and how route tables control inter-VPC traffic.
* Understood centralized routing design with AWS Transit Gateway in multi-VPC environments.

**Hands-on skills**
* **Hybrid DNS:** Configured required DNS components for cross-environment name resolution.
* **Peering:** Successfully created VPC Peering and validated connectivity via SSH/ping.
* **Transit Gateway:** Built TGW, attachments, and route tables for a hub-and-spoke style network.

**Problem solving**
* Resolved connectivity issues caused by missing routes, incorrect route targets, or mismatched security settings between VPCs.
