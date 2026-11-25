---
title: "Worklog Tuần 5"
date: 2026-10-31
weight: 5
chapter: false
pre: " <b>1.5. </b> "
---

### Mục tiêu tuần 5:

* Tìm hiểu dịch vụ AWS Lambda và tự động hóa tác vụ vận hành bằng AWS Lambda.
* Tìm hiểu và triển khai giám sát hệ thống bằng Amazon CloudWatch và Grafana.
* Tổ chức, quản lý tài nguyên AWS thông qua Tags và Resource Groups.
* Quản lý và vận hành máy chủ từ xa bằng AWS Systems Manager và Session Manager.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Tìm hiểu về Serverless Computing và dịch vụ **AWS Lambda** (kiến trúc hướng sự kiện, execution role, triggers). <br> - Thực hành viết hàm Lambda tự động hóa các tác vụ quản trị vận hành: tự động bật/tắt EC2 instances theo lịch trình hoặc tự động dọn dẹp các tài nguyên không sử dụng nhằm tối ưu chi phí. | 26/10/2026 | 26/10/2026 | <https://docs.aws.amazon.com/lambda/latest/dg/welcome.html> |
| 4 | - Nâng cao năng lực giám sát với **Amazon CloudWatch**: cấu hình CloudWatch Agent để thu thập log ứng dụng và các custom metrics chuyên sâu (Memory, Disk). <br> - Tìm hiểu và triển khai **Grafana**: kết nối nguồn dữ liệu từ Amazon CloudWatch. <br> - Thiết kế và xây dựng Dashboard trên Grafana để trực quan hóa hiệu năng hệ thống và tài nguyên theo thời gian thực. | 28/10/2026 | 28/10/2026 | <https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/Install-CloudWatch-Agent.html> <br> <https://grafana.com/docs/grafana/latest/datasources/aws-cloudwatch/> |
| 6 | - Tìm hiểu chiến lược gắn nhãn (**AWS Tags**) và tổ chức nhóm tài nguyên với **AWS Resource Groups**. <br> - Tìm hiểu dịch vụ **AWS Systems Manager (SSM)**: cơ chế hoạt động của SSM Agent, IAM Role cho máy chủ EC2. <br> - Thực hành quản trị máy chủ từ xa an toàn không cần mở port SSH/RDP thông qua **Session Manager** và thực thi lệnh hàng loạt với **Run Command**. | 30/10/2026 | 30/10/2026 | <https://000058.awsfcaj.com> <br> <https://docs.aws.amazon.com/systems-manager/latest/userguide/what-is-systems-manager.html> <br> <https://docs.aws.amazon.com/ARG/latest/userguide/welcome.html> |

### Kết quả đạt được tuần 5:

* **AWS Lambda & Tự động hóa vận hành:**
  * Nắm vững mô hình Serverless và cơ chế Event-driven Execution của AWS Lambda.
  * Xây dựng và triển khai thành công hàm Lambda tự động hóa quy trình quản trị hạ tầng, giúp tiết kiệm chi phí và thời gian vận hành.
* **Giám sát nâng cao với CloudWatch & Grafana:**
  * Cài đặt và cấu hình thành công CloudWatch Agent để thu thập các số liệu chi tiết ở mức hệ điều hành (RAM, Disk Usage).
  * Tích hợp thành công Amazon CloudWatch với Grafana, xây dựng Dashboard trực quan hóa dữ liệu theo dõi sức khỏe hệ thống thời gian thực.
* **Tổ chức tài nguyên & Quản trị từ xa bằng AWS Systems Manager:**
  * Áp dụng quy chuẩn gắn Tag nhất quán và gom nhóm tài nguyên khoa học với AWS Resource Groups.
  * Vận dụng thành công AWS Systems Manager và Session Manager để quản lý, truy cập máy chủ an toàn mà không cần mở port SSH/RDP công khai hay lưu trữ Key Pair.
  * Tận dụng Run Command để tự động hóa tác vụ bảo trì và thực thi câu lệnh đồng thời trên nhiều EC2 instance.
