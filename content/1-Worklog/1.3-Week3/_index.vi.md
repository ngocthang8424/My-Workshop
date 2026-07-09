---
title: "Nhật ký công việc Tuần 3"
date: 2026-05-07
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

### Mục tiêu tuần 3
* Thiết lập DNS kết hợp (Hybrid DNS) sử dụng Route 53 Resolver.
* Triển khai và xác thực kết nối VPC Peering.
* Xây dựng định tuyến tập trung với AWS Transit Gateway.

### Các công việc cần triển khai trong tuần này
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | Thiết lập Hybrid DNS với Route 53 Resolver:<br>- Kết nối đến RDGW<br>- Triển khai Microsoft AD<br>- Cấu hình DNS | 01/05/2026 | 02/05/2026 | Route 53 Resolver Docs |
| 3 | Thiết lập VPC Peering:<br>- Tạo Peering connection<br>- Cấu hình bảng định tuyến (Route Tables) | 03/05/2026 | 04/05/2026 | AWS VPC Peering Guide |
| 4 | Xác thực kết nối liên VPC:<br>- SSH vào máy ảo EC2 trong VPC<br>- Chạy Ping tests qua các VPC đã Peering | 05/05/2026 | 05/05/2026 | EC2 Connectivity Guide |
| 5 | Cấu hình AWS Transit Gateway:<br>- Khởi tạo Transit Gateway<br>- Tạo Transit Gateway Attachments (Tệp đính kèm) | 06/05/2026 | 06/05/2026 | AWS Transit Gateway Docs |
| 6 | Hoàn thiện định tuyến tập trung:<br>- Tạo các Route Tables cho Transit Gateway<br>- Xác minh định tuyến đường truyền hai chiều | 07/05/2026 | 07/05/2026 | Transit Gateway Route Tables |

![Hình 1 - Kết nối SSH vào EC2 trong VPC của tôi](/images/week3/week3-ssh-ec2-vpc.png)
*Hình 1: Kết nối SSH vào EC2 trong VPC.*

![Hình 2 - Khởi tạo CloudFormation template](/images/week3/week3-cloudformation.png)
*Hình 2: Khởi tạo khuôn mẫu CloudFormation.*

![Hình 3 - Ping thành công qua VPC Peering](/images/week3/week3-vpc-peering-ping.png)
*Hình 3: Kết quả ping thành công qua VPC Peering.*

### Kết quả đạt được tuần 3

**Kiến thức**
* Nắm vững luồng hoạt động của Hybrid DNS thông qua Route 53 Resolver, RDGW, và tích hợp Microsoft AD.
* Học cách thiết lập hoàn chỉnh VPC Peering và cách bảng định tuyến (route tables) điều khiển lưu lượng giữa các VPC.
* Nắm được thiết kế định tuyến tập trung với AWS Transit Gateway trong môi trường đa VPC.

**Kỹ năng thực hành**
* **Hybrid DNS:** Thiết lập các thành phần DNS cần thiết cho tính phân giải tên miền xuyên suốt các môi trường.
* **Peering:** Tạo phân cấp thành công VPC Peering và xác nhận kết nối mạng qua SSH/ping.
* **Transit Gateway:** Xây dựng toàn diện TGW, attachments, và route tables dựa trên kiến trúc mạng hình sao (hub-and-spoke).

**Giải quyết vấn đề**
* Khắc phục hiệu quả các vấn đề về kết nối gây ra bởi thiếu sót đường định tuyến (missing routes), trỏ nhầm đích (incorrect route targets), hay những phần không đồng bộ trong tuỳ chỉnh bảo mật kết nối mạng giữa các lưới VPC.


