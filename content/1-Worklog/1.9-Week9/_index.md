---
title: "Worklog Week 9"
date: 2026-06-12
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

### Week 9 Objectives:

* Implement authentication using Cognito/SES, migrate the Express backend to Lambda, and protect the APIs using an API Gateway JWT Authorizer.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | --------------- | ----------------------------------------- |
| Monday | - Create a Cognito User Pool, enable email/password authentication, and configure Cognito Groups (ADMIN, TEACHER, STUDENT) via the AWS Console.                                       | 15/06/2026 | 15/06/2026      | <https://docs.aws.amazon.com/cognito/>    |
| Tuesday | - Update the NguoiDung database model to include cognitoSub, authProvider, emailVerified, and cognitoGroups.<br>- Configure the SES identity and verify the ability to send OTP/reset password emails via Cognito. | 16/06/2026 | 16/06/2026      | <https://www.mongodb.com/docs/atlas/><br><https://docs.aws.amazon.com/ses/> |
| Wednesday | - Update the frontend sign-up, email OTP verification, login, logout, forgot password, and change password flows using Cognito.                                                        | 17/06/2026 | 17/06/2026      | <https://docs.aws.amazon.com/cognito/>    |
| Thursday | - Implement backend verification for Cognito JWTs, sync user profiles into MongoDB, and map Cognito Groups to system user roles.                                                      | 18/06/2026 | 19/06/2026      | <https://docs.aws.amazon.com/cognito/>    |
| Friday | - Decouple the Express app from server.listen(), add a Lambda handler, and test the Lambda Backend API using the /health endpoint.<br>- Review and verify the Lambda Backend API's IAM Role permissions for CloudWatch Logs, Secrets Manager, and API Gateway invocation. | 20/06/2026 | 21/06/2026 | <https://docs.aws.amazon.com/lambda/><br><https://docs.aws.amazon.com/lambda/latest/dg/lambda-permissions.html> |


### Week 9 Achievements:

* Completed the registration flow, email OTP, login, MongoDB profile synchronization, Lambda Backend API integration, and basic API Gateway routing verification.
* ...