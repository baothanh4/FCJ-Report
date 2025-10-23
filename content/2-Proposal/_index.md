---
title: "Proposal"
date: 2025-09-07
weight: 2
chapter: false
pre: " <b> 2. </b> "
---


# Metropolitan Railway Service System with AWS — Secure, Scalable, and Cost-Efficient Cloud Architecture



### 1. Introduction
As Ho Chi Minh City expands rapidly, its transportation system faces congestion and environmental challenges. The Metropolitan Railway Project aims to provide a smart, sustainable, and efficient public transport solution that reduces private vehicle dependency.
To ensure reliability and security, this proposal introduces an AWS-based digital architecture that powers ticket booking, payments, scheduling, and operational analytics — all within a serverless, cost-optimized, and beginner-friendly environment.



### 2. Objectives
* <b>General Objective:</b>
Develop a secure, scalable, and user-friendly digital backbone for the Metropolitan Railway system.
* <b>Specific Objectives:</b>
    + Implement a serverless AWS architecture for cost efficiency and elasticity.
    + Enable cashless e-ticketing, online scheduling, and real-time train updates.
    + Protect passenger data with encryption, IAM, and WAF security layers.
    + Establish monitoring and alerting for operational reliability.

### 3. Scope
+ Location:  Ho Chi Minh City Metro Line 1 (Bến Thành – Suối Tiên)
+ Target Users: Passengers, Metro staff, Administrators
+ Duration: 12 years (from deployment to operation)
+ Limitations: Phase 1 focuses on booking, payment, and schedule management; IoT train automation and predictive analytics will be introduced later.


### 4. AWS Cloud Architecture
* Security Layer
    * AWS WAF – Protect APIs and endpoints from attacks (SQLi, XSS, DDoS).
    * Ensures all communication passes through secure HTTPS channels.
* API & Authentication Layer
    * Amazon API Gateway – Entry point for mobile/web clients, routing requests to backend functions.
    * Amazon Cognito – Manages authentication, sign-up, password recovery, and JWT tokens.
    * Ensures controlled access and user identity verification.
* Backend Layer (Serverless)
    * Each function resides inside a VPC for security and connectivity to private resources:
        * AWS Lambda Functions:
            * Ticket Booking Lambda – Handles booking creation, validation, and ticket code generation.
            * Train Schedule Lambda – Manages train timetables and updates.
            * Payment Lambda – Integrates with third-party payment APIs (e.g., VNPay, Momo).
            * Notification Lambda – Sends email/SMS confirmations to users.
    * Average monthly cost for all Lambda functions: ~$15/month (Free Tier included).
*  Data Layer
    * Amazon RDS (SQL Server) – Stores passenger accounts, ticket transactions, and schedules.
    * Amazon DynamoDB – Handles high-speed data like real-time train status and seat availability.
    * Encrypted using KMS-managed keys for compliance and privacy.
*  Secret & Encryption Layer
    * AWS Secrets Manager – Safely stores credentials, database URIs, and API keys.
    * AWS KMS (Key Management Service) – Manages encryption for S3, RDS, and Lambda data.
    * Ensures sensitive information never appears in plain text in code or environment variables.
*  Storage & Backup Layer
    * Amazon S3 – Hosts frontend web assets (React, Angular), Stores data backups, logs, and user-uploaded receipts.
    * Lifecycle Policies move old data to S3 Glacier for cost savings.
    * Estimated cost: ~$5/month.
*  Monitoring & Alerting Layer
    * Amazon CloudWatch – Tracks Lambda logs, API Gateway metrics, and error rates.
*  Data Analytics & Insights (Phase 2)
    * Amazon Athena – Generate dashboards on passenger volume, route performance, and payment statistics.

![IoT Weather Station Architecture](/images/2-Proposal/aws_metropolitano_train_service.drawio.png)

### 5. Implementation Plan
* Week 1–2: Configure AWS core infrastructure (S3, API Gateway, Lambda, RDS,dynamoDB)
* Week 3–4: Build e-ticketing and authentication with Cognito
* Week 5–6: Enable CloudWatch, dashboards, and WAF security
### 6. Budget & Resources
* Total Estimated Cloud Cost: ≈ USD 100/month 
* Optimization Tools: AWS Cost Explorer, Auto Scaling, and usage of Free Tier where possible
* Team Composition:
    * Cloud Architect
    * Backend Developer (Lambda/API)
    * Frontend Developer
    * Metro Operations & Maintenance Engineers
### 7. Expected Outcomes
* Reduced traffic congestion and air pollution.
* Cashless e-ticketing system powered by AWS backend.
* Secure, scalable digital foundation for future expansion.
* Enhanced passenger convenience and operational transparency.
* Knowledge transfer and skill development in AWS technologies

### 8. Conclusion
The Metropolitan Railway Service System powered by AWS Cloud establishes a secure, scalable, and affordable foundation for urban transport modernization.
By leveraging AWS Lambda, API Gateway, RDS, Cognito, and CloudWatch, the solution remains fully serverless, ensuring minimal operational overhead and easy future expansion into smart-city initiatives.




