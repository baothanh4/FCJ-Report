---
title: "Đề xuất"
date: 2025-09-07
weight: 2
chapter: false
pre: "<b> 2. </b>"
---

# HỆ THỐNG DỊCH VỤ ĐƯỜNG SẮT ĐÔ THỊ TRÊN NỀN TẢNG AWS

---

## Tóm tắt điều hành

Sự phát triển nhanh của đô thị làm gia tăng nhu cầu về hệ thống giao thông công cộng thông minh và bền vững. Một hệ thống Đường Sắt Đô Thị hiện đại cần một nền tảng số **ổn định, mở rộng linh hoạt và sẵn sàng 24/7**.

Tài liệu này trình bày một **kiến trúc AWS xây dựng trên Amazon EC2**, mang lại khả năng kiểm soát hoàn toàn, hiệu suất cao và độ linh hoạt cho các hệ thống quan trọng.

Nền tảng hỗ trợ:

- Đặt vé, lập lịch, thanh toán và giám sát lưu lượng  
- Thu thập dữ liệu hành khách thời gian thực với Amazon Kinesis  
- Dashboard BI và phân tích dự đoán bằng QuickSight và SageMaker  
- Tự động hóa CI/CD và giám sát toàn diện  

---

## Điểm nhấn chính

- Kiến trúc **EC2** với Auto Scaling & ALB  
- Chuỗi bảo mật đầu-cuối: Route53 → CloudFront → WAF → ALB → Private EC2  
- Tự động hóa CI/CD với CodePipeline, CodeBuild, CodeDeploy  
- Xử lý thời gian thực bằng **Kinesis Data Streams**  
- Phân tích dữ liệu với **QuickSight**  
- Đảm bảo HA & khả năng mở rộng trên nhiều AZ  

---

# 1. Mục tiêu dự án

### Mục tiêu chính  
Xây dựng nền tảng số cho hệ thống Đường Sắt Đô Thị với khả năng mở rộng, bảo mật và vận hành ổn định dài hạn.

### Mục tiêu cụ thể
- Triển khai dịch vụ đặt vé, lập lịch, thanh toán, thông báo  
- Kích hoạt vận hành tự động và giám sát toàn hệ thống  
- Xây dựng pipeline CI/CD với khả năng triển khai không downtime lên EC2  
- Hỗ trợ thu thập và phân tích dữ liệu thời gian thực  
- Cung cấp kiến trúc đa-AZ với độ sẵn sàng ≥ 99.95%  

---

# 2. Phạm vi dự án

| Thành phần         | Mô tả                                        |
|--------------------|----------------------------------------------|
| Region             | AWS Singapore (ap-southeast-1)               |
| Người dùng         | Hành khách, nhân viên vận hành, quản trị     |
| Kiến trúc          | Multi-tier trên EC2                          |
| Giai đoạn 1        | Đặt vé, lập lịch, thông báo                  |
| Giai đoạn 2        | Analytics, dashboard BI                      |

---

# 3. Kiến trúc AWS đề xuất

## 3.1 Tổng quan kiến trúc

Kiến trúc **đa tầng** bao gồm:

- **Tầng Edge:** Route53, CloudFront, AWS WAF  
- **Tầng Ứng dụng:** ALB → EC2 Auto Scaling Group  
- **Tầng Dữ liệu:** RDS SQL Server, ElastiCache Redis  
- **Tầng sự kiện:** EventBridge, SNS, SQS  
- **Tầng phân tích:** Kinesis → S3 → QuickSight → SageMaker  
- **Giám sát:** CloudWatch, CloudTrail  
- **CI/CD:** CodePipeline, CodeBuild, CodeDeploy  

---

## 3.2 Tầng mạng và truy cập

- **Route 53:** DNS toàn cầu  
- **CloudFront:** CDN tăng tốc và cache nội dung  
- **AWS WAF:** Lọc bảo mật (SQLi, XSS, bot)  
- **Application Load Balancer:** Điều phối traffic vào EC2  

**Luồng truy cập:**  
**Người dùng → Route53 → CloudFront → WAF → ALB → Private Subnet → EC2**

---

## 3.3 Tầng ứng dụng — EC2 Auto Scaling

### Vì sao chọn EC2?
- Kiểm soát toàn bộ hệ điều hành và môi trường chạy  
- Phù hợp cho cả monolithic và microservice  
- Ổn định cho backend chạy dài hạn  
- Tự động scaling theo CPU, network, request count  
- EC2 role đảm bảo truy cập an toàn vào tài nguyên AWS  

