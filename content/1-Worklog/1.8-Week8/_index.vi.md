---
title: "Nhật ký công việc Tuần 8"
date: 2026-06-08
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Mục tiêu tuần 8
* Giám sát và phân tích lưu lượng mạng với VPC Flow Logs.
* Quản lý quyền truy cập Billing Console thông qua IAM policies.
* Làm chủ AWS Service Quotas để quản lý giới hạn dịch vụ.
* Tối ưu hóa chi phí với AWS Cost Explorer và Cost Management tools.
* Tự động hóa backup EBS với Data Lifecycle Manager (DLM).
* Bắt đầu triển khai hạ tầng nền tảng cho dự án Upscale AI.

### Các công việc cần triển khai trong tuần này
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | VPC Flow Logs và Network Monitoring:<br>- Bật VPC Flow Logs ở VPC và subnet level.<br>- Gửi logs đến CloudWatch Logs và S3.<br>- Phân tích accepted/rejected connections.<br>- Troubleshoot security group rules bằng flow logs. | 03/06/2026 | 03/06/2026 | VPC Flow Logs User Guide |
| 3 | Billing Console Access Management:<br>- Tạo IAM policies cho billing access (ViewBilling, ViewUsage).<br>- Delegate billing access cho IAM users/roles.<br>- Thiết lập least-privilege access cho cost management. | 04/06/2026 | 04/06/2026 | AWS Billing IAM Policies |
| 4 | AWS Service Quotas Management:<br>- Kiểm tra quotas của EC2, VPC, ECS, Lambda.<br>- Request quota increases cho dự án.<br>- Thiết lập CloudWatch alarms cho quota usage. | 05/06/2026 | 05/06/2026 | AWS Service Quotas Guide |
| 5 | Cost Management và Optimization:<br>- Khám phá AWS Cost Explorer với filtering và grouping.<br>- Tạo custom cost reports theo tags.<br>- Phân tích top cost drivers.<br>- Thiết lập budget alerts. | 06/06/2026 | 06/06/2026 | AWS Cost Management |
| 6 | EBS Backup Automation và Project Infrastructure:<br>- Thiết lập DLM lifecycle policies cho EBS snapshots.<br>- Configure retention rules và cross-region copy.<br>- Bắt đầu triển khai VPC cho dự án Upscale AI: tạo VPC với public/private subnets, NAT Gateway, Security Groups. | 07/06/2026 | 08/06/2026 | DLM User Guide |

### Kết quả đạt được tuần 8

**Kiến thức**
* Hiểu cách VPC Flow Logs capture network traffic và cách phân tích flow records để troubleshoot connectivity issues.
* Nắm được IAM policies cho billing access và best practices cho cost governance.
* Hiểu cách AWS Service Quotas hoạt động và process để request increases.
* Thành thạo AWS Cost Explorer để phân tích chi phí theo dimensions (service, region, tags).
* Hiểu lifecycle management cho EBS snapshots với DLM policies.

**Kỹ năng thực hành**
* **VPC Flow Logs:** Thiết lập flow logs, query logs trong CloudWatch Insights, phát hiện suspicious traffic patterns.
* **Billing Access:** Tạo IAM policies với điều kiện (conditions) để control billing access một cách an toàn.
* **Service Quotas:** Monitoring quota usage, request increases, và plan capacity cho dự án.
* **Cost Analysis:** Sử dụng Cost Explorer để identify cost optimization opportunities, tạo monthly cost reports.
* **EBS Automation:** Thiết lập DLM policies với daily/weekly schedules và retention policies.
* **Project VPC:** Triển khai VPC infrastructure cho Upscale AI với proper network segmentation (public/private subnets).

**Giải quyết vấn đề**
* Fix lỗi VPC Flow Logs không gửi data đến CloudWatch do missing IAM role permissions.
* Troubleshoot billing console access denied bằng cách thêm `aws-portal:ViewBilling` permission.
* Xử lý quota limit errors khi deploy nhiều EC2 instances bằng cách request increase.
* Optimize DLM schedules để balance giữa data protection và storage costs.
* Thiết kế VPC CIDR blocks để tránh overlap và đảm bảo đủ IP addresses cho scaling.


