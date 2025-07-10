---
title : "Distribute UI via CloudFront"
date: 2025-07-09 
weight : 3 
chapter : false
pre : " <b> 3.2. </b> "
---
## Introduction to Amazon CloudFront

- **Amazon CloudFront** is a **Content Delivery Network (CDN)** provided by AWS, optimized for performance and security.
  - Distributes content through hundreds of global **Edge Locations**.
  - Reduces latency and accelerates delivery by serving content from locations close to end users.

- **Content Support**
  - Static content: HTML, CSS, JS, images, video.
  - Dynamic content: supports conditional caching and features like:
    - HTTP/2
    - TLS 1.3
    - WebSocket

- **Integration with AWS services**
  - Amazon S3
  - Amazon CloudWatch
  - Amazon CloudFront
  
- **Security features**
  - Geo-restriction and Signed URLs/Cookies for access control.
  - Integration with AWS WAF to filter malicious traffic.
  - DDoS protection with AWS Shield Standard.

- **Scalability and customization**
  - Supports custom headers.
  - Automatically scales with traffic.
  - Suitable for applications with high requirements for:
    - Performance
    - Availability
    - Security