# The Voice Vault

**The Voice Vault** is a low-difficulty, serverless AWS project that automatically converts study notes (text files) into audio files (mini podcasts) using Amazon Polly.

The goal of this project is to demonstrate how cloud-native, event-driven architectures can be used to automate real-world workflows.

<img width="982" height="461" alt="image" src="https://github.com/user-attachments/assets/78a3acdf-6a4a-4975-90da-1cb8834024a3" />



---

## 📌 Project Goal

> Turn written study notes into audio podcasts automatically.

### What happens:
1. A text file is uploaded
2. The system automatically converts it into speech
3. The audio file is stored and ready to listen

---

## 🧠 Architecture Overview

**Services Used:**
- Amazon S3 – Storage
- AWS Lambda – Serverless compute
- Amazon Polly – Text-to-Speech
- AWS IAM – Permissions
- Amazon CloudWatch – Logging & monitoring



The audio file is automatically created using Amazon Polly and stored in the output S3 bucket.

---

## ⚙️ How It Works (Step-by-Step)

1. User uploads a `.txt` file to the input S3 bucket
2. Amazon S3 triggers an AWS Lambda function
3. Lambda reads the text file
4. Lambda sends the text to Amazon Polly
5. Polly converts the text into speech (MP3)
6. Lambda stores the MP3 file in the output S3 bucket
7. Logs are captured in Amazon CloudWatch

---

## 🔐 IAM Permissions

The Lambda execution role includes the following permissions:
- Read objects from S3
- Write objects to S3
- Use Amazon Polly
- Write logs to CloudWatch

(Policies are included in the `iam/` folder.)

---

## 🧪 How to Run This Project

1. Create two S3 buckets:
   - `voice-vault-input-bucket`
   - `voice-vault-output-bucket`

2. Create an IAM role for Lambda with:
   - AmazonS3FullAccess
   - AmazonPollyFullAccess
   - AWSLambdaBasicExecutionRole

3. Create a Lambda function using Python 3.12

4. Paste the Lambda code from:

5. Add an S3 trigger on the input bucket

6. Upload `Globalservices.txt` to the input bucket

7. Check the output bucket for `Globalservices.mp3`

---

## 📊 Logging & Monitoring

- All execution logs are available in **Amazon CloudWatch**
- Errors such as permission issues or invalid files are logged for debugging

---

## 🚀 Future Enhancements

- Support `.docx` and `.pdf` files
- Add an API using Amazon API Gateway
- Add a web UI for uploading notes
- Store metadata in DynamoDB
- Add SSML support for better narration

---

## Resume Description

> Built a serverless AWS application that converts text-based study notes into audio podcasts using S3, Lambda, and Amazon Polly. Implemented event-driven automation, IAM permissions, and logging with CloudWatch.


Note: This project is for learning and demonstration purposes.



