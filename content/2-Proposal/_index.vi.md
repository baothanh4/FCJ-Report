---
title: "Proposal"
date: 2025-09-07
weight: 2
chapter: false
pre: " <b> 2. </b> "
---

# HỆ THỐNG DỊCH VỤ ĐƯỜNG SẮT ĐÔ THỊ TRÊN AWS  
### Kiến Trúc Đám Mây An Toàn — Mở Rộng — Tối Ưu Chi Phí

---

## Executive Summary

Thành phố Hồ Chí Minh đang đối mặt với các thách thức lớn về giao thông, bao gồm tắc nghẽn, ô nhiễm và áp lực dân số đô thị hóa.  
Dự án **Đường sắt Đô thị** được xem là bước đột phá trong việc xây dựng hệ thống giao thông thông minh, bền vững và thân thiện với môi trường.

Bản đề xuất này trình bày một **kiến trúc đám mây toàn diện dựa trên AWS**, được thiết kế để hỗ trợ các chức năng cốt lõi như:

-  Đặt vé điện tử & thanh toán không tiền mặt  
-  Quản lý lịch trình và giám sát vận hành  
-  Phân tích dữ liệu và tối ưu lưu lượng hành khách  

Kiến trúc tuân thủ các nguyên tắc **serverless, event-driven, và CI/CD automation**, bảo đảm:

- Hiệu suất và khả năng mở rộng linh hoạt.  
- Bảo mật đầu-cuối đạt tiêu chuẩn doanh nghiệp.  
- Chi phí vận hành tối ưu theo mô hình pay-as-you-go.

---

##  Key Highlights

* 100% cloud-native & serverless architecture (AWS Lambda, EventBridge) 
* End-to-end enterprise security (Cognito, WAF, KMS) 
* Fully automated CI/CD & observability (CodePipeline, CloudWatch) 
* Seamless e-ticketing & cashless payment (VNPay, MoMo) 
* Real-time analytics & predictive insights (Athena, QuickSight) 

---

## 1. Mục Tiêu Dự Án

**Mục tiêu tổng quát:**  
Xây dựng hạ tầng kỹ thuật số đáng tin cậy, an toàn, và có khả năng mở rộng cho hệ thống Đường sắt Đô thị TP. Hồ Chí Minh trên nền tảng AWS Cloud.

**Mục tiêu cụ thể:**
- Triển khai kiến trúc **serverless & event-driven** sử dụng AWS Lambda và EventBridge.  
- Cung cấp các tính năng **đặt vé, thanh toán, xác thực và cập nhật lịch trình thời gian thực**.  
- Áp dụng **bảo mật đầu-cuối** (WAF, Cognito, KMS, Secrets Manager).  
- Tự động hóa CI/CD với **CodePipeline, CodeBuild, CodeDeploy**.  
- Thiết lập **giám sát và tuân thủ** qua CloudWatch, CloudTrail.

---

## 2. Phạm Vi Dự Án

| Thành phần | Mô tả |
|-------------|--------|
| **Địa điểm** | Tuyến Metro số 1 (Bến Thành – Suối Tiên), TP.HCM |
| **Người dùng mục tiêu** | Hành khách, nhân viên vận hành, quản trị viên |
| **Thời gian triển khai** | 12 năm (bao gồm triển khai & vận hành dài hạn) |
| **Giai đoạn 1** | Đặt vé, xác thực, lịch trình, thanh toán |
| **Giai đoạn mở rộng** | Phân tích dự đoán, IoT giám sát, tối ưu hành khách |

---

### 2.1 Functional Requirements

| ID | Requirement | Priority |
|----|--------------|----------|
| FR-01 | Users can book tickets and pay online | High |
| FR-02 | Real-time schedule updates via API | High |
| FR-03 | Automatic maintenance alerting | Medium |
| FR-04 | Admin can view passenger analytics | Medium |
| FR-05 | Multi-language (EN, VN) support | Low |

---

### 2.2 Non-Functional Requirements

- **Availability:** ≥ 99.95% uptime (Multi-AZ)  
- **Latency:** < 300 ms for booking operations  
- **Security:** Compliance with ISO 27001 & SOC 2 Type II  
- **Scalability:** Auto scale to 100k concurrent users  
- **Cost Efficiency:** ≤ $100/month base infrastructure  

---

## 3. Kiến Trúc AWS Đề Xuất

### 3.1 Tổng Quan

