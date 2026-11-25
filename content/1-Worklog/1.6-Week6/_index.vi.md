---
title: "Worklog Tuần 6"
date: 2026-11-07
weight: 6
chapter: false
pre: " <b>1.6. </b> "
---

### Mục tiêu tuần 6:

* Tìm hiểu và thực hành quản lý quyền truy cập AWS bằng IAM User, IAM Group, IAM Role và IAM Policy theo nguyên tắc Least Privilege. Tích hợp IAM Identity Center và AWS Organizations để quản lý tập trung danh tính, phân quyền và kiểm soát truy cập trên nhiều tài khoản AWS (Multi-Account).
* Tìm hiểu cơ chế IAM Permission Boundary để giới hạn quyền tối đa cho các ủy viên (identities), kiểm soát ủy quyền phân quyền an toàn và ngăn chặn leo thang đặc quyền (Privilege Escalation).
* Tìm hiểu cấu hình IAM Role và các điều kiện (Condition Blocks) nhằm kiểm soát chặt chẽ quyền truy cập theo địa chỉ IP nguồn và khung thời gian cho phép.
* Tìm hiểu AWS Security Hub và triển khai tập trung giám sát cảnh báo an ninh, đánh giá mức độ tuân thủ tiêu chuẩn bảo mật (CIS, AWS Foundational Security Best Practices) và tự động phát hiện rủi ro trên AWS.
* Tìm hiểu AWS WAF (Web Application Firewall) và triển khai bảo vệ ứng dụng web chống lại các lỗ hổng phổ biến (OWASP Top 10) thông qua AWS Managed Rules và custom rules.
* Tìm hiểu AWS KMS và thực hành mã hóa dữ liệu lưu trữ (Encryption at Rest) trên Amazon S3, kết hợp AWS CloudTrail và Amazon Athena để ghi nhật ký, truy vấn và kiểm tra hoạt động giải mã / truy cập dữ liệu.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - **Quản trị danh tính tập trung với AWS IAM Identity Center & AWS Organizations:** <br>&emsp; + Tìm hiểu kiến trúc quản lý Multi-Account và Single Sign-On (SSO) trên AWS. <br>&emsp; + Cấu hình AWS Organizations, kích hoạt IAM Identity Center, quản lý Users/Groups tập trung và định nghĩa Permission Sets. <br>&emsp; + Phân quyền truy cập tài nguyên xuyên suốt các tài khoản AWS theo nguyên tắc đặc quyền tối thiểu (Least Privilege). | 02/11/2026 | 02/11/2026 | <https://000012.awsfcaj.com/> |
| 3 | - **Giới hạn đặc quyền tối đa với IAM Permission Boundary:** <br>&emsp; + Tìm hiểu nguyên lý hoạt động và trường hợp ứng dụng Permission Boundary trong quản trị ủy quyền. <br>&emsp; + Thực hành tạo và áp dụng Managed Policy làm ranh giới quyền (Boundary) cho IAM Users / Roles. <br>&emsp; + Kiểm thử và xác thực cơ chế ngăn chặn leo thang đặc quyền (Privilege Escalation) khi người dùng tự tạo role/policy mới. | 03/11/2026 | 03/11/2026 | <https://000030.awsfcaj.com/> |
| 4 | - **Kiểm soát truy cập nâng cao với IAM Role & Condition:** <br>&emsp; + Tìm hiểu cách sử dụng Condition Elements trong IAM Policy (IP Address Conditions, Date/Time Conditions). <br>&emsp; + Cấu hình AssumeRole Policy và IAM Policy kiểm soát quyền truy cập chỉ cho phép từ dải IP hợp lệ và trong khung giờ làm việc xác định. <br>&emsp; + Kiểm thử chuyển đổi vai trò (Switch Role) và xác minh quyền truy cập tài nguyên khi thỏa mãn hoặc vi phạm điều kiện. | 04/11/2026 | 04/11/2026 | <https://000044.awsfcaj.com/> |
| 5 | - **Giám sát và đánh giá an ninh tập trung với AWS Security Hub:** <br>&emsp; + Tìm hiểu tổng quan về AWS Security Hub và các tiêu chuẩn bảo mật (AWS Foundational Security Best Practices, CIS AWS Foundations Benchmark). <br>&emsp; + Kích hoạt Security Hub, tích hợp và tổng hợp kết quả phân tích (findings) từ các dịch vụ bảo mật khác (GuardDuty, Inspector, IAM Access Analyzer). <br>&emsp; + Đánh giá điểm tuân thủ (Compliance Score), phân tích các phát hiện lỗ hổng/rủi ro và thực hiện các biện pháp khắc phục (Remediation). | 05/11/2026 | 05/11/2026 | <https://000018.awsfcaj.com/> |
| 6 | - **Bảo vệ ứng dụng web với AWS WAF (Web Application Firewall):** <br>&emsp; + Tìm hiểu các mối đe dọa an ninh ứng dụng web phổ biến (SQLi, XSS, DDoS tầng ứng dụng) và kiến trúc AWS WAF. <br>&emsp; + Khởi tạo Web ACL, liên kết bảo vệ với Application Load Balancer (ALB) hoặc Amazon CloudFront. <br>&emsp; + Cấu hình bộ quy tắc được quản lý (AWS Managed Rules) kết hợp xây dựng Rule tùy chỉnh (Rate-based rule, IP set) và kiểm tra khả năng chặn request độc hại. | 06/11/2026 | 06/11/2026 | <https://000026.awsfcaj.com/> |
| 7 | - **Mã hóa dữ liệu lưu trữ với AWS KMS, CloudTrail và Athena:** <br>&emsp; + Tìm hiểu mô hình mã hóa dữ liệu Envelope Encryption và cơ chế quản lý Customer Managed Key (CMK) trong AWS KMS. <br>&emsp; + Thực hành tạo KMS Key, thiết lập Key Policy và cấu hình mã hóa mặc định (Server-Side Encryption) cho Amazon S3 bucket. <br>&emsp; + Bật AWS CloudTrail ghi nhận nhật ký các sự kiện giải mã (KMS Decrypt) và truy xuất đối tượng S3. <br>&emsp; + Sử dụng Amazon Athena tạo bảng và thực thi truy vấn phân tích log CloudTrail để kiểm toán, giám sát việc truy cập dữ liệu. | 07/11/2026 | 07/11/2026 | <https://000033.awsfcaj.com/> |

