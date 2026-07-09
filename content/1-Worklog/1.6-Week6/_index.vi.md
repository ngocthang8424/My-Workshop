---
title: "Nhật ký công việc Tuần 6"
date: 2026-05-27
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Mục tiêu tuần 6
* Tổ chức tài nguyên AWS một cách hiệu quả với chức năng Tag và Resource Groups.
* Áp dụng khả năng kiểm soát truy nhập bằng các mẫu IAM policy và các điều kiện Resource Tag.
* Quản lý các máy chủ từ xa một cách bảo mật qua bảng điều khiển AWS Systems Manager Session Manager.
* Tự động hóa quá trình triển khai hạ tầng với công cụ AWS CloudFormation.

### Các công việc cần triển khai trong tuần này
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | Tổ chức Tài nguyên dựa trên Tag và Resource Groups:<br>- Chuẩn hóa các bộ thẻ cài đặt (Environment, Owner, Project, CostCenter).<br>- Gắn các thẻ (tag) cho EC2, EBS, S3, và IAM roles.<br>- Tạo Resource Groups để quản lý và nhóm tự động các tài nguyên đã gắn thẻ. | 22/05/2026 | 22/05/2026 | AWS Tagging Best Practices |
| 3 | Kiểm soát Truy cập với IAM và Resource Tags:<br>- Xây dựng mẫu policies cho IAM đính kèm điều kiện `aws:ResourceTag`.<br>- Xác thực kiểm tra cấp quyển (allow/deny với theo dạng project hay nhóm environment).<br>- Đánh giá và xác nhận hành vi cấp đặc quyền thấp nhất (least-privilege). | 23/05/2026 | 23/05/2026 | IAM Policy Elements Reference |
| 4 | Tìm hiểu Systems Management qua AWS Session Manager:<br>- Kích hoạt SSM Agent và gắn IAM instance profile.<br>- Cấu hình thông số Session Manager và lưu trữ bản ghi (logging).<br>- Bắt đầu quản trị các phiên (sessions) bảo mật nhưng không cần chìa khóa SSH hay công khai port RDP. | 24/05/2026 | 24/05/2026 | AWS Systems Manager User Guide |
| 5 | Quản trị Truy cập máy chủ với Session Manager:<br>- Quản lý truy cập liên tục cho Linux/Windows thông qua Session Manager.<br>- Khởi chạy một số lệnh điều hành cơ bản và xem lại lịch sử quản trị phiên.<br>- So sánh tính hữu ích về mặt bảo vệ hệ thống so sánh với những máy chủ truy cập bằng truyền thống SSH/RDP. | 25/05/2026 | 25/05/2026 | Session Manager Documentation |
| 6 | Hạ tầng dưới dạng Code với AWS CloudFormation:<br>- Viết các khuôn mẫu cài đặt VPC, subnet, security group, và máy EC2.<br>- Triển khai các nhóm (stack), quản lý sự kiện và thao tác hoàn tác (rollback) trên lỗi.<br>- Sử dụng Change Sets để quản trị chặt quy trình cập nhật stack. | 26/05/2026 | 27/05/2026 | AWS CloudFormation User Guide |

### Kết quả đạt được tuần 6

**Kiến thức**
* Hiểu sâu cách thiết kế cấu trúc phương pháo đánh thẻ (tagging) thống nhất để phục vụ mục tiêu quản trị doanh nghiệp, bám sát hạn mức tài chính và thực nghiệm cấu hình vận hành (operations).
* Hàm thụ cách quản trị quyền sở hữu IAM khi đan chéo các điều kiện dựa trên thẻ nhằm quản lý tính liên quan cấp phép người dùng.
* Hiểu cách truy xuất vào một máy chủ bất kì trực tiếp bằng Session Manager hoàn toàn không cần cấp phát tài khoản port SSH/RDP hiển thị ra mạng ngoài publc.
* Hiểu dòng đời stack của CloudFormation: khái tạo, nâng cấp phiên bản định kì, hồi quy cấu hình tự động (rollback) vào khâu quản trị thay đổi.

**Kỹ năng thực hành**
* **Đánh thẻ (Tagging) & Quản lý Nhóm (Grouping):** Đã thiết kế và đưa vào áp dụng chuẩn mô hình; tạo dựng bộ lọc tự xuất tài nguyên (Resource Groups) tăng nhanh tốc độ kiếm tìm trên môi trường máy chủ ảo đồ sộ.
* **Quyền IAM:** Viết vào vận hành chính xác các cấp quyền gắn biến `Condition` tùy ngữ cảnh căn theo khóa chuẩn `aws:ResourceTag`.
* **Trình quản lý tự hành (Session Manager):** Vị thế đã định dạng hệ thống từ xa mà máy EC2 không để lại một rủi ro hở cấu hình; truy xuất rõ ràng nội dung các phiền tương tác.
* **Hoạt động CloudFormation:** Thiết lập trơn tru công đoạn hệ thống (stack) bằng file định dạng và kịp thời nhận diện cũng như xử trí được chuỗi phản hồi event thất bại của triển khai.

**Giải quyết vấn đề**
* Khắc phục hiệu quả tắc nghẽn liên quan quyền quản lý tính truy cập của công cụ truy tung (Session Manager) đến từ lỗi không đính trực thuộc phiên (inactive) hay lủng lỗ hỏng IAM.
* Gỡ rối trạng thái cấu hình mẫu lệch khung tag (policy mismatches).
* Sử dụng quy trình phục dựng bảo trì template thành công (rollback) thông qua việc phát hiện chệch lỗi phụ thuộc trong mã vận hành của CloudFormation stack.


