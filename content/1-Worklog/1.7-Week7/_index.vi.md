---
title: "Nhật ký công việc Tuần 7"
date: 2026-06-02
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Mục tiêu tuần 7
* Học phương pháp khai báo hạ tầng dạng code (Infrastructure as Code) thông qua AWS Cloud Development Kit (CDK).
* Áp dụng các khái niệm thư viện (constructs), nhóm ứng dụng (stacks) cũng như thiết lập triển khai mẫu CDK từ nền tảng ra chuyên sâu.
* Hoàn thành các phòng máy thực hành tại Chuỗi Lab Hạ Tầng Cơ Sở Code (Infrastructure as Code Workshop Series).
* Tối ưu hóa tải công việc EC2 với thủ pháp Right-Sizing cùng phân tích thông tin sử dụng tối ưu nguồn máy ảo.
* Đề xuất dự án tốt nghiệp cuối kì khóa học (xác nhận tiêu chí ban đầu, đề án hạ tầng kiến trúc và khoanh vùng AWS services được dùng).

### Các công việc cần triển khai trong tuần này
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | AWS CDK Cơ bản (Essentials):<br>- Cài và định cấu hình AWS CDK CLI rồi khởi chạy bộ môi trường (bootstrap).<br>- Định dạng cụm nhóm (app) và xuất các công cụ (ví dụ: S3, Lambda).<br>- Hiểu quá trình tổng hợp kết quả (synthesis `cdk synth`) cùng lệnh triển khai trực tiếp (`cdk deploy`). | 28/05/2026 | 28/05/2026 | AWS CDK Developer Guide |
| 3 | AWS CDK Nâng cao (Advanced):<br>- Thao tác chuyên sâu thư viện tài nguyên mốc cấp L2/L3, tham số bổ trợ và hệ thiết kế môi trường tham gia.<br>- Xếp đặt hệ quy mô multi-stack liên chiếu chéo thông tin cấp ứng dụng.<br>- Khảo sát quá trình tổng thể, đánh tag, và phương án xuất kho tối giản. | 29/05/2026 | 29/05/2026 | AWS CDK Advanced Workshop |
| 4 | Hội thảo Chuỗi IaC (Infrastructure as Code Workshop Series):<br>- So sánh kĩ phương thức mã IaC (giữa các khái niệm cơ chế của CloudFormation, CDK, Terraform).<br>- Lập và tu rèn cập nhật bản hạ tầng qua các đường truyền liên hoàn (pipelines).<br>- Đọc lại thông tin lỗi độ trượt kiến trúc (drift), tổ hợp chuyển hóa an toàn bản update. | 30/05/2026 | 30/05/2026 | AWS IaC Workshop Series |
| 5 | Tối ưu Kích Cỡ cùng Chức Năng Rút Trích Nguồn Máy Ảo EC2 (Right-Sizing):<br>- Đi sâu phân lập đồ hị lượng sử dụng CPU, RAM cùng dải mạng của hệ thiết bị EC2.<br>- Chỉ định tìm các vùng tài nguyên bị đôn tải máy trạm phí dư qua họ instance có ích cho chi phí.<br>- Đúc kết sự hài hòa về trao đổi tính linh động với giá cước thông qua quy chuẩn right-sizing. | 31/05/2026 | 31/05/2026 | AWS Compute Optimizer / EC2 Right-Sizing |
| 6 | Khởi động dự án tốt nghiệp của khóa đào tạo:<br>- Đặt định tiêu chuẩn, vẽ biểu mẫu architecture diagram, ấn định bộ dịch vụ AWS mục tiêu hoàn chỉnh để sử dụng. | 01/06/2026 | 02/06/2026 | — |

### Kết quả đạt được tuần 7

**Kiến thức**
* Hiểu sơ đồ chức pháp tổng quan của CDK: ứng dụng cụm tổng (app), nhóm đơn (stack), thư viện tái sử dụng (construct) và đường quy chiếu trực kết hướng tới cấu trúc CloudFormation.
* Tiếp thu thiết kế phát triển AWS CDK đa lớp cho module linh thiêng thiết lập tự động hóa theo loại hình môi trường đặc chủng.
* Tích lũy cứng cáp kĩ cương IaC: bản sao kiểm chứng chuẩn lưu hệ, hoạt động tải hệ nhiều lần không dứt nhưng lưu xuất bộ cập nhật thông minh được kiểm soát chi li sự thay đổi.
* Hiểu bộ đánh ký hiệu right-sizing của EC2 để từ đó ứng dụng tối hiệu trong kềm hãm thâm hụt tài chính cũng như bứt tốc băng thông truy nhập mạng cục bộ tốt hơn.
* Nhắm trúng mô hình dự án cấp chứng chỉ thông suốt kinh nghiệm hạ tầng, truyền tín hiệu an toàn, kĩ xảo đo tự động bằng các kỹ năng các khóa phía trước.

**Kỹ năng thực hành**
* **Nền CDK cơ bản:** Đã xuất thông tin boot (bootstrap) tự động một khu vực mạng; tổng kết phân tích tổng cấu trúc và xuất trơn tru lệnh khai sinh cụm CDK (deploy).
* **Nền CDK Nâng xa:** Liên kết trích dẫn và truyền thông số các cấu hình cụm tài nguyên song song, xử lý dữ liệu và gắn mẫu truyền hình thức chuyên nghiệp cho quá trình cài đặt nền CDK.
* **Chạy Lab IaC thực thụ:** Lấp ghép trọn vẹn quy chuẩn đường đời: định dạng file code → cài đặt hạ tầng mạng → điều chỉnh theo sự linh hoạt thay đổi để sẵn trớn thu bộ dữ liệu cấu hình lùi (rollback) an toàn.
* **EC2 Hữu Hiệu Hóa:** Trực tiếp dùng đồ thị và giải pháp thông minh tự giới thiệu được bộ xử lý đo kích cỡ tải cho máy trạm (Right-Sizing instances).
* **Dự Án Khóa Học:** Viết rõ đồ đề hệ dự án mang mục tiêu rõ và phác lại đúng cấu trúc sơ đồ dịch vụ AWS theo định mức ra đời bản giao cuối.

**Giải quyết vấn đề**
* Chữa nhanh chóng được cản báo cấm ủy quyền cấu hình lỗi (IAM permission errors) và boot hạ tầng đầu xuất với mảng môi trường lạ lẫm trên cấu hình CDK lúc khởi xướng.
* Hiệu chỉnh triệt hoàn các vấn đề lỗi báo cáo synthesis/lỗi truy xuất dữ kiện ở khối kết thuộc, và xử trị bất đồng nhất địa bàn cấp khu vực/máy trạm ở cấu hình chạy lệnh sai.
* Hiểu kĩ và lọc bỏ thông tin gây nhiễu và hạn chết CloudWatch metrics ngay quá trình đánh định hạng kích thước right sizing bị chèn thông số ảo liên thông từ hạ tầng test.
* Chiết lược mục tiêu mấu chốt thiết lập mốc đánh dự án tối thiểu hóa cấu trúc chức năng để đảm bảo cho một kế hoạch khả dĩ chạy nghiệm thu xuất sắc.


