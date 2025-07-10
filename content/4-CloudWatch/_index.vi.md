---
title : "Giới thiệu CloudWatch"
date: 2025-05-25 
weight : 4 
chapter : false
pre : " <b> 4. </b> "
---


Amazon CloudWatch là một dịch vụ giám sát và quan sát hệ thống do AWS cung cấp, cho phép thu thập, theo dõi và phân tích các log, chỉ số hiệu suất (metrics), và sự kiện từ các tài nguyên AWS cũng như ứng dụng chạy trên nền tảng đám mây hoặc tại chỗ. Với CloudWatch, người dùng có thể dễ dàng theo dõi tình trạng hoạt động của hệ thống, thiết lập cảnh báo (alarm) khi có sự cố hoặc vượt ngưỡng, và trực quan hóa dữ liệu thời gian thực thông qua dashboard. 

CloudWatch đóng vai trò quan trọng trong việc đảm bảo hiệu suất, phát hiện lỗi nhanh chóng và hỗ trợ vận hành hệ thống hiệu quả, đặc biệt trong các kiến trúc serverless hoặc microservices như sử dụng AWS Lambda, API Gateway, EC2, và ECS.

- Lợi ích khi sử dụng CloudWatch

  + Theo dõi hệ thống real-time

  + Tự động cảnh báo khi có sự cố

  + Giảm thời gian phát hiện lỗi

  + Hỗ trợ debug nhanh qua log

  + Dễ tích hợp vào hệ thống CI/CD và serverless