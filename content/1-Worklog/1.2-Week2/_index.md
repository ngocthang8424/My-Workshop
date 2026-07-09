---
title: "Week 2 Worklog"
date: 2026-04-30
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---


### Week 2 Objectives
* Build a secure network environment (VPC) as the system foundation.
* Practice deploying and managing EC2 virtual servers on both Linux and Windows.
* Deploy practical applications (Node.js and User Management) on cloud servers.

### Tasks carried out this week
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | Build basic network infrastructure:<br>- Create VPC and Subnets (Public/Private).<br>- Configure Internet Gateway and Route Table for internet access. | 24/04/2026 | 24/04/2026 | AWS VPC Documentation |
| 3 | Set up security and prepare servers:<br>- Create Security Groups (ports 22, 80, 443, 3389).<br>- Launch basic EC2 instances to get familiar with the interface. | 25/04/2026 | 25/04/2026 | AWS EC2 User Guide |
| 4 | Deploy multi-platform servers:<br>- Launch and connect Windows Server 2025 (via RDP).<br>- Launch and connect Linux instance (via SSH). | 26/04/2026 | 27/04/2026 | Amazon Machine Image (AMI) |
| 5 | Practical deployment (Lab 1):<br>- Install and configure the User Management application on Amazon Linux 2023. | 28/04/2026 | 28/04/2026 | AWS Lab Guide |
| 6 | Practical deployment (Lab 2):<br>- Set up environment and deploy Node.js application on EC2 Windows Server. | 29/04/2026 | 30/04/2026 | Node.js on AWS |

### Network deployment screenshots
![Figure 1 - Public screen](/images/week2/week2-public.png)
*Figure 1: Running screen of the public subnet.*

![Figure 2 - Private screen](/images/week2/week2-private.png)
*Figure 2: Running screen of the private subnet.*

### Week 2 Achievements

**Knowledge**
* Understood AWS network layering: how VPC, Subnet, and Route Table work together for traffic routing.
* Understood operational differences between Linux and Windows in cloud environments.
* Mastered the concept of Security Groups as a stateful firewall for resource protection.

**Hands-on skills**
* **Networking:** Built a complete VPC from scratch (without Wizard) to understand core concepts deeply.
* **Operating systems:** Used SSH for Linux administration and RDP for remote Windows Server management.
* **Deployment:** Successfully deployed a Node.js app, configured environment variables, and opened required ports on Security Groups for public access.

**Problem solving**
* Resolved common connection timeout issues caused by incorrect Route Table configuration or missing Internet Gateway attachment.
