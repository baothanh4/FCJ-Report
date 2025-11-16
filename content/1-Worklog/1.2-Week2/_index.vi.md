---
title: "Tuần 2 Worklog"
date: 2025-09-07
weight: 1
chapter: false
pre: " <b> 1.2. </b> "
---

### Mục tiêu Tuần 2:

* Tìm hiểu về Amazon RDS, AWS S3, AWS EC2 Auto Scaling, AWS DynamoDB và Amazon LightSail.

### Công việc thực hiện trong tuần:
| Ngày | Công việc                                                                                                                                                                                                   | Ngày bắt đầu | Ngày kết thúc | Tài liệu tham khảo                        |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------- | --------------- | ----------------------------------------- |
| 2   | - Học **AWS DynamoDB**, **AWS RDS**, **Amazon Aurora** <br>- **Thực hành:**<br>&emsp; + Tạo **AWS CloudFront** và **AWS S3**                                                                                                   | 14/09/2025 | 15/09/2025      | <https://render.skillbuilder.aws/?module_id=B1DGAV8S16%3A001.000.000&product_id=8D79F3AVR7%3A002.000.000&registration_id=c9de1df5-b12f-5abf-84c4-aac56a36dcae&navigation=digital&parentId=Y4YASRJEVX/> |
| 3   | - **Thực hành:**<br>&emsp; + Tạo **AWS RDS** <br>&emsp; + Tạo **DynamoDB** sử dụng Python và AWS CLI                                            | 15/09/2025 | 16/09/2025      | <https://render.skillbuilder.aws/?module_id=B1DGAV8S16%3A001.000.000&product_id=8D79F3AVR7%3A002.000.000&registration_id=c9de1df5-b12f-5abf-84c4-aac56a36dcae&navigation=digital&parentId=Y4YASRJEVX> |
| 4   | - Dịch Blog | 13/08/2025 | 13/08/2025      | <https://cloudjourney.awsstudygroup.com/> |
| 5   | - Học cơ bản về **EC2 Auto Scaling**, **Simplified Computing với Amazon LightSail** <br> - **Thực hành:** <br>&emsp; + Tạo Database trong **AWS RDS**  <br>&emsp; + Sử dụng **Amazon LightSail**                           | 19/09/2025 | 20/09/2025      | <https://000005.awsstudygroup.com/> <br> <https://000045.awsstudygroup.com/> |
| 6   | - **Thực hành:** <br>&emsp; + Tạo **RDS**, **VPC**, **EC2** với **AWS EC2 Auto Scaling**                                                                                     | 20/09/2025 | 21/09/2025      | <https://000006.awsstudygroup.com/> |


### Thành tựu Tuần 2:

* **Hosting Website tĩnh với Amazon S3:** 
  * Biết cách tạo bucket S3, upload file và quản lý quyền truy cập.
  * Biết cách bật chế độ Static Website Hosting cho bucket.
  * Biết cách cấu hình public để website có thể truy cập qua Internet.
  * Biết cách thiết lập Bucket Policy để chỉ cho phép public đọc.

* **Cơ bản về Database với Amazon RDS:**
  * Hỗ trợ nhiều engine phổ biến như MySQL, PostgreSQL, Oracle, và SQL Server.
  * Biết cách kết nối từ RDS tới EC2.
  * Biết endpoint, port, username/password để truy cập database.
  * Biết cách tạo VPC, subnet, security group để bảo vệ instance RDS.

* **Mở rộng ứng dụng với EC2 Auto Scaling:**
  * Dịch vụ tự động tăng hoặc giảm số lượng EC2 instance dựa trên nhu cầu sản phẩm.
  * Các thành phần của Auto Scaling:
    * Launch Configuration / Launch Template
    * Auto Scaling Group (ASG)
    * Chính sách mở rộng: Dynamic Scaling và Scheduled Scaling
    * Health checks
  * Dựa vào Amazon CloudWatch để thu thập các chỉ số như CPU utilization, network traffic, request count.
