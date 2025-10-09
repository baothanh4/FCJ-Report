---
title: "Proposal"
date: 2025-09-07
weight: 2
chapter: false
pre: " <b> 2. </b> "
---


# Hệ thống dịch vụ đường sắt Metropolitano với AWS: Kiến trúc đám mây có khả năng mở rộng và tối ưu hóa chi phí cho giao thông đô thị thông minh


<!-- ## A Unified AWS Serverless Solution for Real-Time Weather Monitoring -->

### 1.Giới thiệu
Trong bối cảnh Thành phố Hồ Chí Minh tiếp tục đô thị hóa nhanh chóng, ùn tắc giao thông và ô nhiễm không khí đã trở thành những thách thức nghiêm trọng. Phương tiện cá nhân chiếm ưu thế trong giao thông, gây quá tải cho các tuyến đường hiện có và làm giảm hiệu quả di chuyển. Để giải quyết vấn đề này, một hệ thống đường sắt Metropolitano hiện đại đang được phát triển để cung cấp giao thông công cộng an toàn, nhanh chóng và bền vững.
Đề xuất này nêu rõ cáchDịch vụ web của Amazon (AWS)sẽ được sử dụng để xây dựng cơ sở hạ tầng kỹ thuật số của hệ thống — tập trung vào dịch vụ đám mây cốt lõi và thân thiện với người mới bắt đầu để đạt được độ tin cậy, bảo mật và hiệu quả về chi phí



### 2. Mục tiêu
* <b>Mục tiêu chung:</b>
Thiết lập một hệ thống Metropolitano thông minh, hiệu quả và bền vững nhằm cải thiện khả năng di chuyển trong đô thị và giảm tắc nghẽn giao thông.
* <b>Mục tiêu cụ thể:</b>
    + Xây dựng Tuyến Metropolitan số 1(19,7 km) nối ga Bến Thành và ga Suối Tiên.
    + Giảm việc sử dụng xe cá nhân bằng cách 20% trong vòng 5 năm
    + Thực hiện một hệ thống bán vé điện tử an toàn, không dùng tiền mặt có thể truy cập qua điện thoại di động/web.
    + Sử dụng Dịch vụ đám mây AWS để quản lý dữ liệu hành khách, đảm bảo an toàn vận hành và nâng cao trải nghiệm du lịch

### 3. Phạm vi
+ Vị trí: Ho Chi Minh City, Line 1 — Ben Thanh → Suoi Tien
+ Đối tượng người dùng: Người dân, người đi làm và khách du lịch
+ Khoảng thời gian: 12 năm (từ nghiên cứu khả thi đến khi đưa vào vận hành)
+ Hạn chế:Tập trung vào cơ sở hạ tầng đô thị và tích hợp AWS thiết yếu. Vận tải trung chuyển và tự động hóa IoT sẽ được đề cập trong các giai đoạn sau.


### 4. Kiến trúc đám mây AWS
* Lớp Frontend (Phía máy khách)
    * Ứng dụng web (React / Angular) Và Ứng dụng di động(dành cho hành khách và nhân viên).
    * Cả hai đều giao tiếp với phần phụ trợ thông qua Điểm cuối API HTTPS.
    * Dịch vụ AWS:
        * Amazon S3– Lưu trữ các tài sản giao diện tĩnh (HTML, JS, CSS).(~5$/tháng)
        * Amazon CloudFront(tùy chọn) – Tăng tốc độ phân phối nội dung trên toàn cầu. (~10$/tháng)
* Lớp Backend (Dịch vụ ứng dụng)
    * Cổng API của Amazon– Điểm vào cho tất cả các yêu cầu API của khách hàng. (10$/tháng)
    * AWS Lambda– Xử lý logic kinh doanh với giá (15$/tháng):
        * Đặt vé và lên lịch
        * Giao dịch thanh toán
        * Thông báo (email/SMS)
    * Amazon Cognito– Xác thực người dùng và quản lý vai trò (Quản trị viên, Nhân viên, Hành khách) (5$/tháng).
* Lớp dữ liệu
    * Amazon RDS (PostgreSQL)– Lưu trữ dữ liệu có cấu trúc (hành khách, vé, lịch trình).(100$/tháng)
    * Amazon DynamoDB– Lưu trữ dữ liệu hoạt động tàu theo thời gian thực (trạng thái tàu, tình trạng chỗ ngồi).(20$/tháng)
    * Amazon S3– Lưu trữ bản sao lưu, báo cáo và nhật ký. (5$/tháng)
*  Lớp giám sát và phân tích
    * Amazon CloudWatch– Thu thập số liệu hệ thống, nhật ký ứng dụng và cảnh báo lỗi. (5$/tháng)
    * Keo AWS + Athena– Chuyển đổi dữ liệu và truy vấn để phân tích. (15$/tháng)
    * Amazon QuickSight– Bảng thông tin chi tiết về hoạt động và quản lý. (18$/tháng)
*  Lớp bảo mật và mạng
    * AWS WAF– Bảo vệ các điểm cuối API khỏi các cuộc tấn công web phổ biến (SQLi, XSS).
    * Lá chắn AWS– Bảo vệ DDoS cho các điểm cuối công cộng.
    * Amazon VPC– Cô lập phần phụ trợ và cơ sở dữ liệu trong một mạng riêng an toàn.
    * AWS IAM– Quản lý vai trò nội bộ và quyền truy cập.
        * Chi phí ước tính hàng tháng:Tổng cộng ~$8 cho WAF + Shield (các gói khác miễn phí).
![IoT Weather Station Architecture](/images/2-Proposal/AWS-Architecture.png)

### 5. Implementation Plan
* Tuần 1-2: Cấu hình cơ sở hạ tầng cốt lõi của AWS (S3, API Gateway, Lambda, RDS)
* Tuần 3–4: Xây dựng hệ thống vé điện tử và xác thực với Cognito
* Tuần 5–6: Kích hoạt CloudWatch, bảng điều khiển và bảo mật WAF/Shield
### 6. Ngân sách và Nguồn lực
* Tổng chi phí đám mây ước tính:≈211 đô la Mỹ/tháng(~1.266 đô la Mỹ/năm)
* Công cụ tối ưu hóa:AWS Cost Explorer, Auto Scaling và sử dụng Free Tier khi có thể.
* Thành phần đội:
    * Kiến trúc sư đám mây
    * Nhà phát triển Backend (Lambda/API)
    * Nhà phát triển giao diện người dùng
    * Kỹ sư vận hành và bảo trì tàu điện ngầm
### 7. Kết quả mong đợi
* Giảm tắc nghẽn giao thông và ô nhiễm không khí
* Hệ thống bán vé điện tử không dùng tiền mặt được hỗ trợ bởi AWS
* Nền tảng số an toàn, có khả năng mở rộng cho sự mở rộng trong tương lai
* Nâng cao sự tiện lợi cho hành khách và tính minh bạch trong hoạt động
* Chuyển giao kiến ​​thức và phát triển kỹ năng trong công nghệ AWS

### 8. Kết luận
Các Hệ thống đường sắt Metropolitano tích hợp với Cơ sở hạ tầng đám mây AWS đại diện cho bước tiến hướng tới giao thông bền vững tại Thành phố Hồ Chí Minh.
Bằng cách áp dụng các dịch vụ cốt lõi của AWS (API Gateway, Lambda, RDS, S3, Cognito, CloudWatch), hệ thống vẫn đơn giản, tiết kiệm chi phí và an toàn.
Các giai đoạn tương lai có thể kết hợp IoT, AI/ML và phân tích dự đoán để tối ưu hóa khi hệ thống nền tảng ổn định.
