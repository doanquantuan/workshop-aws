---
title: "Worklog Tuần 7"
date: 2026-11-14
weight: 7
chapter: false
pre: " <b>1.7. </b> "
---

### Mục tiêu tuần 7:

* Tìm hiểu và triển khai dịch vụ **AWS Backup** nhằm tập trung hóa và tự động hóa quy trình sao lưu, phục hồi dữ liệu đa dịch vụ (Amazon EBS, EC2, RDS, DynamoDB, EFS, S3) trên nền tảng AWS.
* Thiết lập hệ thống thông báo tự động (Notifications) qua Amazon SNS để theo dõi trạng thái các Backup Job, Restore Job và kiểm thử quy trình khôi phục tài nguyên (Restore Test) đảm bảo mục tiêu RTO/RPO.
* Tìm hiểu cơ chế định tuyến mạng giữa các VPC thông qua **VPC Peering**: thiết lập liên kết ngang hàng, cấu hình Route Table, cập nhật Network ACLs, Security Groups và kích hoạt Cross-VPC Private DNS Resolution.
* Tìm hiểu và triển khai **AWS Transit Gateway (TGW)** như một trung tâm định tuyến đám mây (Cloud Router/Hub-and-Spoke), kết nối nhiều VPC mở rộng quy mô mạng doanh nghiệp an toàn và đơn giản hóa việc quản lý bảng định tuyến tập trung.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - **Tập trung hóa sao lưu dữ liệu với AWS Backup:** <br>&emsp; + Tìm hiểu các khái niệm cốt lõi: Backup Vault, Backup Plan, Backup Rules, Lifecycle (chuyển sang Cold Storage, thời gian lưu trữ). <br>&emsp; + Khởi tạo Backup Vault và cấu hình Backup Plan tự động hóa lịch trình sao lưu tài nguyên theo Tag hoặc Resource ID. <br>&emsp; + Tích hợp Amazon SNS để kích hoạt gửi thông báo tự động khi các tác vụ sao lưu hoàn thành hoặc gặp sự cố. <br>&emsp; + Thực hành quy trình phục hồi dữ liệu (Restore) từ bản sao lưu và xác thực tính toàn vẹn của dữ liệu sau khi khôi phục. | 09/11/2026 | 09/11/2026 | <https://000013.awsfcaj.com/> |
| 4 | - **Thiết lập kết nối mạng ngang hàng với VPC Peering:** <br>&emsp; + Tìm hiểu nguyên lý hoạt động của VPC Peering, các giới hạn kỹ thuật (không hỗ trợ định tuyến bắc cầu - Transitive Routing, không trùng lặp dải CIDR). <br>&emsp; + Chuẩn bị môi trường đa VPC (khởi tạo VPC, Subnet, EC2 và Security Group trên từng mạng). <br>&emsp; + Tạo và chấp thuận liên kết VPC Peering Connection. <br>&emsp; + Cập nhật bảng định tuyến (Route Tables) và Network ACLs trên cả hai VPC để cho phép lưu lượng qua lại. <br>&emsp; + Cấu hình DNS Hostnames và DNS Resolution để cho phép phân giải Private IP giữa các VPC (Cross-peered VPC Private DNS Resolution). | 11/11/2026 | 11/11/2026 | <https://000019.awsfcaj.com/> |
| 6 | - **Mở rộng kết nối mạng đám mây với AWS Transit Gateway:** <br>&emsp; + Tìm hiểu kiến trúc Hub-and-Spoke so với mạng lưới Mesh của VPC Peering khi hệ thống có nhiều VPC. <br>&emsp; + Khởi tạo AWS Transit Gateway (TGW) và thiết lập các TGW Attachments kết nối đến các VPC mục tiêu. <br>&emsp; + Cấu hình và quản lý bảng định tuyến TGW Route Tables (hiểu cơ chế Association và Propagation). <br>&emsp; + Cập nhật Route Table tại các VPC trỏ luồng dữ liệu sang TGW. <br>&emsp; + Kiểm tra và xác nhận khả năng giao tiếp đa chiều giữa các VPC qua Transit Gateway. | 13/11/2026 | 13/11/2026 | <https://000020.awsfcaj.com/> |

