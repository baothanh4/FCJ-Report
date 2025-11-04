---
title: "Đề xuất hệ thống"
date: 2025-09-07
weight: 2
chapter: false
pre: " <b> 2. </b> "
---

# Hệ thống Dịch vụ Đường sắt Đô thị trên AWS — Kiến trúc Đám mây An toàn, Mở rộng và Tối ưu Chi phí

### 1. Giới thiệu
Khi TP. Hồ Chí Minh tiếp tục phát triển nhanh chóng, các vấn đề giao thông như tắc nghẽn và ô nhiễm không khí ngày càng trở nên nghiêm trọng.  
Dự án **Đường sắt Đô thị** là một sáng kiến chiến lược nhằm xây dựng hệ thống giao thông công cộng hiện đại, bền vững và thông minh.  

Bản đề xuất này giới thiệu một **kiến trúc điện toán đám mây toàn diện dựa trên AWS**, được thiết kế để hỗ trợ các chức năng như **đặt vé điện tử, thanh toán không tiền mặt, quản lý lịch trình tàu và phân tích hoạt động vận hành**.  
Giải pháp sử dụng các dịch vụ AWS theo mô hình **phi máy chủ (serverless)**, **hướng sự kiện (event-driven)** và **tự động CI/CD**, nhằm đảm bảo khả năng mở rộng, tối ưu chi phí và bảo mật cao.

---

### 2. Mục tiêu
**Mục tiêu tổng quát:**  
Xây dựng hạ tầng kỹ thuật số đáng tin cậy và an toàn cho hệ thống Đường sắt Đô thị TP. Hồ Chí Minh dựa trên nền tảng AWS Cloud.

**Mục tiêu cụ thể:**
- Triển khai kiến trúc **serverless và hướng sự kiện** sử dụng AWS Lambda và EventBridge.  
- Cung cấp tính năng **đặt vé trực tuyến**, **thanh toán điện tử** và **cập nhật lịch trình tàu theo thời gian thực**.  
- Áp dụng **bảo mật đầu-cuối (end-to-end)** với WAF, Cognito, KMS và Secrets Manager.  
- Tích hợp quy trình **tự động CI/CD** bằng CodePipeline, CodeBuild và CodeDeploy.  
- Thiết lập hệ thống **giám sát và tuân thủ** bằng CloudWatch và CloudTrail.

---

### 3. Phạm vi
- **Địa điểm:** Tuyến Metro số 1 (Bến Thành – Suối Tiên), TP. Hồ Chí Minh  
- **Đối tượng sử dụng:** Hành khách, nhân viên Metro và quản trị viên  
- **Thời gian triển khai:** 12 năm (từ giai đoạn cài đặt đến vận hành dài hạn)  
- **Giai đoạn 1:** Tập trung vào đặt vé, xác thực, lịch trình và thanh toán  
- **Các giai đoạn sau:** Phân tích dữ liệu dự đoán, giám sát IoT và tối ưu lưu lượng hành khách  

---

### 4. Kiến trúc Hệ thống AWS
Hệ thống được xây dựng dựa trên **kiến trúc nhiều lớp (multi-layered)**, **phi máy chủ**, kết hợp khả năng mở rộng, tự động hóa và bảo mật cấp doanh nghiệp.

---

#### **1. Lớp Mạng và Truy cập**
- **Amazon Route 53:**  
  Quản lý định tuyến tên miền cho các cổng web và ứng dụng di động của Metro. Đảm bảo độ sẵn sàng toàn cầu và độ trễ thấp.  
- **Amazon CloudFront (CDN):**  
  Phân phối nội dung tĩnh của giao diện frontend trên toàn cầu, giảm tải cho hệ thống backend.  
- **AWS WAF (Web Application Firewall):**  
  Bảo vệ hệ thống khỏi các cuộc tấn công DDoS, SQL Injection và Cross-Site Scripting.  
- **AWS Shield (tích hợp với CloudFront):**  
  Cung cấp khả năng chống DDoS tự động ở tầng mạng và tầng truyền tải.  

---

#### **2. Lớp Tự động hóa và CI/CD**
- **AWS CodePipeline:**  
  Tự động hóa toàn bộ quy trình xây dựng – kiểm thử – triển khai (build–test–deploy) cho các thành phần ứng dụng.  
- **AWS CodeBuild:**  
  Tự động biên dịch và kiểm thử mã nguồn backend/frontend sau mỗi lần commit từ GitHub.  
- **AWS CodeDeploy:**  
  Triển khai phiên bản mới của Lambda và API mà không gây gián đoạn dịch vụ.  
- **GitHub Integration:**  
  Lưu trữ mã nguồn và kích hoạt pipeline CI/CD thông qua webhook.  

---

#### **3. Lớp Xác thực và Bảo mật**
- **Amazon Cognito:**  
  Quản lý đăng ký, đăng nhập, khôi phục mật khẩu và xác thực đa yếu tố (MFA). Cung cấp token JWT an toàn cho truy cập API.  
- **AWS Secrets Manager:**  
  Lưu trữ an toàn các thông tin nhạy cảm (như mật khẩu RDS, khóa API) và tự động xoay vòng định kỳ.  
- **AWS KMS (Key Management Service):**  
  Mã hóa dữ liệu khi lưu trữ (data-at-rest) trong RDS, S3 và các biến môi trường trong Lambda.  
- **AWS CloudTrail:**  
  Ghi lại và giám sát mọi hoạt động API trên toàn bộ tài khoản AWS, đảm bảo tính minh bạch và tuân thủ.  

---

#### **4. Lớp Ứng dụng và API**
- **Amazon API Gateway:**  
  Cung cấp các endpoint RESTful an toàn cho ứng dụng web/di động và định tuyến đến các hàm Lambda.  
