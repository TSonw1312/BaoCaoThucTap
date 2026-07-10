---
title: "Worklog Tuần 10"
date: 2026-06-19
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---


### Mục tiêu Tuần 10:

* Chuyển luồng upload file sang S3 Upload Bucket bằng presigned URL và tách import Word thành Lambda xử lý bất đồng bộ.

### Các nhiệm vụ cần thực hiện trong tuần này:
| Ngày | Nhiệm vụ | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | --------------- | ----------------------------------------- |
| Thứ Hai | - Tạo S3 Upload Bucket, giữ bucket private, bật SSE-S3 và ghi lại tên bucket để dùng trong biến môi trường Lambda.                                                                     | 22/06/2026 | 22/06/2026      | <https://docs.aws.amazon.com/AmazonS3/latest/userguide/> |
| Thứ Ba | - Tạo IAM policy cho Lambda Backend API với quyền s3:PutObject và s3:GetObject trên S3 Upload Bucket.                                                                                  | 23/06/2026 | 23/06/2026      | <https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies.html> |
| Thứ Tư | - Code endpoint /api/uploads/presigned-url, kiểm tra uploadType, role và sinh object key theo prefix backend quyết định.                                                               | 24/06/2026 | 25/06/2026      | <https://docs.aws.amazon.com/AmazonS3/latest/userguide/ShareObjectPreSignedURL.html> |
| Thứ Năm | - Chuyển upload avatar, ảnh lớp và ảnh đề thi/câu hỏi sang flow presigned URL phía frontend.                                                                                           | 26/06/2026 | 26/06/2026      | |
| Thứ Sáu | - Code Lambda Import Word Processor: nhận S3 event, đọc file .docx, parse câu hỏi và lưu vào MongoDB Atlas.                                                                             | 27/06/2026 | 28/06/2026      | <https://docs.aws.amazon.com/lambda/latest/dg/with-s3.html> |


### Kết quả đạt được trong Tuần 10:

* Presigned URL hoạt động cho các luồng upload chính, file được lưu đúng prefix S3 và Lambda Import Word có thể parse file .docx và lưu câu hỏi vào MongoDB.
* ...