---
title : "Tạo CloudFront Distribution"
date: 2025-07-09 
weight : 1 
chapter : false
pre : " <b> 3.2.1 </b> "
---
## Tạo CloudFront Distribution và cấu hình _Distribution
1. Tạo CloudFront Distribution
- Truy cập vào _AWS Console_
- Tìm _CloudFront_ trên giao diện hoặc thanh tìm kiếm 
- Chọn _CloudFront_
![Cloud](/images/3.connect/20-code.png)
2. Trong giao diện _CloudFront_, chọn _Create distribution_
![Cloud](/images/3.connect/21-code.png)
-  Trong giao diện _Create distribution_
- _Distribution name_: nhập ```fashion-store-web```
- Sau đó chọn _Next_
![Cloud](/images/3.connect/22-code.png)
![Cloud](/images/3.connect/23-code.png)
- Ở bước này, chọn _Amazon S3_ 
![Cloud](/images/3.connect/24-code.png)
- Lướt xuống phần _Origin_chọn browse S3 và chọn tên S3 mình tạo
- rồi bấm Next
![Cloud](/images/3.connect/25-code.png)
![Cloud](/images/3.connect/26-code.png)
- xong nó sẽ hiện phần Step 3 chọn phần Do not enable security protections rồi bấm next 
![Cloud](/images/3.connect/27-code.png)
- ra phần Step 4 khi đó ta rewiew lại toàn bộ sau đó bấm **create distribution**
![Cloud](/images/3.connect/28-code.png)
![Cloud](/images/3.connect/29-code.png)
- sau khi xong thì bấm edit ngay đó 
![Cloud](/images/3.connect/30-code.png)
- ngay ở phần Default root object - optional ghi ngay đó index.html rồi bấm save changes
![Cloud](/images/3.connect/31-code.png)
- ngay sau khi xong thì chờ deploying 
![Cloud](/images/3.connect/32-code.png)
- sau khi xong thì bấm vào đường link này có ở phần Distribution domain name sau khi Last modified xong
![Cloud](/images/3.connect/33-code.png)
![Cloud](/images/3.connect/34-code.png)