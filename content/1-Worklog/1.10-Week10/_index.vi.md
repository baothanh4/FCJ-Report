---
title: "Worklog tuần 10"
date: 2025-09-07
weight: 2
chapter: false
pre: " <b> 1.10. </b> "
---

### Mục tiêu Tuần 10

* Thực hành với các dịch vụ cơ bản của AWS (VPC, EC2, EBS, Postgres)  
* Học AWS SageMaker cho workflow AI/ML  
* Thực hành phân tích dữ liệu AI/ML với SageMaker  
* Học các thành phần AWS Bedrock AgentCore  
* Học AWS Glue và Amazon Athena cho ETL và phân tích dữ liệu  

### Nhiệm vụ tuần này

| Ngày | Nhiệm vụ | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | ---- | ---------- | --------------- | ----------------- |
| 2 | **Thực hành:** <br> &emsp;+ Tạo VPCs <br> &emsp;+ Khởi tạo EC2 instances <br> &emsp;+ Tạo EBS volume <br> &emsp;+ Gắn EBS volume <br> &emsp;+ Cài đặt Postgres <br> &emsp;+ Mount EBS trên EC2 production <br> &emsp;+ Backup Postgres <br> &emsp;+ Mount EBS trên EC2 test <br> &emsp;+ Phục hồi dữ liệu | 08/11/2025 | 10/11/2025 | <https://100000.awsstudygroup.com/> |
| 3 | Học **AWS SageMaker AI**: <br> &emsp;+ SageMaker là gì <br> &emsp;+ Các thành phần <br> &emsp;+ End-to-End Workflow | 10/11/2025 | 12/11/2025 | <https://000200.awsstudygroup.com/> |
| 4 | **Thực hành:** Sử dụng SageMaker AI để phân tích dữ liệu, nhập file Excel, chọn kiểu dữ liệu, xuất kết quả bao gồm biểu đồ | 10/11/2025 | 12/11/2025 | <https://000200.awsstudygroup.com/> |
| 5 | Học **AWS Bedrock AgentCore**: <br> &emsp;+ Identity, Memory, Code Interpreter, Browser, Gateway, Observability <br> &emsp;+ Trường hợp sử dụng: trang bị công cụ cho agent, triển khai an toàn ở quy mô lớn, kiểm tra và giám sát agent | 12/11/2025 | 14/11/2025 | <https://docs.aws.amazon.com/bedrock-agentcore/latest/devguide/what-is-bedrock-agentcore.html> |
| 6 | Học **AWS Glue** và **Amazon Athena** | 14/11/2025 | 16/11/2025 | <https://000040.awsstudygroup.com/> |

### Thành tựu Tuần 10

#### 1. **Thực hành các dịch vụ cơ bản của AWS:**  
  * Tạo VPCs với subnet, route table, Internet Gateway đầy đủ.  
  * Khởi tạo EC2 instances cho môi trường production và test.  
  * Tạo và gắn EBS volume cho EC2 instances.  
  * Cài đặt và cấu hình PostgreSQL trên EC2.  
  * Mount EBS trên cả production và test instances.  
  * Thực hiện backup và phục hồi PostgreSQL thành công.  

#### 2. **Học & Thực hành AWS SageMaker AI:**  
  * Hiểu các thành phần SageMaker: Notebook, Training, Endpoint, Model, Pipelines.  
  * Thực hiện workflow AI/ML từ đầu đến cuối: nhập dữ liệu Excel, phân tích dữ liệu, trực quan hóa biểu đồ.  
  * Chọn kiểu dữ liệu phù hợp, làm sạch dữ liệu và xuất kết quả cho các bước tiếp theo.  

#### 3. **Học AWS Bedrock AgentCore:**  
  * Hiểu các thành phần cốt lõi: Identity, Memory, Code Interpreter, Browser, Gateway, Observability.  
  * Khám phá các trường hợp sử dụng: trang bị công cụ cho agent, triển khai an toàn, giám sát và kiểm tra agent.  

#### 4. **Học AWS Glue & Amazon Athena:**  
  * Thực hành xây dựng pipeline ETL với Glue.  
  * Catalog dữ liệu và chuyển đổi dữ liệu để phân tích.  
  * Truy vấn dữ liệu trên S3 với Athena và kiểm tra kết quả.  
  * Kết nối kết quả truy vấn Athena với QuickSight để báo cáo và trực quan hóa.  

#### 5. **Thành thạo AWS CLI & Management Console:**  
  * Cấu hình AWS CLI với Access Key, Secret Key, và Default Region.  
  * Sử dụng CLI để lấy danh sách region, liệt kê dịch vụ, và kiểm tra cấu hình.  
  * Quản lý tài nguyên AWS bằng CLI và Console linh hoạt.  


