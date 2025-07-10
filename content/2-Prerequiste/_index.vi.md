---
title : "Các bước chuẩn bị"
date: 2025-07-09 
weight : 2 
chapter : false
pre : " <b> 2. </b> "
---
## 1. Yêu cầu hệ thống

- JavaScript ES6 trở lên
- Node.js >= 16
- AWS CLI
- AWS Account với quyền tạo dịch vụ , CloudWatch, CloudFont, S3
- IDE: Visual Studio Code (hoặc editor bạn thích)

## 2. Cài đặt công cụ cần thiết

### Cài AWS CLI

#### macOS
```bash
brew install awscli
```
#### Windows
Tải từ AWS CLI
Cấu hình AWS CLI
```bash
aws configure
```
Nhập:
Access key, secret key
Region: ap-southeast-1
Format: json
Cài Node.js & npm
macOS
```bash
brew install node
```
Ubuntu
```bash
sudo apt update
sudo apt install awscli -y
```
Cài Serverless Framework
```bash
npm install -g serverless
```
Tạo SDK cho JavaScript v3
```bash
npm install @aws-sdk/client-s3 
            @aws-sdk/client-cloudfront 
            @aws-sdk/client-cloudwatch-logs
```
