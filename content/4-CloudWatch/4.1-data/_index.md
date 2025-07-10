---
title : "CloudWatch"
date: 2025-05-25 
weight : 1 
chapter : false
pre : " <b> 4.1 </b> "
---

## Create CloudWatch
- First, create a new S3 Bucket
![CloudWatch](/images/4.S3/01-code.png)
- Then click create bucket
![CloudWatch](/images/4.S3/02-code.png)
- In the Bucket name field, enter ```cf-logs-fashion-store```
![CloudWatch](/images/4.S3/03-code.png)
- In the Block Public Access settings for this bucket, uncheck the box and check the I acknowledge box
![CloudWatch](/images/4.S3/04-code.png)
- Next, click create bucket
![CloudWatch](/images/4.S3/05-code.png)
- After successful registration, you will see the line ```cf-logs-fashion-store```
![CloudWatch](/images/4.S3/06-code.png)
- Then, in the search bar, go to CloudFront and select the most recently created distribution
![CloudWatch](/images/4.S3/07-code.png)
![CloudWatch](/images/4.S3/08-code.png)
- In the distribution, go to logging and select Create a log delivery
![CloudWatch](/images/4.S3/09-code.png)
- When creating, in the destination S3 bucket, select the newly created ```cf-logs-fashion-store``` and click submit
![CloudWatch](/images/4.S3/10-code.png)
- Go back to S3 and open ```cf-logs-fashion-store```, wait 7-20 minutes (depending on access time)
- When you open it, you will see a folder AWSLogs/495599754297/CloudFront/E2MP7VDLOFYRL8.2025-07-09-19.910b6082.gz
![CloudWatch](/images/4.S3/11-code.png)
- Then you have two options: 1) download and open with notepad or VS Code to check, or 2) use the available time information for the last login
![CloudWatch](/images/4.S3/13-code.png)