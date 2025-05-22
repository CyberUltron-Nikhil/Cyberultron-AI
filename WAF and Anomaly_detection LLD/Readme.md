Gen AI Powered Web Security Engine

This repository provides a FastAPI-based API for web security, focusing on Web Application Firewall (WAF) and anomaly detection capabilities:

ShieldNet: Detects suspicious HTTP requests using a BERT-based classifier and generates WAF rules.

PulseSense: Detects anomalous behavior using Isolation Forest and generates alert rules.


📦 Modules

1. 🛡️ ShieldNet (WAF)

The ShieldNet module processes incoming HTTP request data to detect suspicious patterns such as XSS, SQL injection, path traversal, and errors using a WAF model. If a suspicious pattern is detected, it generates a WAF rule to block the request.
![BERT-WAF](https://github.com/user-attachments/assets/722eaf33-7ed3-41dc-b145-be1228225936)





A diagram showing the flow from Client → FastAPI Server → Text Preprocessing → BERT Classifier (ShieldNet) → Rule Generation → GPT-4.0-turbo → Response]






2. 🚨 PulseSense (Anomaly Detection)

The PulseSense module detects anomalous behavior in HTTP requests using a fine-tuned WAF model and Isolation Forest . It generates alert rules for monitoring.

![ISOLATION-ANOMALY](https://github.com/user-attachments/assets/29d4de01-7585-4d55-af7b-3870100d2aea)






A diagram showing the flow from Client → FastAPI Server → Text Preprocessing → Isolation Forest (PulseSense) → Rule Generation → GPT-4.0-turbo → Response]






