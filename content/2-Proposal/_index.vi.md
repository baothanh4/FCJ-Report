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

This proposal presents an **AWS microservices architecture using Amazon ECS Fargate**, enabling:

- Ticket booking, scheduling, payments, and traffic monitoring  
- Real-time passenger data ingestion through Amazon Kinesis  
- BI dashboards and predictive analytics with QuickSight and SageMaker  
- Full CI/CD automation and comprehensive monitoring  

---

## Key Highlights

- **Microservices container architecture** powered by Amazon ECS Fargate  
- End-to-end security: Route53 → CloudFront → WAF → ALB → Private Subnets  
- Fully automated CI/CD using CodePipeline, CodeBuild, CodeDeploy, ECR  
- Real-time processing using **Kinesis Data Streams**  
- Analytics & forecasting with **QuickSight + SageMaker**  
- Scalability for hundreds of thousands of daily ticket requests  

---

# 1. Project Objectives

### Primary Objective  
Build a digital platform for the Urban Rail Transit System with scalability, security, and long-term operational stability.

### Specific Objectives
- Implement ticketing, scheduling, payment, and notification services as microservices  
- Enable automated operations and system-wide monitoring  
- Establish a full CI/CD pipeline with zero downtime  
- Support real-time passenger data ingestion and analytics  
- Provide multi-AZ architecture with ≥ 99.95% system availability  

---

# 2. Project Scope

| Component           | Description                              |
|--------------------|------------------------------------------|
| Region             | AWS Singapore (ap-southeast-1)           |
| Users              | Passengers, operators, administrators     |
| Architecture Style | Microservices on ECS Fargate             |
| Phase 1            | Ticketing, scheduling, notifications      |
| Phase 2            | Analytics, BI dashboards, AI forecasting |

---

# 3. Proposed AWS Architecture

## 3.1 Architecture Overview

A **multi-tier microservices architecture** will be deployed, including:

- **Edge Layer:** Route53, CloudFront, AWS WAF  
- **Application Layer:** ALB → ECS Fargate → ECR  
- **Data Layer:** RDS SQL Server, ElastiCache Redis  
- **Event Layer:** EventBridge, SNS, SQS  
- **Analytics Layer:** Kinesis → S3 → QuickSight → SageMaker  
- **Monitoring Layer:** CloudWatch, CloudTrail  
- **CI/CD Layer:** CodePipeline, CodeBuild, CodeDeploy  

---

## 3.2 Networking & Access Layer

- **Route 53:** Global DNS routing  
- **CloudFront:** CDN caching and low-latency access  
- **AWS WAF:** Protection from DDoS, SQL injection, XSS  
- **Application Load Balancer:** Routes traffic to microservices  

**Traffic Flow:**  
**User → Route53 → CloudFront → WAF → ALB → Private Subnet → ECS Fargate**

---

## 3.3 Application Layer — Microservices on ECS Fargate

### Why Fargate?
- No server management  
- Autoscaling based on CPU/Memory  
- High security in private subnets  

### Microservices
- Booking Service  
- Schedule Service  
- Payment Service  
- Notification Service  
- User Service  
- Staff & Operation Service  

**Docker Images** stored in **Amazon ECR**

---

## 3.4 Data Layer

### Amazon RDS (SQL Server)
- Stores tickets, schedules, user accounts, payments  
- Multi-AZ high availability  
- Automated backup and failover  

### ElastiCache Redis
- Cache schedules → reduce RDS load  
- Increase API performance up to 10×  

### Amazon S3
- Stores reports, invoices, files  
- Destination for streaming data from Kinesis  

---

## 3.5 Event & Messaging Layer

### Amazon EventBridge
Automates workflows, including:
- PaymentSuccess → CreateInvoice → NotifyUser  
- ScheduleUpdate → BroadcastToMobile  

### Amazon SQS
- Queue system for notifications and ticket processing  
- Protects services during traffic spikes  

### Amazon SNS
- Sends SMS, email, and push notifications  

---

## 3.6 Real-Time Analytics

### Kinesis Data Streams
- Ingests passenger traffic in real time  
- Application logs → Kinesis → S3  

### QuickSight
- Dashboards for daily sales, station load, peak hours  

### SageMaker
- Predict passenger demand  
- Optimize train frequencies during peak hours  

---

## 3.7 Monitoring & Observability

- **CloudWatch Metrics:** CPU, Memory, ALB latency  
- **CloudWatch Logs:** Fargate application logs  
- **SNS Alerts:** Error notifications  
- **CloudTrail:** Governance & admin activity tracking  

---

## 3.8 CI/CD Pipeline

Developer Commit  
→ CodePipeline  
→ CodeBuild  
→ Build Docker Image  
→ ECR  
→ CodeDeploy  
→ ECS Fargate

### Features:
- Rolling deployments with **zero downtime**  
- ALB health checks  
- Automatic rollback on failure  

---

# 4. Deployment Plan

| Phase | Duration | Deliverables                        |
|-------|----------|-------------------------------------|
| 1     | 1 week   | Route53, CloudFront, WAF, VPC, ALB |
| 2     | 3 weeks  | ECS, ECR, RDS, ElastiCache          |
| 3     | 1 week   | EventBridge, SQS, SNS               |
| 4     | 3 weeks  | Kinesis, S3, QuickSight             |
| 5     | 2 weeks  | CI/CD Pipeline                      |
| 6     | 2 weeks  | Security hardening, cost tuning     |

---

# 5. Estimated Monthly Operational Cost

| Service                         | Cost/Month |
|--------------------------------|------------|
| CloudFront + Route53 + WAF     | $24        |
| ECS Fargate                    | $40        |
| RDS                             | $19        |
| ElastiCache Redis              | $73        |
| S3 + Kinesis                   | $1         |
| Monitoring                     | $37        |
| CI/CD                          | $18        |
| **Total Estimated Cost**       | **$212**   |

---

# 6. Expected Outcomes

- Stable 24/7 rail transit operations  
- 1,000+ concurrent users supported  
- Secure and automated payment processing  
- Accurate passenger demand forecasting  
- Reduced operation costs through autoscaling and CI/CD  

---

# Appendix A — AWS Services Summary

| Category     | AWS Services                                      |
|--------------|---------------------------------------------------|
| Edge         | Route53, CloudFront, WAF                          |
| Networking   | VPC, ALB                                          |
| Compute      | ECS Fargate, ECR                                  |
| Database     | RDS SQL Server, ElastiCache                       |
| Event        | EventBridge, SNS, SQS                             |
| Analytics    | Kinesis, S3, QuickSight, SageMaker                |
| Monitoring   | CloudWatch, CloudTrail                            |
| CI/CD        | CodePipeline, CodeBuild, CodeDeploy               |

![AWS-architecture](/images/2-Proposal/aws_architecture.png)