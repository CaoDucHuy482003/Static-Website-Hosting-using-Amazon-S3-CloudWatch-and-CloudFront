---
title : "Upload Data and Configuration"
date: 2025-07-09 
weight : 2
chapter : false
pre : " <b> 3.1.2 </b> "
---
## Upload Data  

- Currently, we do not have any _objects_
![S3](/images/3.connect/08-code.png)
- We need to upload the UI source to S3
- *Note*: Please adjust the path according to your UI folder location or manually add files/folders as needed
![S3](/images/3.connect/09-code.png)

## Configuration  
- Select _permission_ in the _bucket_, scroll down to the _bucket policy_ section and select _edit_.
![S3](/images/3.connect/10-code.png)
- Then configure S3 as follows:
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
- Then select _save changes_
![S3](/images/3.connect/11-code.png)
- Note: In your package.json, remember to add ``` "homepage": "http://fashion-store-web.s3-website-ap-southeast-1.amazonaws.com", ```
![S3](/images/3.connect/12-code.png)
- Next, go to _Properties_, scroll down to _Static website hosting_ and select edit
![S3](/images/3.connect/13-code.png)
- Select _enable_
![S3](/images/3.connect/15-code.png)
- _Index document_: enter index.html
- _Error document_: enter 404.html (note: the error document depends on your web, it can be index.html or 404.html)
- Then click _Save change_
![S3](/images/3.connect/14-code.png)
![S3](/images/3.connect/16-code.png)
- In the _Static website hosting_ section, there is a _Bucket website endpoint_, you will get the link to your static UI
![S3](/images/3.connect/17-code.png)
- After success, you will have a link like ```http://fashion-store-web.s3-website-ap-southeast-1.amazonaws.com ```
Click that link to access your website
![S3](/images/3.connect/18-code.png)
![S3](/images/3.connect/19-code.png)