### Kết quả đạt được tuần 7:

* **Tự động hóa sao lưu và phục hồi với AWS Backup (Workshop 000013):**
  * Nắm vững kiến trúc tập trung của AWS Backup, loại bỏ sự phụ thuộc vào các script snapshot thủ công trên từng dịch vụ riêng lẻ.
  * Thiết lập thành công **Backup Vault** với cơ chế mã hóa KMS và xây dựng **Backup Plan** tự động sao lưu định kỳ theo lịch trình (cron) gắn liền với vòng đời lưu trữ (Lifecycle rules).
  * Cấu hình cơ chế chọn tài nguyên thông minh (Resource Assignment) thông qua AWS Tags, đảm bảo mọi tài nguyên mới có gắn nhãn quy định đều tự động được bảo vệ.
  * Tích hợp thành công **Amazon Simple Notification Service (SNS)** để nhận cảnh báo tức thời qua Email khi có sự kiện sao lưu (Backup Job Started/Completed/Failed).
  * Thực hành kiểm thử quy trình khôi phục (Restore Test) từ điểm phục hồi (Recovery Point), khởi tạo lại tài nguyên hoạt động bình thường và đáp ứng tốt các chỉ số an toàn dữ liệu RTO (Recovery Time Objective) và RPO (Recovery Point Objective).

* **Kết nối liên mạng trực tiếp với VPC Peering (Workshop 000019):**
  * Hiểu rõ cơ chế kết nối Layer 3 giữa 2 VPC trên nền tảng hạ tầng bảo mật của AWS (sử dụng địa chỉ IP nội bộ, không đi qua Internet công cộng).
  * Nắm vững các điều kiện tiên quyết của VPC Peering: hai VPC không được trùng dải mạng IPv4 CIDR và không thể thực hiện định tuyến bắc cầu (Non-transitive).
  * Thiết lập thành công **VPC Peering Connection**: khởi tạo yêu cầu (Requester) và chấp thuận liên kết (Accepter).
  * Cập nhật chính xác bảng định tuyến (**Route Tables**) tại cả 2 đầu VPC và điều chỉnh **Network ACLs / Security Groups** cho phép lưu lượng ICMP/TCP cần thiết qua lại an toàn.
  * Bật tính năng **DNS Resolution Support** trên peering connection, cho phép các máy chủ EC2 ở 2 VPC khác nhau phân giải được Private DNS Name của nhau thành Private IP thay vì Public IP.

* **Kiến trúc mạng tập trung với AWS Transit Gateway (Workshop 000020):**
  * Hiểu rõ sự khác biệt giữa mô hình Full Mesh (sử dụng nhiều cặp VPC Peering tốn kém công sức quản lý: $N(N-1)/2$ kết nối) và mô hình tập trung Hub-and-Spoke với AWS Transit Gateway khi hệ thống mở rộng từ hàng chục đến hàng trăm VPC.
  * Khởi tạo thành công **AWS Transit Gateway (TGW)** và gắn kết các mạng thông qua **VPC Attachments**.
  * Làm chủ nguyên lý hoạt động của bảng định tuyến TGW: phân biệt rõ ràng giữa **Associations** (xác định TGW Route Table mà một Attachment liên kết tới) và **Propagations** (quảng bá dải mạng CIDR của VPC vào TGW Route Table).
  * Định tuyến luồng mạng thành công: các máy chủ EC2 thuộc các VPC độc lập có thể ping và giao tiếp mượt mà với nhau thông qua Transit Gateway, tạo nền tảng vững chắc cho việc mở rộng kiến trúc hạ tầng mạng quy mô lớn trong tương lai.
