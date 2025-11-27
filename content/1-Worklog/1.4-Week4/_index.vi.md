---
title: "Worklog tuần 4"
date: 2025-09-07
weight: 1
chapter: false
pre: " <b> 1.4. </b> "
---

### Mục tiêu Tuần 4

- Luyện tập tạo, quản lý và triển khai tài nguyên AWS thông qua nhiều công cụ (Console, CLI, SDK, Elastic Beanstalk...).
- Xây dựng một ứng dụng web mẫu sử dụng Lambda, S3, DynamoDB và API Gateway.

### Công việc đã thực hiện trong tuần

| Ngày | Công việc | Bắt đầu | Hoàn thành | Tài liệu tham khảo |
| --- | --------- | -------- | ---------- | ------------------ |
| 2 | **Thực hành:** Tạo bảng trong **AWS DynamoDB** bằng **AWS CLI** hoặc Python SDK thông qua Access Key. | 28/09/2025 | 29/09/2025 | |
| 3 | **Thực hành:** Xây dựng ứng dụng Book Store sử dụng **Lambda**, **S3** và **DynamoDB**. | 30/09/2025 | 01/10/2025 | <https://000078.awsstudygroup.com/> |
| 4 | Học mô hình dữ liệu JSON & Document. | 01/10/2025 | 02/10/2025 | |
| 5 | **Thực hành:** <br>&emsp;+ Triển khai và kiểm tra tài nguyên AWS bằng **CloudFormation Template**.<br>&emsp;+ Sử dụng AWS Tools for Eclipse để deploy ứng dụng Java lên **Elastic Beanstalk**.<br>&emsp;+ Cài đặt và cấu hình **Elastic Beanstalk CLI**.<br>&emsp;+ Dùng EB CLI để deploy bản cập nhật cho môi trường có sẵn.<br>&emsp;+ Dùng AWS SDK để truy vấn và chỉnh sửa môi trường AWS bằng code. | 03/10/2025 | 04/10/2025 | <https://000050.awsstudygroup.com/> |
| 6 | **Thực hành:** Xây dựng web frontend kết nối đến database qua **Lambda** và **API Gateway**. | 04/10/2025 | 05/10/2025 | <https://000079.awsstudygroup.com/> |

---

### Kết quả đạt được

#### 1. Làm việc với AWS DynamoDB
- Tạo và quản lý các bảng DynamoDB bằng CLI và Python SDK.
- Hiểu cách định nghĩa Partition Key, Sort Key và cấu hình Read/Write Capacity.

#### 2. Xây dựng ứng dụng Book Store (Lambda + S3 + DynamoDB)
- Tạo Lambda function xử lý CRUD cho dữ liệu sách.
- Kết nối API Gateway với Lambda để xây dựng REST API.
- Lưu ảnh bìa sách và file tĩnh trong Amazon S3.

#### 3. Hiểu mô hình JSON & Document
- Nắm cách DynamoDB lưu trữ dữ liệu bán cấu trúc.
- Biết cách truy vấn và cập nhật dữ liệu ở dạng JSON.

#### 4. Triển khai ứng dụng Java với Elastic Beanstalk
- Triển khai hạ tầng qua Console và CloudFormation.
- Cài đặt EB CLI và deploy bản cập nhật.
- Sử dụng AWS SDK để thao tác với tài nguyên AWS bằng mã nguồn Java.

#### 5. Xây dựng frontend kết nối backend serverless
- Tạo giao diện cho phép thêm, sửa, xóa dữ liệu trong DynamoDB.
- Hiểu quy trình: **Fr**
