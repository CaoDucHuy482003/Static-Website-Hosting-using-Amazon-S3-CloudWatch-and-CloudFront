+++
title = "Clean up resources"
date = 2021
weight = 5
chapter = false
pre = "<b>5. </b>"
+++

We will follow these steps to delete the resources we created in this lab.

#### Delete S3

1. Go to [S3 service management console]
  + Click **delete** (first empty the bucket by clicking Empty bucket, then click permanently delete)
  + After deleting, click on fashion-store-web and then delete bucket
  + Do the same for cf-logs-fashion-store

2. Go to [CloudFront service management console]
  + Click on the created distribution, then click Disable. A notification will appear, click Disable.
  + Wait 30 seconds to 2 minutes for the service to be disabled and wait for Disabled status to appear to complete
  ![Delete](/images/5.fwd/01-code.png)