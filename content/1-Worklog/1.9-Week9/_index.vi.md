---
title: "Worklog tuần 9"
date: 2025-09-07
weight: 1
chapter: false
pre: " <b> 1.9. </b> "
---

### Mục tiêu Tuần 9

* Hiểu và áp dụng **AWS AppSync** để xây dựng GraphQL API với nhiều nguồn dữ liệu khác nhau.  
* Học và cấu hình **AWS EBS Data Lifecycle Manager** để tự động hóa snapshot và backup.  
* Khám phá **AWS GuardDuty** cho việc phát hiện mối đe dọa thông minh dựa trên ML và phân tích hành vi.  
* Học **AWS Macie** để nhận diện và bảo vệ dữ liệu nhạy cảm trong S3 bằng machine learning.  

### Nhiệm vụ tuần này

| Ngày | Nhiệm vụ | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | ---- | ---------- | --------------- | ----------------- |
| 2 | Học **AWS AppSync**: <br> &emsp;+ GraphQL APIs: Query, Mutation, Subscription <br> &emsp;+ Nguồn dữ liệu: DynamoDB, RDS/Aurora, Lambda, HTTP Endpoints, OpenSearch <br> &emsp;+ Xác thực và phân quyền: IAM, API Keys, Cognito User Pools, OpenID Connect <br> &emsp;+ Hỗ trợ realtime subscription, caching, offline <br> **Thực hành:** <br> &emsp;+ Tạo GraphQL API <br> &emsp;+ Định nghĩa schema và gắn với nguồn dữ liệu <br> &emsp;+ Cấu hình request/response mapping template | 02/11/2025 | 03/11/2025 | <https://000086.awsstudygroup.com/1-introduction/> |
| 3 | Học **AWS EBS Data Lifecycle Manager**: <br> &emsp;+ Tự động backup và recovery <br> &emsp;+ Giảm chi phí lưu trữ <br> &emsp;+ Đảm bảo tuân thủ và bảo vệ dữ liệu <br> &emsp;+ Hiểu chính sách Lifecycle: EBS Snapshot Policy, EBS-backed AMI Policy, Cross-region/Cross-account Copy Policy | 03/11/2025 | 05/11/2025 | <https://000088.awsstudygroup.com/> |
| 4 | **Thực hành:** <br> &emsp;+ Khởi tạo EC2 instance và cấu hình lifecycle policies <br> &emsp;+ Chọn tài nguyên cần backup, lịch trình, và thời gian lưu trữ <br> Học **AWS GuardDuty**: <br> &emsp;+ Phát hiện mối đe dọa dựa trên ML và phân tích hành vi | 03/11/2025 | 06/11/2025 | <https://000098.awsstudygroup.com/> |
| 5 | Học **AWS Macie**: <br> &emsp;+ Tính năng chính: Khám phá dữ liệu, phân loại, hiển thị cấp bucket <br> &emsp;+ Cách Macie hoạt động <br> &emsp;+ Trường hợp sử dụng và mô hình giá | 14/08/2025 | 15/08/2025 | <https://000090.awsstudygroup.com/> |
| 6 | **Thực hành AWS Macie:** <br> &emsp;+ Tạo và cấu hình S3 bucket <br> &emsp;+ Kích hoạt dịch vụ Macie <br> &emsp;+ Tạo các job để quét và phân loại dữ liệu | 15/08/2025 | 15/08/2025 | <https://000090.awsstudygroup.com/> |

### Thành tựu Tuần 9

* **AWS AppSync**: Xây dựng GraphQL API tích hợp DynamoDB và Lambda, hiểu cách thiết kế schema, resolvers và mapping templates.  
* **AWS EBS Lifecycle Manager**: Cấu hình chính sách backup tự động, tăng độ tin cậy và tối ưu chi phí trên EC2.  
* **AWS GuardDuty**: Hiểu cách phát hiện mối đe dọa liên tục dựa trên ML và phân tích hành vi bất thường.  
* **AWS Macie**: Kích hoạt Macie trên S3, chạy job phân loại dữ liệu và đánh giá các rủi ro dữ liệu nhạy cảm, đảm bảo tuân thủ.