Hệ thống được xây dựng theo **mô hình đa lớp (multi-tier)**, **phi máy chủ (serverless)**, và **tự động (automated)**, đảm bảo khả năng mở rộng động, vận hành tin cậy và bảo mật toàn diện.

---

### Architecture Diagram Summary

| Layer | Service | Role |
|--------|----------|------|
|  **Frontend** | CloudFront + S3 | Static hosting, caching, HTTPS delivery |
|  **API Layer** | API Gateway + Lambda | Business logic, event-driven functions |
|  **Data** | RDS + S3 + DynamoDB | Persistent and analytical data storage |
|  **Security** | WAF + Cognito + KMS | Authentication, encryption, protection |
|  **Monitoring** | CloudWatch + GuardDuty | Metrics, alerts, and anomaly detection |

---

### 3.2 Lớp Mạng & Truy Cập
- **Amazon Route 53:** Quản lý DNS, đảm bảo độ sẵn sàng toàn cầu.  
- **Amazon CloudFront (CDN):** Phân phối nội dung tĩnh và giảm tải backend.  
- **AWS WAF:** Bảo vệ trước các tấn công DDoS, SQL Injection, XSS.

---

### 3.3 Lớp Ứng Dụng & API
- **Amazon API Gateway:** Cung cấp các endpoint RESTful bảo mật.  
- **AWS Lambda:** Xử lý logic nghiệp vụ chính:
  - `BookingServiceLambda`: Xử lý đặt vé.  
  - `PaymentLambda`: Tích hợp thanh toán VNPay/MoMo.  
  - `ScheduleLambda`: Cập nhật lịch trình.  
  - `NotificationLambda`: Gửi thông báo (SNS, email, SMS).  
- **Amazon EventBridge:** Tự động điều phối quy trình (payment → invoice → notify).  

---

### 3.4 Lớp Dữ Liệu & Lưu Trữ
- **Amazon RDS (SQL Server):** Lưu trữ dữ liệu người dùng, vé, thanh toán.  
- **Amazon S3:** Lưu trữ file tĩnh, log, hóa đơn, dữ liệu sao lưu.  
  - Tích hợp **Lifecycle Policy → S3 Glacier** để tiết kiệm chi phí.  

---

### 3.5 Lớp Bảo Mật & Xác Thực
- **Amazon Cognito:** Đăng ký, đăng nhập, MFA, cấp JWT token.  
- **AWS Secrets Manager:** Lưu trữ và xoay vòng khóa bí mật.  
- **AWS KMS:** Mã hóa dữ liệu RDS/S3.  
- **AWS CloudTrail:** Ghi nhật ký và giám sát API, đảm bảo compliance.

---

### 3.6 Lớp Giám Sát & Tuân Thủ
- **Amazon CloudWatch:** Theo dõi hiệu suất và log Lambda/API.  
- **CloudWatch Alarms + SNS:** Gửi cảnh báo tự động.  
- **CloudTrail:** Theo dõi thay đổi hệ thống và hoạt động người dùng.

---

### 3.7 Lớp CI/CD & Tự Động Hóa
- **AWS CodePipeline:** Tự động build–test–deploy.  
- **AWS CodeBuild:** Kiểm thử mã backend/frontend mỗi lần commit.  
- **AWS CodeDeploy:** Triển khai an toàn, không downtime.  
- **GitHub Webhook:** Tự động kích hoạt pipeline sau commit.

---

### Data Flow (Simplified)
User -> CloudFront ->API Gateway -> Lambda -> RDS<br>
|v
EventBridge -> SNS/Email Notification<br>
|v
CloudWatch -> Admin Dashboard

---

## 4. Kế Hoạch Triển Khai

| Giai đoạn | Thời gian | Hạng mục chính |
|------------|------------|----------------|
| 1 | Tuần 1–2 | Thiết lập Route 53, CloudFront, API Gateway, Lambda, RDS |
| 2 | Tuần 3–4 | Phát triển đặt vé, xác thực (Cognito, Lambda, EventBridge) |
| 3 | Tuần 5–6 | Tích hợp thanh toán, giám sát CloudWatch, cấu hình WAF |
| 4 | Tuần 7–8 | CI/CD (CodePipeline, CodeBuild, CodeDeploy) |
| 5 | Mở rộng | Phân tích dữ liệu (Athena, QuickSight) |

---

## 5. Ngân Sách & Nhân Sự

