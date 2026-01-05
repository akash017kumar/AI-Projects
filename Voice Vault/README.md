# The Voice Vault

**The Voice Vault** is a low-difficulty, serverless AWS project that automatically converts study notes (text files) into audio files (mini podcasts) using Amazon Polly.

The goal of this project is to demonstrate how cloud-native, event-driven architectures can be used to automate real-world workflows.

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



