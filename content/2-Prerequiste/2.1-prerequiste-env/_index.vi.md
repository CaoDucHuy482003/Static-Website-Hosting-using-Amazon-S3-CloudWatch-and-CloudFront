---
title: "Chuẩn bị môi trường phát triển WebApp bán hàng thời trang"
date: 2025-07-09
weight: 1
chapter: false
pre: "<b> 2.1 </b>"
---

Trong bước này, chúng ta sẽ chuẩn bị môi trường để phát triển và triển khai một ứng dụng thương mại điện tử sử dụng **ReactJS + TailwindCSS** cho frontend, và triển khai lên AWS sử dụng các dịch vụ **S3**, **CloudFront** và **CloudWatch**. Mục tiêu là tạo một môi trường phát triển thuận tiện, hiện đại, hỗ trợ theo dõi hoạt động thực tế của người dùng.

---

## 🧩 Kiến trúc tổng quan

Ứng dụng **Fashion Store WebApp** được chia thành hai phần chính:

- **Frontend tĩnh** (ReactJS) được build và lưu trữ trên **Amazon S3**
- Phân phối toàn cầu thông qua **Amazon CloudFront**
- Giám sát truy cập, lỗi, và hoạt động hệ thống bằng **AWS CloudWatch**

---

## 🧰 Các công cụ cần thiết

### 1. Công cụ cài đặt trên máy

- **Node.js >= 16**
- **npm >= 8**
- **Visual Studio Code** hoặc bất kỳ trình soạn thảo nào
- **AWS CLI**
- **AWS Account**


---
### 1. Công cụ cài đặt trên máy

## 🗂 Tạo cấu trúc dự án ReactJS

Cấu trúc dự án chuẩn đã được khởi tạo với `create-react-app` và thư mục như sau:

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

### 2. Viết mã nguồn cấp quyền để thực hiện các thao tác CRUD
- Cấu hình IAM:
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


### 3. Viết lại cấu hình API 
- Cấu hình API Gateway
- Cấu hình bảo vệ API bằng API Key:
```bash
apiGateway:
    apiKeySourceType: HEADER
    apiKeys:
      - name: ProductApiKey-${sls:stage}
        description: "API Key cho Product App"
        enabled: true
    usagePlan:
      throttle:
        rateLimit: 100
        burstLimit: 50
      quota:
        limit: 1000
        period: MONTH
```





           
 