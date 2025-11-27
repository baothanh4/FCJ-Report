---
title: "Worklog tuần 5"
date: 2025-09-07
weight: 1
chapter: false
pre: " <b> 1.5. </b> "
---

### Mục tiêu Tuần 5

- Khám phá và thực hành xác thực người dùng và lưu trữ dữ liệu sử dụng **AWS Amplify**.
- Hiểu và triển khai ứng dụng serverless sử dụng **AWS SAM** (Serverless Application Model).
- Học và triển khai xác thực người dùng với **Amazon Cognito**.

### Nhiệm vụ đã hoàn thành trong tuần

| Ngày | Nhiệm vụ | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | ---- | ---------- | ---------------- | ----------------- |
| 2   | Học **AWS Amplify**. | 05/10/2025 | 06/10/2025 | <https://aws.amazon.com/vi/amplify/> |
| 3   | **Thực hành:** Sử dụng **Amplify Authentication** và **Amplify Storage** cho ứng dụng serverless. | 06/10/2025 | 09/10/2025 | <https://000134.awsstudygroup.com/> |
| 4   | Học **AWS SAM**: <br> &emsp;+ Cấu trúc template SAM và SAM CLI <br> &emsp;+ SAM Accelerate và tích hợp SAM CLI | 09/10/2025 | 10/10/2025 | <https://aws.amazon.com/vi/serverless/sam/> |
| 5   | **Thực hành:** <br> &emsp;+ Cài đặt SAM CLI <br> &emsp;+ Triển khai frontend và Lambda function <br> &emsp;+ Cấu hình API Gateway và kiểm thử API bằng Postman | 10/10/2025 | 11/10/2025 | <https://000080.awsstudygroup.com/> |
| 6   | Học **Amazon Cognito** và **Thực hành:** Triển khai xác thực người dùng với Cognito. | 11/10/2025 | 13/10/2025 | <https://000081.awsstudygroup.com/> |

---

### Thành tựu Tuần 5

#### 1. Làm việc với AWS Amplify
- Hiểu kiến trúc Amplify và cách tích hợp với hệ thống serverless.
- Triển khai **Amplify Authentication** cho luồng đăng ký và đăng nhập người dùng.
- Sử dụng **Amplify Storage** để quản lý upload file và truy cập dữ liệu trên Amazon S3.
- Quản lý môi trường Amplify bằng CLI và tích hợp với ứng dụng frontend.

#### 2. Học và áp dụng AWS SAM (Serverless Application Model)
- Hiểu cấu trúc template SAM; nắm cách SAM sử dụng CloudFormation.
- Cài đặt và cấu hình SAM CLI cho phát triển và triển khai cục bộ.
- Thực hành triển khai ứng dụng serverless sử dụng **SAM Accelerate**.
- Triển khai Lambda function và kiểm thử endpoint API qua API Gateway bằng Postman.
- Hiểu quy trình làm việc: **SAM → Lambda → API Gateway → CloudFormation**.

#### 3. Học và thực hành Amazon Cognito
- Hiểu **Cognito User Pools** (xác thực) và **Identity Pools** (phân quyền + truy cập dịch vụ AWS).
- Triển khai luồng xác thực người dùng bằng Cognito.
- Tích hợp Cognito với AWS Amplify để xác thực liền mạch trên frontend.
- Thử nghiệm thành công các luồng: đăng ký, đăng nhập, xác nhận và xác thực token.

#### 4. Kết hợp AWS Amplify, SAM và Cognito
- Xây dựng ứng dụng serverless hoàn chỉnh, hỗ trợ xác thực người dùng, tương tác API và triển khai trên cloud.
- Nâng cao hiểu biết về kiến trúc serverless, chuẩn bị cho các dự án phát triển cloud-native nâng cao trong các tuần tới.
