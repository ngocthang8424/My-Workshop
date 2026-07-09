---
title: "Week 4 Worklog"
date: 2026-05-14
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Week 4 Objectives
* Deploy AWS Backup to protect and recover data in the system.
* Practice File Storage Gateway and AWS Storage Gateway.
* Start with Amazon S3: static websites, public access settings, and testing.

### Tasks carried out this week
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | Deploy AWS Backup to the System:<br>- Create backup vault and backup plan<br>- Assign resources to protect (EC2/EBS or related)<br>- Monitor backup jobs and verify basic restore | 08/05/2026 | 09/05/2026 | AWS Backup Documentation |
| 3 | Using File Storage Gateway:<br>- Review File Gateway architecture<br>- Use AWS Storage Gateway (create gateway, connect to S3)<br>- Configure file share and test mount from client | 10/05/2026 | 11/05/2026 | AWS Storage Gateway User Guide |
| 4 | Finalize Storage Gateway:<br>- Tune cache and access permissions<br>- Validate file access and sync behavior via gateway | 11/05/2026 | 12/05/2026 | File Gateway Best Practices |
| 5 | STARTING WITH AMAZON S3:<br>- Enable static website feature<br>- Configuring public access block<br>- Configuring public objects | 12/05/2026 | 13/05/2026 | Amazon S3 Static Website Hosting |
| 6 | Test static website on S3:<br>- Test website (endpoint, index/error documents)<br>- Review bucket policy and object permissions | 13/05/2026 | 14/05/2026 | S3 User Guide |

### Week 4 Achievements

**Knowledge**
* Understood AWS Backupâ€™s role in data protection and disaster recovery.
* Learned how File Storage Gateway connects on-premises file workloads to Amazon S3.
* Learned S3 static website hosting, Public Access Block, and public object configuration.

**Hands-on skills**
* **Backup:** Implemented backup plans and performed backup/restore validation in lab context.
* **Storage Gateway:** Created and configured gateway and file shares using AWS Storage Gateway.
* **S3:** Enabled static website hosting, configured public access block, set public objects, and verified website access.

**Problem solving**
* Resolved common website access issues (403/404) caused by bucket policy, block public access, or object ACL/ownership settings.
