Gen AI Powered Web Security Engine

This repository provides a FastAPI-based API for web security, focusing on Web Application Firewall (WAF) and anomaly detection capabilities:

ShieldNet: Detects suspicious HTTP requests using a BERT-based classifier and generates WAF rules.
PulseSense: Detects anomalous behavior using a BERT-based classifier and generates alert rules.

The system processes HTTP request logs using a fine-tuned bert-base-uncased model for classification and leverages GPT-3.5-turbo to summarize the generated security rules.

📦 Modules

1. 🛡️ ShieldNet (WAF)

The ShieldNet module processes incoming HTTP request data to detect suspicious patterns such as XSS, SQL injection, path traversal, and errors using a fine-tuned bert-base-uncased model. If a suspicious pattern is detected, it generates a WAF rule to block the request.
![WAF](https://github.com/user-attachments/assets/2d0e275b-c8e9-4eb0-b867-30008c45abe4)

A diagram showing the flow from Client → FastAPI Server → Text Preprocessing → BERT Classifier (ShieldNet) → Rule Generation → GPT-4.0-turbo → Response]

⚙️ Flow Explanation

Client sends POST request
An HTTP request log is sent via a POST request to the /predict/ endpoint (e.g., {"http_request": "ERROR 404: PAGE NOT FOUND"}).

FastAPI Server receives the request
The API extracts the http_request field from the request body.

Preprocessing and Tokenization module
The HTTP request string is tokenized using the BERT tokenizer (bert-base-uncased), converting the text into a format suitable for the model (e.g., token IDs, attention masks).

Traffic Classifier (BERT Sequence Classifier)
A fine-tuned bert-base-uncased model analyzes the tokenized request and classifies it as "Suspicious" or "Normal".
The model outputs a probability score for the "Suspicious" class (e.g., 0.9 for "ERROR 404: PAGE NOT FOUND").

Suspicious Pattern Detected?
If the probability of "Suspicious" exceeds a threshold (e.g., 0.5), proceed to rule generation.
If not, set shieldnet: 0 and skip to the response step.

WAF Rule Generator
Based on the classification and logits from BERT, ShieldNet generates a WAF rule (e.g., {"type": "WAF Rule", "rule_name": "Error Page Not Found", "action": "Block", "place_at": "Last"}).
The rule name is determined by analyzing the request context (e.g., presence of ERROR suggests an error-related rule).

Proceed to Anomaly Detection
The request is also passed to PulseSense for anomaly detection (see below).

Rule Summary Generator (GPT-4.0-turbo)
GPT-4.0-turbo generates a summary of the rules (e.g., "The rules include a WAF Rule to block an error page not found issue...").

Return JSON Response
A JSON response is returned to the client, containing shieldnet, pulsesense, the generated rules, and the summary.


2. 🚨 PulseSense (Anomaly Detection)

The PulseSense module detects anomalous behavior in HTTP requests using a fine-tuned bert-base-uncased model. It generates alert rules for monitoring.
![Anomaly_Detection](https://github.com/user-attachments/assets/78b17b6b-c447-42ea-9b99-95b0e8e0e7d7)

A diagram showing the flow from Client → FastAPI Server → Text Preprocessing → BERT Classifier (PulseSense) → Rule Generation → GPT-4.0-turbo → Response]

⚙️ Flow Explanation

Client sends POST request
An HTTP request log is sent via a POST request to the /predict/ endpoint (same as ShieldNet).

FastAPI Server receives the request
The API extracts the http_request field from the request body.

Preprocessing and Tokenization module
The HTTP request string is tokenized using the BERT tokenizer (bert-base-uncased), shared with ShieldNet.

Anomaly Classifier (BERT Sequence Classifier)
A fine-tuned bert-base-uncased model (separate from ShieldNet’s model) classifies the request as "Anomalous" or "Normal".
The model outputs a probability score for the "Anomalous" class (e.g., 0.7 for "ERROR 404: PAGE NOT FOUND").

Anomaly Detected?
If the probability of "Anomalous" exceeds a threshold (e.g., 0.5), or if ShieldNet detected a suspicious pattern (shieldnet: 1), set pulsesense: -1 and proceed to rule generation.
If not, set pulsesense: 1.

Anomaly Rule Generator
If an anomaly is detected, PulseSense generates an anomaly rule (e.g., {"type": "Anomaly Detection Rule", "rule_name": "Unusual Behavior", "action": "Alert"}).

Rule Summary Generator (GPT-4.0-turbo)
GPT-4.0-turbo generates a summary of all rules (shared with ShieldNet).

Return JSON Response
The response includes shieldnet, pulsesense, the combined rules from ShieldNet and PulseSense, and the summary.



