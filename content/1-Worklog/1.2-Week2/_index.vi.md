---
title: "Worklog Tuần 2"
date: 2025-09-07
weight: 1
chapter: false
pre: " <b> 1.2. </b> "
---

### **Mục tiêu tuần 2**
- Tìm hiểu về Amazon RDS, AWS S3, AWS EC2 Auto Scaling, DynamoDB và Amazon Lightsail.

---

## **Các nhiệm vụ thực hiện trong tuần**

| Ngày | Nhiệm vụ | Bắt đầu | Hoàn thành | Tài liệu tham khảo |
|------|----------|----------|-------------|--------------------|
| 2 | - Học **AWS DynamoDB**, **AWS RDS**, **Amazon Aurora**.<br>**Thực hành:**<br>&emsp;+ Tạo **CloudFront** và **S3** | 14/09/2025 | 15/09/2025 | https://render.skillbuilder.aws |
| 3 | **Thực hành:**<br>&emsp;+ Tạo **AWS RDS**<br>&emsp;+ Tạo **DynamoDB** bằng Python và AWS CLI | 15/09/2025 | 16/09/2025 | https://render.skillbuilder.aws |
| 4 | Dịch Blog | 13/09/2025 | 13/09/2025 | https://cloudjourney.awsstudygroup.com/ |
| 5 | Học **EC2 Auto Scaling**, **Amazon Lightsail**.<br>**Thực hành:**<br>&emsp;+ Tạo Database trên **RDS**<br>&emsp;+ Sử dụng **Amazon Lightsail** | 19/09/2025 | 20/09/2025 | https://000005.awsstudygroup.com/ <br> https://000045.awsstudygroup.com/ |
| 6 | **Thực hành:**<br>&emsp;+ Tạo **RDS**, **VPC**, **EC2** với **EC2 Auto Scaling** | 20/09/2025 | 21/09/2025 | https://000006.awsstudygroup.com/ |

---

## **Kết quả đạt được trong tuần**

### 1. Static Website Hosting với Amazon S3
- Biết cách tạo S3 Bucket, upload file và quản lý truy cập.
- Cấu hình **Static Website Hosting** để bucket hoạt động như một website.
- Thiết lập quyền public giúp website được truy cập từ Internet.
- Cấu hình **Bucket Policy** để chỉ cho phép đọc công khai (public read-only).

---

### 2. Kiến thức về Amazon RDS – Dịch vụ cơ sở dữ liệu quan hệ
- Hỗ trợ các hệ quản trị phổ biến: MySQL, PostgreSQL, Oracle, SQL Server.
- Biết cách kết nối RDS từ EC2.
- Nắm rõ endpoint, port, username/password để đăng nhập DB.
- Tự tạo và cấu hình VPC, subnet, security group để bảo vệ RDS Instance.

---

### 3. Mở rộng ứng dụng với EC2 Auto Scaling
- Hiểu EC2 Auto Scaling là dịch vụ tự động **tăng/giảm** số lượng EC2 dựa trên nhu cầu thực tế.
- Thành phần chính của Auto Scaling:
  - **Launch Configuration / Launch Template**
  - **Auto Scaling Group (ASG)**
  - **Scaling Policies**: Dynamic Scaling và Scheduled Scaling
  - **Health Checks**
- Biết cách sử dụng Amazon CloudWatch để thu thập các metric như CPU Utilization, Network Traffic, Request Count… giúp ASG đưa ra quyết định scale hợp lý.

---

