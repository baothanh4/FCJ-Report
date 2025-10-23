---
title: "Đề Xuất Dự Án"
date: 2025-09-07
weight: 2
chapter: false
pre: " <b> 2. </b> "
---

# Hệ Thống Dịch Vụ Đường Sắt Đô Thị — Kiến Trúc AWS An Toàn, Mở Rộng và Tối Ưu Chi Phí

### 1. Giới thiệu
Khi Thành phố Hồ Chí Minh phát triển nhanh chóng, hệ thống giao thông đô thị đang đối mặt với tình trạng tắc nghẽn và ô nhiễm môi trường. Dự án Đường sắt đô thị được triển khai nhằm cung cấp một giải pháp giao thông thông minh, bền vững và hiệu quả, góp phần giảm sự phụ thuộc vào phương tiện cá nhân.  
Để đảm bảo tính tin cậy và an toàn, đề xuất này giới thiệu kiến trúc hạ tầng số dựa trên **AWS Cloud**, hỗ trợ các chức năng như đặt vé, thanh toán, quản lý lịch trình và phân tích vận hành — tất cả đều hoạt động trong mô hình **serverless**, tiết kiệm chi phí và thân thiện với người mới bắt đầu.

---

### 2. Mục tiêu
* **Mục tiêu chung:**  
Phát triển nền tảng số an toàn, có khả năng mở rộng và thân thiện với người dùng cho hệ thống Đường sắt đô thị.

* **Mục tiêu cụ thể:**  
    + Xây dựng kiến trúc AWS serverless để tối ưu chi phí và khả năng mở rộng linh hoạt.  
    + Hỗ trợ hệ thống **vé điện tử**, **đặt lịch trực tuyến**, và **cập nhật thời gian thực**.  
    + Bảo vệ dữ liệu hành khách bằng **mã hóa**, **IAM**, và **WAF**.  
    + Thiết lập hệ thống **giám sát và cảnh báo tự động** nhằm đảm bảo độ tin cậy khi vận hành.

---

### 3. Phạm vi
+ **Địa điểm triển khai:** Tuyến Metro số 1 TP.HCM (Bến Thành – Suối Tiên)  
+ **Đối tượng sử dụng:** Hành khách, nhân viên vận hành và ban quản lý  
+ **Thời gian:** 12 năm (từ khi triển khai đến vận hành)  
+ **Giới hạn:** Giai đoạn 1 tập trung vào các chức năng đặt vé, thanh toán và quản lý lịch trình; các tính năng IoT tự động hóa và phân tích dự đoán sẽ được mở rộng ở giai đoạn sau.

---

### 4. Kiến trúc AWS Cloud

* **Lớp Bảo mật (Security Layer)**  
    * **AWS WAF & AWS Shield** – Bảo vệ API và endpoint khỏi các tấn công (SQLi, XSS, DDoS).  
    * Đảm bảo mọi kết nối đều sử dụng giao thức HTTPS an toàn.

* **Lớp API & Xác thực (API & Authentication Layer)**  
    * **Amazon API Gateway** – Cổng vào cho ứng dụng web/mobile, điều hướng yêu cầu đến backend.  
    * **Amazon Cognito** – Quản lý đăng nhập, đăng ký, khôi phục mật khẩu, và JWT token.  
    * Đảm bảo quyền truy cập được kiểm soát và xác thực danh tính người dùng.

* **Lớp Backend (Serverless Layer)**  
    * Mỗi chức năng chạy trong **VPC riêng biệt** để tăng bảo mật và kết nối với tài nguyên nội bộ.  
    * **AWS Lambda Functions:**  
        * *Ticket Booking Lambda* – Xử lý tạo vé, xác thực và sinh mã vé.  
        * *Train Schedule Lambda* – Quản lý và cập nhật lịch trình tàu.  
        * *Payment Lambda* – Tích hợp với các cổng thanh toán bên thứ ba (VNPay, Momo).  
        * *Notification Lambda* – Gửi email hoặc tin nhắn xác nhận cho người dùng.  
    * Chi phí trung bình hàng tháng cho Lambda: khoảng **15 USD** (bao gồm Free Tier).

