---
title: "Week 7 Worklog"
date: 2025-09-07
weight: 1
chapter: false
pre: " <b> 1.7. </b> "
---



### Week 7 Objectives:

* Learn the AWS services that use to optimized performance
* The neccessary services for optimizing performance like ECS, EKS,CodePipeline, Storage gateway
* Learn about Docker, Kubernetes, and relationship between Docker and kubernetes

### Tasks to be carried out this week:
| Day | Task                                                                                                                                                                                                   | Start Date | Completion Date | Reference Material                        |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------- | --------------- | ----------------------------------------- |
| 2   | - Learn the **AWS EKS** : <br>&emsp; + Control Plane(AWS managed) <br>&emsp; + Workder Nodes(user-managed) <br>&emsp; + All component in EKS :Cluster, Node group, Pod, Deployment Service                                                                                                   | 20/10/2025 | 21/10/2025      |<https://000126.awsstudygroup.com/1-introduce/>
| 3   | - **Practice:** : <br>&emsp; + Create network:VPC, subnets, internet gateway <br>&emsp; + Create Auth for control plane <br>&emsp; + Create EKS cluster <br>&emsp; + Setting the addon: VPC-cni, kube proxy <br>&emsp; + Create Auth for worker node <br>&emsp; + Create worker node <br>&emsp; + Install addon: coredns <br>&emsp; + Test nginx deployment                                              | 21/10/2025 | 22/10/2025      | <https://000126.awsstudygroup.com/1-introduce> |
| 4   | - Learn **AWS ECS**: <br>&emsp; + Cluster, task denifition, task, service, container agent <br>&emsp; + ECS launch types <br>&emsp; + Networking in ECS <br>&emsp; + Integrate with another services <br>&emsp; + ECS Auto Scaling  | 22/10/2025 | 24/10/2025      | <https://cloudjourney.awsstudygroup.com/> |
| 5   | - Learn **AWS Storage Gateway**: <br> - **Practice:**<br>&emsp; + Create ECS cluster <br>&emsp; + Config the Docker image <br>&emsp; + Create Task definition <br>&emsp; + Register namespace in Cloud Map                        | 23/10/2025 | 25/10/2025      | <https://000016.awsstudygroup.com/1-introduction/> |
| 6   | - Learn **AWS CodePipeline**: <br>&emsp; + Source stage: Take code from GitHub,Codecommit or S3 <br>&emsp; + Build stage: Call CodeBuild to translate <br>&emsp; + Deploy stage: Call CodeDeploy to deploy                                                                                      | 25/10/2025 | 27/10/2025      | <https://000017.awsstudygroup.com/> |


### Week 7 Achievements:
* Learn **AWS EKS**: 
  * Understadn the architecture EKS include Control Plane (AWS managed) and Worker Nodes (self-managed).
  * Definition about Cluster, Node Group, Pod, Deployment, Service.
  * Understand how to connect kubectl to EKS Cluster and manage workloads.

* Practice on **EKS**:
  * Create VPC, Subnets, Internet Gateway, Route Table.
  * Give Authentication EKS Control Plane (IAM Role).
  * Create EKS Cluster and install addon: vpc-cni, kube-proxy.
  * Create Node Group for Worker Node and install addon coredns.
  * Deploy Nginx Deployment successfully on EKS and access through LoadBalancer.

* Learn **AWS ECS**:
  * Understand how ECS Cluster work, Task Definition, Service, Container Agent.
  * Discriminate ECS Launch Type (EC2 / Fargate).
  * Understand to config the internet (ECS networking modes: bridge, host, awsvpc).
  * Understand how to intergrate ECS with CloudWatch, Load Balancer and Auto Scaling.

* Practice to deploy **ECS**:
  * Create **ECS Cluster** (Fargate).
  * Build and push Docker image into ECR.
  * Create Task Definition and Service run container.
  * Register namespace on Cloud Map that ECS can service discovery.
  * Learn the AWS Storage Gateway basic and hybrid storage model.    

* Learn **AWS CodePipeline**:
  * Understand pipeline CI/CD include 3 stage: Source → Build → Deploy.
  * Understand how to intergrate CodePipeline with GitHub, CodeBuild and CodeDeploy.
  * Understand the automation build and deploy Application Spring Boot or React into EC2/S3.
  * Write file buildspec.yml and appspec.yml template.