| Thành phần | Dịch vụ | Ước tính (USD/tháng) |
|-------------|----------|------------------------|
| Mạng & CDN | Route 53, CloudFront, WAF | $15 |
| Backend Serverless | Lambda, API Gateway, EventBridge | $20 |
| Dữ liệu & Lưu Trữ | RDS, S3 | $35 |
| CI/CD | CodePipeline, CodeBuild, CodeDeploy | $10 |
| Bảo mật & Giám sát | CloudWatch, CloudTrail, Cognito, KMS | $15 |
| **Tổng cộng** | — | **≈ $95–100/tháng** |

**Nhân sự:**
- Cloud Architect  
- Backend Developer (Lambda, API Gateway)  
- Frontend Developer (React, S3/CloudFront)  
- DevOps Engineer (CI/CD & Monitoring)  
- Metro Operations Specialist  

---

## 6. Kết Quả Kỳ Vọng
- Nền tảng vận hành **an toàn, hiện đại, dựa trên AWS Cloud**.  
- **Thanh toán không tiền mặt** và **xác nhận vé tự động**.  
- **Hạ tầng mở rộng linh hoạt**, sẵn sàng cho tích hợp IoT.  
- **Minh bạch vận hành** qua dashboard phân tích dữ liệu.  
- **Chi phí tối ưu** nhờ mô hình trả theo mức sử dụng.

---

## 7. Rủi Ro & Giải Pháp

| Rủi ro | Giải pháp |
|--------|------------|
| Gián đoạn mạng AWS | Thiết lập Multi-AZ, failover tự động |
| Quá tải Lambda | Bật autoscaling và giới hạn timeout |
| Tấn công bảo mật | Sử dụng WAF, IAM least privilege, KMS |
| Sai lệch dữ liệu | Tự động sao lưu và khôi phục RDS |
| Lỗi triển khai | CI/CD rollback và CloudFormation drift detection |

---

### 7.1 Risk Classification Matrix

| Risk | Likelihood | Impact | Mitigation |
|-------|-------------|---------|-------------|
| Network outage | Medium | High | Multi-AZ + Failover |
| API overload | High | Medium | Lambda concurrency + autoscaling |
| Data breach | Low | High | KMS encryption + WAF |
| CI/CD failure | Medium | Low | Rollback + versioning |

---

## 8. Tuân Thủ & Bảo Mật

- **Compliance:** ISO 27001, GDPR-ready, SOC2 Type II  
- **Encryption:** AES-256 (KMS-managed)  
- **IAM Policies:** Principle of Least Privilege  
- **Monitoring:** Continuous Audit với CloudTrail & GuardDuty  

---

## 9. Kết Luận

Hệ thống **Đường Sắt Đô Thị Trên AWS** là nền tảng chiến lược giúp chuyển đổi số ngành giao thông công cộng tại TP.HCM.  
Với kiến trúc **serverless – event-driven – CI/CD automation**, giải pháp này đáp ứng các yêu cầu hiện đại về **bảo mật, hiệu suất và chi phí**.  
Đây không chỉ là dự án kỹ thuật, mà còn là **bước tiến hướng tới thành phố thông minh trong tương lai**.

---

## 10. Success Metrics

| KPI | Target | Measurement Tool |
|------|--------|------------------|
| System Availability | ≥ 99.95% | CloudWatch uptime metrics |
| API Latency | < 300 ms | CloudWatch logs |
| Ticket Processing | 10,000+/day | Lambda invocation count |
| Cost Optimization | < $100/month | AWS Cost Explorer |
| Security Compliance | 100% | GuardDuty & IAM Audit |

---

## Appendix A — AWS Services Summary

| Category | Services Used | Purpose |
|-----------|----------------|----------|
| Networking | Route 53, CloudFront | DNS, CDN, HTTPS |
| Compute | Lambda | Serverless compute |
| API | API Gateway | REST API endpoints |
| Database | RDS (SQL Server) | Transactional data |
| Storage | S3 + Glacier | File storage & archival |
| Security | Cognito, WAF, KMS, Secrets Manager | Authentication & protection |
| DevOps | CodePipeline, CodeBuild, CodeDeploy | CI/CD automation |
| Monitoring | CloudWatch, CloudTrail, GuardDuty | Observability & compliance |

---

🖼️ *Hình minh họa:*  
![AWS Architecture Diagram](/images/2-Proposal/aws_metropolitano_train_service.drawio.png)
