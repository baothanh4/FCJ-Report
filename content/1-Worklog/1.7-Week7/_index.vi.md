---
title: "Worklog Tuần 7"
date: 2025-09-07
weight: 1
chapter: false
pre: " <b> 1.7. </b> "
---



### Mục tiêu tuần 7:

* Tìm hiểu những dịch vụ của AWS để tối ưu hiệu năng
* Những dịch vụ cần thiết cho việc tối ưu hiệu năng như ECS, EKS,CodePipeline, Storage gateway
* Tìm hiểu về Docker, Kubernetes, và mối quan hệ giữa Docker và kubernetes

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Tìm hiểu AWS EKS : <br>&emsp; + Control Plane(AWS managed) <br>&emsp; + Workder Nodes(user-managed) <br>&emsp; + Tất cả thành phần trong EKS :Cluster, Node group, Pod, Deployment/Service                                                                                                 | 20/10/2025   | 21/10/2025      |<https://000126.awsstudygroup.com/1-introduce/>
| 3   | - **Thực hành:** : <br>&emsp; + Tạo network:VPC, subnets, internet gateway <br>&emsp; + Tạo quyền cho control plane <br>&emsp; + Khởi tạo EKS cluster <br>&emsp; + Cài đặt addon: vpc-cni, kube-proxy <br>&emsp; + Tạo quyền cho worker node <br>&emsp; + Khởi tạo worker node <br>&emsp; + Cài đặt addon: coredns <br>&emsp; + Test nginx deployment                                             | 21/10/2025   | 22/10/2025      | <https://000126.awsstudygroup.com/1-introduce> |
| 4   | - Tìm hiểu AWS ECS: <br>&emsp; + Cluster, task denifition, task, service, container agent <br>&emsp; + ECS launch types <br>&emsp; + Networking trong ECS <br>&emsp; + Tích hợp với dịch vụ khác <br>&emsp; + ECS Auto Scaling | 22/10/2025   | 24/10/2025      | <https://cloudjourney.awsstudygroup.com/> |
| 5   | - Tìm hiểu AWS Storage Gateway <br> - **Thực hành:**<br>&emsp; + Tạo ECS cluster <br>&emsp; + Cấu hình Docker image <br>&emsp; + Tạo Task definition <br>&emsp; + Đăng kí namespace trong Cloud Map                   | 23/10/2025   | 25/10/2025      | <https://000016.awsstudygroup.com/1-introduction/> |
| 6   | - Tìm hiểu AWS CodePipeline: <br>&emsp; + Giai đoạn Source: Lấy code từ GitHub, CodeCommit hoặc S3 <br>&emsp; + Giai đoạn Build: Gọi CodeBuild để biên dịch <br>&emsp; + Giai đoạn Deploy: Gọi CodeDeploy để triển khai +                                                                                         | 25/10/2025   | 27/10/2025      | <https://000017.awsstudygroup.com/> |


### Kết quả đạt được tuần 7:
* Tìm hiểu AWS EKS: 
  * Hiểu rõ kiến trúc EKS bao gồm Control Plane (AWS managed) và Worker Nodes (self-managed).
  * Nắm vững khái niệm Cluster, Node Group, Pod, Deployment, Service.
  * Biết cách kết nối kubectl tới EKS Cluster và quản lý workloads.

* Thực hành triển khai EKS:
  * Tạo VPC, Subnets, Internet Gateway, Route Table.
  * Cấp quyền cho EKS Control Plane (IAM Role).
  * Khởi tạo EKS Cluster và cài addon: vpc-cni, kube-proxy.
  * Tạo Node Group cho Worker Node và cài addon coredns.
  * Triển khai thành công Nginx Deployment trên EKS và truy cập qua LoadBalancer.

* Tìm hiểu AWS ECS:
  * Hiểu cơ chế hoạt động của ECS Cluster, Task Definition, Service, Container Agent.
  * Phân biệt ECS Launch Type (EC2 / Fargate).
  * Nắm cấu hình mạng (ECS networking modes: bridge, host, awsvpc).
  * Biết cách tích hợp ECS với CloudWatch, Load Balancer và Auto Scaling.

* Thực hành triển khai ECS:
  * Tạo ECS Cluster (Fargate).
  * Build và push Docker image lên ECR.
  * Tạo Task Definition và Service chạy container.
  * Đăng ký namespace trong Cloud Map để ECS có thể service discovery.
  * Tìm hiểu cơ bản về AWS Storage Gateway và mô hình hybrid storage.    

* Tìm hiểu AWS CodePipeline:
  * Hiểu pipeline CI/CD gồm 3 stage: Source → Build → Deploy.
  * Biết cách tích hợp CodePipeline với GitHub, CodeBuild và CodeDeploy.
  * Hiểu quy trình tự động build và deploy ứng dụng Spring Boot hoặc React lên EC2/S3.
  * Soạn file buildspec.yml và appspec.yml mẫu.