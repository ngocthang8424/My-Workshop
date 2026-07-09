---
title: "Nhật ký công việc Tuần 9"
date: 2026-06-14
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

### Mục tiêu tuần 9
* Cài đặt môi trường lập trình (development environment) bằng công cụ bổ trợ AWS Toolkit cho VS Code.
* Nghiên cứu tính đồng bộ danh tính người dùng và các biểu đồ cấp quyền với dịch vụ trung tâm thẻ nhận diện IAM (AWS IAM Identity Center - SSO).
* Đúc kết bản sao thiết kế và biểu diễn họa đồ chi tiết cụm kiến trúc kiến thiết hạ tầng dự án tốt nghiệp (capstone project architecture diagram).
* Tiếp tục hoàn chỉnh và lập vòng lặp nâng cao những phân loại mô-đun để tiến tới kỳ tích cho dự án (Capstone) vào thời hạn chót cuối kỳ.

### Các công việc cần triển khai trong tuần này
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | Khơi môi trường bằng AWS Toolkit trên máy với trình IDE VS Code:<br>- Nhúng gói cài và tinh chỉnh cài đặt bộ AWS Toolkit trong trình VS Code.<br>- Tìm hiểu sâu cách đi tắt thông tin từ máy chạm cấu hình vùng AWS để hiển thị các luồng nhánh resource vây quanh IDE.<br>- Xuất triển khai test báo lỗi (debug), cấu hình code tại serverless cùng quản lý luồng AWS mà chưa cần ra khỏi IDE. | 09/06/2026 | 09/06/2026 | AWS Toolkit for VS Code User Guide |
| 3 | Đồng hóa quyền nhân danh qua cấu trúc Sign-On của AWS:<br>- Khai thông đường ngạch IAM Identity Center (truyền thống là SSO) phân khu vùng mỏ cấp quản lý cho đối tượng tham gia truy cập chung.<br>- Tái cài định vùng tập cấp quyền (permission sets) cho vùng tài khoản được quy hoạch.<br>- Log thẳng thông qua nhánh liên thông SSO (federated access) trên các hạ tầng trực tiếp AWS cung cấp. | 10/06/2026 | 10/06/2026 | AWS IAM Identity Center Documentation |
| 4 | Đúc Đồ Hình Tổng Quang cho Đồ Án Cuối Khóa:<br>- Tạo bản đồ ánh xạ hạ tầng frontend/backend cùng quá trình ứng dụng Trí Tuệ Nhân Tạo (AI processing), nền lưu kho và không để quên hệ cảnh giới theo dõi (monitoring layers).<br>- Tầm quét bao quát mọi giới tuyến, chu trình gửi dữ liệu, chặn trạm bảo mật an ninh khu tiếp nhận máy lưu server.<br>- Trình ấn bản họa hình hạ tầng mẫu trọn vẹn cho phần dự án AI Upscaler (Đồ Án Siêu Tăng Kích Ảnh AI). | 11/06/2026 | 11/06/2026 | — |
| 5 | Tiến Rút Đoạn Kết - Nghiệm Thu Đồ Án Cuối Khóa:<br>- Tiến mạnh đi thẳng vào code cốt lõi từ bảng mẫu họa đồ bản phác.<br>- Đan ghép cơ trạm xác thực đăng nhập (auth), cổng dẫn (API) tới kho tiếp nhận trạm trung chuyển (storage).<br>- Hoàn lại bài cũ và kiểm kê lần lượt những thành quả trước đợt đồ án (như cài mới VPC, rào mạng IAM, rà lỗi log monitor). | 12/06/2026 | 12/06/2026 | — |
| 6 | Tiếp Tục Nâng Tầm Đồ Án Đích Cuối Kì:<br>- Tạo lực bẩy cho khâu AI học máy (AI processing) luyên mượt mã hậu phương Backend thông tuệ theo dòng truyền việc (workflows).<br>- Giám kịch test tổng toàn hệ từ nguồn tới đích (end-to-end flows).<br>- Định dạng chuẩn lộ trình đọ sát lại thành tích qua mỗi đợt chốt chặn kiểm thu đồ án đã lên lịch sẵn. | 13/06/2026 | 14/06/2026 | — |

