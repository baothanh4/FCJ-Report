---
title: "Week 4 Worklog"
date: 2025-09-07
weight: 1
chapter: false
pre: " <b> 1.4. </b> "
---

### Week 4 Objectives

- Practice creating, managing, and deploying AWS resources using various tools (Console, CLI, SDK, Elastic Beanstalk, etc.).
- Build a prototype web application using Lambda, S3, DynamoDB, and API Gateway.

### Tasks Completed This Week

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ----- | ---------- | ---------------- | ------------------ |
| 2 | **Practice:** Create a table in **AWS DynamoDB** using the **AWS CLI** or Python SDK (boto3) with Access Keys. | 28/09/2025 | 29/09/2025 |  |
| 3 | **Practice:** Build a Book Store application using **AWS Lambda**, **S3**, and **DynamoDB**. | 30/09/2025 | 01/10/2025 | <https://000078.awsstudygroup.com/> |
| 4 | Learn JSON & Document data models. | 01/10/2025 | 02/10/2025 |  |
| 5 | **Practice:**<br> &emsp;+ Deploy and verify AWS resources using an **AWS CloudFormation template**.<br> &emsp;+ Use AWS Tools for Eclipse to deploy a Java application to an **Elastic Beanstalk** environment.<br> &emsp;+ Install and configure the **Elastic Beanstalk CLI**.<br> &emsp;+ Use the EB CLI to deploy updates to an existing environment.<br> &emsp;+ Use the AWS SDK to query and modify AWS resources programmatically. | 03/10/2025 | 04/10/2025 | <https://000050.awsstudygroup.com/> |
| 6 | **Practice:** Build a frontend web application that interacts with the database through **Lambda** and **API Gateway**. | 04/10/2025 | 05/10/2025 | <https://000079.awsstudygroup.com/> |

---

### Week 4 Achievements

#### 1. Working with AWS DynamoDB
- Created and managed DynamoDB tables using AWS CLI and Python SDK (boto3).
- Defined Primary Keys, Sort Keys, and configured Read/Write Capacity Modes.

#### 2. Built a Book Store Application (Lambda + S3 + DynamoDB)
- Created Lambda functions to perform CRUD operations on book data.
- Integrated API Gateway with Lambda to build a RESTful backend.
- Stored book images and static web assets in Amazon S3.

#### 3. Understood JSON & Document Data Models
- Learned how DynamoDB stores semi-structured data.
- Queried and updated data using JSON-based structures.

#### 4. Deployed a Java Application with Elastic Beanstalk
- Deployed infrastructure using AWS Console and CloudFormation templates.
- Installed and configured the Elastic Beanstalk CLI.
- Deployed updates to an existing environment.
- Used the AWS SDK for Java to interact programmatically with AWS.

#### 5. Built a Frontend Web App with Serverless Backend
- Created a simple UI for adding, editing, and deleting items in DynamoDB.
- Understood the workflow: **Frontend → API Gateway → Lambda → DynamoDB**.
- Learned basic approaches to securing serverless APIs.
