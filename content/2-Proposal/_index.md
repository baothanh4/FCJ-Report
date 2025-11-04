---
title: "Proposal"
date: 2025-09-07
weight: 2
chapter: false
pre: " <b> 2. </b> "
---

# Metropolitan Railway Service System on AWS — Secure, Scalable, and Cost-Optimized Cloud Architecture

### 1. Introduction
As Ho Chi Minh City continues to expand rapidly, transportation challenges such as congestion and air pollution are intensifying.  
The **Metropolitan Railway Project** represents a strategic initiative to deliver a modern, sustainable, and intelligent public transportation system.  

This proposal introduces a **comprehensive AWS-based cloud architecture** designed to power digital ticket booking, cashless payments, train scheduling, and operational analytics.  
The solution leverages **serverless**, **event-driven**, and **CI/CD-enabled** AWS services to ensure scalability, cost efficiency, and robust security.

---

### 2. Objectives
**General Objective:**  
To build a reliable and secure digital infrastructure for the Ho Chi Minh City Metropolitan Railway using AWS Cloud.

**Specific Objectives:**
- Deploy a **serverless and event-driven** cloud architecture using AWS Lambda and EventBridge.  
- Enable **online booking**, **digital payments**, and **real-time train schedule updates**.  
- Implement **end-to-end security** via WAF, Cognito, KMS, and Secrets Manager.  
- Integrate **CI/CD automation** with CodePipeline, CodeBuild, and CodeDeploy.  
- Establish **monitoring and compliance** with CloudWatch and CloudTrail.

---

### 3. Scope
- **Location:** Ho Chi Minh City Metro Line 1 (Bến Thành – Suối Tiên)  
- **Target Users:** Passengers, Metro Staff, Administrators  
- **Project Duration:** 12 years (from initial deployment to long-term operations)  
- **Phase 1 Coverage:** Ticket booking, authentication, scheduling, and payments  
- **Future Phases:** Predictive analytics, IoT-based train monitoring, and passenger flow optimization  

---

### 4. AWS Cloud Architecture
The proposed system follows a **multi-layered, serverless AWS architecture** combining scalability, automation, and enterprise-grade security.

---

#### **1. Network and Access Layer**
- **Amazon Route 53:**  
  Manages domain routing for the Metro web and mobile portals. Ensures global DNS availability and low-latency routing.  
- **Amazon CloudFront (CDN):**  
  Distributes static frontend assets globally with low latency, reducing load on backend systems.  
- **AWS WAF (Web Application Firewall):**  
  Protects the application from DDoS, SQL injection, and cross-site scripting attacks.  
- **AWS Shield (Integrated with CloudFront):**  
  Provides automatic DDoS protection for network and transport layers.  

---

#### **2. CI/CD and Automation Layer**
- **AWS CodePipeline:**  
  Automates the entire build–test–deploy workflow, ensuring continuous integration and delivery for all application components.  
- **AWS CodeBuild:**  
  Compiles and tests backend and frontend code automatically after each GitHub commit.  
- **AWS CodeDeploy:**  
  Deploys new versions of Lambda functions and API configurations without downtime.  
- **GitHub Integration:**  
  Serves as the source control repository, triggering CI/CD pipelines via webhook events.  

---

#### **3. Authentication and Security Layer**
- **Amazon Cognito:**  
  Manages user registration, login, password recovery, and MFA-based authentication. Issues secure JWT tokens for API access.  
- **AWS Secrets Manager:**  
  Stores sensitive credentials (e.g., RDS passwords, API keys) securely and rotates them automatically.  
- **AWS KMS (Key Management Service):**  
  Provides encryption for data at rest in RDS, S3, and environment variables in Lambda.  
- **AWS CloudTrail:**  
  Logs and monitors every API call across all AWS accounts, ensuring compliance and traceability.  

---

#### **4. Application and API Layer**
- **Amazon API Gateway:**  
  Exposes secure RESTful endpoints for mobile/web clients and routes requests to backend Lambda functions.  
