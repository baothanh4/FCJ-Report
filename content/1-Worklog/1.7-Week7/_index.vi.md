---
title: "Tuần 7 Worklog"
date: 2025-09-07
weight: 1
chapter: false
pre: " <b> 1.7. </b> "
---

### Mục tiêu Tuần 7:

* Tìm hiểu các dịch vụ AWS tối ưu hiệu năng.
* Nắm các dịch vụ cần thiết cho tối ưu hiệu năng như ECS, EKS, CodePipeline, Storage Gateway.
* Tìm hiểu về Docker, Kubernetes và mối quan hệ giữa Docker và Kubernetes.

### Công việc thực hiện trong tuần:
| Ngày | Công việc                                                                                                                                                                                                   | Ngày bắt đầu | Ngày kết thúc | Tài liệu tham khảo                        |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------- | --------------- | ----------------------------------------- |
| 2   | - Học **AWS EKS**: <br>&emsp; + Control Plane (AWS quản lý) <br>&emsp; + Worker Nodes (người dùng quản lý) <br>&emsp; + Các thành phần trong EKS: Cluster, Node Group, Pod, Deployment, Service                                                                                                   | 20/10/2025 | 21/10/2025      | <https://000126.awsstudygroup.com/1-introduce/> |
| 3   | - **Thực hành:** <br>&emsp; + Tạo mạng: VPC, Subnets, Internet Gateway <br>&emsp; + Cấu hình Auth cho Control Plane <br>&emsp; + Tạo EKS Cluster <br>&emsp; + Cài addon: VPC-CNI, kube-proxy <br>&emsp; + Tạo Auth cho Worker Node <br>&emsp; + Tạo Worker Node <br>&emsp; + Cài addon: CoreDNS <br>&emsp; + Triển khai Nginx Deployment | 21/10/2025 | 22/10/2025      | <https://000126.awsstudygroup.com/1-introduce/> |
| 4   | - Học **AWS ECS**: <br>&emsp; + Cluster, Task Definition, Task, Service, Container Agent <br>&emsp; + ECS Launch Types <br>&emsp; + Networking trong ECS <br>&emsp; + Tích hợp với các dịch vụ khác <br>&emsp; + ECS Auto Scaling | 22/10/2025 | 24/10/2025      | <https://cloudjourney.awsstudygroup.com/> |
| 5   | - Học **AWS Storage Gateway**: <br>- **Thực hành:** <br>&emsp; + Tạo ECS Cluster <br>&emsp; + Cấu hình Docker Image <br>&emsp; + Tạo Task Definition <br>&emsp; + Đăng ký Namespace trên Cloud Map | 23/10/2025 | 25/10/2025      | <https://000016.awsstudygroup.com/1-introduction/> |
| 6   | - Học **AWS CodePipeline**: <br>&emsp; + Source Stage: Lấy code từ GitHub, CodeCommit hoặc S3 <br>&emsp; + Build Stage: Gọi CodeBuild để build code <br>&emsp; + Deploy Stage: Gọi CodeDeploy để deploy ứng dụng | 25/10/2025 | 27/10/2025      | <https://000017.awsstudygroup.com/> |

### Thành tựu Tuần 7:

* Học **AWS EKS**:  
  * Hiểu kiến trúc EKS bao gồm Control Plane (AWS quản lý) và Worker Nodes (người dùng quản lý).  
  * Hiểu định nghĩa Cluster, Node Group, Pod, Deployment, Service.  
  * Hiểu cách kết nối kubectl với EKS Cluster và quản lý workloads.

* Thực hành trên **EKS**:  
  * Tạo VPC, Subnets, Internet Gateway, Route Table.  
  * Cấu hình Authentication cho EKS Control Plane (IAM Role).  
  * Tạo EKS Cluster và cài addon: VPC-CNI, kube-proxy.  
  * Tạo Node Group cho Worker Node và cài addon CoreDNS.  
  * Triển khai thành công Nginx Deployment trên EKS và truy cập qua LoadBalancer.

* Học **AWS ECS**:  
  * Hiểu cách ECS Cluster hoạt động, Task Definition, Service, Container Agent.  
  * Phân biệt ECS Launch Type (EC2 / Fargate).  
  * Hiểu cách cấu hình mạng trong ECS (bridge, host, awsvpc).  
  * Hiểu cách tích hợp ECS với CloudWatch, Load Balancer và Auto Scaling.

* Thực hành triển khai **ECS**:  
  * Tạo **ECS Cluster** (Fargate).  
  * Build và push Docker Image lên ECR.  
  * Tạo Task Definition và Service chạy container.  
  * Đăng ký Namespace trên Cloud Map để ECS có thể thực hiện Service Discovery.  
  * Hiểu cơ bản về **AWS Storage Gateway** và mô hình lưu trữ hybrid.

* Học **AWS CodePipeline**:  
  * Hiểu pipeline CI/CD gồm 3 stage: Source → Build → Deploy.  
  * Hiểu cách tích hợp CodePipeline với GitHub, CodeBuild và CodeDeploy.  
  * Hiểu tự động build và deploy ứng dụng Spring Boot hoặc React lên EC2/S3.  
  * Viết file **buildspec.yml** và **appspec.yml** theo template chuẩn.
