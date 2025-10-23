---
title: "Worklog Tuần 7"
date: 2025-09-07
weight: 1
chapter: false
pre: " <b> 1.7. </b> "
---



### Mục tiêu tuần 7:

* Kết nối, làm quen với các thành viên trong First Cloud Journey.
* Hiểu dịch vụ AWS cơ bản, cách dùng console & CLI.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Tìm hiểu AWS EKS : <br>&emsp; + Control Plane(AWS managed) <br>&emsp; + Workder Nodes(user-managed) <br>&emsp; + Tất cả thành phần trong EKS :Cluster, Node group, Pod, Deployment/Service                                                                                                 | 20/10/2025   | 21/10/2025      |<https://000126.awsstudygroup.com/1-introduce/>
| 3   | - **Thực hành:** : <br>&emsp; + Tạo network:VPC, subnets, internet gateway <br>&emsp; + Tạo quyền cho control plane <br>&emsp; + Khởi tạo EKS cluster <br>&emsp; + Cài đặt addon: vpc-cni, kube-proxy <br>&emsp; + Tạo quyền cho worker node <br>&emsp; + Khởi tạo worker node <br>&emsp; + Cài đặt addon: coredns <br>&emsp; + Test nginx deployment                                             | 21/10/2025   | 22/10/2025      | <https://000126.awsstudygroup.com/1-introduce> |
| 4   | - Tìm hiểu AWS ECS: <br>&emsp; + Cluster, task denifition, task, service, container agent <br>&emsp; + ECS launch types <br>&emsp; + Networking trong ECS <br>&emsp; + Tích hợp với dịch vụ khác <br>&emsp; + ECS Auto Scaling | 22/10/2025   | 24/10/2025      | <https://cloudjourney.awsstudygroup.com/> |
| 5   | - Tìm hiểu EC2 cơ bản: <br>&emsp; + Instance types <br>&emsp; + AMI <br>&emsp; + EBS <br>&emsp; + ... <br> - Các cách remote SSH vào EC2 <br> - Tìm hiểu Elastic IP   <br>                  | 14/08/2025   | 15/08/2025      | <https://cloudjourney.awsstudygroup.com/> |
| 6   | - **Thực hành:** <br>&emsp; + Tạo EC2 instance <br>&emsp; + Kết nối SSH <br>&emsp; + Gắn EBS volume                                                                                         | 15/08/2025   | 15/08/2025      | <https://cloudjourney.awsstudygroup.com/> |


### Kết quả đạt được tuần 7:

* Hiểu AWS là gì và nắm được các nhóm dịch vụ cơ bản: 
  * Compute
  * Storage
  * Networking 
  * Database
  * ...

* Đã tạo và cấu hình AWS Free Tier account thành công.

* Làm quen với AWS Management Console và biết cách tìm, truy cập, sử dụng dịch vụ từ giao diện web.

* Cài đặt và cấu hình AWS CLI trên máy tính bao gồm:
  * Access Key
  * Secret Key
  * Region mặc định
  * ...

* Sử dụng AWS CLI để thực hiện các thao tác cơ bản như:

  * Kiểm tra thông tin tài khoản & cấu hình
  * Lấy danh sách region
  * Xem dịch vụ EC2
  * Tạo và quản lý key pair
  * Kiểm tra thông tin dịch vụ đang chạy
  * ...

* Có khả năng kết nối giữa giao diện web và CLI để quản lý tài nguyên AWS song song.
* ...


