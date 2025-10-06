---
title: "Worklog Tuần 4"
date: 2025-09-07
weight: 1
chapter: false
pre: " <b> 1.4. </b> "
---



### Mục tiêu tuần 4:

* Thực hành tạo, quản lý, và triển khai các tài nguyên AWS thông qua các công cụ khác nhau (Console, CLI, SDK, Elastic Beanstalk...).
* Xây dựng ứng dụng mẫu sử dụng Lambda, S3, DynamoDB, và API Gateway.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - **Pratice:** Tạo table trong AWS DynamoDB bằng cách sử dụng AWS CLI hoặc Python thông qua AccessKey                                                                                              | 28/09/2025   | 29/09/2025      |
| 3   | - **Thực hành:**Tạo book store bằng cách sử dụng Lambda, S3 và DynamoDB                                           | 30/09/2025   | 01/10/2025      | <https://000078.awsstudygroup.com/> |
| 4   | - Tìm hiểu về Json & Document Model| 01/10/2025   | 02/10/2025      | |
| 5   | - **Thực hành:** <br>&emsp;+ Sử dụng AWS Console để deploy và xác minh AWS resources bằng AWS CloudFormation template. <br>&emsp; + Sử dụng AWS Tools cho Eclipse IDE để triển khai 1 ứng dụng Java trong môi trường Elastic Beanstalk. <br>&emsp; + Cài đặt và định cấu hình công cụ AWS Elastic Beanstalk CLI. <br>&emsp; + Sử dụng AWS Elastic Beanstalk CLI để triển khai 1 bản cập nhật trong môi trường Elastic Beanstalk environment có sẵn. <br>&emsp; + Sử dụng AWS SDK truy vấn và sửa đổi môi trường AWS environment bằng code.                  | 03/10/2025   | 04/10/2025      | <https://000050.awsstudygroup.com/> |
| 6   | - **Thực hành:** <br>&emsp; + dựng một ứng dụng web (front-end) để tương tác với cơ sở dữ liệu thông qua Lambda và API Gateway.                                                                                        | 04/10/2025   | 05/10/2025      | <https://000079.awsstudygroup.com/> |


### Kết quả đạt được tuần 4:

* Hiểu và thao tác được với AWS DynamoDB: 
  * Tạo và quản lý bảng DynamoDB thông qua AWS CLI và Python SDK (boto3) bằng Access Key.
  * Biết cách xác định Primary Key, Sort Key, và cấu hình Read/Write Capacity Mode.


* Xây dựng ứng dụng Book Store sử dụng AWS Lambda, S3, và DynamoDB:
  * Tạo Lambda function để xử lý CRUD operations cho dữ liệu sách.
  * Kết nối API Gateway với Lambda để tạo REST API phục vụ giao tiếp với frontend.
  * Lưu trữ ảnh bìa sách và dữ liệu tĩnh trên S3 Bucket.

* Nắm vững mô hình dữ liệu JSON & Document Model:
  * Hiểu cách lưu trữ dữ liệu phi cấu trúc trong DynamoDB và cách truy xuất thông qua JSON format.

* Triển khai ứng dụng Java bằng Elastic Beanstalk:
  * Sử dụng AWS Console và CloudFormation Template để tự động hoá việc tạo môi trường.
  * Cấu hình và sử dụng Elastic Beanstalk CLI để deploy và cập nhật ứng dụng.
  * Tích hợp AWS SDK for Java để tương tác với môi trường ứng dụng


* Xây dựng ứng dụng web (frontend) kết nối Lambda + API Gateway + DynamoDB:

  * Tạo giao diện web đơn giản cho phép người dùng thêm, sửa, xóa dữ liệu trong DynamoDB.
  * Hiểu quy trình Frontend → API Gateway → Lambda → DynamoDB và cách bảo mật endpoint.





