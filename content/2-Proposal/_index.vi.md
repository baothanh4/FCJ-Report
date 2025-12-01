---
title: "Đề xuất"
date: 2025-09-07
weight: 2
chapter: false
pre: "<b> 2. </b>"
---

# HỆ THỐNG DỊCH VỤ ĐƯỜNG SẮT ĐÔ THỊ TRÊN AWS

---

## Tóm tắt điều hành

Sự phát triển nhanh của đô thị đã làm tăng nhu cầu về giao thông công cộng thông minh và bền vững. Một Hệ thống Đường sắt Đô thị hiện đại cần một **nền tảng số tin cậy, có khả năng mở rộng và luôn hoạt động 24/7**.

Đề xuất này trình bày **kiến trúc microservices trên AWS sử dụng Amazon ECS Fargate**, cho phép:

- Đặt vé, lập lịch, thanh toán và giám sát giao thông  
- Nhập dữ liệu hành khách theo thời gian thực qua Amazon Kinesis  
- Báo cáo BI và phân tích dự đoán với QuickSight và SageMaker  
- Tự động hóa CI/CD đầy đủ và giám sát toàn diện  

---

## Điểm nổi bật chính

- **Kiến trúc microservices container** chạy trên Amazon ECS Fargate  
- Bảo mật end-to-end: Route53 → CloudFront → WAF → ALB → Private Subnets  
- CI/CD tự động hoàn toàn bằng CodePipeline, CodeBuild, CodeDeploy, ECR  
- Xử lý dữ liệu theo thời gian thực với **Kinesis Data Streams**  
- Phân tích và dự đoán với **QuickSight + SageMaker**  
- Khả năng mở rộng cho hàng trăm nghìn yêu cầu đặt vé mỗi ngày  

---

# 1. Mục tiêu dự án

### Mục tiêu chính  
Xây dựng nền tảng số cho Hệ thống Đường sắt Đô thị với khả năng mở rộng, bảo mật và ổn định vận hành dài hạn.

### Mục tiêu cụ thể
- Triển khai các dịch vụ vé, lịch trình, thanh toán và thông báo dưới dạng microservices  
- Hỗ trợ vận hành tự động và giám sát hệ thống toàn diện  
- Thiết lập pipeline CI/CD hoàn chỉnh với zero downtime  
- Hỗ trợ nhập dữ liệu hành khách theo thời gian thực và phân tích  
- Cung cấp kiến trúc đa AZ với ≥ 99,95% độ sẵn sàng hệ thống  

---

# 2. Phạm vi dự án

| Thành phần           | Mô tả                                   |
|---------------------|----------------------------------------|
| Khu vực (Region)    | AWS Singapore (ap-southeast-1)         |
| Người dùng          | Hành khách, nhân viên vận hành, quản trị viên |
| Kiến trúc            | Microservices trên ECS Fargate         |
| Giai đoạn 1         | Vé, lịch trình, thông báo               |
| Giai đoạn 2         | Phân tích, dashboard BI, dự báo AI     |

---

# 3. Kiến trúc AWS đề xuất

## 3.1 Tổng quan kiến trúc

Một **kiến trúc microservices nhiều tầng** sẽ được triển khai, bao gồm:

- **Lớp Edge:** Route53, CloudFront, AWS WAF  
- **Lớp ứng dụng:** ALB → ECS Fargate → ECR  
- **Lớp dữ liệu:** RDS SQL Server, ElastiCache Redis  
- **Lớp sự kiện:** EventBridge, SNS, SQS  
- **Lớp phân tích:** Kinesis → S3 → QuickSight → SageMaker  
- **Lớp giám sát:** CloudWatch, CloudTrail  
- **Lớp CI/CD:** CodePipeline, CodeBuild, CodeDeploy  

---

## 3.2 Mạng và lớp truy cập

- **Route 53:** Định tuyến DNS toàn cầu  
- **CloudFront:** CDN, caching, truy cập độ trễ thấp  
- **AWS WAF:** Bảo vệ khỏi DDoS, SQL injection, XSS  
- **Application Load Balancer:** Phân phối traffic tới các microservices  

**Luồng traffic:**  
**Người dùng → Route53 → CloudFront → WAF → ALB → Private Subnet → ECS Fargate**

---

## 3.3 Lớp ứng dụng — Microservices trên ECS Fargate

### Vì sao chọn Fargate?
- Không quản lý server  
- Autoscaling dựa trên CPU/Memory  
- Bảo mật cao trong private subnet  

