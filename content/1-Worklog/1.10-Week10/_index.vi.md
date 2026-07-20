---
title: "Nhật ký công việc Tuần 10"
date: 2026-06-20
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Mục tiêu tuần 10
* Triển khai IAM Permission Boundaries để giới hạn quyền tối đa.
* Thiết lập IAM policies với điều kiện (conditions) cho context-aware authorization.
* Implement toàn bộ IAM architecture cho dự án Upscale AI.
* Develop và deploy Backend API (FastAPI) lên ECS.
* Thiết lập messaging queue với Amazon SQS cho async AI processing.

### Các công việc cần triển khai trong tuần này
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | IAM Permission Boundaries:<br>- Tạo permission boundaries cho developer và service roles.<br>- Phân tích interaction giữa identity policies và boundaries.<br>- Test và verify permission denials.<br>- Document boundary policies cho team. | 15/06/2026 | 15/06/2026 | IAM Boundaries Guide |
| 3 | Advanced IAM Policies với Conditions:<br>- Viết policies với conditions (tags, IP, MFA, time).<br>- Implement resource-based policies cho S3 buckets.<br>- Setup cross-account access với proper conditions.<br>- Test least-privilege access patterns. | 16/06/2026 | 16/06/2026 | IAM Policy Reference |
| 4 | Complete IAM Architecture cho Project:<br>- ECS Task Role: S3 (read/write), SQS (send/receive), Secrets Manager (read).<br>- EC2 Instance Role: ECR pull, EFS mount, CloudWatch logs.<br>- Lambda Execution Role: S3, DynamoDB, ElastiCache access.<br>- Cognito authenticated role: API Gateway invoke, S3 presigned URLs. | 17/06/2026 | 17/06/2026 | Project IAM Design |
| 5 | Develop Backend API:<br>- Create FastAPI application với endpoints: upload, status, download.<br>- Implement S3 presigned URL generation.<br>- Integrate với SQS để queue AI processing jobs.<br>- Setup Redis caching cho job status tracking.<br>- Containerize với Docker và push to ECR. | 18/06/2026 | 18/06/2026 | FastAPI Documentation |
| 6 | Deploy Backend to ECS:<br>- Create ECS service với ALB integration.<br>- Configure health checks và auto-scaling policies.<br>- Setup CloudWatch log groups.<br>- Deploy SQS queues với DLQ.<br>- Test end-to-end: upload → queue → status check. | 19/06/2026 | 20/06/2026 | ECS Service Deployment |

### Kết quả đạt được tuần 10

**Kiến thức**
* Hiểu sâu về permission boundaries và cách chúng tạo maximum permissions ceiling cho IAM entities.
* Nắm được cách viết sophisticated IAM policies với multiple conditions để implement fine-grained access control.
* Hiểu architecture của least-privilege access: mỗi service chỉ có đúng permissions cần thiết cho chức năng của nó.
* Học được patterns cho async processing với SQS: producer (API) → queue → consumer (AI processor).

**Kỹ năng thực hành**
* **Permission Boundaries:** Implement boundaries cho ECS task roles để prevent privilege escalation.
* **IAM Policies:** 
  - S3 bucket policy: allow access only from VPC endpoints
  - ECS task role: scoped to specific S3 prefixes (uploads/*, processed/*)
  - Conditions: `aws:SourceVpc`, `aws:SecureTransport`, resource tags
* **Backend API Development:**
  - FastAPI app với endpoints: `POST /upload`, `GET /status/{job_id}`, `GET /download/{job_id}`
  - S3 presigned URLs với 1-hour expiry
  - SQS message format: `{job_id, s3_key, parameters}`
  - Redis caching: job status và progress updates
* **ECS Deployment:**
  - Service với 2 tasks (min), 10 tasks (max)
  - Target tracking scaling: CPU > 70% → scale out
  - ALB health check: `GET /health` endpoint
  - CloudWatch logs: structured JSON logging

**Giải quyết vấn đề**
* Fix IAM policy evaluation issues: identity policy allows nhưng boundary denies → cần expand boundary.
* Debug ECS task startup failures: missing IAM permissions cho EFS mount → add `elasticfilesystem:ClientMount`.
* Resolve S3 access denied: bucket policy requires VPC endpoint → update security groups.
* Fix SQS message visibility timeout: AI processing takes >5 minutes → increase timeout to 15 minutes.
* Optimize API response time: cache S3 presigned URLs in Redis với appropriate TTL.