### Kết quả đạt được tuần 6:

* **Quản trị danh tính tập trung với AWS IAM Identity Center & AWS Organizations (Workshop 000012):**
  * Nắm vững mô hình kiến trúc Multi-Account và cách thức AWS Organizations gom nhóm tài khoản thành viên thông qua Organizational Units (OUs).
  * Kích hoạt và cấu hình thành công AWS IAM Identity Center (tiền thân là AWS SSO), thiết lập thư mục quản lý User và Group tập trung thay vì phải tạo IAM User phân mảnh trên từng tài khoản con.
  * Xây dựng và gán các bộ quyền (Permission Sets) kết hợp AWS Managed Policies và Customer Managed Policies cho các tài khoản mục tiêu; hỗ trợ cấu hình truy cập thông qua cả AWS Management Console và AWS CLI v2 (`aws configure sso`).
  * Nắm vững cơ chế kiểm soát truy cập dựa trên thời gian (Time-based Access Control) và cách thức gọi các Identity Store APIs để tự động hóa quản trị danh tính.

* **Kiểm soát ranh giới quyền với IAM Permission Boundary (Workshop 000030):**
  * Hiểu sâu cơ chế ủy quyền an toàn (Delegated Administration): cho phép quản trị viên phân quyền cho các Lead/Dev tự tạo IAM User/Role mà không lo ngại việc họ tự cấp quyền Administrator cho chính mình.
  * Nắm rõ nguyên lý toán học "Intersection of Permissions" (phép giao quyền): một hành động chỉ được phép thực thi khi và chỉ khi nó được ALLOW đồng thời ở cả Identity-based Policy VÀ Permissions Boundary Policy.
  * Tạo thành công Permissions Boundary Managed Policy để giới hạn trần quyền lực tối đa và ép buộc (enforce) điều kiện: mọi User/Role mới được tạo bắt buộc phải đính kèm Boundary này.
  * Thực hành kiểm thử và xác nhận: khi User cố gắng thực hiện hành động nằm ngoài Boundary (hoặc cố gắng gỡ bỏ Boundary), hệ thống lập tức trả về lỗi `Access Denied`, qua đó loại bỏ hoàn toàn nguy cơ leo thang đặc quyền (Privilege Escalation).

