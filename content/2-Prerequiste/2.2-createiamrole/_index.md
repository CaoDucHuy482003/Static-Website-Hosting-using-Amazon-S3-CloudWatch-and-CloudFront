---
---
title: "Build and Deploy the User Interface"
date: 2025-07-09
weight: 2
chapter: false
pre: " <b> 2.2 </b> "
---

After completing the serverless backend, the next step is to build and deploy the user interface with React.

---
## Preparation Steps
## 🖥️ UI Architecture

The user interface will be a single-page React application, **built statically and stored on S3**, distributed via **CloudFront**, and monitored via **CloudWatch**.

---

## 🧰 Required Tools and Resources

### 1. Development Tools
- Node.js >= 18
- npm or yarn
- React + React DOM
- Visual Studio Code (VS Code)

### 2. Required AWS Resources
- S3 bucket (for hosting static website)
- CloudFront
- CloudWatch

### 3. Build the UI
- After building the UI, run:
```bash
npm run build
```
- After running the command, your UI source will be packaged into the _build_ folder, which you will use for the next step.
![S3](/images/2.prerequisite/01-code2.2.png)