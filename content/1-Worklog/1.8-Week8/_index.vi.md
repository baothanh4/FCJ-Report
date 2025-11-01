---
title: "Báo cáo Tuần 8"
date: 2025-09-07
weight: 1
chapter: false
pre: " <b> 1.8. </b> "
---

###  Mục tiêu Tuần 8 (Week 8 Objectives):
* Hiểu các khái niệm cơ bản và trường hợp sử dụng của **AWS Step Functions**, bao gồm **7 loại trạng thái chính** và cách phối hợp các bước để điều phối các quy trình phức tạp.  

* Thực hành tạo và kiểm thử **workflow trong AWS Cloud9**, tập trung vào việc điều phối tác vụ (task orchestration) và xử lý lỗi (error handling).  

* Tìm hiểu các tính năng chính và các bước triển khai của **Amazon FSx**, bao gồm các biến thể khác nhau: **FSx for Windows File Server**, **FSx for Lustre**, **FSx for NetApp ONTAP**, và **FSx for OpenZFS**.  

* Thực hành cấu hình **hệ thống tệp FSx** tích hợp với **AWS Managed Microsoft AD**, đảm bảo thiết lập đúng về **mạng, xác thực và chia sẻ tệp (file sharing)**.  

* Khám phá **AWS X-Ray** để hiểu cách theo dõi và trực quan hóa các yêu cầu trong ứng dụng phân tán nhằm **tối ưu hóa hiệu năng và xử lý lỗi**.  

---

### Nhiệm vụ thực hiện trong tuần (Tasks to be carried out this week):
| Ngày | Nhiệm vụ                                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo                        |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------- | --------------- | ----------------------------------------- |
| 2   | - Học về **AWS Step Functions**: <br>&emsp; + 7 trạng thái: Task state, Choice state, Fail/Success state, Pass state, Wait state, Parallel state, Map state <br>&emsp; + Các trường hợp sử dụng Step Functions <br>&emsp; + Lợi ích của AWS Step Functions | 26/10/2025 | 27/10/2025      | <https://000047.awsstudygroup.com/1-intro/> |
| 3   | - **Thực hành:** <br>&emsp; + Tạo môi trường **Cloud9** <br>&emsp; + Tạo các dịch vụ mẫu <br>&emsp; + Khởi tạo workflow <br>&emsp; + Xử lý lỗi | 27/10/2025 | 28/10/2025 | <https://000047.awsstudygroup.com/1-intro/> |
| 4   | - Học về **Amazon FSx**: <br>&emsp; + FSx for Windows File Server <br>&emsp; + FSx for Lustre <br>&emsp; + FSx for NetApp ONTAP <br>&emsp; + FSx for OpenZFS | 28/10/2025 | 29/10/2025 | <https://000025.awsstudygroup.com/> |
| 5   | - **Thực hành:** <br>&emsp; + Cấu hình chi tiết hệ thống tệp <br>&emsp; + Chọn VPC hiện có <br>&emsp; + Chọn **AWS Managed Microsoft AD** (Cung cấp tên miền DNS, tài khoản dịch vụ và mật khẩu) <br>&emsp; + Đặt tên chia sẻ tệp Windows (chọn AWS Managed Microsoft AD) <br>&emsp; + Kiểm tra và tạo hệ thống | 29/10/2025 | 30/10/2025 | <https://000025.awsstudygroup.com/> |
| 6   | - Học về **AWS X-Ray**: <br>&emsp; + Trace <br>&emsp; + Segment <br>&emsp; + Subsegment <br>&emsp; + Annotation / Metadata <br>&emsp; + Service Map | 30/10/2025 | 31/10/2025 | <https://000140.awsstudygroup.com/> |

---

### Thành tựu Tuần 8 (Week 8 Achievements):
* Đã học và giải thích được **7 trạng thái của AWS Step Functions**, bao gồm vai trò của từng trạng thái trong việc tự động hóa và điều phối quy trình.  

* Thực hành **xây dựng workflow mẫu** bằng AWS Step Functions trong Cloud9, triển khai cơ chế **xử lý lỗi và xác minh luồng thực thi** thành công.  

* Nắm vững kiến thức về **các loại Amazon FSx** và trường hợp sử dụng phù hợp cho từng nhu cầu: **hệ thống Windows, tính toán hiệu năng cao, và lưu trữ doanh nghiệp**.  

* Hoàn thành thực hành **cấu hình FSx for Windows File Server**, bao gồm: cấu hình hệ thống tệp, tích hợp **VPC và Active Directory**, và tạo chia sẻ file (file share).  

* Hiểu rõ cách **AWS X-Ray thu thập và hiển thị trace, segment, subsegment**, đồng thời **quan sát Service Map** để phát hiện nút thắt hiệu năng và lỗi trong ứng dụng.  

* Hoàn tất toàn bộ mục tiêu học tập và thực hành đề ra cho **tuần 8**.  

---
