---
title: "Nhật ký công việc Tuần 8"
date: 2026-06-08
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Mục tiêu tuần 8
* Theo dõi và giám sát lưu lượng mạng VPC bằng tính năng VPC Flow Logs, sau đó bắt tay vào phân tích dữ liệu dòng chảy mạng.
* Cấp quyền ủy nhiệm an toàn vào trang quản lý thanh toán (billing console) để có cái nhìn tổng quan về chi phí và vận hành tài khoản chung.
* Quản lý các giới hạn sử dụng và hạn mức của dịch vụ AWS thông qua Service Quotas.
* Theo dõi và phân tích chi tiêu với các công cụ quản lý chi phí chuyên dụng (Cost and Usage Management).
* Tự động khởi tạo các bản sao lưu (snapshots) ổ đĩa EBS nhờ công cụ quản lý chu kỳ sống của dữ liệu (Data Lifecycle Manager - DLM).
* Phát hiện những hoạt động backup bị bất thường từ mạng bằng ứng dụng đánh giá sự cố ngoại lai khi backup EBS (anomaly detection).
* Tiếp tục xây dựng dự án đồ án tốt nghiệp cuối kì.

### Các công việc cần triển khai trong tuần này
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | Giám sát Mạng bằng VPC Flow Logs:<br>- Bật chức năng VPC Flow Logs trên cả không gian mạng lưới VPC hay giới hạn trong phạm vi ngách mạng subnet.<br>- Đẩy nhật ký thu thập (logs) tới CloudWatch Logs hoặc S3, sau đó phân tích các luồng truy cập được thông qua (accepted) hoặc phân phát chặn (rejected).<br>- Tái dụng lại kết xuất của flow records vào mục đích xác định nguyên cớ ngắt hỏng dòng mạng từ rules bên Security Group. | 03/06/2026 | 03/06/2026 | Amazon VPC Flow Logs User Guide |
| 3 | Ủy Quyền Billing Console:<br>- Viết định dạng IAM policies phục vụ phân quyền theo dõi chi trả, giá thành.<br>- Giao phó, xác lập quyền hiển thị billing console riêng tới 1 role hay một user trực thuộc có xác thực độ tin cậy được ủy quyền.<br>- Đánh giá quyền tối thiểu chi li đủ thấy bảng sao kê ngân sách, cách thanh toán hóa đơn. | 04/06/2026 | 04/06/2026 | AWS Billing and Cost Management |
| 4 | Kìm Giới Hạn Hạn Mức Thông Qua Quản Lí Service Quotas:<br>- Truy xuất hạn lượng định chuẩn của những dịch vụ máy chủ lớn (EC2, Lambda, VPC...).<br>- Lập đơn đề bạt xin thêm năng lực sử dụng phần ngọn trong những nhu cầu cần quá ngưỡng của dự án.<br>- Không ngừng đánh giá việc hụt ngạch quota ảnh hưởng lỗi truy xuất lúc cần. | 05/06/2026 | 05/06/2026 | AWS Service Quotas User Guide |
| 5 | Quản Trị Hệ Việc Quản Khống Và Báo Cáo Kế Toán Chi:(Cost and Usage Management):<br>- Thám hiểm cơ sở Cost Explorer, thử ứng dụng báo cáo thẻ phân hệ tiền cước.<br>- Lục báo cáo thói quen để rà lọt được top phân hạng ngốn tài nguyên tài chính nhất.<br>- Đóng bộ quy chuẩn làm quen với cảnh báo vượt lạm. | 06/06/2026 | 06/06/2026 | AWS Cost Management Documentation |
| 6 | Tự động hóa backup EBS và quá trình dự án cuối kĩ:<br>- Khởi động chức năng thiết lập chính sách quy trình vòng xoáy định mệnh DLM (lifecycle policies) cho kịch bản backup rập khuôn ảnh gốc EBS.<br>- Trang bị phần ngoại lệ dò tìm dị thường tín hiệu trên nhịp hành vi backup EBS.<br>- Áp dụng những điều này trực thuộc việc tái cấu trúc hoàn chỉnh dự án tổng hợp đồ án tốt nghiệp. | 07/06/2026 | 08/06/2026 | Amazon EBS / Data Lifecycle Manager |

### Kết quả đạt được tuần 8

**Kiến thức**
* Mường tượng cấu trúc bắt IP traffic của hệ bảo mật VPC Flow Logs cùng cơ chế giúp giám sát viên rò đường bế tắc trên mạng lưới.
* Học mô chuẩn giao phó trọng trách hóa đơn nhằm thắt gút truy xuất IAM tới khâu giao diện tài chính.
* Tiếp nhận kiến thức vận dụng Service Quotas coi như đại sảnh trung tâm hiển thị trần giới hạn cũng như nhận và gửi phản hồi yều cần vượt trần.
* Củng cố chặt tầm quan sát tiền cước với các công cụ giám trắc Cost Explorer hay báo cáo cước tích lũy.
* Chiếu sáng luồng tư duy backup lưu kho thông qua DLM (EBS snapshot automation).

**Kỹ năng thực hành**
* **VPC Flow Logs:** Thiết lập được mạng dò báo log luồng đi, xem qua lại record, liên đới tính phân tích qua lại với mảng bảo mật bảo hiến Security Group và tầng NACLs.
* **Cấp quyền tài chính (Billing delegation):** Phóng tạo mẫu policies trong IAM ghim chết được ai có thể tới khâu giao dịch chi ngân (billing console).
* **Service Quotas:** Dò số liệu ngưỡng trần (quotas), chủ động trình giấy gọi gia hạn, quy khoanh tài nguyên hợp ngạch cấp trong một giới hạn có sắp xếp.
* **Cost management:** Phác được lượng phân tích tiền thuế cũng như định hình được phương trời hỗ trợ vạch ngân sách ra đề.
* **EBS backups:** Kéo thiết lập chu trình vòng lưu chuyển (DLM policies), và duyệt đọc định hình dạng ngoại lai có liên quan đến việc backup.
* **Đề Đạt Đồ Án Kì:** Áp đặt bước tiến ứng dụng bằng việc gom tính năng quản trị giám sát, chi phí tài chính cùng vận định thói quen backup từ đầu ngày qua thẳng hệ thống đồ án.

**Giải quyết vấn đề**
* Khắc chế biểu chứng thất tán mất log tại không báo về kho bằng cách tái coi lại IAM roles đích hướng trả log từ cụm thu nhập cấu hình chắp đoạn ngắt liên tiếp (aggregation intervals).
* Giải lỗi kẹt quyền hạn tại sổ sách do xỉn quyền sai lệch và khai kích billing hụt từ thẻ (activation).
* Trị thành tựu báo mã lỗi giới hạn deploy (deploy failures) bắt phải yêu cầu (request adjustments) hạn mức trần.
* Ổn định và tinh thông mảng lịch hẹn (DLM schedules)/ giữ lệnh bảo lưu tài nguyên theo nhu cầu, điều tiết được tài nguyên lưu cũng như tối hóa độ phục hồi tương thích giá của thiết bị lưu trữ.


