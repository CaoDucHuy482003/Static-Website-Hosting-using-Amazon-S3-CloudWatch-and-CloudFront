---
title : "Tải dữ liệu và cấu hình"
date: 2025-07-09 
weight : 2
chapter : false
pre : " <b> 3.1.2 </b> "
---
## Tải dữ liệu  



- Hiện tại chúng ta chưa có _object_ nào
![S3](/images/3.connect/08-code.png)
- Chúng ta cần ta cần tải source giao diện lên S3
- *Lưu ý*: hãy sửa lại đường dẫn tùy theo đường vị trí dẫn đến folder giao diện của bạn hoặc chỉnh bằng tay khi thêm các file hoặc folder
![S3](/images/3.connect/09-code.png)
## Cấu hình  
- Chọn _permission_ trong _bucket_, lướt xuống phần _bucket policy_ chọn _edit_. 
![S3](/images/3.connect/10-code.png)
- Sau đó cấu hình cho S3
```
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "PublicReadGetObject",
            "Effect": "Allow",
            "Principal": "*",
            "Action": "s3:GetObject",
            "Resource": "arn:aws:s3:::fashion-store-web/*"
        }
    ]
}
```
- Sau đó chọn _save changes_
![S3](/images/3.connect/11-code.png)
- lưu ý phải nhớ ở phần code ở phần package.json nhớ thêm phần ``` "homepage": "http://fashion-store-web.s3-website-ap-southeast-1.amazonaws.com", ```
![S3](/images/3.connect/12-code.png)
- Tiếp theo, bạn chọn vào _Properties_, lướt xuống phần _Static website hosting_ chọn edit
![S3](/images/3.connect/13-code.png)
- Chọn _enable_
![S3](/images/3.connect/15-code.png)
- _Index document_ nhập index.html
- _Error document_ nhập 404.html ( lưu ý error sẽ phụ thuộc vào web của bạn để là gì có thể vẫn là index.html hoặc 404.html)
- Sau đó nhấn _Save change_
![S3](/images/3.connect/14-code.png)
![S3](/images/3.connect/16-code.png)
- Trong phần _Static website hosting_ có phần _Bucket website endpoint_, bạn sẽ nhận được đường dẫn đến giao diện tĩnh của bạn
![S3](/images/3.connect/17-code.png)
- sau khi thành công thì có sẽ có link ```http://fashion-store-web.s3-website-ap-southeast-1.amazonaws.com ```
nhấn vào đường link đó sẽ vào thẳng web
![S3](/images/3.connect/18-code.png)
![S3](/images/3.connect/19-code.png)