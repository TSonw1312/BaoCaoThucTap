---
title: "Worklog Week 10"
date: 2026-06-19
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---


### Week 10 Objectives:

* Migrate the file upload flow to the S3 Upload Bucket using presigned URLs and decouple the Word import module into an independent asynchronous Lambda function.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | --------------- | ----------------------------------------- |
| Monday | - Provision the S3 Upload Bucket, ensure the bucket remains private, enable SSE-S3 encryption, and reference the bucket name within the Lambda environment variables.               | 22/06/2026 | 22/06/2026      | <https://docs.aws.amazon.com/AmazonS3/latest/userguide/> |
| Tuesday | - Create an IAM policy for the Lambda Backend API granting s3:PutObject and s3:GetObject permissions on the S3 Upload Bucket.                                                          | 23/06/2026 | 23/06/2026      | <https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies.html> |
| Wednesday | - Develop the /api/uploads/presigned-url endpoint, validate uploadType and roles, and generate object keys based on backend-defined prefixes.                                        | 24/06/2026 | 25/06/2026      | <https://docs.aws.amazon.com/AmazonS3/latest/userguide/ShareObjectPreSignedURL.html> |
| Thursday | - Refactor the frontend upload flows for avatars, classroom images, and quiz/exam images to utilize the new presigned URL mechanism.                                                   | 26/06/2026 | 26/06/2026      | |
| Friday | - Implement the Lambda Word Importer function: configure it to ingest S3 ObjectCreated events, read .docx files, parse exam questions, and save them directly to MongoDB Atlas.         | 27/06/2026 | 28/06/2026      | <https://docs.aws.amazon.com/lambda/latest/dg/with-s3.html> |


### Week 10 Achievements:

* Presigned URLs are working properly for core upload routes, objects are stored with the correct S3 prefixes, and the Word Import Lambda parses .docx data successfully into MongoDB.
* ...