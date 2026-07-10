---
title: "Blog 3"
date: 2026-07-04
weight: 3
chapter: false
pre: " <b> 3.3. </b> "
---

# [KNOWLEDGE SHARING] OPTIMIZING EC2 COSTS BY ANALYZING CAPACITY RESERVATIONS WITH AMAZON ATHENA

Hello everyone, when working with AWS at scale, one of the most expensive yet easily overlooked issues is underutilized Capacity Reservations. This article on the AWS Compute Blog guides you on how to combine EC2 Capacity Manager and Amazon Athena to track, analyze, and optimize capacity utilization based on long-term historical data.

### The Challenge with On-Demand Capacity Reservations

With On-Demand Capacity Reservations (ODCR), you pay for the capacity whether you use it or not. If a reservation is left empty or underutilized, wasted costs accumulate over time without anyone realizing it, especially in organizations with multiple accounts and Regions. The AWS Console only allows you to review data from the past 90 days, which is insufficient for detecting long-term wasteful patterns.

### The Solution: Exporting Data to S3 and Querying with Athena

EC2 Capacity Manager allows you to export all hourly capacity data to Amazon S3 in Parquet format (optimized for analytics). From there, Amazon Athena can query directly on S3 using standard SQL without requiring ETL or a separate data warehouse. The great thing is that Athena uses Partition Projection to automatically recognize new data when Capacity Manager exports on a schedule, eliminating the need to manually run metadata update commands each time new data arrives.

### What Can Be Analyzed

Once configured, you can run queries to identify which reservations are wasting the most budget, view average utilization rates by instance type, discover hourly utilization patterns to understand when workloads peak, or compare capacity distribution across Regions and Availability Zones. All of this is based on real-world data stored long-term on S3, free from the 90-day limitation of the Console.

### Conclusion

This is a highly practical pattern for controlling EC2 costs at an enterprise scale, especially when multiple accounts and teams share capacity reservations. Instead of waiting until the end of the month to look at the invoice, you can proactively detect wasteful reservations and make timely adjustments. If you want to scale this further, the article also suggests integrating this data with EventBridge Scheduler for automated periodic refreshes, or combining it with BI tools like Amazon QuickSight for a more visual dashboard.

Original article link for your reference:
https://aws.amazon.com/blogs/compute/maximize-amazon-ec2-capacity-reservation-utilization-using-amazon-athena/
![](/images/3-BlogsPosted/blog3.jpg)