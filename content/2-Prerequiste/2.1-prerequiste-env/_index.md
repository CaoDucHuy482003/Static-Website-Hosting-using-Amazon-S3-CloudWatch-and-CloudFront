---
---
title: "Preparing the Fashion Store WebApp Development Environment"
date: 2025-07-09
weight: 1
chapter: false
pre: "<b> 2.1 </b>"
---

In this step, we will prepare the environment to develop and deploy an e-commerce application using **ReactJS + TailwindCSS** for the frontend, and deploy to AWS using **S3**, **CloudFront**, and **CloudWatch**. The goal is to create a convenient, modern development environment that supports real user activity monitoring.

---

## 🧩 Architecture Overview

The **Fashion Store WebApp** application is divided into two main parts:

- **Static frontend** (ReactJS) is built and stored on **Amazon S3**
- Global distribution via **Amazon CloudFront**
- Access, error, and system activity monitoring with **AWS CloudWatch**

---

## 🧰 Required Tools

### 1. Tools to install on your machine

- **Node.js >= 16**
- **npm >= 8**
- **Visual Studio Code** or any code editor
- **AWS CLI**
- **AWS Account**

---

## 🗂 Create ReactJS Project Structure

The standard project structure has been initialized with `create-react-app` and the folders are as follows:

```plaintext
FASHION_STORE_WEBAPP-MAIN/
├── public/                     
├── src/                        
│   ├── components/             
│   │   ├── admin/              
│   │   ├── auth/               
│   │   ├── cart/               
│   │   └── product/            
│   ├── context/                
│   ├── pages/                  
│   ├── services/               
│   ├── utils/                  
├── App.js                      
├── App.css                     
├── index.js                    
├── index.css                   
├── tailwind.config.js          
├── postcss.config.js           
├── package.json                
└── README.md        
```

### 2. Write IAM permission code for CRUD operations
- IAM configuration:
```bash
 iam:
    role:
      statements:
        - Effect: Allow
          Action:
            - dynamodb:PutItem
            - dynamodb:GetItem
            - dynamodb:UpdateItem
            - dynamodb:DeleteItem
            - dynamodb:Scan
            - dynamodb:Query
          Resource: 
            - arn:aws:dynamodb:ap-southeast-1:*:table/ProductsTable
            
```


### 3. API configuration
- API Gateway configuration
- Protect API with API Key:
```bash
apiGateway:
    apiKeySourceType: HEADER
    apiKeys:
      - name: ProductApiKey-${sls:stage}
        description: "API Key for Product App"
        enabled: true
    usagePlan:
      throttle:
        rateLimit: 100
        burstLimit: 50
      quota:
        limit: 1000
        period: MONTH
```