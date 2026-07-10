---
title: "Worklog Tuần 11"
date: 2026-06-26
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---


### Mục tiêu Tuần 11:

* Tách logic chấm bài khỏi request nộp bài bằng SQS Grading Queue và Lambda Grading Worker.

### Các nhiệm vụ cần thực hiện trong tuần này:
| Ngày | Nhiệm vụ | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | --------------- | ----------------------------------------- |
| Thứ Hai | - Phân tích logic chấm bài hiện tại và xác định cần tách khỏi request nộp bài bằng SQS.                                                                                                | 29/06/2026 | 29/06/2026      | |
| Thứ Ba | - Tạo SQS Grading Queue và ghi lại Queue URL để cấu hình biến môi trường cho Lambda Backend API.                                                                                      | 30/06/2026 | 30/06/2026      | <https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/> |
| Thứ Tư | - Sửa backend submit bài: lưu kết quả với trạng thái đang chấm và gửi grading job ngắn vào SQS.                                                                                        | 01/07/2026 | 02/07/2026      | <https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/> |
| Thứ Năm | - Code Lambda Grading Worker: nhận SQS message, đọc MongoDB, tính điểm và cập nhật kết quả bài thi.                                                                                    | 03/07/2026 | 03/07/2026      | <https://docs.aws.amazon.com/lambda/latest/dg/with-sqs.html> |
| Thứ Sáu | - Kiểm tra CloudWatch Logs của Lambda Grading Worker sau khi test nộp bài và ghi nhận lỗi runtime nếu có.                                                                              | 04/07/2026 | 05/07/2026      | <https://docs.aws.amazon.com/AmazonCloudWatch/latest/logs/> |


### Kết quả đạt được trong Tuần 11:

* Backend lưu bài làm với trạng thái đang chấm, gửi job vào SQS và worker xử lý chấm điểm/cập nhật kết quả về MongoDB.
* ...