- **AWS Lambda (Serverless Backend):**  
  Xử lý toàn bộ logic nghiệp vụ thông qua các vi dịch vụ (microservices) như:
  - `BookingServiceLambda` — Tạo và xác thực yêu cầu đặt vé.  
  - `PaymentLambda` — Xử lý thanh toán qua VNPay hoặc Momo.  
  - `ScheduleLambda` — Quản lý và cập nhật lịch trình tàu.  
  - `NotificationLambda` — Gửi email/SMS xác nhận qua Amazon SNS.  
  - `EventBridge` — Tự động kích hoạt quy trình (ví dụ: thanh toán thành công → gửi hóa đơn).  
- **Amazon EventBridge:**  
  Điều phối các sự kiện bất đồng bộ như xác nhận đặt vé, hủy vé, hoặc báo trễ chuyến.  

---

#### **5. Lớp Dữ liệu và Lưu trữ**
- **Amazon RDS (SQL Server):**  
  Lưu trữ dữ liệu có cấu trúc — hồ sơ hành khách, đặt vé, và giao dịch thanh toán. Chạy trong subnet riêng và sao lưu hàng ngày lên S3.  
- **Amazon DynamoDB (Tùy chọn mở rộng):**  
  Cung cấp bộ nhớ đệm thời gian thực cho dữ liệu lịch trình và phiên người dùng.  
- **Amazon S3:**  
  - Lưu trữ giao diện web tĩnh (ứng dụng React).  
  - Lưu trữ log, biên lai, và tệp sao lưu.  
  - Áp dụng **Lifecycle Policy** để tự động lưu trữ dữ liệu cũ sang **S3 Glacier** nhằm tiết kiệm chi phí.  

---

#### **6. Lớp Giám sát, Nhật ký và Tuân thủ**
- **Amazon CloudWatch:**  
  Theo dõi hiệu suất, log Lambda và độ trễ của API Gateway. Cảnh báo khi có sự cố bất thường.  
- **CloudWatch Alarms + SNS:**  
  Gửi thông báo cho nhóm vận hành khi vượt ngưỡng hiệu năng (CPU, lỗi 5XX, v.v.).  
- **AWS CloudTrail:**  
  Ghi lại toàn bộ hoạt động API phục vụ kiểm toán và tuân thủ (ISO/GDPR).  

---

### 5. Kế hoạch Triển khai
| **Giai đoạn** | **Thời gian** | **Hạng mục chính** |
|----------------|----------------|----------------------|
| **Giai đoạn 1** | Tuần 1–2 | Thiết lập hạ tầng: Route 53, CloudFront, API Gateway, Lambda, RDS |
| **Giai đoạn 2** | Tuần 3–4 | Phát triển chức năng đặt vé và xác thực (Cognito, Lambda, EventBridge) |
| **Giai đoạn 3** | Tuần 5–6 | Tích hợp thanh toán, giám sát CloudWatch và bảo vệ bằng WAF |
| **Giai đoạn 4** | Tuần 7–8 | Cấu hình pipeline CI/CD với CodePipeline, CodeBuild và CodeDeploy |
| **Giai đoạn 5** | Giai đoạn mở rộng | Thêm lớp phân tích dữ liệu (Athena, QuickSight) |

---

### 6. Ngân sách & Nguồn lực
| **Thành phần** | **Dịch vụ chính** | **Chi phí ước tính (USD/tháng)** |
|----------------|-------------------|----------------------------------|
| Mạng & CDN | Route 53, CloudFront, WAF | $15 |
| Backend Serverless | Lambda, API Gateway, EventBridge | $20 |
| Cơ sở dữ liệu & Lưu trữ | RDS, S3 | $35 |
| CI/CD | CodePipeline, CodeBuild, CodeDeploy | $10 |
| Bảo mật & Giám sát | CloudWatch, CloudTrail, Cognito, Secrets Manager, KMS | $15 |
| **Tổng cộng** | — | **≈ $95–100/tháng** |

**Nhân sự tham gia:**
- Kiến trúc sư Cloud (Cloud Architect)  
- Lập trình viên Backend (Lambda / API Gateway)  
- Lập trình viên Frontend (React)  
- Kỹ sư DevOps (CI/CD & Monitoring)  
- Chuyên viên vận hành Metro  

---

### 7. Kết quả Kỳ vọng
- Hệ thống quản lý đường sắt đô thị **an toàn, hiện đại và dựa trên đám mây**.  
- Tích hợp **đặt vé không tiền mặt** và xác nhận tự động.  
- Kiến trúc mở rộng linh hoạt, sẵn sàng tích hợp IoT trong tương lai.  
- Nâng cao khả năng giám sát và minh bạch hóa hoạt động thông qua dashboard phân tích.  
- Tối ưu chi phí vận hành nhờ mô hình tính phí theo mức sử dụng (pay-as-you-go).  

---

### 8. Kết luận
Hệ thống **Dịch vụ Đường sắt Đô thị trên AWS** là nền tảng vững chắc cho quá trình **chuyển đổi số giao thông đô thị**.  
Bằng việc kết hợp **điện toán phi máy chủ (serverless)**, **tự động CI/CD**, và **bảo mật đầu-cuối của AWS**, hệ thống đảm bảo hiệu quả vận hành, khả năng mở rộng và tuân thủ các tiêu chuẩn dữ liệu hiện đại.  
Kiến trúc này không chỉ đáp ứng nhu cầu đặt vé và quản lý hiện tại, mà còn mở đường cho việc **tích hợp thành phố thông minh và ra quyết định dựa trên dữ liệu** trong tương lai.

---

![Sơ đồ kiến trúc AWS](/images/2-Proposal/aws_metropolitano_train_service.drawio.png)
