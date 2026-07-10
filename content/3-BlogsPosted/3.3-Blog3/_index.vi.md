---
title: "Blog 3"
date: 2026-07-04
weight: 3
chapter: false
pre: " <b> 3.3. </b> "
---

# [GÓC CHIA SẺ] TỐI ƯU CHI PHÍ EC2 BẰNG CÁCH PHÂN TÍCH CAPACITY RESERVATIONS VỚI AMAZON ATHENA

Chào anh chị và các bạn, khi làm việc với AWS ở quy mô lớn, một trong những vấn đề tốn kém nhất nhưng lại dễ bị bỏ qua nhất chính là Capacity Reservations không được sử dụng hết. Bài viết này trên AWS Compute Blog hướng dẫn cách kết hợp EC2 Capacity Manager và Amazon Athena để theo dõi, phân tích và tối ưu hóa việc sử dụng capacity theo dữ liệu lịch sử dài hạn.

### Vấn đề với On-Demand Capacity Reservations

Khi đặt trước capacity EC2 (ODCR), bạn trả tiền cho dù có dùng hay không. Nếu reservation bị để trống hoặc sử dụng dưới mức, chi phí lãng phí sẽ tích lũy theo thời gian mà không ai hay biết, đặc biệt khi tổ chức có nhiều account và nhiều Region khác nhau. AWS Console chỉ cho phép xem lại dữ liệu trong vòng 90 ngày gần nhất, không đủ để phát hiện các pattern lãng phí dài hạn.

### Giải pháp: Export dữ liệu ra S3 và query bằng Athena

EC2 Capacity Manager cho phép export toàn bộ dữ liệu capacity theo giờ ra Amazon S3 dưới định dạng Parquet (tối ưu cho phân tích). Từ đó, Amazon Athena có thể query trực tiếp trên S3 bằng SQL thông thường mà không cần ETL hay data warehouse riêng. Điểm hay là Athena dùng Partition Projection để tự động nhận diện dữ liệu mới khi Capacity Manager export theo lịch, không cần chạy lệnh cập nhật metadata thủ công mỗi lần có dữ liệu mới.

### Những gì có thể phân tích được

Sau khi cấu hình xong, bạn có thể chạy các query để tìm ra reservation nào đang lãng phí chi phí nhiều nhất, xem tỷ lệ sử dụng trung bình theo từng loại instance, phát hiện pattern sử dụng theo giờ trong ngày để hiểu workload tập trung vào khung giờ nào, hoặc so sánh mức độ dàn trải capacity giữa các Region và Availability Zone. Tất cả đều dựa trên dữ liệu thực tế lưu lâu dài trên S3, không bị giới hạn 90 ngày như trên Console.

### Tóm lại

Đây là một pattern rất thực tế để kiểm soát chi phí EC2 ở quy mô tổ chức, đặc biệt khi có nhiều account và nhiều team cùng sử dụng capacity reservation. Thay vì chờ đến cuối tháng mới nhìn vào hóa đơn, bạn có thể chủ động phát hiện reservation lãng phí và điều chỉnh kịp thời. Nếu muốn mở rộng thêm, bài viết cũng gợi ý tích hợp dữ liệu này với EventBridge Scheduler để tự động refresh định kỳ, hoặc kết hợp với các công cụ BI như Amazon QuickSight để có dashboard trực quan hơn.

Link gốc bài viết mọi người có thể tham khảo thêm:
https://aws.amazon.com/blogs/compute/maximize-amazon-ec2-capacity-reservation-utilization-using-amazon-athena/
![](/images/3-BlogsPosted/blog3.jpg)
