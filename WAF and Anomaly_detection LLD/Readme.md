Gen AI Powered Web Security Engine

This repository provides a FastAPI-based API for web security, focusing on Application Firewall and anomaly detection capabilities:

ShieldNet: Detects suspicious HTTP requests using a BERT-based classifier and generates Fire wall rules.

PulseSense: Detects anomalous behavior using Isolation Forest and generates alert rules.


📦 Modules

1. 🛡️ ShieldNet (Application Fire wall)

The ShieldNet module processes incoming HTTP request data to detect suspicious patterns such as XSS, SQL injection, path traversal, and errors using a Fire wall model. If a suspicious pattern is detected, it generates rules to block the request.
![Fire Wall ](https://github.com/user-attachments/assets/93044cf4-806c-4f6a-94d1-94a85ee8de31)





A diagram showing the flow from Client → FastAPI Server → Text Preprocessing → BERT Classifier (ShieldNet) → Rule Generation → GPT-4.0-turbo → Response]






2. 🚨 PulseSense (Anomaly Detection)

The PulseSense module detects anomalous behavior in HTTP requests using a fine-tuned Fire wall model and Isolation Forest . It generates alert rules for monitoring.
![AnomalyDetection](https://github.com/user-attachments/assets/4f61130a-821f-407c-a865-f5a6a072266e)







A diagram showing the flow from Client → FastAPI Server → Text Preprocessing → Isolation Forest (PulseSense) → Rule Generation → GPT-4.0-turbo → Response]