- **AWS Lambda (Serverless Backend):**  
  Handles all business logic through modular microservices:
  - `BookingServiceLambda` — Creates bookings and validates requests.  
  - `PaymentLambda` — Processes VNPay or Momo payments.  
  - `ScheduleLambda` — Manages timetable queries and updates.  
  - `NotificationLambda` — Sends email/SMS notifications through SNS.  
  - `EventBridge` — Triggers automated workflows (e.g., payment success → send receipt).  
- **Amazon EventBridge:**  
  Coordinates asynchronous events such as booking confirmation, cancellations, or delayed schedules.  

---

#### **5. Data and Storage Layer**
- **Amazon RDS (SQL Server):**  
  Hosts structured data — passenger profiles, bookings, and payment transactions. Runs in private subnets with daily backups to S3.  
- **Amazon DynamoDB (Optional Extension):**  
  Provides real-time caching for schedules and session data.  
- **Amazon S3:**  
  - Hosts static frontend web assets (React app).  
  - Stores logs, receipts, and backup files.  
  - Implements lifecycle policies to archive data to **S3 Glacier** for cost optimization.  

---

#### **6. Monitoring, Logging, and Compliance**
- **Amazon CloudWatch:**  
  Tracks performance metrics, Lambda logs, and API Gateway latency. Generates alarms for operational anomalies.  
- **CloudWatch Alarms + SNS:**  
  Notifies the DevOps team about threshold breaches (CPU usage, 5XX errors, etc.).  
- **AWS CloudTrail:**  
  Records all API activities for auditing and compliance (ISO/GDPR-ready).  

---

### 5. Implementation Plan
| **Phase** | **Duration** | **Key Deliverables** |
|------------|--------------|----------------------|
| **Phase 1** | Weeks 1–2 | Set up core AWS infrastructure: Route 53, CloudFront, API Gateway, Lambda, RDS |
| **Phase 2** | Weeks 3–4 | Develop booking and authentication (Cognito, Lambda, EventBridge) |
| **Phase 3** | Weeks 5–6 | Integrate payments, CloudWatch monitoring, and WAF protection |
| **Phase 4** | Weeks 7–8 | Configure CI/CD pipelines using CodePipeline, CodeBuild, and CodeDeploy |
| **Phase 5** | Future | Add analytics layer (Athena, QuickSight) |

---

### 6. Budget & Resources
| **Component** | **Main Services** | **Estimated Monthly Cost (USD)** |
|----------------|-------------------|----------------------------------|
| Network & CDN | Route 53, CloudFront, WAF | $15 |
| Serverless Backend | Lambda, API Gateway, EventBridge | $20 |
| Database & Storage | RDS, S3 | $35 |
| CI/CD | CodePipeline, CodeBuild, CodeDeploy | $10 |
| Security & Monitoring | CloudWatch, CloudTrail, Cognito, Secrets Manager, KMS | $15 |
| **Total Estimate** | — | **≈ $95–100/month** |

**Human Resources:**
- Cloud Architect  
- Backend Developer (Lambda / API Gateway)  
- Frontend Developer (React)  
- DevOps Engineer (CI/CD & Monitoring)  
- Metro Operations Specialist  

---

### 7. Expected Outcomes
- A **secure, cloud-native railway management platform** for passengers and administrators.  
- Seamless **cashless ticketing** with automated booking confirmations.  
- Scalable architecture supporting future IoT integration.  
- Improved transparency and monitoring through analytics dashboards.  
- Cost-effective operations with pay-as-you-go cloud pricing.  

---

### 8. Conclusion
The proposed **Metropolitan Railway Service System on AWS** establishes a strong foundation for digital transformation in urban transportation.  
By combining **serverless computing**, **CI/CD automation**, and **end-to-end AWS security**, the system ensures operational excellence, scalability, and compliance with modern data standards.  
This architecture not only supports current ticketing and scheduling needs but also positions the Metro for **future smart-city integration and data-driven decision-making**.

---

![AWS Architecture Diagram](/images/2-Proposal/aws_metropolitano_train_service.drawio.png)
