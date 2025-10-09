---
title: "Proposal"
date: 2025-09-07
weight: 2
chapter: false
pre: " <b> 2. </b> "
---


# Metropolitano Railway Service System with AWS: A Scalable, Cost-Optimized Cloud Architecture for Smart Urban Mobility

<!-- ## A Unified AWS Serverless Solution for Real-Time Weather Monitoring -->

### 1. Introduction
As Ho Chi Minh City continues to experience rapid urbanization, traffic congestion and air pollution have become critical challenges. Private vehicles dominate transportation, overloading existing roads and reducing mobility efficiency. To address this, a modern Metropolitano railway system is being developed to provide safe, fast, and sustainable public transport.
This proposal outlines how Amazon Web Services (AWS) will be used to build the system’s digital infrastructure — focusing on core and beginner-friendly cloud services to achieve reliability, security, and cost efficiency.



### 2. Objectives
* <b>General Objective:</b>
Establish a smart, efficient, and sustainable Metropolitano system that improves urban mobility and reduces road congestion.
* <b>Specific Objectives:</b>
    + Construct Metropolitano Line 1 (19.7 km) connecting Ben Thanh and Suoi Tien stations.
    + Reduce private vehicle usage by 20% within 5 years.
    + Implement a secure, cashless e-ticketing system accessible via mobile/web.
    + Use AWS cloud services to manage passenger data, ensure operational safety, and enhance the travel experience.

### 3. Scope
+ Location:  Ho Chi Minh City, Line 1 — Ben Thanh → Suoi Tien
+ Target Users:  Citizens, commuters, and tourists
+ Duration: 12 years (from feasibility study to full operation)
+ Limitations: Focus on metro infrastructure and essential AWS integration. Feeder transport and IoT automation will be addressed in later phases.


### 4. AWS Cloud Architecture
* Frontend Layer (Client Side)
    * Web App (React / Angular) and Mobile App (for passengers and staff).
    * Both communicate with the backend through HTTPS API endpoints.
    * AWS Services:
        * Amazon S3 – Hosts static frontend assets (HTML, JS, CSS).(~5$/month)
        * Amazon CloudFront (optional) – Speeds up content delivery globally.(~10$/month)
* Backend Layer (Application Services)
    * Amazon API Gateway – Entry point for all client API requests.(10$/month)
    * AWS Lambda – Handles business logic for(15$/month):
        * Ticket booking & scheduling
        * Payment transactions
        * Notifications (email/SMS)
    * Amazon Cognito – User authentication & role management (Admin, Staff, Passenger)(5$/month).
* Data Layer
    * Amazon RDS (PostgreSQL) – Stores structured data (passengers, tickets, schedules).(100$/month)
    * Amazon DynamoDB – Stores real-time train operation data (train status, seat availability).(20$/month)
    * Amazon S3 – Stores backups, reports, and logs.(5$/month)
*  Monitoring & Analytics Layer
    * Amazon CloudWatch – Collects system metrics, application logs, and error alerts.(5$/month)
    * AWS Glue + Athena – Data transformation and querying for analytics.(15$/month)
    * Amazon QuickSight – Dashboards for operations and management insights.(18$/month)
*  Security & Networking Layer
    * AWS WAF – Protects API endpoints from common web attacks (SQLi, XSS).
    * AWS Shield – DDoS protection for public endpoints.
    * Amazon VPC – Isolates backend and databases in a secure private network
    * AWS IAM – Manages internal roles and access permissions.
        * Estimated monthly cost: ~$8 total for WAF + Shield (others free-tier).
![IoT Weather Station Architecture](/images/2-Proposal/AWS-Architecture.png)

### 5. Implementation Plan
* Week 1–2: Configure AWS core infrastructure (S3, API Gateway, Lambda, RDS)
* Week 3–4: Build e-ticketing and authentication with Cognito
* Week 5–6: Enable CloudWatch, dashboards, and WAF/Shield security
### 6. Budget & Resources
* Total Estimated Cloud Cost: ≈ USD 211/month (~USD 1,266/year)
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
The Metropolitano Railway System integrated with AWS Cloud Infrastructure represents a forward-looking step toward sustainable transportation in Ho Chi Minh City.
 By adopting core AWS services (API Gateway, Lambda, RDS, S3, Cognito, CloudWatch), the system remains simple, cost-efficient, and secure.
Future phases can incorporate IoT, AI/ML, and predictive analytics for optimization once the foundational system stabilizes.




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
