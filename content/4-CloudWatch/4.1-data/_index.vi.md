---
title : "CloudWatch"
date: 2025-05-25 
weight : 1 
chapter : false
pre : " <b> 4.1 </b> "
---

##  Tạo CloudWatch 
- thì cần tạo Bucket S3 mới 
![CloudWatch](/images/4.S3/01-code.png)
- sau đó bấm vào create bucket
![CloudWatch](/images/4.S3/02-code.png)
- ở phần Bucket name để tên là ```cf-logs-fashion-store```
![CloudWatch](/images/4.S3/03-code.png)
- rồi ở phần Block Public Access settings for this bucket bỏ giấu tích và tích vào phần I acknowledge 
![CloudWatch](/images/4.S3/04-code.png)
- tiếp theo bấm phần create bucket 
![CloudWatch](/images/4.S3/05-code.png)
- sau khi đăng ký thành công sẽ hiện dòng ```cf-logs-fashion-store```
![CloudWatch](/images/4.S3/06-code.png)
- sau khi xong thì vào thành tìm kiếm vào phần CloudFront chọn cái phần tạo gần nhất
![CloudWatch](/images/4.S3/07-code.png)
![CloudWatch](/images/4.S3/08-code.png)
- sau khi vào thì bấm vào phần logging rồi chọn Create a log delivery
![CloudWatch](/images/4.S3/09-code.png)
- sau khi create vào ở phần destinaltion S3 bucket ```cf-logs-fashion-store``` mới tạo rồi bấm summit
![CloudWatch](/images/4.S3/10-code.png)`
- quay lại S3 rồi nhập vào ```cf-logs-fashion-store```đợi 7-20p (tùy vào thời điểm người truy cập)
- sau khi ấn vào sẽ hiện một thư mục AWSLogs/ 495599754297/CloudFront/E2MP7VDLOFYRL8.2025-07-09-19.910b6082.gz
![CloudWatch](/images/4.S3/11-code.png)`
- sau đó ta có 2 lựa chọn 1 là tải về rồi bật notepad hoặc vs code lên để kiểm tra 2 là có phần thời gian có sẵn về lần đăng nhập cuối                 
![CloudWatch](/images/4.S3/13-code.png)`