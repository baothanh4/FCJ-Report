---
title: "Week 7 Worklog"
date: 2025-09-07
weight: 1
chapter: false
pre: " <b> 1.7. </b> "
---

### Week 7 Objectives

- Learn the AWS services used to optimize performance.  
- Understand necessary services for performance optimization: **ECS, EKS, CodePipeline, Storage Gateway**.  
- Learn about **Docker, Kubernetes**, and the relationship between Docker and Kubernetes.  

### Tasks to be carried out this week

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ----------------- |
| 2 | Learn **AWS EKS**: Control Plane (AWS managed), Worker Nodes (user-managed), Components: Cluster, Node Group, Pod, Deployment, Service | 20/10/2025 | 21/10/2025 | <https://000126.awsstudygroup.com/1-introduce/> |
| 3 | **Practice EKS:** Create network (VPC, subnets, Internet Gateway), Auth for control plane, Create EKS cluster, Install addons (vpc-cni, kube-proxy), Auth for worker node, Create worker node, Install addon coredns, Test Nginx deployment | 21/10/2025 | 22/10/2025 | <https://000126.awsstudygroup.com/1-introduce/> |
| 4 | Learn **AWS ECS**: Cluster, Task Definition, Task, Service, Container Agent, ECS Launch Types, Networking in ECS, Integrate with other services, ECS Auto Scaling | 22/10/2025 | 24/10/2025 | <https://cloudjourney.awsstudygroup.com/> |
| 5 | Learn **AWS Storage Gateway** and **Practice ECS**: Create ECS cluster, Configure Docker image, Create Task Definition, Register namespace in Cloud Map | 23/10/2025 | 25/10/2025 | <https://000016.awsstudygroup.com/1-introduction/> |
| 6 | Learn **AWS CodePipeline**: Source stage (GitHub, CodeCommit, S3), Build stage (CodeBuild), Deploy stage (CodeDeploy) | 25/10/2025 | 27/10/2025 | <https://000017.awsstudygroup.com/> |

### Week 7 Achievements

#### 1. **AWS EKS**  
- Understand EKS architecture: Control Plane (AWS-managed) and Worker Nodes (self-managed).  
- Learned definitions: Cluster, Node Group, Pod, Deployment, Service.  
- Connected `kubectl` to EKS Cluster and managed workloads.  

#### 2. **Practice on EKS**  
- Created VPC, Subnets, Internet Gateway, Route Table.  
- Provided authentication for EKS Control Plane (IAM Role).  
- Created EKS Cluster, installed addons: vpc-cni, kube-proxy.  
- Created Node Group for Worker Nodes, installed addon coredns.  
- Deployed Nginx successfully on EKS, accessible via LoadBalancer.  

#### 3. **AWS ECS**  
- Understood ECS Cluster, Task Definition, Service, Container Agent.  
- Differentiated ECS Launch Types: EC2 vs Fargate.  
- Learned ECS networking modes: bridge, host, awsvpc.  
- Integrated ECS with CloudWatch, Load Balancer, Auto Scaling.  

#### 4. **Practice ECS**  
- Created ECS Cluster (Fargate), built and pushed Docker images to ECR.  
- Created Task Definition and Service to run containers.  
- Registered namespace in Cloud Map for service discovery.  
- Learned AWS Storage Gateway basics and hybrid storage model.  

#### 5. **AWS CodePipeline**  
- Learned CI/CD pipeline stages: Source → Build → Deploy.  
- Integrated CodePipeline with GitHub, CodeBuild, CodeDeploy.  
- Automated build and deployment of Spring Boot or React applications to EC2/S3.  
- Wrote template files: `buildspec.yml` and `appspec.yml`.
