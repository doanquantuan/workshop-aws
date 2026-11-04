---
title: "Worklog Tuần 2"
date: 2024-01-01
weight: 1
chapter: false
prev: "/1-worklog/1.1-week1/"
next: "/1-worklog/1.3-week3/"
---

### Mục tiêu tuần 2:

* Tìm hiểu dịch vụ Amazon VPC, các tính năng chính trong mạng VPC hiện đại và kiến trúc VPC.
* Hiểu cách tạo và cấu hình VPC, EC2, định tuyến và các thành phần mạng trên AWS.
* Biết cách thiết lập Site-to-Site VPN, kiểm tra kết nối giữa các mạng và xử lý sự cố.


### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                              |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------ | --------------- | -------------------------------------- |
| 2   | - Học VPC cơ bản: <br>&emsp; + Subnets <br>&emsp; + Route Table <br>&emsp; + Internet Gateway <br>&emsp; + NAT Gateway <br> - Học Firewall trong VPC:<br>&emsp; + Security Group <br>&emsp; + Network ACLs <br>&emsp; + VPC Resource Map <br> - Thực hành tạo VPC, Subnets, Route Table, Internet Gateway, NAT Gateway, Security Group, cấu hình VPC flow logs..                                                                                             | 06/10/2026   | 06/10/2026      | <https://000003.awsfcaj.com/1-introduce/> <https://000003.awsfcaj.com/2-firewallinvpc/> <https://000003.awsfcaj.com/3-prerequisite/> |
| 3   | - Triển khai hạ tầng EC2: <br>&emsp; + Tạo, kết nối và quản lý EC2 Instance. <br>&emsp; + Cấu hình NAT Gateway, kiểm tra kết nối mạng. <br>&emsp; + Giám sát và cảnh báo bằng CloudWatch.                                            | 07/10/2026   | 07/10/2026      | <https://000003.awsfcaj.com/4-createec2server/> |
| 4   | - Thiết lập Site-to-Site VPN trên AWS: <br>&emsp; + Tạo VPC, EC2 và cấu hình kết nối VPN. <br>&emsp; + Thiết lập Virtual Private Gateway, Customer Gateway và định tuyến. <br>&emsp; + Kiểm tra kết nối và xử lý sự cố VPN.                                            | 08/10/2026   | 08/10/2026      | <https://000003.awsfcaj.com/5-vpnsitetosite/> |

### Kết quả đạt được tuần 2:

* Tạo và cấu hình thành công VPC với Public/Private Subnets, Route Tables, Internet Gateway và NAT Gateway.
* Triển khai các EC2 Instances và kiểm tra khả năng kết nối giữa mạng Public và Private.
* Cấu hình các cơ chế kiểm soát truy cập mạng bằng Security Groups và Network ACLs.
* Thiết lập và kiểm thử kết nối AWS Site-to-Site VPN giữa AWS và một mạng On-premises mô phỏng.
* Cấu hình các công cụ giám sát và khắc phục sự cố mạng bằng VPC Flow Logs, Reachability Analyzer và CloudWatch.
