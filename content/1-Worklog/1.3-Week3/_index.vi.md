---
title: "Worklog Tuần 3"
date: 2025-09-07
weight: 1
chapter: false
pre: " <b> 1.3. </b> "
---

### Mục tiêu Tuần 3

- Hiểu các khái niệm bảo mật cơ bản của AWS.
- Tìm hiểu các dịch vụ bảo mật quan trọng như **AWS KMS**, **Amazon Macie**, **AWS Certificate Manager**.
- Hiểu cách bảo vệ hạ tầng AWS.

### Công việc đã thực hiện trong tuần

| Ngày | Công việc | Bắt đầu | Hoàn thành | Tài liệu tham khảo |
| --- | --------- | -------- | ---------- | ------------------ |
| 2 | Tìm hiểu cách bảo vệ dữ liệu bằng các cơ chế sẵn có của AWS (**S3**, **EBS**, **DynamoDB**) và các dịch vụ bảo mật (**KMS**, **Macie**, **Certificate Manager**). | 22/09/2025 | 23/09/2025 | Link SkillBuilder |
| 3 | Tìm hiểu cách bảo vệ mạng và ứng dụng thông qua bảo mật hạ tầng (Security Groups, ELB, Regions) và dịch vụ bảo vệ (**AWS Shield**, **AWS WAF**). | 23/09/2025 | 24/09/2025 | Link SkillBuilder |
| 4 | Tìm hiểu quy trình phát hiện và phản hồi sự cố bảo mật với **Amazon Inspector**, **GuardDuty**, **Amazon Detective**, **AWS Security Hub**. | 24/09/2025 | 25/09/2025 | Link SkillBuilder |
| 5 | Tìm hiểu cách ngăn truy cập trái phép bằng các dịch vụ như **IAM Identity Center**, **Secrets Manager**, **Systems Manager**. | 25/09/2025 | 26/09/2025 | Link SkillBuilder |
| 6 | **Thực hành:** <br>&emsp;+ Cấu hình liên kết danh tính (Identity Federation) với **AWS Single Sign-On**. | 26/09/2025 | 29/09/2025 | <https://000012.awsstudygroup.com/> |

---

### Kết quả đạt được

#### 1. Bảo vệ dữ liệu và quản trị bảo mật
- Hiểu:
  - Mã hóa & quản lý khóa bằng **AWS KMS**
  - Quét dữ liệu nhạy cảm với **Amazon Macie**
  - Quản lý chứng chỉ bằng **AWS Certificate Manager**
  - Các chế độ bảo mật có sẵn của **S3**, **EBS**, **DynamoDB**

#### 2. Bảo mật mạng và ứng dụng
- Nắm được các khái niệm bảo mật nhiều lớp:
  - Security Groups
  - Elastic Load Balancer
  - Chiến lược bảo vệ đa vùng (Multi-Region)
- Hiểu cách **AWS Shield** và **AWS WAF** giảm thiểu tấn công DDoS và tấn công web.

#### 3. Phát hiện & ứng phó sự cố bảo mật
- Hiểu vai trò của:
  - **Amazon Inspector** – kiểm tra lỗ hổng
  - **Amazon GuardDuty** – phát hiện mối đe dọa
  - **Amazon Detective** – phân tích điều tra
  - **AWS Security Hub** – quản lý tuân thủ & tổng hợp cảnh báo

#### 4. Ngăn truy cập trái phép
- Hiểu cơ bản về:
  - **IAM Identity Center (SSO)**
  - **Secrets Manager**
  - **Systems Manager**
