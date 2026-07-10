---
title: "Worklog Week 11"
date: 2026-06-26
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

### Week 11 Objectives:

* Decouple the grading engine from the main submission API request using an SQS Grading Queue and a Lambda Grading Worker.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | --------------- | ----------------------------------------- |
| Monday | - Analyze the legacy synchronous grading workflow and formulate the decoupled asynchronous system architecture using AWS SQS.                                                         | 29/06/2026 | 29/06/2026      | |
| Tuesday | - Deploy the AWS SQS Grading Queue and record the Queue URL to initialize environment variables inside the primary Lambda Backend API.                                                | 30/06/2026 | 30/06/2026      | <https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/> |
| Wednesday | - Refactor the backend submission API: save the initial exam record with a 'grading' status and immediately dispatch a lightweight grading job message payload into the SQS queue.     | 01/07/2026 | 02/07/2026      | <https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/> |
| Thursday | - Build the Lambda Grading Worker logic: handle incoming SQS message triggers, read target records from MongoDB, execute grading calculations, and update exam metrics.              | 03/07/2026 | 03/07/2026      | <https://docs.aws.amazon.com/lambda/latest/dg/with-sqs.html> |
| Friday | - Validate the system telemetry using CloudWatch Logs for the Lambda Grading Worker post-submission, identifying and fixing potential database connectivity or unhandled runtime exceptions. | 04/07/2026 | 05/07/2026 | <https://docs.aws.amazon.com/AmazonCloudWatch/latest/logs/> |


### Week 11 Achievements:

* Successfully decoupled the heavy evaluation logic from the primary submission path, drastically minimizing API overhead. The worker securely processes queue records and pushes results back to MongoDB.
* ...