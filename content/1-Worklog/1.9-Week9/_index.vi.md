---
title: "Week 9 Worklog"
date: 2025-09-07
weight: 1
chapter: false
pre: " <b> 1.9. </b> "
---

### Mục tiêu Tuần 9:
- Hiểu và áp dụng **AWS AppSync** để xây dựng GraphQL API với nhiều nguồn dữ liệu khác nhau.  
- Học và cấu hình **AWS EBS Data Lifecycle Manager** để tự động hóa việc sao lưu và khôi phục dữ liệu.  
- Tìm hiểu **AWS GuardDuty** để phát hiện mối đe dọa thông minh bằng Machine Learning và phân tích hành vi.  
- Nghiên cứu **AWS Macie** nhằm phát hiện và bảo vệ dữ liệu nhạy cảm trong S3 bucket bằng trí tuệ nhân tạo.  

---

### Nhiệm vụ thực hiện trong tuần:
| Ngày | Nhiệm vụ | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | ---------- | ------------- | ---------------- | ------------------ |
| 2 | - Học **AWS AppSync**: <br> &emsp; + GraphQL APIs: Query, Mutation, Subscription <br> &emsp; + Nguồn dữ liệu: DynamoDB, RDS/Aurora, AWS Lambda, HTTP Endpoints, OpenSearch <br> &emsp; + Xác thực và phân quyền: AWS IAM, API Keys, Cognito User Pools, OpenID Connect <br> &emsp; + Hỗ trợ Realtime, Caching, Offline <br> - **Thực hành:** <br> &emsp; + Tạo GraphQL API <br> &emsp; + Thiết kế schema và gắn với data source <br> &emsp; + Cấu hình request/response mapping templates | 02/11/2025 | 03/11/2025 | <https://000086.awsstudygroup.com/1-introduction/> |
| 3 | - Học **AWS EBS Data Lifecycle Manager**: <br> &emsp; + Tự động hóa sao lưu và khôi phục dữ liệu <br> &emsp; + Giảm chi phí lưu trữ <br> &emsp; + Đảm bảo tuân thủ và bảo mật dữ liệu <br> &emsp; + Hiểu về các loại Lifecycle Policies: EBS Snapshot Policy, EBS-backed AMI Policy, Cross-region/ Cross-account Copy Policy | 03/11/2025 | 05/11/2025 | <https://000088.awsstudygroup.com/> |
| 4 | - **Thực hành:** <br> &emsp; + Khởi tạo EC2 và cấu hình lifecycle policies <br> &emsp; + Xác định tài nguyên cần sao lưu, tần suất và thời gian lưu trữ <br> - Học **AWS GuardDuty**: <br> &emsp; + Hiểu cơ chế phát hiện mối đe dọa bằng ML và phân tích hành vi | 03/11/2025 | 06/11/2025 | <https://000098.awsstudygroup.com/> |
| 5 | - Học **AWS Macie**: <br> &emsp; + Các tính năng chính: Data Discovery, Classification, Bucket-level Visibility <br> &emsp; + Cách hoạt động của Macie <br> &emsp; + Trường hợp sử dụng và mô hình tính phí | 08/14/2025 | 08/15/2025 | <https://000090.awsstudygroup.com/> |
| 6 | - **Thực hành với AWS Macie:** <br> &emsp; + Tạo và cấu hình S3 bucket <br> &emsp; + Kích hoạt dịch vụ Macie <br> &emsp; + Tạo Macie job để quét và phân loại dữ liệu | 08/15/2025 | 08/15/2025 | <https://000090.awsstudygroup.com/> |

---

### Kết quả đạt được trong tuần:
- **AWS AppSync:** Xây dựng thành công GraphQL API tích hợp với DynamoDB và Lambda, nắm được cách thiết kế schema, resolver và mapping template.  
- **AWS EBS Lifecycle Manager:** Cấu hình chính sách sao lưu tự động giúp tăng tính tin cậy và giảm chi phí vận hành.  
- **AWS GuardDuty:** Hiểu cơ chế phát hiện mối đe dọa tự động dựa trên Machine Learning và phân tích hành vi bất thường.  
- **AWS Macie:** Kích hoạt Macie cho S3, chạy job phân loại dữ liệu và phân tích kết quả phát hiện dữ liệu nhạy cảm để đảm bảo tuân thủ bảo mật.
