---
title: "Nhật ký công việc Tuần 7"
date: 2026-06-02
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Mục tiêu tuần 7
* Làm chủ AWS Cloud Development Kit (CDK) - công cụ Infrastructure as Code thế hệ mới.
* Thực hành triển khai hạ tầng AWS bằng code với CDK (TypeScript/Python).
* Tối ưu hóa chi phí EC2 thông qua phân tích Right-Sizing và Compute Optimizer.
* Xác định và đề xuất dự án tốt nghiệp: **Upscale AI Platform** - Nền tảng nâng cấp ảnh bằng AI trên AWS.

### Các công việc cần triển khai trong tuần này
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | AWS CDK Cơ bản:<br>- Cài đặt và cấu hình AWS CDK CLI.<br>- Bootstrap môi trường CDK cho region.<br>- Tạo CDK app đầu tiên với S3 bucket và Lambda function.<br>- Thực hành `cdk synth` và `cdk deploy`. | 28/05/2026 | 28/05/2026 | AWS CDK Developer Guide |
| 3 | AWS CDK Nâng cao:<br>- Làm việc với Constructs L1, L2, L3.<br>- Tạo multi-stack application với cross-stack references.<br>- Áp dụng CDK Context, Parameters, và Outputs.<br>- Best practices: tagging, naming conventions. | 29/05/2026 | 29/05/2026 | AWS CDK Workshop |
| 4 | Infrastructure as Code Workshop Series:<br>- So sánh CloudFormation vs CDK vs Terraform.<br>- Quản lý infrastructure drift detection.<br>- Tích hợp IaC vào CI/CD pipeline.<br>- Rollback strategies và stack updates. | 30/05/2026 | 30/05/2026 | AWS IaC Best Practices |
| 5 | EC2 Right-Sizing và Cost Optimization:<br>- Phân tích CloudWatch metrics (CPU, Memory, Network).<br>- Sử dụng AWS Compute Optimizer để đề xuất instance types.<br>- Tính toán tiết kiệm chi phí khi right-sizing.<br>- Lên kế hoạch migration instance types. | 31/05/2026 | 31/05/2026 | AWS Compute Optimizer Guide |
| 6 | Đề xuất dự án tốt nghiệp - Upscale AI:<br>- Xác định yêu cầu chức năng: upload ảnh, xử lý AI (Real-ESRGAN), theo dõi tiến trình.<br>- Thiết kế kiến trúc: Frontend (S3+CloudFront), Backend (ECS+EC2), AI Processing (GPU), Storage (S3+EFS).<br>- Lên danh sách AWS services: VPC, ECS, EC2, S3, EFS, CloudFront, ALB, ElastiCache, SQS, WAF. | 01/06/2026 | 02/06/2026 | Project Proposal Document |

### Kết quả đạt được tuần 7

**Kiến thức**
* Hiểu rõ kiến trúc AWS CDK: App → Stack → Construct và cách CDK synthesize thành CloudFormation templates.
* Nắm được lợi ích của IaC: version control, reproducibility, automation, documentation as code.
* Hiểu cách AWS Compute Optimizer phân tích usage patterns và đề xuất instance types phù hợp.
* Xác định được kiến trúc tổng quan cho dự án Upscale AI với các thành phần chính và luồng dữ liệu.

**Kỹ năng thực hành**
* **AWS CDK:** Triển khai thành công stacks với CDK, sử dụng constructs để tạo VPC, EC2, S3, Lambda.
* **IaC Management:** Quản lý infrastructure changes, detect drift, và thực hiện safe updates với CDK.
* **Cost Optimization:** Phân tích metrics và xác định được các EC2 instances cần right-sizing để tiết kiệm 20-30% chi phí.
* **Architecture Design:** Thiết kế sơ đồ kiến trúc cho dự án Upscale AI với các lớp: Frontend, API, AI Processing, Data, Security, Monitoring.

**Giải quyết vấn đề**
* Xử lý lỗi IAM permissions khi bootstrap CDK environment.
* Debug synthesis errors trong CDK stack do circular dependencies.
* Giải quyết vấn đề CloudWatch metrics không đầy đủ cho việc right-sizing bằng cách enable detailed monitoring.
* Điều chỉnh kiến trúc dự án để phù hợp với AWS Free Tier và tối ưu chi phí (~$230/tháng cho môi trường test).


