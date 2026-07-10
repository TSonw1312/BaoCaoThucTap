---
title: "Blog 1"
date: 2026-06-30
weight: 1
chapter: false
pre: " <b> 3.1. </b> "
---

# TỰ ĐỘNG HÓA REFRESH DỮ LIỆU GIỮA CÁC TÀI KHOẢN AWS CHO AMAZON RDS MULTI-AZ DB CLUSTER

Khi vận hành nhiều môi trường (production, staging, testing) trên các tài khoản AWS tách biệt, việc cập nhật dữ liệu mới nhất từ production sang các môi trường còn lại thường tốn nhiều công sức thủ công và tiềm ẩn rủi ro sai sót. Bài viết này trên AWS Database Blog hướng dẫn cách xây dựng một pipeline serverless tự động hóa toàn bộ quy trình refresh dữ liệu cho Amazon RDS Multi-AZ DB Cluster giữa hai tài khoản AWS.

Các điểm cốt lõi cần nắm vững:

* **Vượt qua giới hạn chia sẻ snapshot:** Amazon RDS hỗ trợ chia sẻ snapshot giữa các tài khoản cho DB instance thông thường, nhưng không hỗ trợ trực tiếp với Multi-AZ DB Cluster. Giải pháp đi vòng qua hạn chế này bằng cách phục hồi cluster snapshot thành một DB instance đơn AZ tạm thời, sau đó tạo một instance snapshot từ instance đó để chia sẻ cross-account.
* **Điều phối tự động bằng AWS Lambda, Step Functions và EventBridge:** Toàn bộ quy trình gồm bảy bước trải dài trên hai tài khoản được điều phối tự động chỉ với một lệnh kích hoạt. AWS Lambda xử lý từng tác vụ cụ thể như tạo snapshot, phục hồi instance, chia sẻ snapshot; AWS Step Functions quản lý vòng lặp chờ và kiểm tra trạng thái; Amazon EventBridge đóng vai trò cầu nối, chuyển sự kiện thành công từ tài khoản nguồn sang tài khoản đích để tự động kích hoạt bước tiếp theo.
* **Bảo mật xuyên suốt bằng AWS KMS:** Cluster nguồn bắt buộc phải được mã hóa bằng customer-managed KMS key ngay từ đầu. Khi snapshot được chia sẻ và copy sang tài khoản đích, dữ liệu sẽ được giải mã và mã hóa lại bằng đúng KMS key của tài khoản đích, đảm bảo dữ liệu luôn được bảo vệ trong suốt quá trình di chuyển giữa hai tài khoản.

Link bài viết: https://aws.amazon.com/vi/blogs/database/automating-cross-account-refresh-for-amazon-rds-multi-az-db-clusters/
![](/images/3-BlogsPosted/blog1.jpg)