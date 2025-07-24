# SmartSecureDocs-AWS

An **AI-powered document access control system** built with AWS.  
This system allows users to upload confidential documents (PDFs/JPGs), automatically extract text, classify sensitivity, apply PII masking, and enable role-based access and secure Q&A via chatbot.

---

**Note:**  
This is a self-study project designed to help me gain hands-on experience with core AWS services including S3 buckets, DynamoDB, IAM roles, Cognito, and Lambda. Through building SmartSecureDocs-AWS, I aim to deepen my practical understanding of cloud architecture, security, and serverless workflows—turning theory into real-world skills.

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

```

---

## 🧩 Project Roadmap

| Phase | Description |
|-------|-------------|
| **✅ Phase 1: Setup** | - Create S3 bucket<br>- Create DynamoDB table<br>- Create IAM role for Lambda<br>- Set up Cognito user pool & groups (admin, HR, employee) |
| **⚙️ Phase 2: Upload & Textract** | - Implement S3-triggered Lambda function<br>- Extract text using Textract<br>- Store raw text in S3 or DynamoDB |
| **🔍 Phase 3: NLP & PII Masking** | - Classify sensitivity with Comprehend<br>- Mask PII using regex or Macie<br>- Save masked document version |
| **🔐 Phase 4: Role-Based Access** | - Configure Cognito group-based access<br>- Use API Gateway + Lambda to serve masked/unmasked content |
| **🤖 Phase 5: Chatbot Interface** | - Convert text to embeddings<br>- Integrate Bedrock or LangChain for Q&A<br>- Filter answers by user role |
| **📊 Phase 6 : Dashboard & Logs** | - Build  admin dashboard<br>- Display uploads, status, and access logs |

