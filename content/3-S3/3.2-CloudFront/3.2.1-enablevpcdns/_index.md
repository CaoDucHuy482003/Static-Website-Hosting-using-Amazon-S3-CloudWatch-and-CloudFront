---
title : "Create CloudFront Distribution"
date: 2025-07-09 
weight : 1 
chapter : false
pre : " <b> 3.2.1 </b> "
---
## Create CloudFront Distribution and configure Distribution
1. Create CloudFront Distribution
- Go to the _AWS Console_
- Search for _CloudFront_ in the interface or search bar
- Select _CloudFront_
![Cloud](/images/3.connect/20-code.png)
2. In the _CloudFront_ interface, select _Create distribution_
![Cloud](/images/3.connect/21-code.png)
- In the _Create distribution_ interface
- _Distribution name_: enter ```fashion-store-web```
- Then select _Next_
![Cloud](/images/3.connect/22-code.png)
![Cloud](/images/3.connect/23-code.png)
- At this step, select _Amazon S3_ 
![Cloud](/images/3.connect/24-code.png)
- Scroll down to the _Origin_ section, click browse S3 and select the S3 bucket you created
- Then click Next
![Cloud](/images/3.connect/25-code.png)
![Cloud](/images/3.connect/26-code.png)
- In Step 3, select _Do not enable security protections_ and click next
![Cloud](/images/3.connect/27-code.png)
- In Step 4, review everything and then click **create distribution**
![Cloud](/images/3.connect/28-code.png)
![Cloud](/images/3.connect/29-code.png)
- After finishing, click edit right there
![Cloud](/images/3.connect/30-code.png)
- In the _Default root object - optional_ section, enter index.html and click save changes
![Cloud](/images/3.connect/31-code.png)
- After that, wait for deploying
![Cloud](/images/3.connect/32-code.png)
- When done, click the link in the Distribution domain name section after Last modified
![Cloud](/images/3.connect/33-code.png)
![Cloud](/images/3.connect/34-code.png)