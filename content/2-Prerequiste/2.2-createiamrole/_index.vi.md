---
title: "Xây dựng và triển khai giao diện người dùng"
date: 2025-07-09
weight: 2
chapter: false
pre: " <b> 2.2 </b> "
---

Sau khi hoàn tất việc xây dựng backend serverless, bước tiếp theo là xây dựng và triển khai giao diện người dùng với React.

---
## Các bước chuẩn bị
## 🖥️ Kiến trúc giao diện

Giao diện người dùng sẽ là một ứng dụng React đơn trang , được **build tĩnh và lưu trữ trên S3**, phân phối qua **CloudFront**, Phân phối qua **CloudWatch**.

---

## 🧰 Công cụ và tài nguyên cần chuẩn bị

### 1. Công cụ phát triển
- Node.js >= 18
- npm hoặc yarn
- React + React DOM
- Visual Studio Code (VS Code)

### 2. Tài nguyên AWS cần thiết
- S3 bucket (hosting static website)
- CloudFront 
- CloudWatch

### 3. Build giao diện
- Sau khi xây dựng xong giao diện
```bash
npm run build
```
- Sau khi chạy lệnh, source giao diện của bạn sẽ đóng gói lại thành file _build_, bạn sẽ sử dụng file này cho bước tiếp theo
![S3](/images/2.prerequisite/01-code2.2.png)
