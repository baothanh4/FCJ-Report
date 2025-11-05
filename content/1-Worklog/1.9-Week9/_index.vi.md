---
title: "Worklog Tuần 9"
date: 2025-09-07
weight: 1
chapter: false
pre: " <b> 1.9. </b> "
---
{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}


### Mục tiêu tuần 9:

* Kết nối, làm quen với các thành viên trong First Cloud Journey.
* Hiểu dịch vụ AWS cơ bản, cách dùng console & CLI.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Tìm hiểu AWS AppSync: <br>&emsp; + GraphQL APIs: Query, Mutation, Subcription <br>&emsp; + Data Sources: DynamoDB, RDS/Aurora, AWS Lambda, HTTP Endpoints, Elasticsearch/OpenSearch <br>&emsp; + Phân quyền và ủy quyền: AWS IAM, API Keys, Cognito User Pools, OpenID Connect <br>&emsp; + Realtime Subcriptions, Caching, Offline support  <br>- **Thực hành:**<br>&emsp; + Tạo GraphQL API <br>&emsp; + Tạo schema và data source <br>&emsp; + Sau khi tạo schema, chọn API muốn gắn <br>&emsp; + Cấu hình mẫu ánh xạ                                                                                             | 02/11/2025   | 03/11/2025      | <https://000086.awsstudygroup.com/1-introduction/>
| 3   | - Tìm AWS EBS Data lifecycle Manager: <br>&emsp; + Tự động hóa sao lưu <br>&emsp; + Giảm chi phí lưu trữ <br>&emsp; + Đảm bảo tuân thủ <br>&emsp; + Phục hồi nhanh chóng <br>&emsp; Lifecycle Policies: EBS Snapshot Policy, EBS-backed AMI Policy, Cross-region/ Cross-account Copy Policy                                            | 03/11/2025   | 05/11/2025      | <https://000088.awsstudygroup.com/> |
| 4   | - **Thực hành:**<br>&emsp; + Khởi động EC2 và cấu hình lifecycle policies trong EC2 <br>&emsp; + Xác định Tài nguyên, Lịch Snapshot, và thời gian giữ lại <br> - Tìm hiểu AWS GuardDuty bằng cách sử dụng machine learning, phân tích hành vi và nguồn dữ liệu tình báo bảo mật | 03/11/2025   | 06/11/2025      | <https://000098.awsstudygroup.com/> |
| 5   | - Tìm hiểu EC2 cơ bản: <br>&emsp; + Instance types <br>&emsp; + AMI <br>&emsp; + EBS <br>&emsp; + ... <br> - Các cách remote SSH vào EC2 <br> - Tìm hiểu Elastic IP   <br>                  | 14/08/2025   | 15/08/2025      | <https://cloudjourney.awsstudygroup.com/> |
| 6   | - **Thực hành:** <br>&emsp; + Tạo EC2 instance <br>&emsp; + Kết nối SSH <br>&emsp; + Gắn EBS volume                                                                                         | 15/08/2025   | 15/08/2025      | <https://cloudjourney.awsstudygroup.com/> |


### Kết quả đạt được tuần 9:

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