<!-- ### AWS Services Used
- **AWS IoT Core**: Ingests MQTT data from 5 stations, scalable to 15.
- **AWS Lambda**: Processes data and triggers Glue jobs (two functions).
- **Amazon API Gateway**: Facilitates web app communication.
- **Amazon S3**: Stores raw data in a data lake and processed outputs (two buckets).
- **AWS Glue**: Crawlers catalog data, and ETL jobs transform and load it.
- **AWS Amplify**: Hosts the Next.js web interface.
- **Amazon Cognito**: Secures access for lab users.

### Component Design
- **Edge Devices**: Raspberry Pi collects and filters sensor data, sending it to IoT Core.
- **Data Ingestion**: AWS IoT Core receives MQTT messages from the edge devices.
- **Data Storage**: Raw data is stored in an S3 data lake; processed data is stored in another S3 bucket.
- **Data Processing**: AWS Glue Crawlers catalog the data, and ETL jobs transform it for analysis.
- **Web Interface**: AWS Amplify hosts a Next.js app for real-time dashboards and analytics.
- **User Management**: Amazon Cognito manages user access, allowing up to 5 active accounts.

### 4. Technical Implementation
**Implementation Phases**
This project has two parts—setting up weather edge stations and building the weather platform—each following 4 phases:
- Build Theory and Draw Architecture: Research Raspberry Pi setup with ESP32 sensors and design the AWS serverless architecture (1 month pre-internship)
- Calculate Price and Check Practicality: Use AWS Pricing Calculator to estimate costs and adjust if needed (Month 1).
- Fix Architecture for Cost or Solution Fit: Tweak the design (e.g., optimize Lambda with Next.js) to stay cost-effective and usable (Month 2).
- Develop, Test, and Deploy: Code the Raspberry Pi setup, AWS services with CDK/SDK, and Next.js app, then test and release to production (Months 2-3).

**Technical Requirements**
- Weather Edge Station: Sensors (temperature, humidity, rainfall, wind speed), a microcontroller (ESP32), and a Raspberry Pi as the edge device. Raspberry Pi runs Raspbian, handles Docker for filtering, and sends 1 MB/day per station via MQTT over Wi-Fi.
- Weather Platform: Practical knowledge of AWS Amplify (hosting Next.js), Lambda (minimal use due to Next.js), AWS Glue (ETL), S3 (two buckets), IoT Core (gateway and rules), and Cognito (5 users). Use AWS CDK/SDK to code interactions (e.g., IoT Core rules to S3). Next.js reduces Lambda workload for the fullstack web app.

### 5. Timeline & Milestones
**Project Timeline**
- Pre-Internship (Month 0): 1 month for planning and old station review.
- Internship (Months 1-3): 3 months.
    - Month 1: Study AWS and upgrade hardware.
    - Month 2: Design and adjust architecture.
    - Month 3: Implement, test, and launch.
- Post-Launch: Up to 1 year for research.

### 6. Budget Estimation
You can find the budget estimation on the [AWS Pricing Calculator](https://calculator.aws/#/estimate?id=621f38b12a1ef026842ba2ddfe46ff936ed4ab01).  
Or you can download the [Budget Estimation File](../attachments/budget_estimation.pdf).

### Infrastructure Costs
- AWS Services:
    - AWS Lambda: $0.00/month (1,000 requests, 512 MB storage).
    - S3 Standard: $0.15/month (6 GB, 2,100 requests, 1 GB scanned).
    - Data Transfer: $0.02/month (1 GB inbound, 1 GB outbound).
    - AWS Amplify: $0.35/month (256 MB, 500 ms requests).
    - Amazon API Gateway: $0.01/month (2,000 requests).
    - AWS Glue ETL Jobs: $0.02/month (2 DPUs).
    - AWS Glue Crawlers: $0.07/month (1 crawler).
    - MQTT (IoT Core): $0.08/month (5 devices, 45,000 messages).

Total: $0.7/month, $8.40/12 months

- Hardware: $265 one-time (Raspberry Pi 5 and sensors).

### 7. Risk Assessment
#### Risk Matrix
- Network Outages: Medium impact, medium probability.
- Sensor Failures: High impact, low probability.
- Cost Overruns: Medium impact, low probability.

#### Mitigation Strategies
- Network: Local storage on Raspberry Pi with Docker.
- Sensors: Regular checks and spares.
- Cost: AWS budget alerts and optimization.

#### Contingency Plans
- Revert to manual methods if AWS fails.
- Use CloudFormation for cost-related rollbacks.

### 8. Expected Outcomes
#### Technical Improvements: 
Real-time data and analytics replace manual processes.  
Scalable to 10-15 stations.
#### Long-term Value
1-year data foundation for AI research.  
Reusable for future projects. -->