![Cấu Trúc Hạ Tầng Đồ Án Trọng Đạt - Siêu Phân Giải Ảnh AI (AI Upscaler)](/images/week9/project-architecture-ai-upscaler.png)
*Biểu Tượng Hình Phân Giải: Hệ lưới chặn WAF → Rẽ tuyến đường CloudFront → Hosting thông qua Amplify (bằng Next.js); Tường đăng nhập Cognito → Giao liên trọng tải ALB → Hệ xử lý ảo máy EC2 (Code FastAPI backend); Hệ khay AI phụ bao trọn (SQS làm tin báo bưu phẩm, Rekognition nhận dạng khuôn thâm, SageMaker là nguồn chúa tể render, đóng gói với serverless Lambda functions); Trữ vào kho lưu như S3, dùng bộ cơ sở truy vấn lẹ làng qua DynamoDB và hệ nhớ tạm qua ElastiCache; Luôn được mã hóa các điểm vào với Secrets Manager báo tin sự cố qua đám mây CloudWatch Alerts.*

### Kết quả đạt được tuần 9

**Kiến thức**
* Hiểu bộ hỗ trợ phát triển điện toán AWS Toolkit làm trơn luồng mượt code và tối ưu từ ngay cấp trình IDE (VS Code).
* Mở khóa mảng quyền hạn đăng kí người sử dụng tổng quát cấp multi-account nhờ hệ chức năng tổng quản IAM Identity Center (truyền thống tên AWS SSO).
* Vạch định rành rõ hạ tầng của một siêu dự án (Capstone) vào phần đồ hình lớp thứ cấp: UI frontend, khối ngầm API hạch tâm backend, mảng quy hoạc cấu dữ liệu cho trí tuệ nhân tạo (AI processing), trạm lót data tạm rồi tới vùng giám hành hệ Cloud.
* Trích đường luồng mạch dẫn gói dữ kiện, bắt đầu bởi truy vấn trạm user thông nối sang cửa kiểm ngạch Web tường lửa (WAF), trượt phân mảng lưới toàn cầu (CloudFront), hạ tới mã ngầm Backend sau rùng tới dàn đường ống xử lý kỹ năng học máy đồ sộ AI Pipeline.

**Kỹ năng thực hành**
* **Mở trạm VS Code:** Truy xuất IDE móc tròng lên dịch vụ khu AWS, tự lật bảng mục lục tài sản dịch vụ (resources), ứng nghiệm kịch bản debug-deploy tại chỗ chưa từng trải nghiệm qua console AWS truyền thống.
* **Mạng SSO / IAM Identity Center:** Nắn nót lại một bộ quyền giới phân ban cho cấp quản trị, xuất file cấu thử qua liên mạch truy vấn kiểm duyệt xác nhận đăng nhập qua luồng bảo hộ.
* **Xây Dựng Hình Kiến Trúc:** Mô tả sắc sảo lên sơ đồ luồng luân chuyển mô đun siêu dự án của tôi. Hết sức vinh dự là đã liệt kê rất nhiều cựu thần chiến trận mảng AWS (như tường lửa máy thủ - WAF, Cụm giao mạng CDN - CloudFront, AWS Amplify, Cognito xác thực, ALB loadbalancers cân bằng trọng tả, máy EC2, AWS SageMaker máy học nhân tạo, Cloud hệ thống khối S3, Dynamo DB tốc độ bàn thờ và CloudWatch mắt tuệ giác).
* **Bắt Mạch Dự Án Đồ Án:** Nhấn nốt những khung kiến trúc xương cá bằng bản ngã code tự phát triển thông qua mảng mấu họa hình sơ đồ mạng nãy giờ.

**Giải quyết vấn đề**
* Đánh gãy rắc rối credential lằng nhằng hoặc đụng trạng profile lúc chuyển tài khoản (switching accounts) / đổi khu (regions) mảng mã trạm trực tiếp ở giao thức AWS Toolkit tại VS Code IDE.
* Va bóp đắp lỗi sập chặn mảng cấp quyền ở SSO bằng cách nới chỉnh các file cấu đặc quyền sets quyền tham nhượng trong nhánh tài khoản phân chia.
* Đồng nhất thiết kế và khả thi khả thi để cấu vào điều kiện khuôn giới (tiết giảm nợ phí (cost), hạn ngạch giới định (quotas) cùng thói quen của người thiết lập vận dụng AWS services trứ danh).
* Tách việc tạo dựng và xé nhỏ lớp kiến trúc từ sơ đồ vạn chưởng nhằm đạt tới triển hạn trơn tru qua mô típ nhỏ nhẹ, từng mảng triển khai khớp theo hệ diagram thiết họa lúc sáng tạo thiết đồ án.


