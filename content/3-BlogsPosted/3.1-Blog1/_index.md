---
title: "Blog 1"
date: 2026-06-30
weight: 1
chapter: false
pre: " <b> 3.1. </b> "
---
# AUTOMATING CROSS-ACCOUNT DATA REFRESH FOR AMAZON RDS MULTI-AZ DB CLUSTERS

When operating multiple environments (production, staging, testing) across separate AWS accounts, updating the latest data from production to the remaining environments usually requires significant manual effort and poses potential risks of human error. This article on the AWS Database Blog guides you on how to build a serverless pipeline to automate the entire data refresh process for Amazon RDS Multi-AZ DB Clusters between two AWS accounts.

Key points to know:

* **Bypassing snapshot sharing limitations:** Amazon RDS supports cross-account snapshot sharing for standard DB instances, but does not directly support it for Multi-AZ DB Clusters. The workaround addresses this limitation by restoring the cluster snapshot into a temporary Single-AZ DB instance, then creating an instance snapshot from that instance to share cross-account.
* **Automated orchestration using AWS Lambda, Step Functions, and EventBridge:** The entire process consists of seven steps spanning two accounts, automated and orchestrated with just a single trigger. AWS Lambda handles specific tasks such as creating snapshots, restoring instances, and sharing snapshots; AWS Step Functions manages the wait loops and status checks; Amazon EventBridge acts as a bridge, forwarding success events from the source account to the destination account to automatically trigger the next step.
* **End-to-end security via AWS KMS:** The source cluster must be encrypted with a customer-managed KMS key from the beginning. When the snapshot is shared and copied to the destination account, the data will be decrypted and re-encrypted using the destination account's exact KMS key, ensuring the data is always protected throughout its journey between the two accounts.

Article Link: https://aws.amazon.com/vi/blogs/database/automating-cross-account-refresh-for-amazon-rds-multi-az-db-clusters/

![](/images/3-BlogsPosted/blog1.jpg)