---
title: "Worklog Tuần 9"
date: 2026-06-12
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---


### Mục tiêu Tuần 9:

* Triển khai xác thực bằng Cognito/SES, đưa Express backend lên Lambda và bảo vệ API bằng API Gateway JWT Authorizer.

### Các nhiệm vụ cần thực hiện trong tuần này:
| Ngày | Nhiệm vụ | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | --------------- | ----------------------------------------- |
| Thứ Hai | - Tạo Cognito User Pool, bật email/password và tạo Cognito Groups ADMIN, TEACHER, STUDENT trên AWS Console.                                                                            | 15/06/2026 | 15/06/2026      | <https://docs.aws.amazon.com/cognito/>    |
| Thứ Ba | - Sửa model NguoiDung để bổ sung cognitoSub, authProvider, emailVerified và cognitoGroups.<br>- Cấu hình SES identity và kiểm tra khả năng gửi email OTP/reset password qua Cognito.   | 16/06/2026 | 16/06/2026      | <https://www.mongodb.com/docs/atlas/><br><https://docs.aws.amazon.com/ses/> |
| Thứ Tư | - Sửa frontend đăng ký, xác thực OTP email, login, logout, quên mật khẩu và đổi mật khẩu bằng Cognito.                                                                                | 17/06/2026 | 17/06/2026      | <https://docs.aws.amazon.com/cognito/>    |
| Thứ Năm | - Sửa backend verify Cognito JWT, sync profile vào MongoDB và mapping Cognito Groups sang role hệ thống.                                                                               | 18/06/2026 | 19/06/2026      | <https://docs.aws.amazon.com/cognito/>    |
| Thứ Sáu | - Tách Express app khỏi server.listen(), thêm Lambda handler và test Lambda Backend API bằng /health.<br>- Kiểm tra IAM Role của Lambda Backend API: quyền CloudWatch Logs, Secrets Manager và API Gateway invoke Lambda. | 20/06/2026 | 21/06/2026 | <https://docs.aws.amazon.com/lambda/><br><https://docs.aws.amazon.com/lambda/latest/dg/lambda-permissions.html> |


### Kết quả đạt được trong Tuần 9:

* Hoàn thành luồng đăng ký, OTP email, login, sync profile MongoDB, Lambda Backend API và test API Gateway cơ bản.
* ...