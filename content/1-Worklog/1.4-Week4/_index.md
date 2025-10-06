---
title: "Week 4 Worklog"
date: 2025-09-07
weight: 1
chapter: false
pre: " <b> 1.4. </b> "
---



### Week 4 Objectives:

* Practice create, management, và deploy all AWS resource through all different tools (Console, CLI, SDK, Elastic Beanstalk...).
* Build a prototype web application by using Lambda, S3, DynamoDB, and API Gateway.

### Tasks to be carried out this week:
| Day | Task                                                                                                                                                                                                   | Start Date | Completion Date | Reference Material                        |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------- | --------------- | ----------------------------------------- |
| 2   | - **Practice:** Create table in AWS DynamoDB by using AWS CLI or Python through accessKey                                                                                                  | 28/09/2025 | 29/09/2025      |
| 3   | -**Practice:** Create book store by using Lambda,S3 and DynamoDB                                          | 30/09/2025 | 01/10/2025      | <https://000078.awsstudygroup.com/> |
| 4   | - Learn JSON & Document model | 01/10/2025 | 02/10/2025      |  |
| 5   | - **Pratice:** <br>&emsp;+ Use the AWS Console to deploy and verify AWS resources using an AWS CloudFormation template. <br>&emsp; + Use AWS Tools for Eclipse to deploy a Java Application to an Elastic Beanstalk environment. <br>&emsp; + Install and configure the AWS Elastic Beanstalk CLI tool. <br>&emsp; + Use the AWS Elastic Beanstalk CLI to deploy an update to an existing Elastic Beanstalk environment. <br>&emsp; + Use the AWS SDK to query and modify the AWS environment using code.                              | 03/10/2025 | 04/10/2025      | <https://000050.awsstudygroup.com/> |
| 6   | - **Practice:** <br>&emsp; + Build a web application(Front-end) to interact with database through Lambda and API Gateway                                                     | 04/10/2025 | 05/10/2025      | <https://000079.awsstudygroup.com/> |


### Week 4 Achievements:

* Understood and worked with AWS DynamoDB: 
  * Created and managed DynamoDB tables using AWS CLI and Python SDK (boto3) with Access Keys.
  * Learned how to define Primary Key, Sort Key, and configure Read/Write Capacity Modes.


* Developed a Book Store application using AWS Lambda, S3, and DynamoDB:
  * Built Lambda functions to handle CRUD operations for book data.
  * Connected API Gateway with Lambda to create a REST API for frontend interaction.
  * Stored book cover images and static files in an S3 Bucket.

* Explored JSON and Document Data Models:
 * Understood how to store semi-structured data in DynamoDB and query it using JSON format.

* Deployed a Java application using AWS Elastic Beanstalk:
  * Used AWS Console and CloudFormation Templates to automate environment setup.
  * Installed and configured Elastic Beanstalk CLI to deploy and update applications.
  * Integrated AWS SDK for Java to query and modify AWS environments programmatically.


* Built a web application (frontend) to interact with the database via Lambda and API Gateway:

  * Developed a simple web interface that allows users to add, edit, and delete data in DynamoDB.
  * Understood the workflow Frontend → API Gateway → Lambda → DynamoDB and how to secure endpoints.


