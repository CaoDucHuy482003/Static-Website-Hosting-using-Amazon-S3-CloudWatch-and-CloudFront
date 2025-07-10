---
title : "Preparation Steps"
date: 2025-07-09
weight : 2
chapter : false
pre : " <b> 2. </b> "
---
## 1. System Requirements

- JavaScript ES6 or later
- Node.js >= 16
- AWS CLI
- AWS Account with permissions to create services, CloudWatch, CloudFront, S3
- IDE: Visual Studio Code (or your preferred editor)

## 2. Install Required Tools

### Install AWS CLI

#### macOS
```bash
brew install awscli
```
#### Windows
Download from AWS CLI
Configure AWS CLI
```bash
aws configure
```
Enter:
Access key, secret key
Region: ap-southeast-1
Format: json

Install Node.js & npm
macOS
```bash
brew install node
```
Ubuntu
```bash
sudo apt update
sudo apt install awscli -y
```

Install Serverless Framework
```bash
npm install -g serverless
```

Install AWS SDK for JavaScript v3
```bash
npm install @aws-sdk/client-s3 \
            @aws-sdk/client-cloudfront \
            @aws-sdk/client-cloudwatch-logs
```