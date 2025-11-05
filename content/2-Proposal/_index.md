---
title: "Proposal"
date: 2025-09-07
weight: 2
chapter: false
pre: " <b> 2. </b> "
---

# URBAN RAILWAY SERVICE SYSTEM ON AWS  
### Secure — Scalable — Cost-Optimized Cloud Architecture

---

## Executive Summary

Ho Chi Minh City faces major transportation challenges, including congestion, pollution, and rapid urbanization.  
The **Urban Railway Project** is seen as a breakthrough toward building a smart, sustainable, and eco-friendly transportation system.

This proposal presents a **comprehensive AWS-based cloud architecture**, designed to support core functions such as:

- E-ticketing & cashless payment  
- Schedule management & operational monitoring  
- Data analytics & passenger flow optimization  

The architecture follows the principles of **serverless, event-driven, and CI/CD automation**, ensuring:

- High performance and elastic scalability.  
- Enterprise-grade end-to-end security.  
- Cost-efficient operation through a pay-as-you-go model.

---

## Key Highlights

*  100% cloud-native & serverless architecture (AWS Lambda, EventBridge)  
*  End-to-end enterprise security (Cognito, WAF, KMS)  
*  Fully automated CI/CD & observability (CodePipeline, CloudWatch)  
*  Seamless e-ticketing & cashless payment (VNPay, MoMo)  
*  Real-time analytics & predictive insights (Athena, QuickSight)  

---

## 1. Project Objectives

**General Objective:**  
To build a reliable, secure, and scalable digital infrastructure for Ho Chi Minh City’s Urban Railway System on AWS Cloud.

**Specific Objectives:**
- Deploy a **serverless & event-driven** architecture using AWS Lambda and EventBridge.  
- Provide **ticket booking, payment, authentication, and real-time schedule updates**.  
- Apply **end-to-end security** with WAF, Cognito, KMS, and Secrets Manager.  
- Automate CI/CD with **CodePipeline, CodeBuild, CodeDeploy**.  
- Enable **monitoring and compliance** through CloudWatch and CloudTrail.

---

## 2. Project Scope

| Component | Description |
|------------|-------------|
| **Location** | Metro Line 1 (Ben Thanh – Suoi Tien), Ho Chi Minh City |
| **Target Users** | Passengers, Operators, Administrators |
| **Implementation Duration** | 12 years (including deployment & long-term operation) |
| **Phase 1** | Ticketing, authentication, scheduling, payment |
| **Expansion Phase** | Predictive analytics, IoT monitoring, passenger optimization |

---

### 2.1 Functional Requirements

| ID | Requirement | Priority |
|----|--------------|----------|
| FR-01 | Users can book tickets and pay online | High |
| FR-02 | Real-time schedule updates via API | High |
| FR-03 | Automatic maintenance alerting | Medium |
| FR-04 | Admin dashboard for passenger analytics | Medium |
| FR-05 | Multi-language support (EN, VN) | Low |

---

### 2.2 Non-Functional Requirements

- **Availability:** ≥ 99.95% uptime (Multi-AZ)  
- **Latency:** < 300 ms for booking operations  
- **Security:** ISO 27001 & SOC 2 Type II compliant  
- **Scalability:** Auto-scale up to 100k concurrent users  
- **Cost Efficiency:** ≤ $100/month base infrastructure  

---

## 3. Proposed AWS Architecture

### 3.1 Overview

The system is designed with a **multi-tier, serverless, and automated** model, ensuring dynamic scalability, reliable operation, and comprehensive security.

---

### Architecture Diagram Summary

| Layer | Service | Role |
|--------|----------|------|
| **Frontend** | CloudFront + S3 | Static hosting, caching, HTTPS delivery |
| **API Layer** | API Gateway + Lambda | Business logic, event-driven functions |
| **Data** | RDS + S3 + DynamoDB | Persistent and analytical data storage |
| **Security** | WAF + Cognito + KMS | Authentication, encryption, protection |
| **Monitoring** | CloudWatch + GuardDuty | Metrics, alerts, and anomaly detection |

---

### 3.2 Networking & Access Layer
- **Amazon Route 53:** DNS management for global availability.  
- **Amazon CloudFront (CDN):** Distributes static content and reduces backend load.  
- **AWS WAF:** Protects against DDoS, SQL Injection, and XSS attacks.

---

### 3.3 Application & API Layer
- **Amazon API Gateway:** Provides secure RESTful endpoints.  
- **AWS Lambda:** Handles core business logic:
  - `BookingServiceLambda`: Ticket booking processing.  
  - `PaymentLambda`: VNPay/MoMo payment integration.  
  - `ScheduleLambda`: Schedule updates.  
  - `NotificationLambda`: Sends notifications (SNS, email, SMS).  
- **Amazon EventBridge:** Automates workflows (payment → invoice → notify).

---

### 3.4 Data & Storage Layer
- **Amazon RDS (SQL Server):** Stores users, tickets, and payment data.  
- **Amazon S3:** Stores static files, logs, invoices, and backups.  
  - Includes **Lifecycle Policy → S3 Glacier** for cost savings.  

---

### 3.5 Security & Authentication Layer
- **Amazon Cognito:** User registration, login, MFA, JWT token issuance.  
- **AWS Secrets Manager:** Stores and rotates sensitive keys.  
- **AWS KMS:** Encrypts RDS and S3 data.  
- **AWS CloudTrail:** Logs API activity for compliance and auditing.