* **Lớp Dữ liệu (Data Layer)**  
    * **Amazon RDS (SQL Server)** – Lưu thông tin hành khách, vé và lịch trình.  
    * **Amazon DynamoDB** – Xử lý dữ liệu tốc độ cao như trạng thái tàu hoặc số ghế trống theo thời gian thực.  
    * Dữ liệu được **mã hóa bằng khóa KMS** để đảm bảo tuân thủ bảo mật.

* **Lớp Quản lý Bí mật & Mã hóa (Secret & Encryption Layer)**  
    * **AWS Secrets Manager** – Lưu trữ an toàn các thông tin nhạy cảm (API key, chuỗi kết nối DB, mật khẩu).  
    * **AWS KMS (Key Management Service)** – Quản lý khóa mã hóa cho S3, RDS và Lambda.  
    * Đảm bảo không có thông tin bí mật nào được lưu ở dạng rõ trong mã nguồn.

* **Lớp Lưu trữ & Sao lưu (Storage & Backup Layer)**  
    * **Amazon S3** – Lưu trữ giao diện web (React/Angular), dữ liệu backup, log và hóa đơn tải lên.  
    * **Chính sách Lifecycle** tự động chuyển dữ liệu cũ sang **S3 Glacier** để giảm chi phí.  
    * Chi phí ước tính: **khoảng 5 USD/tháng**.

* **Lớp Giám sát & Cảnh báo (Monitoring & Alerting Layer)**  
    * **Amazon CloudWatch** – Theo dõi log Lambda, chỉ số API Gateway, và tỷ lệ lỗi hệ thống.  

* **Phân tích dữ liệu & Báo cáo (Giai đoạn 2)**  
    * **Amazon Athena** – Tạo bảng phân tích về lượng hành khách, hiệu suất tuyến và thống kê thanh toán.

![Sơ đồ kiến trúc hệ thống AWS Metro Train](/images/2-Proposal/aws_metropolitano_train_service.drawio.png)

---

### 5. Kế hoạch triển khai
* **Tuần 1–2:** Cấu hình hạ tầng AWS (S3, API Gateway, Lambda, RDS, DynamoDB)  
* **Tuần 3–4:** Xây dựng chức năng **đặt vé điện tử** và **xác thực người dùng bằng Cognito**  
* **Tuần 5–6:** Kích hoạt **CloudWatch**, thiết lập dashboard giám sát và cấu hình bảo mật WAF  

---

### 6. Ngân sách & Nguồn lực
* **Tổng chi phí ước tính:** ≈ **100 USD/tháng**  
* **Công cụ tối ưu hóa chi phí:** AWS Cost Explorer, Auto Scaling, và Free Tier  
* **Thành phần đội ngũ:**  
    * Kiến trúc sư AWS Cloud  
    * Lập trình viên Backend (Lambda/API)  
    * Lập trình viên Frontend  
    * Kỹ sư vận hành & bảo trì Metro  

---

### 7. Kết quả mong đợi
* Giảm ùn tắc giao thông và ô nhiễm không khí.  
* Hệ thống **vé điện tử không tiền mặt** được vận hành trên AWS.  
* Hạ tầng số **an toàn, dễ mở rộng và tiết kiệm chi phí**.  
* Nâng cao sự tiện lợi cho hành khách và tính minh bạch trong vận hành.  
* Chuyển giao kiến thức và kỹ năng về công nghệ AWS cho đội ngũ nội bộ.  

---

### 8. Kết luận
Hệ thống Dịch vụ Đường sắt Đô thị được triển khai trên nền tảng **AWS Cloud** mang lại một kiến trúc **an toàn, linh hoạt và tiết kiệm**, tạo tiền đề cho quá trình hiện đại hóa giao thông đô thị.  
Bằng việc tận dụng **AWS Lambda, API Gateway, RDS, Cognito và CloudWatch**, hệ thống duy trì mô hình **serverless hoàn toàn**, giúp giảm chi phí vận hành và dễ dàng mở rộng sang các sáng kiến **Smart City** trong tương lai.
