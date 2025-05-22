Gen AI Powered Web Security Engine

This repository provides a FastAPI-based API for web security, focusing on Web Application Firewall (WAF) and anomaly detection capabilities:

ShieldNet: Detects suspicious HTTP requests using a BERT-based classifier and generates WAF rules.

PulseSense: Detects anomalous behavior using Isolation Forest and generates alert rules.


📦 Modules

1. 🛡️ ShieldNet (WAF)

The ShieldNet module processes incoming HTTP request data to detect suspicious patterns such as XSS, SQL injection, path traversal, and errors using a fine-tuned bert-base-uncased model. If a suspicious pattern is detected, it generates a WAF rule to block the request.
![WAF_Bert](https://github.com/user-attachments/assets/019baeef-af17-4399-80de-d93981ec8f3d)




A diagram showing the flow from Client → FastAPI Server → Text Preprocessing → BERT Classifier (ShieldNet) → Rule Generation → GPT-4.0-turbo → Response]






2. 🚨 PulseSense (Anomaly Detection)

The PulseSense module detects anomalous behavior in HTTP requests using a fine-tuned bert-base-uncased model and Isolation Forest . It generates alert rules for monitoring.

![Anomoly](https://github.com/user-attachments/assets/f662b48f-3c53-4e2c-b281-82a4ca11cc73)





A diagram showing the flow from Client → FastAPI Server → Text Preprocessing → Isolation Forest (PulseSense) → Rule Generation → GPT-4.0-turbo → Response]






