Gen AI Powered Web Security Engine

This repository provides a FastAPI-based API for web security, focusing on Web Application Firewall (WAF) and anomaly detection capabilities:

ShieldNet: Detects suspicious HTTP requests using a BERT-based classifier and generates WAF rules.
PulseSense: Detects anomalous behavior using Isolation Forest and generates alert rules.

The system processes HTTP request logs using a fine-tuned bert-base-uncased model for classification and leverages GPT-3.5-turbo to summarize the generated security rules.

📦 Modules

1. 🛡️ ShieldNet (WAF)

The ShieldNet module processes incoming HTTP request data to detect suspicious patterns such as XSS, SQL injection, path traversal, and errors using a fine-tuned bert-base-uncased model. If a suspicious pattern is detected, it generates a WAF rule to block the request.
![WAF-BERT](https://github.com/user-attachments/assets/c4723a92-23a0-4500-b030-f72ae711833b)



A diagram showing the flow from Client → FastAPI Server → Text Preprocessing → BERT Classifier (ShieldNet) → Rule Generation → GPT-4.0-turbo → Response]






2. 🚨 PulseSense (Anomaly Detection)

The PulseSense module detects anomalous behavior in HTTP requests using a fine-tuned bert-base-uncased model and Isolation Forest . It generates alert rules for monitoring.

![Anomaly](https://github.com/user-attachments/assets/036411c6-f3ef-433a-9769-9089e508f1fd)



A diagram showing the flow from Client → FastAPI Server → Text Preprocessing → Isolation Forest (PulseSense) → Rule Generation → GPT-4.0-turbo → Response]






