---
title: "Tuần 8 Worklog"
date: 2025-09-07
weight: 1
chapter: false
pre: " <b> 1.8. </b> "
---

### Mục tiêu Tuần 8:

* Hiểu các kiến thức cơ bản và các trường hợp sử dụng của **AWS Step Functions**, bao gồm 7 loại state chính và cách phối hợp các workflow phức tạp.

* Thực hành tạo và kiểm thử workflow trong **AWS Cloud9**, tập trung vào điều phối tác vụ và xử lý lỗi.

* Tìm hiểu các tính năng chính và các bước triển khai của **Amazon FSx**, bao gồm các biến thể: Windows File Server, Lustre, NetApp ONTAP, OpenZFS.

* Thực hành cấu hình hệ thống FSx tích hợp với **AWS Managed Microsoft AD**, đảm bảo thiết lập mạng, xác thực, và chia sẻ file đúng chuẩn.

* Khám phá **AWS X-Ray** để hiểu cách trace và trực quan hóa các request trong ứng dụng phân tán, phục vụ tối ưu hiệu năng và debug.

### Công việc thực hiện trong tuần:
| Ngày | Công việc                                                                                                                                                                                                   | Ngày bắt đầu | Ngày kết thúc | Tài liệu tham khảo                        |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------- | --------------- | ----------------------------------------- |
| 2   | - Học **AWS Step Functions**: <br>&emsp; + 7 state: Task, Choice, Fail / Success, Pass, Wait, Parallel, Map <br>&emsp; + Các trường hợp sử dụng AWS Step Functions <br>&emsp; + Lợi ích của AWS Step Functions | 26/10/2025 | 27/10/2025      | <https://000047.awsstudygroup.com/1-intro/> |
| 3   | - **Thực hành:** <br>&emsp; + Tạo môi trường **Cloud9** <br>&emsp; + Tạo các dịch vụ mẫu <br>&emsp; + Khởi tạo workflow <br>&emsp; + Xử lý lỗi | 27/10/2025 | 28/10/2025      | <https://000047.awsstudygroup.com/1-intro/> |
| 4   | - Học **Amazon FSx**: <br>&emsp; + FSx for Windows File Server <br>&emsp; + FSx for Lustre <br>&emsp; + FSx for NetApp ONTAP <br>&emsp; + FSx for OpenZFS | 28/10/2025 | 29/10/2025      | <https://000025.awsstudygroup.com/> |
| 5   | - **Thực hành:** <br>&emsp; + Cấu hình chi tiết File system <br>&emsp; + Chọn VPC hiện có <br>&emsp; + Chọn **AWS Managed Microsoft AD** (cung cấp DNS domain, username và password cho Service account) <br>&emsp; + Đặt tên chia sẻ Windows file share (dùng AD đã chọn) <br>&emsp; + Xem lại và tạo | 29/10/2025 | 30/10/2025      | <https://000025.awsstudygroup.com/> |
| 6   | - Học **AWS X-Ray**: <br>&emsp; + Trace <br>&emsp; + Segment <br>&emsp; + Subsegment <br>&emsp; + Annotation / Metadata <br>&emsp; + Service Map | 30/10/2025 | 31/10/2025      | <https://000140.awsstudygroup.com/> |

### Thành tựu Tuần 8:

* Hiểu và giải thích 7 state của **AWS Step Functions**, bao gồm vai trò của từng state trong tự động hóa workflow và chuyển đổi trạng thái.

* Thực hành xây dựng workflow mẫu với **AWS Step Functions** trên Cloud9, triển khai xử lý lỗi và xác nhận luồng thực thi.

* Hiểu rõ các tùy chọn **Amazon FSx** và ứng dụng lý tưởng của chúng cho workloads Windows, tính toán hiệu năng cao, và lưu trữ doanh nghiệp.

* Hoàn tất việc cấu hình thực hành **FSx for Windows File Server**, bao gồm thiết lập file system, tích hợp VPC và AD, và tạo chia sẻ file.

* Nắm cách **AWS X-Ray** thu thập traces, segments, subsegments, và trực quan hóa Service Map để nhận diện bottleneck và lỗi trong các dịch vụ AWS.