---

### 3.6 Monitoring & Compliance Layer
- **Amazon CloudWatch:** Tracks performance metrics and Lambda/API logs.  
- **CloudWatch Alarms + SNS:** Sends automatic alerts.  
- **CloudTrail:** Monitors user and system activity.

---

### 3.7 CI/CD & Automation Layer
- **AWS CodePipeline:** Automates build–test–deploy workflows.  
- **AWS CodeBuild:** Tests backend/frontend code upon each commit.  
- **AWS CodeDeploy:** Enables zero-downtime deployment.  
- **GitHub Webhook:** Triggers pipelines automatically after commits.

---

### Data Flow (Simplified)
User -> CloudFront ->API Gateway -> Lambda -> RDS<br>
|v
EventBridge -> SNS/Email Notification<br>
|v
CloudWatch -> Admin Dashboard

---

## 4. Implementation Plan

| Phase | Duration | Key Tasks |
|--------|-----------|-----------|
| 1 | Weeks 1–2 | Setup Route 53, CloudFront, API Gateway, Lambda, RDS |
| 2 | Weeks 3–4 | Develop booking & authentication (Cognito, Lambda, EventBridge) |
| 3 | Weeks 5–6 | Integrate payments, configure CloudWatch & WAF |
| 4 | Weeks 7–8 | Setup CI/CD (CodePipeline, CodeBuild, CodeDeploy) |
| 5 | Expansion | Data analytics (Athena, QuickSight) |

---

## 5. Budget & Team

| Component | Services | Estimated Cost (USD/month) |
|------------|-----------|-----------------------------|
| Networking & CDN | Route 53, CloudFront, WAF | $15 |
| Backend Serverless | Lambda, API Gateway, EventBridge | $20 |
| Data & Storage | RDS, S3 | $35 |
| CI/CD | CodePipeline, CodeBuild, CodeDeploy | $10 |
| Security & Monitoring | CloudWatch, CloudTrail, Cognito, KMS | $15 |
| **Total** | — | **≈ $95–100/month** |

**Team Members:**
- Cloud Architect  
- Backend Developer (Lambda, API Gateway)  
- Frontend Developer (React, S3/CloudFront)  
- DevOps Engineer (CI/CD & Monitoring)  
- Metro Operations Specialist  

---

## 6. Expected Outcomes
- A **secure, modern platform** built on AWS Cloud.  
- **Cashless payments** and **automated ticket validation**.  
- **Scalable infrastructure**, ready for IoT integration.  
- **Operational transparency** via analytics dashboard.  
- **Optimized costs** under pay-as-you-go model.

---

## 7. Risks & Mitigation

| Risk | Mitigation |
|-------|-------------|
| AWS network outage | Implement Multi-AZ with automatic failover |
| Lambda overload | Enable autoscaling and set timeout limits |
| Security attack | Use WAF, IAM least privilege, and KMS |
| Data inconsistency | Automate RDS backup and recovery |
| Deployment errors | Enable CI/CD rollback and CloudFormation drift detection |

---

### 7.1 Risk Classification Matrix

| Risk | Likelihood | Impact | Mitigation |
|-------|-------------|---------|-------------|
| Network outage | Medium | High | Multi-AZ + Failover |
| API overload | High | Medium | Lambda concurrency + autoscaling |
| Data breach | Low | High | KMS encryption + WAF |
| CI/CD failure | Medium | Low | Rollback + versioning |

---

## 8. Compliance & Security

- **Compliance:** ISO 27001, GDPR-ready, SOC2 Type II  
- **Encryption:** AES-256 (KMS-managed)  
- **IAM Policies:** Principle of Least Privilege  
- **Monitoring:** Continuous auditing via CloudTrail & GuardDuty  

---

## 9. Conclusion

The **Urban Railway Service System on AWS** serves as a strategic foundation for digital transformation in Ho Chi Minh City’s public transportation sector.  
With a **serverless, event-driven, and CI/CD automated architecture**, this solution meets modern requirements for **security, performance, and cost efficiency**.  
Beyond technology, it is a key step toward a **smart city future**.

---

## 10. Success Metrics

| KPI | Target | Measurement Tool |
|------|--------|------------------|
| System Availability | ≥ 99.95% | CloudWatch uptime metrics |
| API Latency | < 300 ms | CloudWatch logs |
| Ticket Processing | 10,000+/day | Lambda invocation count |
| Cost Optimization | < $100/month | AWS Cost Explorer |
| Security Compliance | 100% | GuardDuty & IAM Audit |

---

## Appendix A — AWS Services Summary

| Category | Services Used | Purpose |
|-----------|----------------|----------|
| Networking | Route 53, CloudFront | DNS, CDN, HTTPS |
| Compute | Lambda | Serverless compute |
| API | API Gateway | REST API endpoints |
| Database | RDS (SQL Server) | Transactional data |
| Storage | S3 + Glacier | File storage & archival |
| Security | Cognito, WAF, KMS, Secrets Manager | Authentication & protection |
| DevOps | CodePipeline, CodeBuild, CodeDeploy | CI/CD automation |
| Monitoring | CloudWatch, CloudTrail, GuardDuty | Observability & compliance |

---

🖼️ *Illustration:*  
![AWS Architecture Diagram](/images/2-Proposal/aws_metropolitano_train_service.drawio.png)

