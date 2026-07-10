---
title: "Week 8 Worklog"
date: 2026-06-05
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---
### Week 8 Objectives:

* Scope the MVP boundaries, review the current source code, and finalize the AWS Serverless Hybrid architecture for Examora.

### Tasks to be executed this week:
| Day | Task | Start Date | Completion Date | Reference Documents |
| --- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | --------------- | ----------------------------------------- |
| Monday | - Conduct an overall review of the current Examora source code: React/Vite frontend, Express backend, MongoDB models, and core routes.<br>- Self-study AWS Identity & Security service group to prepare for Cognito, IAM, and Secrets Manager. | 10/06/2026 | 10/06/2026      | <https://cloudjourney.awsstudygroup.com/> |
| Tuesday | - Read IAM Role/Policy documentation and note down the principle of least privilege for Lambda.                                                                                                   | 11/06/2026 | 11/06/2026      | <https://docs.aws.amazon.com/IAM/latest/UserGuide/> |
| Wednesday | - Finalize the MVP scope for Examora: keep MongoDB Atlas, remove Google Login, payment, chatbot, Telegram, and advanced anti-cheating features.                                             | 12/06/2026 | 12/06/2026      | |
| Thursday | - Prepare the AWS Console configuration checklist for IAM, Secrets Manager, and MongoDB Atlas access permissions.                                                                                    | 13/06/2026 | 13/06/2026      | <https://docs.aws.amazon.com/secretsmanager/> |
| Friday | - Draw the initial AWS Serverless Hybrid architecture diagram and split workflows into authentication, Word upload/import, and submit/grading.                                             | 14/06/2026 | 16/06/2026      | <https://docs.aws.amazon.com/>            |


### Results achieved in Week 8:

* Gained a solid understanding of the frontend/backend structure, identified modules to retain versus modules to migrate to AWS, and established the initial deployment backlog.
* ...