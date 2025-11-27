---
title: "Worklog Tuần 8"
date: 2025-09-07
weight: 1
chapter: false
pre: " <b> 1.8. </b> "
---

### Mục tiêu Tuần 8

* Hiểu cơ bản và các trường hợp sử dụng của **AWS Step Functions**, bao gồm 7 loại trạng thái chính và cách điều phối các workflow phức tạp.  
* Thực hành tạo và kiểm thử workflow trong **AWS Cloud9**, tập trung vào điều phối tác vụ và xử lý lỗi.  
* Học các tính năng chính và các bước triển khai của **Amazon FSx**, bao gồm các biến thể khác nhau (Windows File Server, Lustre, NetApp ONTAP, OpenZFS).  
* Thực hành cấu hình FSx tích hợp với **AWS Managed Microsoft AD**, đảm bảo cấu hình mạng, xác thực và chia sẻ file đúng.  
* Khám phá **AWS X-Ray** để theo dõi và trực quan hóa các yêu cầu trong ứng dụng phân tán nhằm tối ưu hiệu năng và debug.

### Nhiệm vụ tuần này

| Ngày | Nhiệm vụ | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | ---- | ---------- | --------------- | ----------------- |
| 2 | Học **AWS Step Functions**: <br> &emsp;+ 7 trạng thái: Task, Choice, Fail/Success, Pass, Wait, Parallel, Map <br> &emsp;+ Các trường hợp sử dụng Step Functions <br> &emsp;+ Lợi ích của Step Functions | 26/10/2025 | 27/10/2025 | <https://000047.awsstudygroup.com/1-intro/> |
| 3 | **Thực hành:** <br> &emsp;+ Tạo môi trường **Cloud9** <br> &emsp;+ Tạo dịch vụ mẫu <br> &emsp;+ Khởi tạo workflow <br> &emsp;+ Xử lý lỗi | 27/10/2025 | 28/10/2025 | <https://000047.awsstudygroup.com/1-intro/> |
| 4 | Học **Amazon FSx**: <br> &emsp;+ FSx cho Windows File Server <br> &emsp;+ FSx cho Lustre <br> &emsp;+ FSx cho NetApp ONTAP <br> &emsp;+ FSx cho OpenZFS | 28/10/2025 | 29/10/2025 | <https://000025.awsstudygroup.com/> |
| 5 | **Thực hành:** <br> &emsp;+ Cấu hình chi tiết hệ thống file <br> &emsp;+ Chọn VPC hiện có <br> &emsp;+ Chọn AWS Managed Microsoft AD (cung cấp DNS, username/password của Service Account) <br> &emsp;+ Đặt tên chia sẻ file Windows <br> &emsp;+ Kiểm tra và tạo | 29/10/2025 | 30/10/2025 | <https://000025.awsstudygroup.com/> |
| 6 | Học **AWS X-Ray**: <br> &emsp;+ Trace <br> &emsp;+ Segment <br> &emsp;+ Subsegment <br> &emsp;+ Annotation / Metadata <br> &emsp;+ Service Map | 30/10/2025 | 31/10/2025 | <https://000140.awsstudygroup.com/> |

### Thành tựu Tuần 8

* Hiểu và giải thích 7 trạng thái của **AWS Step Functions**, bao gồm vai trò của từng trạng thái trong tự động hóa workflow và chuyển trạng thái.  
* Thực hành tạo workflow mẫu trong Cloud9 với **Step Functions**, bao gồm xử lý lỗi và xác nhận luồng thực thi.  
* Nắm vững các tùy chọn của **Amazon FSx** và các trường hợp sử dụng phù hợp cho Windows workloads, HPC và lưu trữ doanh nghiệp.  
* Hoàn thành cấu hình FSx cho Windows File Server, bao gồm cấu hình hệ thống file, tích hợp VPC/AD và tạo chia sẻ file.  
* Học cách **AWS X-Ray** thu thập trace, segment, subsegment và trực quan hóa Service Map để nhận diện bottleneck và lỗi trong hệ thống.
