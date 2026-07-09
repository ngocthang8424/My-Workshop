---
title: "Nhật ký công việc Tuần 10"
date: 2026-06-20
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Mục tiêu tuần 10
* Quản lý phân quyền với ranh giới quyền IAM (IAM permission boundaries) nhằm đặt giới hạn mức quyền cao nhất có thể cấp.
* Áp dụng khả năng kiểm soát độ ưu tiên quyền thông qua biểu đồ policies IAM và điều kiện khóa quy nhập (condition keys) tạo cấu trúc ủy quyền dựa trên ngữ cảnh (context-aware authorization).
* Liên kết rành mạch sơ đồ chính sách cấp Role IAM sang kiến trúc đồ án tốt nghiệp (bao phủ Cognito, EC2, Lambda, S3, và những dịch vụ có dính líu).
* Tiến lại tiếp chặng áp dụng dự án đồ án tới bến cuối qua mô típ bảo mật đặc quyền thấp nhất (least-privilege) bám đúng mô phỏng bảng cấu trúc gốc ban đầu.

### Các công việc cần triển khai trong tuần này
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | Quản Trị Đặc Quyền Với Quyền Ranh Theo Biên (Permission Boundaries):<br>- Gắn và cấu trúc quy hoạch tính năng permission boundaries cho nhóm user lẫn tổ nhóm vai quản trị (roles).<br>- Phân tích hiệu ứng cấp hiệu dụng và cách thức hoạt hạn cấp quyền gắt gao giữa danh tính identity policies với permission boundaries.<br>- Code test độ an toàn và ngưng quyền tác nghiệp ngoại lai. | 15/06/2026 | 15/06/2026 | IAM Permissions Boundaries Guide |
| 3 | Điều Tiết Uy Quyền Thông Qua Tập Lệnh Policies Cùng Tham Số (Conditions):<br>- Viết khung policies IAM ràng bằng các thẻ `Condition` theo cấu khối (ví dụ tags, chặn source IP, MFA, nhận diện resource ARN...).<br>- Khợp luật (allow/deny) nhằm khuấy giới hạn mức trần cấp độ giới nghiêm truy cập trong vòng dự án.<br>- Tính an toàn bảo mật least-privilege sẽ liên tục được thẩm tra mô phỏng hoặc lấy tài khoản test thử. | 16/06/2026 | 16/06/2026 | IAM Policy Elements Reference |
| 4 | Dóng Lớp Thiết Cấu Họa Hình Vào Đồ Án Kì – Tầng IAM:<br>- Đặc cách chỉ ra roles đúng chuẩn chỉ cho từng cỗ máy (EC2 / FastAPI), nhánh ngầm Lambda, tổ hợp máy học SageMaker đi khớp sơ đồ đồ án (AI Upscaler).<br>- Co hẹp phạm vị quyền tác oai của hòm mạng S3, DynamoDB, SQS (tin hòm) và rương mã khóa Secrets Manager xuống hạn thấp nhất có thể.<br>- Quy nạp cấu hình cổng nhận diên Cognito và luồng hậu kiểm vào đúng vách phân API backend. | 17/06/2026 | 17/06/2026 | — |
| 5 | Gấp Rút Tiến Trình – Khởi Triển Khai Độ Bảo Mật:<br>- Khớp lệnh ranh quyền boundaries vào cụm projects roles tinh vi.<br>- Chạy nghiệm liên hoàn mạch dòng chảy cấp quyền tin cậy IAM: WAF → CloudFront → Amplify → Cognito → ALB → EC2.<br>- Test bảo mạng truy thu cơ sở luồng lưu trữ qua liên tiếp khâu API và vùng dữ kiện. | 18/06/2026 | 18/06/2026 | — |
| 6 | Gấp Rút Tiến Trình – Chốt Cuối & Hoàn Lặp Hồi Cứu Kiến Trúc:<br>- Gia cứng bảo an tổ đội Lambda và vòi nhánh máy trí tuệ nhân tạo (SQS, Trí tuệ Thị giác Rekognition, AI SageMaker).<br>- Đọc lại đặc quyền xem có lỗi chệnh quan giới để mảng Secret Manager cùng Mắt Mây CloudWatch lượm tin hoạt động.<br>- Cập nhật ghi chú kĩ việc sử quyết các chốt chặn IAM rải khắp sơ đồ mạng đồ tạo. | 19/06/2026 | 20/06/2026 | — |

### Kết quả đạt được tuần 10

**Kiến thức**
* Hiểu sâu công năng thiết đặt ranh giới kềm hãm nấc thang quyền (permission boundaries) làm mức trần trói lại bộ IAM identities.
* Vận rành cách thả mồi điều kiện cấp quyền IAM sử dụng mã cấu hình tags, chặn quyền trỏ nhánh resource, và cách nạp bối cảnh bảo an context-aware access.
* Vạch định rành rõ hạ tầng của luồng đi IAM đắp ghép theo mô hình đồ họa (AI Upscaler).
* Nẹp khung móng tư tưởng an mật thấp điểm truy quét (least-privilege) ngay quá trình kết mạng người Cognito qua tuyến AI, mạng trạm, mạng lưu data.

**Kỹ năng thực hành**
* **Trạm Khóa Ranh Quyền Boundaries:** Chào đời những trạm biên chặn và thực diễn được thành trạng qua các nhóm test roles.
* **Cụm Lệnh Ban (Policies) & Giải Thuật (Conditions):** Sáng tác tự tại và code nghiệm thử trơn tru bảng mã `Condition` ứng đối bối cảnh ngoài hiện thực.
* **Tầng Họa Sơ Đồ IAM Đồ Án:** Tức tốc áp chế mô men sơ đồ mạng Tuần 9 vô mảng role kĩ sư để cấp xuống khu nhậm S3, DynamoDB, tới Lambda Cognito.
* **Thành Tiết Đồ Án:** Hoàn ứng và phân tách ứng dụng kèm thành tố theo quy định ranh quyền nghiêm phòng chặt có khóa policy móc kèm.

**Giải quyết vấn đề**
* Đập ngưng chặn ván truy cập lỗi thừa thả rông qua bước tách rời giới lộ IAM Identity, dải quyền boundary rào giậu đi riêng ra tách với policies lõi.
* Hạ bệ hàng loạt nhầm nhọt mismatch điều kiện đi sai khung khóa (wrong key, bấn tên tag, đi lạc đường khai ARN) làm sinh từ chối lỗi rát ngẫu hứng.
* Hòa lưới hàng chuỗi roles công sở phục vị theo tuyến AI quy mô lớn lách khéo khỏi ngạch lấn cướp dải mây (privilege creep) chéo quàng quyền giữa 3 chân vạc máy SageMaker, nhánh EC2, và ống mây ngầm Lambda.


