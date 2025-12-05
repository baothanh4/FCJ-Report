---
title: "Tuần 13 Worklog"
date: 2025-09-07
weight: 2
chapter: false
pre: " <b> 1.13. </b> "
---

### Mục tiêu Tuần 12

Trong tuần này, mục tiêu chính là học và thực hành các dịch vụ và công cụ liên quan đến việc di chuyển hạ tầng (Migration), phục hồi thảm họa (Disaster Recovery), và chuyển đổi cơ sở dữ liệu (Database Conversion). Cụ thể gồm:

- Tìm hiểu và thực hành **AWS VM Import/Export**.
- Nghiên cứu và sử dụng **AWS Database Migration Service (DMS)** và **AWS Schema Conversion Tool (SCT)**.
- Tìm hiểu và thực hành **AWS Elastic Disaster Recovery (DRS)**.

---

### Nhiệm vụ trong tuần

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | Learn AWS VM Import/Export | 02/12/2025 | 03/12/2025 | https://000014.awsstudygroup.com/ |
| 3 | Practice AWS VM Import/Export | 03/12/2025 | 04/12/2025 | https://000014.awsstudygroup.com/ |
| 4 | Learn and Practice AWS Database Migration Service (DMS) and Schema Conversion Tool (SCT) | 04/12/2025 | 05/12/2025 | https://000043.awsstudygroup.com/ |
| 5 | Learn AWS Elastic Disaster Recovery | 05/12/2025 | 06/12/2025 | https://000100.awsstudygroup.com/ |
| 6 | Practice AWS Elastic Disaster Recovery | 06/12/2025 | 07/12/2025 | https://000113.awsstudygroup.com/ |

---

### Thành tích Tuần 13

#### **1. AWS VM Import/Export**
- Hiểu quy trình import máy ảo (OVA/VMDK) lên AWS.
- Tạo IAM role `vmimport`, cấu hình S3 bucket, và thực hiện import AMI thành công.
- Thực hành export AMI về lại dạng OVA cho môi trường on-prem.

#### **2. AWS Database Migration Service + Schema Conversion Tool**
- Dùng SCT để phân tích và chuyển đổi schema (vd: SQL Server → PostgreSQL).
- Xử lý các phần không tương thích do SCT báo cáo.
- Thiết lập DMS: replication instance + source/target endpoints.
- Thực hiện full load + CDC (Change Data Capture) để đồng bộ dữ liệu realtime.

#### **3. AWS Elastic Disaster Recovery**
- Nắm kiến trúc đầy đủ: replication agent, replication server, staging area subnet.
- Cài đặt DRS Agent trên máy nguồn và replicate dữ liệu sang AWS.
- Thực hiện test failover → launch server trên AWS → đánh giá RTO/RPO.
- Khôi phục lại (failback) thành công.