### Microservices
- Booking Service  
- Schedule Service  
- Payment Service  
- Notification Service  
- User Service  
- Staff & Operation Service  

**Docker Images** lưu trữ trong **Amazon ECR**

---

## 3.4 Lớp dữ liệu

### Amazon RDS (SQL Server)
- Lưu vé, lịch trình, tài khoản người dùng, thanh toán  
- Multi-AZ để đảm bảo tính sẵn sàng cao  
- Backup và failover tự động  

### ElastiCache Redis
- Cache lịch trình → giảm tải RDS  
- Tăng hiệu năng API lên đến 10×  

### Amazon S3
- Lưu báo cáo, hóa đơn, tệp tin  
- Là nơi lưu dữ liệu streaming từ Kinesis  

---

## 3.5 Lớp sự kiện & messaging

### Amazon EventBridge
Tự động hóa workflow, ví dụ:  
- PaymentSuccess → CreateInvoice → NotifyUser  
- ScheduleUpdate → BroadcastToMobile  

### Amazon SQS
- Hệ thống queue cho thông báo và xử lý vé  
- Bảo vệ dịch vụ khi lưu lượng tăng đột biến  

### Amazon SNS
- Gửi SMS, email, push notification  

---

## 3.6 Phân tích thời gian thực

### Kinesis Data Streams
- Thu thập dữ liệu hành khách theo thời gian thực  
- Logs ứng dụng → Kinesis → S3  

### QuickSight
- Dashboard cho doanh thu hàng ngày, tải trạm, giờ cao điểm  

### SageMaker
- Dự đoán nhu cầu hành khách  
- Tối ưu tần suất chạy tàu trong giờ cao điểm  

---

## 3.7 Giám sát & quan sát

- **CloudWatch Metrics:** CPU, Memory, độ trễ ALB  
- **CloudWatch Logs:** logs ứng dụng Fargate  
- **SNS Alerts:** thông báo lỗi  
- **CloudTrail:** theo dõi hoạt động quản trị & tuân thủ  

---

## 3.8 Pipeline CI/CD

Commit của developer  
→ CodePipeline  
→ CodeBuild  
→ Build Docker Image  
→ Push ECR  
→ CodeDeploy  
→ ECS Fargate  

### Tính năng:
- Rolling deployments **zero downtime**  
- Kiểm tra sức khỏe ALB  
- Tự động rollback khi thất bại  

---

# 4. Kế hoạch triển khai

| Giai đoạn | Thời gian | Kết quả bàn giao                       |
|-----------|-----------|---------------------------------------|
| 1         | 1 tuần    | Route53, CloudFront, WAF, VPC, ALB    |
| 2         | 3 tuần    | ECS, ECR, RDS, ElastiCache           |
| 3         | 1 tuần    | EventBridge, SQS, SNS                 |
| 4         | 3 tuần    | Kinesis, S3, QuickSight               |
| 5         | 2 tuần    | Pipeline CI/CD                         |
| 6         | 2 tuần    | Tăng cường bảo mật, tối ưu chi phí     |

---

# 5. Ước tính chi phí vận hành hàng tháng

| Dịch vụ                          | Chi phí/Tháng |
|---------------------------------|---------------|
| CloudFront + Route53 + WAF       | $24           |
| ECS Fargate                       | $40           |
| RDS                               | $19           |
| ElastiCache Redis                | $73           |
| S3 + Kinesis                     | $1            |
| Giám sát                          | $37           |
| CI/CD                             | $18           |
| **Tổng chi phí ước tính**        | **$212**      |

---

# 6. Kết quả kỳ vọng

- Hoạt động đường sắt ổn định 24/7  
- Hỗ trợ ≥ 1.000 người dùng đồng thời  
- Thanh toán an toàn và tự động  
- Dự báo nhu cầu hành khách chính xác  
- Giảm chi phí vận hành nhờ autoscaling và CI/CD  

---

# Phụ lục A — Tóm tắt dịch vụ AWS

| Danh mục      | Dịch vụ AWS                                      |
|---------------|--------------------------------------------------|
| Edge          | Route53, CloudFront, WAF                         |
| Networking    | VPC, ALB                                         |
| Compute       | ECS Fargate, ECR                                 |
| Database      | RDS SQL Server, ElastiCache                      |
| Event         | EventBridge, SNS, SQS                            |
| Analytics     | Kinesis, S3, QuickSight, SageMaker              |
| Giám sát      | CloudWatch, CloudTrail                            |
| CI/CD         | CodePipeline, CodeBuild, CodeDeploy              |


![AWS-architecture](/images/2-Proposal/aws_architecture.png)
