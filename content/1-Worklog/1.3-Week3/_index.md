---
title: "Worklog Tuần 3"
date: 2026-10-17
weight: 3
chapter: false
pre: " <b>1.3. </b> "
---

### Mục tiêu tuần 3:

* Tìm hiểu dịch vụ Amazon S3 và các cơ chế kiểm soát quyền truy cập thông qua IAM Policies, Bucket Policies và Access Control Lists (ACLs).
* Tìm hiểu Amazon CloudFront và cách phân phối nội dung thông qua mạng lưới CDN.
* Tìm hiểu dịch vụ Amazon RDS, các loại cơ sở dữ liệu được hỗ trợ, mô hình triển khai và các tính năng quản lý cơ sở dữ liệu.
* Hiểu được vai trò của Amazon CloudWatch trong việc giám sát, theo dõi và đánh giá tình trạng hoạt động của tài nguyên AWS.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                              |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------ | --------------- | -------------------------------------- |
| 2   | - Làm quen với Amazon S3 (Simple Storage Service) và cách phân quyền truy cập tài nguyên bằng IAM Policies. <br> - Thực hành tạo bucket S3, tải dữ liệu lên và cấu hình quyền truy cập dữ liệu bằng Bucket Policies. <br> Lưu trữ và triển khai một website tĩnh trên S3, đồng thời kiểm soát truy cập bằng ACLs (Access Control Lists). <br> - Thiết lập kiểm soát truy cập bằng CloudFront cho website tĩnh được lưu trữ trên S3: CloudFront phân phối nội dung, cho phép giữ bucket và đối tượng ở trạng thái riêng tư (không công khai), qua đó tăng cường bảo mật. <br> - Tìm hiểu cách CloudFront phân phối nội dung với độ trễ thấp và tốc độ truyền nhanh, nhờ lưu nội dung đệm tại các Edge Location gần người dùng nhất.                                                                                             | 12/10/2026   | 12/10/2026      | 1. <https://000057.awsfcaj.com/> 2. <https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html> 3. <https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Introduction.html> |
| 3   | - Tìm hiểu dịch vụ Amazon RDS, các thành phần và nguyên lý hoạt động của cơ sở dữ liệu quan hệ trên AWS. <br> - Nghiên cứu và hiểu kiến trúc hạ tầng mạng phục vụ kết nối giữa Amazon RDS và Amazon EC2. <br> - Thiết lập các tài nguyên mạng cần thiết, bao gồm VPC, Public/Private Subnet, Security Group và DB Subnet Group. <br> - Thực hành khởi tạo và cấu hình RDS Instance, thiết lập quyền truy cập và kết nối từ EC2 đến cơ sở dữ liệu. <br> - Triển khai ứng dụng trên EC2, cấu hình thông tin kết nối đến Amazon RDS và kiểm tra khả năng hoạt động của ứng dụng.                                            | 14/10/2026   | 14/10/2026      | <https://000005.awsfcaj.com/> |
| 4   | - Tìm hiểu dịch vụ Amazon CloudWatch, AWS CloudFormation và vai trò của các dịch vụ trong việc giám sát, quản lý hạ tầng AWS. <br> - Tìm hiểu ý nghĩa và cách theo dõi các chỉ số giám sát (Metrics) như CPU Utilization, Network In/Out, Disk Read/Write và trạng thái hoạt động của EC2. <br> - Thực hành thu thập, quản lý và theo dõi nhật ký hệ thống (Logs) thông qua CloudWatch Logs. <br> - Tìm hiểu và cấu hình CloudWatch Alarms để thiết lập cảnh báo khi các chỉ số vượt ngưỡng cho phép. <br> - Làm quen với AWS CloudFormation Dashboard và thực hành quản lý, triển khai tài nguyên hạ tầng thông qua các Stack.                                            | 16/10/2026   | 16/10/2026      | <https://000008.awsfcaj.com/> |

### Kết quả đạt được tuần 3:

* Amazon S3:
  * Nắm được sự khác biệt và cách áp dụng IAM Policies, Bucket Policies và ACLs trong kiểm soát quyền truy cập.
  * Hiểu được lý do không nên công khai S3 Bucket khi triển khai website thực tế và lợi ích của việc sử dụng CloudFront kết hợp với Origin Access Control (OAC).
  * Nắm được quy trình và triển khai thành công website tĩnh trên S3 và sử dụng CloudFront để phân phối nội dung.
  * Hiểu được cơ chế CDN hoạt động thông qua Edge Locations và cách Caching giúp giảm độ trễ, hạn chế số lượng request trực tiếp đến máy chủ gốc.
* Amazon RDS:
  * Hiểu được lý do nên tách biệt máy chủ ứng dụng (EC2) và máy chủ cơ sở dữ liệu (RDS) nhằm tăng tính bảo mật, khả năng quản lý và mở rộng hệ thống.
  * Nắm được vai trò của VPC, Public Subnet, Private Subnet và cách tổ chức mạng để bảo vệ tài nguyên nội bộ, nguyên lý hoạt động của Security Group và cách thiết lập quy tắc truy cập giữa EC2 và RDS.
  * Vận dụng triển khai thành công ứng dụng trên EC2 và cấu hình kết nối với Amazon RDS.
* Amazon CloudWatch:
  * Hiểu được tầm quan trọng của việc giám sát tài nguyên để phát hiện sớm các vấn đề về hiệu suất và tình trạng hoạt động của hệ thống.
  * Phân biệt được Metrics, Logs và Alarms cũng như vai trò của từng thành phần trong quá trình giám sát.
  * Hiểu được cách sử dụng ngưỡng cảnh báo (Threshold) để phát hiện tình trạng sử dụng tài nguyên vượt mức cho phép.
  * Hiểu được lý do nên sử dụng Infrastructure as Code (IaC) và lợi ích của AWS CloudFormation trong việc tự động hóa triển khai, quản lý và tái sử dụng hạ tầng.
  * Nắm được khái niệm Stack và mối quan hệ giữa CloudFormation Template với các tài nguyên AWS được khởi tạo.

