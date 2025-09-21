---
title: "Worklog Tuần 2"
date: 2025-09-07
weight: 1
chapter: false
pre: " <b> 1.2. </b> "
---
<!-- {{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}} -->


### Mục tiêu tuần 2:

* Học về Amazon RDS,AWS S3, AWS EC2 Auto Scaling, AWS DynamoDB và Amazon LightSail.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Tìm hiểu AWS DynamoDB,AWS RDS,Amazon Aurora <br>-**Practice:**<br>&emsp; +Tạo AWS CloudFront và AWS S3 tập                                                                                             | 14/09/2025   | 15/09/2025      |<https://render.skillbuilder.aws/?module_id=B1DGAV8S16%3A001.000.000&product_id=8D79F3AVR7%3A002.000.000&registration_id=c9de1df5-b12f-5abf-84c4-aac56a36dcae&navigation=digital&parentId=Y4YASRJEVX>
| 3   | -**Thực hành:**<br>&emsp;+Tạo AWS RDS <br>&emsp;+Tạo DynamoDB bằng cách sử dụng Python và AWS CLI                                                | 15/09/2025   | 16/09/2025      | <https://render.skillbuilder.aws/?module_id=B1DGAV8S16%3A001.000.000&product_id=8D79F3AVR7%3A002.000.000&registration_id=c9de1df5-b12f-5abf-84c4-aac56a36dcae&navigation=digital&parentId=Y4YASRJEVX> |
| 4   | - Dịch blog  | 13/08/2025   | 13/08/2025      | <https://cloudjourney.awsstudygroup.com/> |
| 5   | - Tìm hiểu EC2 Auto Scaling cơ bản, điện toán đơn giản hóa cùng Amazon LightSail <br> - **Thực hành:** <br>&emsp; +Tạo Database trong AWS RDS  <br>&emsp;+Sử dụng Amazon LightSail               | 19/09/2025   | 20/09/2025      | <https://000005.awsstudygroup.com/> <br> <https://000045.awsstudygroup.com/>  |
| 6   | - **Thực hành:** <br>&emsp; + Tạo RDS, VPC, EC2 cùng dịch vụ AWS EC2 Auto Scaling                      | 20/09/2025   | 21/09/2025      | <https://000006.awsstudygroup.com/> |


### Kết quả đạt được tuần 2:

* Lưu trữ và triển khai websites tĩnh với Amazon S3: 
  * Biết cách tạo bucket S3, tải file lên và quản lý quyền truy cập.
  * Biết cách bật tính năng Static Website Hosting cho bucket. 
  * Học cách cấu hình quyền public để website có thể truy cập qua Internet.
  * Học cách cấu hình Bucket policy để chỉ cho phép truy cập đọc công khai.

* Cơ sở dữ liệu thiết yếu cùng với Amazon Relational Databases Services:
  * Hỗ trợ nhiều engine phổ biến như MySQL,PostgreSQL,Oracle, và SQL Server.
  * Học cách kết nối đến RDS từ EC2.
  * Hiểu về endpoint, port,username/password để truy cập DB.
  * Học cách sử dụng VPC, subnet, security group để bảo vệ RDS instance. 


* Ứng dụng mở rộng quy mô với EC2 Auto Scaling:
  * Là dịch vụ giúp tự động tăng hoặc giảm số lượng Amazon EC2 instance dựa trên nhu cầu ứng dụng.
  * Thành phần của Auto Scaling:
    * Launch Configuration/ Launch Template
    * Auto Scaling Group(ASG)
    * Chính sách mở rộng: Dynamic Scaling và Schedule Scaling
    * Health checks
  * Dựa vào Amazon CloudWatch để thu thập metrics như: CPU utilization, network traffic, request const.