### Mô hình triển khai ứng dụng
- Backend chạy trên **Auto Scaling Group**  
- EC2 đặt trong **Private Subnet** để tăng bảo mật  
- Triển khai qua **CodeDeploy (Blue/Green hoặc Rolling)**  

### Các backend service:
- Booking Service  
- Schedule Service  
- Payment Service  
- Notification Service  
- User Service  
- Operation & Reporting Service  

---

## 3.4 Tầng dữ liệu

### Amazon RDS (SQL Server)
- Lưu vé, lịch, tài khoản người dùng, thanh toán  
- Multi-AZ đảm bảo HA  
- Tự động backup, tự động failover  
- Hỗ trợ IAM authentication & mã hóa dữ liệu  

### Amazon S3
- Lưu tài liệu, báo cáo, log, dữ liệu phân tích  
- Lưu dữ liệu stream từ Kinesis  
- Tự động tối ưu chi phí nhờ lifecycle  

---

## 3.5 Tầng sự kiện & nhắn tin

### Amazon EventBridge
Tự động hóa quy trình, ví dụ:
- PaymentSuccess → CreateInvoice → NotifyUser  
- TrainDelay → PushNotifications → Cập nhật dashboard  

### Amazon SQS
- Hàng đợi buffer cho workload lớn  
- Ngăn hệ thống quá tải giờ cao điểm  

### Amazon SNS
- Gửi thông báo đa kênh (SMS, email, push)  

---

## 3.6 Phân tích thời gian thực

### Kinesis Data Streams
- Thu thập dữ liệu hành khách theo thời gian thực  
- Ứng dụng ghi log → Kinesis → S3  

### QuickSight
- Dashboard kinh doanh: doanh thu vé, giờ cao điểm, sự cố  

---

## 3.7 Giám sát & quan sát

- **CloudWatch Metrics:** Theo dõi EC2, ALB, RDS  
- **CloudWatch Logs:** Nhận log từ EC2  
- **SNS Alerts:** Cảnh báo sự cố  
- **CloudTrail:** Giám sát thao tác hệ thống  

---

## 3.8 CI/CD Pipeline

Developer Commit  
→ CodePipeline  
→ CodeBuild  
→ Artifact Storage  
→ CodeDeploy  
→ EC2 Auto Scaling Group

### Tính năng triển khai
- Blue/Green hoặc Rolling  
- Kiểm tra sức khỏe qua ALB  
- Tự động rollback  
- Cập nhật không downtime  

---

# 4. Kế hoạch triển khai

| Giai đoạn | Thời gian | Kết quả bàn giao                         |
|-----------|-----------|-------------------------------------------|
| 1         | 1 tuần    | Route53, CloudFront, WAF, VPC, ALB       |
| 2         | 3 tuần    | EC2 ASG, RDS                              |
| 3         | 1 tuần    | EventBridge, SQS, SNS                     |
| 4         | 3 tuần    | Kinesis, S3, QuickSight                   |
| 5         | 2 tuần    | CI/CD (CodeDeploy)                        |
| 6         | 2 tuần    | Hardening & tối ưu chi phí                |

---

# 5. Ước tính chi phí hàng tháng (Kiến trúc EC2)

| Dịch vụ                       | Chi phí/tháng |
|-------------------------------|---------------|
| CloudFront + Route53 + WAF   | $24           |
| EC2 ASG (t3.micro x 2 AZ)     | $38           |
| RDS                           | $19           |
| S3 + Kinesis                 | $1            |
| Monitoring                   | $37           |
| CI/CD                        | $18           |
| **Tổng cộng**                | **$210**      |

---

# 6. Kết quả kỳ vọng

- Hệ thống đường sắt vận hành ổn định 24/7  
- Backend EC2 HA với autoscaling  
- Bảo mật thanh toán và endpoint  
- Phân tích dữ liệu hành khách thời gian thực  
- Tối ưu chi phí vận hành  
- Triển khai không downtime + dễ bảo trì  

---

# Phụ lục A — Danh sách dịch vụ AWS

| Nhóm          | Dịch vụ AWS                                      |
|---------------|---------------------------------------------------|
| Edge          | Route53, CloudFront, WAF                          |
| Networking    | VPC, ALB                                          |
| Compute       | EC2, Auto Scaling Group                           |
| Database      | RDS SQL Server                                    |
| Event         | EventBridge, SNS, SQS                             |
| Analytics     | Kinesis, S3, QuickSight                           |
| Monitoring    | CloudWatch, CloudTrail                            |
| CI/CD         | CodePipeline, CodeBuild, CodeDeploy               |

![AWS-architecture](/images/2-Proposal/aws_metropolitano_train_service.png)
