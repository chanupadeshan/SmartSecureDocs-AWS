# SmartSecureDocs-AWS

An **AI-powered document access control system** built with AWS.  
This system allows users to upload confidential documents (PDFs/JPGs), automatically extract text, classify sensitivity, apply PII masking, and enable role-based access and secure Q&A via chatbot.

---

## 🚀 Features

- 📤 Upload confidential documents to **Amazon S3**
- 🧾 Extract text using **Amazon Textract**
- 🧠 Classify sensitivity & detect entities using **Amazon Comprehend**
- 🔒 Detect and mask **PII** (emails, IDs, names)
- 👥 Control access using **Cognito user roles** (admin, HR, employee)
- 💬 Interact with documents using a **chatbot interface** (Bedrock or LangChain)
- 📊 Track and store metadata in **Amazon DynamoDB**

---

## 🛠️ Tech Stack

| Component        | Service/Tool              |
|------------------|---------------------------|
| Storage          | Amazon S3                 |
| OCR              | Amazon Textract           |
| NLP & Sentiment  | Amazon Comprehend         |
| User Auth        | Amazon Cognito            |
| Access Logic     | AWS Lambda + API Gateway  |
| Data Store       | Amazon DynamoDB           |
| Chatbot          | Amazon Bedrock / LangChain|
| Frontend         | HTML,CSS                  |

---

## 📂 Project Structure

```bash
SmartSecureDocs-AWS/
├── lambda/
│   ├── textractHandler.py
│   ├── comprehendHandler.py
│   └── utils/
├── frontend/ (HTML + CSS)
│   ├── index.html
│   ├── styles.css
│   └── scripts/
│       └── app.js
├── docs/
│   └── screenshots/
├── README.md
└── architecture-diagram.png


---

## 🧩 Project Phases

### ✅ Phase 1: Setup
- [ ] Create S3 bucket
- [ ] Create DynamoDB table
- [ ] Create IAM Role for Lambda
- [ ] Set up Cognito User Pool and user groups (admin, hr, employee)

### ⚙️ Phase 2: Document Upload + Textract
- [ ] Create Lambda function triggered by S3
- [ ] Use Amazon Textract to extract content
- [ ] Store raw text in DynamoDB or S3

### 🔍 Phase 3: NLP & PII Masking
- [ ] Use Comprehend to analyze text and classify sensitivity
- [ ] Detect and mask PII using regex or Macie
- [ ] Save masked version in S3/DynamoDB

### 🔐 Phase 4: Role-Based Access
- [ ] Use Cognito group-based access control
- [ ] API Gateway + Lambda to serve masked/unmasked based on role

### 🤖 Phase 5: Chatbot Interface
- [ ] Convert text to embeddings
- [ ] Use LangChain or Bedrock for Q&A chatbot
- [ ] Role-based filtered answers

### 📊 Phase 6: Dashboard + Logs (Optional)
- [ ] Create admin dashboard (React)
- [ ] Show uploaded docs, status, access logs