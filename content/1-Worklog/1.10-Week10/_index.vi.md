---
title: "Tuần 10 Worklog"
date: 2025-09-07
weight: 2
chapter: false
pre: " <b> 1.10. </b> "
---

### Mục tiêu Tuần 10:

- Thực hành các dịch vụ cốt lõi của AWS (VPC, EC2, EBS, Postgres)
- Học AWS SageMaker cho workflow AI/ML
- Thực hành phân tích dữ liệu AI/ML với SageMaker
- Học các thành phần AWS Bedrock AgentCore
- Học AWS Glue và Amazon Athena cho ETL và phân tích dữ liệu

### Công việc thực hiện trong tuần:
| Ngày | Công việc                                                                                                                                                                                                   | Ngày bắt đầu | Ngày kết thúc | Tài liệu tham khảo                        |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------- | --------------- | ----------------------------------------- |
| 2   | - **Thực hành:** <br>&emsp; + Tạo VPC <br>&emsp; + Khởi tạo EC2 instances <br>&emsp; + Tạo ổ EBS <br>&emsp; + Gắn ổ EBS <br>&emsp; Cài đặt Postgres <br>&emsp; Mount EBS EC2 production <br>&emsp; + Backup Postgres <br>&emsp; Mount EBS EC2 test <br>&emsp; + Khôi phục dữ liệu                                                                                                 | 08/11/2025 | 10/11/2025      |                                           |
| 3   | - Học **AWS SageMaker AI**:<br>&emsp; + SageMaker là gì <br>&emsp; + Các thành phần của SageMaker <br>&emsp; + Quy trình end-to-end                                              | 10/11/2025 | 12/11/2025      | <https://000200.awsstudygroup.com/>       |
| 4   | - **Thực hành:** Sử dụng Amazon SageMaker AI để phân tích dữ liệu, nhập file Excel, chọn kiểu dữ liệu và xuất kết quả kèm biểu đồ                       | 10/11/2025 | 12/11/2025      | <https://000200.awsstudygroup.com/>       |
| 5   | - Học **AWS Bedrock AgentCore**:<br>&emsp; + Identity <br>&emsp; + Memory <br>&emsp; + Code Interpreter <br>&emsp; + Browser <br>&emsp; + Gateway <br>&emsp; + Observability <br>&emsp; + Các trường hợp sử dụng phổ biến: Trang bị agent với các công cụ và khả năng sẵn có, Triển khai an toàn ở quy mô lớn, Giám sát và kiểm tra agent | 12/11/2025 | 14/11/2025      | <https://docs.aws.amazon.com/bedrock-agentcore/latest/devguide/what-is-bedrock-agentcore.html> |
| 6   | - Học **AWS Glue** và **Amazon Athena**                                                                                  | 14/11/2025 | 16/11/2025      | <https://000040.awsstudygroup.com/>       |

### Thành tựu Tuần 10:

* **Thực hành các dịch vụ cơ bản của AWS:**
  * Tạo VPC với các subnet, bảng định tuyến và Internet Gateway hợp lý.
  * Khởi tạo EC2 cho môi trường production và test.
  * Tạo và gắn EBS vào các instance EC2.
  * Cài đặt và cấu hình PostgreSQL trên EC2.
  * Mount EBS trên cả production và test instance.
  * Thực hiện backup và phục hồi dữ liệu PostgreSQL thành công.

* **Học và thực hành AWS SageMaker AI:**
  * Hiểu các thành phần của SageMaker: Notebook, Training, Endpoint, Model, Pipelines.
  * Hoàn thành workflow AI/ML end-to-end: nhập dữ liệu Excel, phân tích dữ liệu, trực quan hóa biểu đồ.
  * Học cách chọn kiểu dữ liệu phù hợp, làm sạch dữ liệu và xuất kết quả để sử dụng tiếp.

* **Học AWS Bedrock AgentCore:**
  * Nắm các thành phần chính: Identity, Memory, Code Interpreter, Browser, Gateway, Observability.
  * Khám phá các trường hợp sử dụng phổ biến:
    - Trang bị các công cụ và khả năng sẵn có cho agent.
    - Triển khai agent an toàn ở quy mô lớn.
    - Giám sát và kiểm tra agent trong thực tế.

* **Học AWS Glue & Amazon Athena:**
  * Thực hành xây dựng pipeline ETL với AWS Glue.
  * Học cách catalog dữ liệu và chuyển đổi dữ liệu phục vụ phân tích.
  * Truy vấn dữ liệu từ S3 bằng Amazon Athena và xác minh kết quả.
  * Kết nối các truy vấn Athena với dashboard QuickSight để báo cáo và trực quan hóa.

* **Thành thạo AWS CLI & Management Console:**
  * Cấu hình AWS CLI với Access Key, Secret Key và Default Region.
  * Sử dụng CLI để kiểm tra các region, danh sách dịch vụ và thông tin cấu hình.
  * Quản lý tài nguyên AWS song song giữa CLI và giao diện web.

* **Thành tựu tổng quát:**
  * Có kinh nghiệm thực hành trực tiếp với nhiều dịch vụ AWS khác nhau.
  * Tự tin kết nối các dịch vụ để xây dựng workflow thực tế.
  * Kết hợp được compute, storage, networking, database, AI/ML, ETL và analytics trong các bài tập thực hành.
