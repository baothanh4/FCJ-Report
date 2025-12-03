---
title: "Proposal"
date: 2025-09-07
weight: 2
chapter: false
pre: "<b> 2. </b>"
---

# URBAN RAIL TRANSIT SERVICE SYSTEM ON AWS

---

## Executive Summary

Rapid urban development has increased the need for intelligent and sustainable public transportation. A modern Urban Rail Transit System requires a reliable, scalable, and highly available digital platform operating 24/7.

This proposal presents an **AWS architecture built on Amazon EC2**, ensuring full control, high performance, and flexibility for mission-critical workloads.

The platform supports:

- Ticket booking, scheduling, payments, and traffic monitoring  
- Real-time passenger data ingestion through Amazon Kinesis  
- BI dashboards and predictive analytics with QuickSight and SageMaker  
- Full CI/CD automation and comprehensive monitoring  

---

## Key Highlights

- **EC2-based architecture** with Auto Scaling & ALB  
- End-to-end security: Route53 → CloudFront → WAF → ALB → Private EC2  
- Fully automated CI/CD using CodePipeline, CodeBuild, CodeDeploy  
- Real-time processing using **Kinesis Data Streams**  
- Analytics with **QuickSight**  
- High availability & scalability across multiple AZs  

---

# 1. Project Objectives

### Primary Objective  
Build a digital platform for the Urban Rail Transit System with scalability, security, and long-term operational stability.

### Specific Objectives
- Implement ticketing, scheduling, payment, and notification services  
- Enable automated operations and system-wide monitoring  
- Establish a full CI/CD pipeline with zero downtime deployment to EC2  
- Support real-time passenger data ingestion and analytics  
- Provide multi-AZ architecture with ≥ 99.95% availability  

---

# 2. Project Scope

| Component           | Description                              |
|---------------------|------------------------------------------|
| Region              | AWS Singapore (ap-southeast-1)           |
| Users               | Passengers, operators, administrators    |
| Architecture Style  | Multi-tier architecture on EC2           |
| Phase 1             | Ticketing, scheduling, notifications     |
| Phase 2             | Analytics, BI dashboards                 |

---

# 3. Proposed AWS Architecture

## 3.1 Architecture Overview

A **multi-tier architecture** will be deployed, including:

- **Edge Layer:** Route53, CloudFront, AWS WAF  
- **Application Layer:** ALB → EC2 Auto Scaling Group  
- **Data Layer:** RDS SQL Server, ElastiCache Redis  
- **Event Layer:** EventBridge, SNS, SQS  
- **Analytics Layer:** Kinesis → S3 → QuickSight → SageMaker  
- **Monitoring Layer:** CloudWatch, CloudTrail  
- **CI/CD Layer:** CodePipeline, CodeBuild, CodeDeploy  

---

## 3.2 Networking & Access Layer

- **Route 53:** Global DNS routing  
- **CloudFront:** CDN caching and global acceleration  
- **AWS WAF:** Security filtering (SQLi, XSS, bots)  
- **Application Load Balancer:** Routes traffic to EC2  

**Traffic Flow:**  
**User → Route53 → CloudFront → WAF → ALB → Private Subnet → EC2 Instances**

---

## 3.3 Application Layer — EC2 Auto Scaling

### Why EC2?
- Full control over OS, runtime, and application environment  
- Suitable for monolithic or microservice deployments  
- Reliable for long-running backend services  
- Auto Scaling based on CPU, network, request count  
- EC2 roles for secure access to AWS resources  

### Application Deployment Model
- Backend components deployed on **EC2 Auto Scaling Group**  
- EC2 instances in **Private Subnets** for security  
- Deployed via **CodeDeploy (Blue/Green or Rolling)**  

### Backend Services Include:
- Booking Service  
- Schedule Service  
- Payment Service  
- Notification Service  
- User Service  
- Operation & Reporting Service  

---

## 3.4 Data Layer

### Amazon RDS (SQL Server)
- Stores tickets, schedules, user accounts, payments  
- Multi-AZ deployment ensures HA  
- Automated backups and failover  
- IAM authentication + encryption  

### Amazon S3
- Stores documents, reports, logs, analytics data  
- Destination for Kinesis stream data  
- Lifecycle storage tiering for cost reduction  

---

## 3.5 Event & Messaging Layer

### Amazon EventBridge
Automates operations, e.g.:
- PaymentSuccess → CreateInvoice → NotifyUser  
- TrainDelay → PushNotifications → Dashboard Update  

### Amazon SQS
- Buffer queue for heavy workloads  
- Prevents overload during peak hours  

### Amazon SNS
- Sends multi-channel notifications (SMS, email, push)  

---

## 3.6 Real-Time Analytics

### Kinesis Data Streams
- Real-time ingestion of passenger flow data  
- App logs → Kinesis → S3 for analytics  

### QuickSight
- Business dashboards: ticket sales, peak traffic, service delays  



---

## 3.7 Monitoring & Observability

- **CloudWatch Metrics:** EC2 performance, ALB latency, RDS metrics  
- **CloudWatch Logs:** Application logs from EC2 via CloudWatch Agent  
- **SNS Alerts:** Critical system alerts  
- **CloudTrail:** Governance and audit logs  

---

## 3.8 CI/CD Pipeline

Developer Commit  
→ CodePipeline  
→ CodeBuild (build + test)  
→ Artifact Storage  
→ CodeDeploy  
→ EC2 Auto Scaling Group

### Deployment Features
- Blue/Green or Rolling EC2 deployment  
- Health check via ALB  
- Automatic rollback on failure  
- Zero downtime upgrade capability  

---

# 4. Deployment Plan

| Phase | Duration | Deliverables                        |
|-------|----------|-------------------------------------|
| 1     | 1 week   | Route53, CloudFront, WAF, VPC, ALB  |
| 2     | 3 weeks  | EC2 ASG, RDS                        |
| 3     | 1 week   | EventBridge, SQS, SNS               |
| 4     | 3 weeks  | Kinesis, S3, QuickSight             |
| 5     | 2 weeks  | CI/CD Pipeline (CodeDeploy)         |
| 6     | 2 weeks  | Hardening, cost optimization        |

---

# 5. Estimated Monthly Operational Cost (EC2 Architecture)

| Service                         | Cost/Month |
|--------------------------------|------------|
| CloudFront + Route53 + WAF     | $24        |
| EC2 ASG (t3.micro x 2 AZ)       | $38        |
| RDS                             | $19        |
| S3 + Kinesis                   | $1         |
| Monitoring                     | $37        |
| CI/CD                          | $18        |
| **Total Estimated Cost**       | **$210**   |

---

# 6. Expected Outcomes

- Reliable 24/7 transit system operations  
- High-availability EC2 backend with autoscaling  
- Secure payment processing and protected endpoints  
- Real-time passenger analytics  
- Optimized operational cost with correctly sized instances  
- Zero-downtime deployment and easy maintenance  

---

# Appendix A — AWS Services Summary

| Category     | AWS Services                                      |
|--------------|---------------------------------------------------|
| Edge         | Route53, CloudFront, WAF                          |
| Networking   | VPC, ALB                                          |
| Compute      | EC2, Auto Scaling Group                           |
| Database     | RDS SQL Server                 |
| Event        | EventBridge, SNS, SQS                             |
| Analytics    | Kinesis, S3, QuickSight                           |
| Monitoring   | CloudWatch, CloudTrail                            |
| CI/CD        | CodePipeline, CodeBuild, CodeDeploy               |

![AWS-architecture](/images/2-Proposal/aws_metropolitano_train_service.png)
