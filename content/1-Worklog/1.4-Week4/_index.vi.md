---
title: "Nhật ký công việc Tuần 4"
date: 2026-05-14
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Mục tiêu tuần 4
* Triển khai AWS Backup để bảo vệ và phục hồi dữ liệu trong hệ thống.
* Thực hành sử dụng File Storage Gateway và AWS Storage Gateway.
* Làm quen với Amazon S3: triển khai trang web tĩnh (static websites), cài đặt public access, và thử nghiệm.

### Các công việc cần triển khai trong tuần này
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | Triển khai AWS Backup vào hệ thống:<br>- Tạo backup vault và backup plan<br>- Gán các tài nguyên cần bảo vệ (EC2/EBS hoặc liên quan)<br>- Giám sát các tiến trình sao lưu và xác thực khôi phục cơ bản | 08/05/2026 | 09/05/2026 | AWS Backup Documentation |
| 3 | Sử dụng File Storage Gateway:<br>- Xem xét kiến trúc File Gateway<br>- Sử dụng AWS Storage Gateway (tạo gateway, kết nối đến S3)<br>- Cấu hình file share và mount thử nghiệm từ máy khách (client) | 10/05/2026 | 11/05/2026 | AWS Storage Gateway User Guide |
| 4 | Hoàn thiện Storage Gateway:<br>- Tinh chỉnh bộ đệm và quyền truy cập<br>- Xác thực quyền truy cập tệp và hành vi đồng bộ hóa qua gateway | 11/05/2026 | 12/05/2026 | File Gateway Best Practices |
| 5 | BẮT ĐẦU VỚI AMAZON S3:<br>- Kích hoạt tính năng tĩnh hóa website<br>- Cấu hình block public access<br>- Cấu hình đối tượng (objects) được phép public | 12/05/2026 | 13/05/2026 | Amazon S3 Static Website Hosting |
| 6 | Thử nghiệm website tĩnh trên S3:<br>- Truy cập thử website (endpoint, cấu hình trang báo lỗi/trang chủ)<br>- Rà soát bucket policy và phân quyền của từng cụm object | 13/05/2026 | 14/05/2026 | S3 User Guide |

### Kết quả đạt được tuần 4

**Kiến thức**
* Hiểu vai trò của AWS Backup trong việc bảo vệ dữ liệu và phục hồi sau thảm họa.
* Học cách File Storage Gateway đóng vai trò kết nối khối lượng công việc ở file nội bộ vào môi trường Amazon S3.
* Học mô hình lưu trữ trang web tĩnh với S3, hiểu được khái niệm Chặn Truy Cập Công Cộng (Public Access Block) và cấu hình object thành dạng công khai (public).

**Kỹ năng thực hành**
* **Backup:** Áp dụng các kế hoạch sao lưu (backup plans) và kiểm tra khôi phục thành công.
* **Storage Gateway:** Tạo, cấu hình cổng và chia sẻ dữ liệu thành công sử dụng AWS Storage Gateway.
* **S3:** Kích hoạt chức năng trang web tĩnh, cài đăt chế độ Public Access Block, thiết lập index và phân quyền để truy cập trang web thông suốt.

**Giải quyết vấn đề**
* Khắc phục hiệu quả các lỗi truy cập trang web hay gặp (như 403/404), đặc biệt liên quan đến cài đặt cấu trúc bucket policy, block public access, hoặc ACL ownership/tùy chỉnh đối tượng.


