---
title: "Worklog Tuần 6"
date: 2025-09-07
weight: 1
chapter: false
pre: " <b> 1.6. </b> "
---



### Mục tiêu tuần 6:

- Hiểu và thực hành **AWS Backup**, bao gồm Backup Vault, Backup Plan, và triển khai bằng **AWS CloudFormation**.  
- Nắm bắt cách hoạt động của **AWS WAF (Web Application Firewall)** và **AWS PrivateLink**, hiểu các thành phần như ACL, Rule, Rule Group, VPC Endpoint Service và Network Load Balancer.  
- Tìm hiểu **AWS KMS (Key Management Service)** — bao gồm symmetric/asymmetric keys và vai trò của mã hóa trong bảo mật hệ thống.  
- Nắm vững khái niệm **Containerization với Docker**, hiểu quy trình tạo và triển khai ứng dụng bằng **Docker Image** và **Docker Compose**.  
- Thực hành tạo, cấu hình, và triển khai tài nguyên AWS theo mô hình **Infrastructure as Code** và container-based deployment.  

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - TÌm hiểu AWS Backup: <br>&emsp; + Backup vault <br>&emsp; + Backup plan <br>&emsp; + Sử dụng cloudFormation để tạo backup plan                                                                                            | 13/10/2025   | 15/10/2025      |<https://000013.awsstudygroup.com/>
| 3   |  - **Thực hành:** <br>&emsp; + Tạo backup plan <br>&emsp; +Tạo on-demand backup <br>&emsp; + Tạo backup vaults                                     | 13/10/2025   | 15/10/2025      | <https://cloudjourney.awsstudygroup.com/> |
| 4   | - Tìm hiểu AWS WAF và AWS privateLink : <br>&emsp; + ACL <br>&emsp; + Rules <br>&emsp; + Rules groups <br>&emsp; + VPC Endpoint Service <br>&emsp; + VPC Endpoint <br>&emsp; + Network Load Balancer| 15/10/2025   | 17/10/2025      | <https://000026.awsstudygroup.com/>  <br> <https://000111.awsstudygroup.com/> |
| 5   | - Tìm hiểu AWS KMS : <br>&emsp; + Symetric Key <br>&emsp; + Asymetric Key <br> -**Practice:** <br>&emsp; + Tạo ACLs <br>&emsp; + Create rules and rules group                   | 17/10/2025   | 19/10/2025      | <https://000033.awsstudygroup.com/> |
| 6   | - Tìm hiểu sự vận chuyển hàng container cùng với Docker:  <br>&emsp; + Docker là gì <br>&emsp; + Triển khai chỉ sử dụng Docker Image  <br&emsp; + Triển khai Docker compose và đẩy image                                     | 19/10/2025   | 21/10/2025      | <https://000015.awsstudygroup.com/> |


### Kết quả đạt được tuần 6:
- Hoàn thành việc học và thực hành **AWS Backup**, tạo thành công **Backup Vault**, **Backup Plan**, và **On-demand Backup** thông qua giao diện AWS và CloudFormation template.  
- Thiết lập và thử nghiệm **AWS WAF**, bao gồm việc tạo **ACLs**, **Rules**, và **Rule Groups** để bảo vệ ứng dụng web.  
- Hiểu rõ cơ chế hoạt động của **AWS PrivateLink**, triển khai **VPC Endpoint Service** và **VPC Endpoint** kết nối qua **Network Load Balancer**.  
- Nghiên cứu và áp dụng **AWS KMS**, tạo và quản lý **Symmetric** và **Asymmetric keys** để mã hóa dữ liệu.  
- Tạo và triển khai ứng dụng bằng **Docker**, thực hành build Docker Image, chạy container, triển khai với **Docker Compose**, và push image lên Docker Hub.  
- Củng cố kiến thức về **Cloud Security** và **Containerization**, chuẩn bị nền tảng cho việc triển khai hệ thống thực tế trên môi trường **AWS Cloud**. 