---
title: "Week 13 Worklog"
date: 2025-09-07
weight: 2
chapter: false
pre: " <b> 1.13. </b> "
---

### Week 13 Objectives

This week focuses on learning and practicing AWS services related to infrastructure migration, database conversion, and disaster recovery. Specifically:

- Learn and practice **AWS VM Import/Export**.
- Study and use **AWS Database Migration Service (DMS)** and **AWS Schema Conversion Tool (SCT)**.
- Learn and practice **AWS Elastic Disaster Recovery (DRS)**.

---

### Tasks to be carried out this week

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | Learn AWS VM Import/Export | 02/12/2025 | 03/12/2025 | https://000014.awsstudygroup.com/ |
| 3 | Practice AWS VM Import/Export | 03/12/2025 | 04/12/2025 | https://000014.awsstudygroup.com/ |
| 4 | Learn & Practice AWS DMS and SCT | 04/12/2025 | 05/12/2025 | https://000043.awsstudygroup.com/ |
| 5 | Learn AWS Elastic Disaster Recovery | 05/12/2025 | 06/12/2025 | https://000100.awsstudygroup.com/ |
| 6 | Practice AWS Elastic Disaster Recovery | 06/12/2025 | 07/12/2025 | https://000113.awsstudygroup.com/ |

---


### **Achievements**

#### **1. AWS VM Import/Export**
- Learned how to import VMs (OVA/VMDK) to AWS.
- Created the `vmimport` IAM role and configured S3 for VM storage.
- Successfully imported an AMI and exported it back to OVA format.

#### **2. AWS Database Migration Service + Schema Conversion Tool**
- Used SCT to analyze and convert schema across different database engines (ex: SQL Server → PostgreSQL).
- Fixed incompatibilities reported by SCT.
- Configured DMS replication instance and endpoints.
- Performed full-load and CDC (Change Data Capture) replication with continuous synchronization.

#### **3. AWS Elastic Disaster Recovery**
- Understood architecture: replication agent, replication server, staging area subnet.
- Installed the DRS agent on source machines and replicated to AWS.
- Executed test failover and validated RPO/RTO performance.
- Completed successful failback to the original environment.