* **Ủy quyền bảo mật nâng cao với IAM Role & Condition (Workshop 000044):**
  * Nắm vững cơ chế ủy quyền tạm thời thông qua STS (Security Token Service) và hành động `sts:AssumeRole`, giúp loại bỏ việc chia sẻ thông tin xác thực tĩnh (Access Key / Secret Key).
  * Vận dụng thành thạo khối điều kiện (`Condition Block`) trong Trust Policy và Identity Policy với các khóa ngữ cảnh:
    * `aws:SourceIp`: Giới hạn hành động AssumeRole và thao tác tài nguyên chỉ được phép diễn ra từ các địa chỉ IP mạng công ty/VPN tin cậy.
    * `aws:CurrentTime`: Thiết lập khung giờ truy cập hợp lệ (ví dụ: chỉ cho phép từ 08:00 đến 17:00 các ngày làm việc).
  * Cấu hình và thực hiện Switch Role thành công trên AWS Management Console; đồng thời kiểm thử các kịch bản thực tế khi truy cập từ IP lạ hoặc ngoài giờ quy định để đảm bảo hệ thống từ chối truy cập chính xác theo thiết kế.

* **Giám sát an ninh và đánh giá tuân thủ với AWS Security Hub (Workshop 000018):**
  * Nắm vững vai trò trung tâm thông tin an ninh (Security Posture Management) của AWS Security Hub trong việc liên tục kiểm tra và tổng hợp kết quả đánh giá bảo mật trên toàn bộ môi trường AWS.
  * Kích hoạt thành công các bộ tiêu chuẩn an ninh hàng đầu: **AWS Foundational Security Best Practices (FSBP)** và **CIS AWS Foundations Benchmark v1.2.0 / v1.4.0**.
  * Hiểu cách tính toán và theo dõi điểm số bảo mật (Security Score); phân tích chi tiết các phát hiện (Findings) theo mức độ nghiêm trọng (Critical, High, Medium, Low).
  * Nắm được quy trình phân tích nguyên nhân gốc rễ và thực hiện các bước khắc phục (Remediation) đối với các tài nguyên vi phạm tiêu chuẩn (như S3 công khai, IAM Root có access key, Security Group mở port nhạy cảm).

* **Tăng cường an ninh ứng dụng web với AWS WAF (Workshop 000026):**
  * Hiểu rõ cơ chế lọc gói tin HTTP/HTTPS tại tầng ứng dụng (Layer 7) và sự kết hợp giữa AWS WAF với các điểm phân phối/cân bằng tải (ALB, CloudFront).
  * Triển khai thành công Web ACL và tích hợp bộ quy tắc được AWS quản lý (**AWS Managed Rules - Common Rule Set**), bảo vệ ứng dụng trước các lỗ hổng phổ biến thuộc OWASP Top 10 như SQL Injection (SQLi), Cross-Site Scripting (XSS).
  * Thiết kế và áp dụng các Custom Rule nâng cao:
    * Tạo **IP Match Condition / IP Set** để chủ động cho phép (Allow) hoặc chặn (Block) các dải IP nguy hại.
    * Cấu hình **Rate-based Rules** nhằm giới hạn số lượng request từ một địa chỉ IP trong khoảng thời gian xác định, chủ động ngăn chặn các cuộc tấn công HTTP Flood / Brute-force / DoS tầng ứng dụng.
  * Kích hoạt và cấu hình CloudWatch Metrics / WAF Logging để theo dõi lưu lượng truy cập, kiểm chứng việc chặn thành công các request mô phỏng tấn công.

* **Mã hóa và kiểm toán truy cập dữ liệu với AWS KMS, S3, CloudTrail & Athena (Workshop 000033):**
  * Hiểu rõ mô hình mã hóa phân tầng Envelope Encryption và sự kết hợp giữa khóa do AWS quản lý với khóa do khách hàng quản lý (**Customer Managed Key - CMK**).
  * Khởi tạo thành công Symmetric KMS Key, cấu hình Key Policy phân tách rạch ròi giữa quyền quản trị khóa (Key Administrator) và quyền sử dụng khóa để mã hóa/giải mã (Key User).
  * Áp dụng mã hóa mặc định SSE-KMS (Server-Side Encryption with AWS KMS) cho Amazon S3 Bucket, đảm bảo toàn bộ dữ liệu lưu trữ (Data at Rest) đều được bảo vệ tự động bằng CMK.
  * Cấu hình AWS CloudTrail để ghi lại toàn bộ Data Events và Management Events liên quan đến thao tác S3 (`GetObject`, `PutObject`) và KMS (`kms:Decrypt`, `kms:GenerateDataKey`).
  * Tích hợp thành công **Amazon Athena**: tự động ánh xạ cấu trúc log từ CloudTrail lưu trên S3 thành bảng dữ liệu (Table Schema) và thực thi các câu lệnh SQL để truy vấn tức thì: xác định chính xác ai (IAM Identity), vào thời điểm nào, từ IP nào đã gọi giải mã và truy xuất vào các tập tin nhạy cảm.
