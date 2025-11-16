---
title: "Tuần 4 Worklog"
date: 2025-09-07
weight: 1
chapter: false
pre: " <b> 1.4. </b> "
---

### Mục tiêu Tuần 4:

* Thực hành tạo, quản lý và triển khai tất cả tài nguyên AWS qua các công cụ khác nhau (Console, CLI, SDK, Elastic Beanstalk...).
* Xây dựng prototype ứng dụng web sử dụng Lambda, S3, DynamoDB và API Gateway.

### Công việc thực hiện trong tuần:
| Ngày | Công việc                                                                                                                                                                                                   | Ngày bắt đầu | Ngày kết thúc | Tài liệu tham khảo                        |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------- | --------------- | ----------------------------------------- |
| 2   | - **Thực hành:** Tạo bảng trong **AWS DynamoDB** bằng **AWS CLI** hoặc Python qua AccessKey                                                                                                  | 28/09/2025 | 29/09/2025      |                                           |
| 3   | - **Thực hành:** Tạo ứng dụng cửa hàng sách bằng **Lambda**, **S3** và **DynamoDB**                                          | 30/09/2025 | 01/10/2025      | <https://000078.awsstudygroup.com/> |
| 4   | - Tìm hiểu **JSON & Document model** | 01/10/2025 | 02/10/2025      |                                           |
| 5   | - **Thực hành:** <br>&emsp;+ Sử dụng AWS Console triển khai và kiểm tra tài nguyên AWS thông qua **AWS CloudFormation template** <br>&emsp;+ Dùng **AWS Tools for Eclipse** để triển khai ứng dụng Java lên Elastic Beanstalk <br>&emsp;+ Cài đặt và cấu hình **AWS Elastic Beanstalk CLI** <br>&emsp;+ Dùng Elastic Beanstalk CLI để cập nhật môi trường <br>&emsp;+ Dùng AWS SDK để truy vấn và thay đổi môi trường AWS bằng code. | 03/10/2025 | 04/10/2025      | <https://000050.awsstudygroup.com/> |
| 6   | - **Thực hành:** <br>&emsp;+ Xây dựng ứng dụng web (frontend) tương tác với cơ sở dữ liệu thông qua Lambda và API Gateway                                                     | 04/10/2025 | 05/10/2025      | <https://000079.awsstudygroup.com/> |

### Thành tựu Tuần 4:

* Hiểu và làm việc với **AWS DynamoDB**: 
  * Tạo và quản lý bảng DynamoDB sử dụng AWS CLI và Python SDK (boto3) với Access Keys.
  * Học cách định nghĩa Primary Key, Sort Key và cấu hình Read/Write Capacity Mode.

* Phát triển ứng dụng cửa hàng sách sử dụng **AWS Lambda, S3, DynamoDB**:
  * Xây dựng Lambda function để xử lý CRUD cho dữ liệu sách.
  * Kết nối API Gateway với Lambda để tạo REST API cho frontend.
  * Lưu ảnh bìa sách và file tĩnh trong S3 Bucket.

* Khám phá **JSON & Document Data Models**:
  * Hiểu cách lưu dữ liệu bán cấu trúc trong DynamoDB và truy vấn bằng định dạng JSON.

* Triển khai ứng dụng Java với **AWS Elastic Beanstalk**:
  * Sử dụng AWS Console và CloudFormation Template để tự động thiết lập môi trường.
  * Cài đặt và cấu hình Elastic Beanstalk CLI để triển khai và cập nhật ứng dụng.
  * Tích hợp AWS SDK cho Java để truy vấn và thay đổi môi trường AWS bằng code.

* Xây dựng ứng dụng web (frontend) tương tác với cơ sở dữ liệu thông qua Lambda và API Gateway:
  * Phát triển giao diện đơn giản cho phép người dùng thêm, sửa, xóa dữ liệu trong DynamoDB.
  * Hiểu quy trình Frontend → API Gateway → Lambda → DynamoDB và cách bảo mật các endpoint.
