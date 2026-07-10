---
title: "Worklog Tuần 8"
date: 2026-06-05
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---
### Mục tiêu Tuần 8:

* Định hướng phạm vi MVP, rà soát source code hiện tại và chốt kiến trúc AWS Serverless Hybrid cho Examora.

### Các nhiệm vụ cần thực hiện trong tuần này:
| Ngày | Nhiệm vụ | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | --------------- | ----------------------------------------- |
| Thứ Hai | - Rà soát tổng thể source Examora hiện tại: frontend React/Vite, backend Express, models MongoDB và các route chính.<br>- Tự học lại nhóm dịch vụ AWS Identity & Security để chuẩn bị cho phần Cognito, IAM và Secrets Manager. | 10/06/2026 | 10/06/2026      | <https://cloudjourney.awsstudygroup.com/> |
| Thứ Ba | - Đọc tài liệu IAM Role/Policy và ghi chú nguyên tắc cấp quyền tối thiểu cho Lambda.                                                                                                   | 11/06/2026 | 11/06/2026      | <https://docs.aws.amazon.com/IAM/latest/UserGuide/> |
| Thứ Tư | - Chốt phạm vi MVP cho Examora: giữ MongoDB Atlas, bỏ Google Login, payment, chatbot, Telegram và chống gian lận nâng cao.                                                             | 12/06/2026 | 12/06/2026      | |
| Thứ Năm | - Chuẩn bị checklist cấu hình AWS Console cho IAM, Secrets Manager và quyền truy cập MongoDB Atlas.                                                                                    | 13/06/2026 | 13/06/2026      | <https://docs.aws.amazon.com/secretsmanager/> |
| Thứ Sáu | - Vẽ sơ đồ kiến trúc AWS Serverless Hybrid ban đầu và chia luồng thành authentication, upload/import Word, submit/grading.                                                             | 14/06/2026 | 16/06/2026      | <https://docs.aws.amazon.com/>            |


### Kết quả đạt được trong Tuần 8:

* Nắm được cấu trúc frontend/backend, xác định các module giữ lại, các module cần chuyển sang AWS và có backlog triển khai ban đầu.
* ...