---
title: "Worklog Tuần 12"
date: 2026-07-03
weight: 12
chapter: false
pre: " <b> 1.12. </b> "
---


### Mục tiêu Tuần 12:

* Triển khai frontend lên Amplify Hosting, chuẩn bị Route 53/domain và hoàn thiện test, proposal, workshop report.

### Các nhiệm vụ cần thực hiện trong tuần này:
| Ngày | Nhiệm vụ | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | --------------- | ----------------------------------------- |
| Thứ Hai | - Kiểm tra CORS API Gateway cho Amplify domain và localhost trước khi deploy lại frontend.                                                                                             | 06/07/2026 | 06/07/2026      | <https://docs.aws.amazon.com/apigateway/latest/developerguide/http-api-cors.html> |
| Thứ Ba | - Sửa backend đọc FRONTEND_ORIGINS nhiều domain để hỗ trợ local, Amplify domain và domain examora.click.                                                                               | 07/07/2026 | 08/07/2026      | <https://docs.aws.amazon.com/apigateway/latest/developerguide/http-api-cors.html> |
| Thứ Tư | - Rà soát phần IAM/Secrets/Security trong tài liệu báo cáo để đảm bảo không ghi quyền quá rộng cho production.                                                                         | 09/07/2026 | 09/07/2026      | |
| Thứ Năm | - Tổng hợp lại kiến trúc, proposal, mapping dịch vụ AWS và worklog theo kiến trúc Route 53 + Amplify.                                                                                   | 10/07/2026 | 12/07/2026      | <https://gohugo.io/documentation/>        |


### Kết quả đạt được trong Tuần 12:

* Frontend chạy trên Amplify, CORS hỗ trợ local/Amplify/domain, các luồng chính được test lại và tài liệu được cập nhật theo kiến trúc mới.
* ...