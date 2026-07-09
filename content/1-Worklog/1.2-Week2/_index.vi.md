---
title: "Nhật ký công việc Tuần 2"
date: 2026-04-30
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---


### Mục tiêu tuần 2
* Xây dựng môi trường mạng bảo mật (VPC) làm nền tảng hệ thống.
* Thực hành triển khai và quản lý máy chủ ảo EC2 trên cả Linux và Windows.
* Triển khai ứng dụng thực tế (Node.js và User Management) trên máy chủ đám mây.

### Các công việc cần triển khai trong tuần này
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | Xây dựng hạ tầng mạng cơ bản:<br>- Tạo VPC và Subnets (Public/Private).<br>- Cấu hình Internet Gateway và Route Table để truy cập internet. | 24/04/2026 | 24/04/2026 | AWS VPC Documentation |
| 3 | Thiết lập bảo mật và chuẩn bị máy chủ:<br>- Tạo Security Groups (mở port 22, 80, 443, 3389).<br>- Khởi tạo các EC2 instance cơ bản để làm quen giao diện. | 25/04/2026 | 25/04/2026 | AWS EC2 User Guide |
| 4 | Triển khai máy chủ đa nền tảng:<br>- Khởi tạo và kết nối Windows Server 2025 (qua RDP).<br>- Khởi tạo và kết nối Linux instance (qua SSH). | 26/04/2026 | 27/04/2026 | Amazon Machine Image (AMI) |
| 5 | Thực hành triển khai (Lab 1):<br>- Cài đặt và cấu hình ứng dụng User Management trên Amazon Linux 2023. | 28/04/2026 | 28/04/2026 | AWS Lab Guide |
| 6 | Thực hành triển khai (Lab 2):<br>- Thiết lập môi trường và triển khai ứng dụng Node.js trên máy chủ EC2 Windows. | 29/04/2026 | 30/04/2026 | Node.js on AWS |

### Giao diện kết quả triển khai mạng
![Hình 1 - Màn hình Public](/images/week2/week2-public.png)
*Hình 1: Màn hình chạy của public subnet.*

![Hình 2 - Màn hình Private](/images/week2/week2-private.png)
*Hình 2: Màn hình chạy của private subnet.*

### Kết quả đạt được tuần 2

**Kiến thức**
* Hiểu cách chia lớp mạng AWS: cách VPC, Subnet, và Route Table phối hợp quản lý luồng dữ liệu.
* Hiểu sự khác biệt trong vận hành giữa Linux và Windows trên môi trường đám mây.
* Nắm vững khái niệm Security Groups như một tường lửa trạng thái để bảo vệ tài nguyên.

**Kỹ năng thực hành**
* **Mạng (Networking):** Tự xây dựng cấu hình VPC hoàn chỉnh từ đầu (không dùng Wizard) để hiểu sâu các khái niệm lõi.
* **Hệ điều hành:** Dùng SSH để quản trị Linux và RDP để điều khiển từ xa Windows Server.
* **Triển khai:** Triển khai thành công ứng dụng Node.js, cấu hình biến môi trường, và mở đúng port trên Security Groups cho phép truy cập từ public internet.

**Giải quyết vấn đề**
* Khắc phục các lỗi kết nối timeout phổ biến do sai lệch cấu hình Route Table hoặc chưa gắn Internet Gateway.
