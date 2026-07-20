---
title: "Nhật ký công việc Tuần 9"
date: 2026-06-14
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

### Mục tiêu tuần 9
* Cài đặt và làm quen AWS Toolkit for Visual Studio Code.
* Triển khai AWS IAM Identity Center (AWS SSO) cho multi-account access.
* Hoàn thiện thiết kế kiến trúc chi tiết cho dự án Upscale AI.
* Bắt đầu implement các core components của dự án: ECS cluster, ECR, S3 buckets.

### Các công việc cần triển khai trong tuần này
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | AWS Toolkit for VS Code:<br>- Cài đặt và cấu hình AWS Toolkit extension.<br>- Connect đến AWS account và explore resources.<br>- Debug và deploy Lambda functions từ VS Code.<br>- Browse S3, CloudWatch Logs trực tiếp trong IDE. | 09/06/2026 | 09/06/2026 | AWS Toolkit User Guide |
| 3 | IAM Identity Center (AWS SSO):<br>- Thiết lập IAM Identity Center cho organization.<br>- Tạo permission sets cho different roles.<br>- Configure SSO access cho multiple AWS accounts.<br>- Test federated login workflow. | 10/06/2026 | 10/06/2026 | IAM Identity Center Guide |
| 4 | Finalize Architecture Design:<br>- Vẽ chi tiết architecture diagram với tất cả components.<br>- Document data flows: upload → processing → download.<br>- Define security boundaries và network segmentation.<br>- List tất cả IAM roles và policies cần thiết. | 11/06/2026 | 11/06/2026 | Architecture Document |
| 5 | Implement Storage Layer:<br>- Tạo S3 buckets: uploads, processed-images, model-weights.<br>- Configure bucket policies, versioning, lifecycle rules.<br>- Setup EFS for persistent storage (PostgreSQL data, model weights).<br>- Test cross-service access permissions. | 12/06/2026 | 12/06/2026 | S3 và EFS Documentation |
| 6 | Implement Container Infrastructure:<br>- Setup Amazon ECR repositories cho Docker images.<br>- Tạo ECS cluster với EC2 launch type.<br>- Configure Auto Scaling Group với GPU instances (g4dn.xlarge).<br>- Setup ECS task definitions với EFS mount points. | 13/06/2026 | 14/06/2026 | ECS và ECR Documentation |

![Architecture Diagram - Upscale AI Platform](/images/2-Proposal/sodo.jpg)
*Sơ đồ kiến trúc tổng quan: CloudFront + WAF → S3 (Frontend) → ALB → ECS (Backend) → S3 + EFS (Storage), với ElastiCache Redis và SQS cho async processing.*

### Kết quả đạt được tuần 9

**Kiến thức**
* Hiểu cách AWS Toolkit tích hợp development workflow với AWS services ngay trong IDE.
* Nắm được IAM Identity Center architecture và cách manage multi-account access với SSO.
* Hoàn thiện hiểu biết về container orchestration với ECS trên EC2 (không phải Fargate).
* Hiểu lý do chọn ECS+EC2 thay vì Lambda: cần GPU cho AI inference, task execution time dài (>15 phút).

**Kỹ năng thực hành**
* **AWS Toolkit:** Sử dụng VS Code để browse AWS resources, debug Lambda locally, view CloudWatch logs real-time.
* **IAM Identity Center:** Thiết lập SSO với permission sets, assign users/groups, test federated access.
* **Architecture Design:** Tạo detailed architecture diagram với Lucidchart/Draw.io, document tất cả connections và data flows.
* **S3 Implementation:** 
  - Bucket `upscale-ai-uploads`: CORS enabled, presigned URLs cho upload
  - Bucket `upscale-ai-processed`: CloudFront distribution cho delivery
  - Bucket `upscale-ai-models`: Private, chứa Real-ESRGAN weights
* **ECS Setup:** 
  - Cluster `upscale-ai-cluster` với capacity provider (Auto Scaling Group)
  - ECR repositories: `backend-api`, `ai-processor`
  - Task definitions với GPU support và EFS volumes

**Giải quyết vấn đề**
* Fix AWS Toolkit credential issues bằng cách configure proper AWS CLI profile.
* Troubleshoot SSO permission set assignments khi users không thấy expected accounts.
* Giải quyết ECS task placement constraints để ensure tasks chạy trên GPU instances.
* Debug EFS mount issues trong ECS tasks bằng cách verify security groups và mount targets.
* Optimize Docker images để reduce pull time từ ECR (multi-stage builds, layer caching).


