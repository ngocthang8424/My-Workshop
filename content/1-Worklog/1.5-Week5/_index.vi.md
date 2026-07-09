---
title: "Nhật ký công việc Tuần 5"
date: 2026-05-21
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Mục tiêu tuần 5
* Làm việc với Amazon DynamoDB qua Console, CloudShell và AWS SDK.
* Triển khai CloudFront với nguồn là bucket S3 và khám phá Lambda@Edge.
* Tối ưu hóa chi phí EC2 bằng cách dùng Lambda (kết hợp với tags, IAM role và function).
* Thiết lập hệ thống giám sát nâng cao cùng CloudWatch và Grafana.

### Các công việc cần triển khai trong tuần này
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | Làm việc với Amazon DynamoDB:<br>- Quản lý thông qua AWS Management Console<br>- Sử dụng AWS CloudShell *(chưa hoàn thành)*<br>- Làm quen với AWS SDK | 15/05/2026 | 16/05/2026 | Amazon DynamoDB Developer Guide |
| 3 | CloudFront kết nối với origin S3:<br>- Tạo distribution và gắn S3 làm origin<br>- Cấu hình cache behavior và xác minh lại truy cập qua CloudFront | 16/05/2026 | 17/05/2026 | CloudFront + S3 Origin Docs |
| 4 | Edge computing (điện toán vùng biên) với CloudFront và Lambda@Edge:<br>- Hoàn tất phần CloudFront<br>- Lambda@Edge *(chưa hoàn thành)* | 17/05/2026 | 18/05/2026 | Lambda@Edge Developer Guide |
| 5 | Tối ưu chi phí EC2 với Lambda:<br>- Tạo các Tag cho máy ảo (Instance)<br>- Tạo Role cho Lambda<br>- Thiết lập Hàm Lambda (Lambda Function) | 18/05/2026 | 19/05/2026 | AWS Lambda + EC2 Cost Optimization |
| 6 | Giám sát nâng cao với CloudWatch và Grafana:<br>- Thu thập metrics/logs vào CloudWatch<br>- Triển khai Grafana, làm nguồn data sources, kiểm tra lại giao diện các dashboard | 19/05/2026 | 21/05/2026 | CloudWatch + Grafana Docs |

![Hình 1 - Truy cập EC2 thành công](/images/week5/week5-ec2-connection.png)
*Hình 1: Kết nối thành công lên EC2 instance.*

![Hình 2 - Giao diện nền Grafana](/images/week5/week5-grafana.png)
*Hình 2: Giao diện nền tảng Grafana.*

### Kết quả đạt được tuần 5

**Kiến thức**
* Học cách quản trị hệ cơ sở dữ liệu DynamoDB bằng Console và bắt đầu lập trình giao tiếp (SDK).
* Hiểu sâu cơ chế gửi/nhận nội dung từ CloudFront từ những bucket S3 và vai trò của tính năng điện toán biên Lambda@Edge.
* Nắm chắc giải pháp kết hợp Lambda, Tagging EC2, và CloudWatch/Grafana nhằm hỗ trợ chi phí và hoàn thiện năng lực vận hành.

**Kỹ năng thực hành**
* **DynamoDB:** Quản trị các tables (bảng lưu trữ) thông qua Console; thực sự bắt đầu tự code SDK (CloudShell vẫn còn pending).
* **Mạng phân phối (CDN):** Triển khai hiệu quả hệ thống CloudFront gắn định tuyến tới origin S3 bucket.
* **Lambda:** Tạo các thông số tags instance, role cấp quyền IAM, và phát triển thành công Lambda chức năng cho việc tự tối ưu hóa chi phí EC2 (bài lab).
* **Quản trị (Monitoring):** Đăng nhập trơn tru thông qua SSH vào EC2 và có khả năng đọc chỉ số tại Grafana.

**Giải quyết vấn đề**
* Thiết lập để theo dõi các đầu việc tồn (pending như CloudShell, Lambda@Edge) để hỗ trợ hoàn thành ở tuần tiếp tới.
* Gỡ các lỗi khi cố kết nối nền tảng đồ họa theo dõi: xử lý security groups chặn port, và đồng bộ lại cấu hình endpoint để sử dụng thành công web EC2/Grafana.


