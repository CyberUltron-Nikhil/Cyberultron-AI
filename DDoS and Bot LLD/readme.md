# 🛡️ Gen AI powered API Security Engine

This repository provides two independent Flask-based APIs for network security:

- **DDoS Sentry**: Detects DDoS attacks and generates mitigation rules.
- **Bot Sentry**: Detects bad bot traffic and generates mitigation rules.

Each module processes network logs, uses a lightweight transformer (DistilBERT) for classification, and utilizes GPT-4o to generate appropriate security rules.

---

## 📦 Modules

### 1. 🚨 DDoS Sentry

The **DDoS Sentry** module processes incoming network log data and determines whether a **DDoS attack** is occurring. If an attack is detected, it uses a GPT-4o-based rule generator to produce mitigation strategies.

#### 🖼️ Flowchart

<img src="./DDoS Sentry.jpg" width="600" />

#### ⚙️ Flow Explanation

1. **Client sends POST request**  
   - A network log dataset is sent via a POST request to the DDoS Agent API.

2. **Flask API Server receives the request**  
   - The API extracts network log data from the request body.

3. **Preprocessing and Tokenization module**  
   - The network logs are cleaned and tokenized into a structured format.
   - Global traffic characteristics may also be derived.

4. **Traffic Classifier (DistilBERT Sequence Classifier)**  
   - A fine-tuned DistilBERT model analyzes the logs and classifies the traffic.

5. **DDoS Attack Detected?**  
   - If the classifier detects a DDoS attack, proceed to the next step.
   - Otherwise, respond with `"Allow"`.

6. **DDoS Mitigation Rule Generator (GPT-4o)**  
   - If an attack is detected, GPT-4o is used to generate mitigation rules.

7. **Return JSON Response**  
   - A JSON response is returned to the client, containing the generated rule(s).

---

### 2. 🤖 Bot Sentry

The **Bot Sentry** module is responsible for detecting and mitigating bad bot activity. It follows a very similar architecture to the DDoS Sentry, with bot-specific logic and rule generation.

#### 🖼️ Flowchart

<img src="./Bot Sentry.jpg" width="600" />

#### ⚙️ Flow Explanation

1. **Client sends POST request**  
   - A network log dataset is sent via a POST request to the Bot Agents API.

2. **Flask API Server receives the request**  
   - Network log data is extracted from the request body.

3. **Preprocessing and Tokenization module**  
   - The logs are cleaned and tokenized.
   - Global traffic characteristics may also be considered.

4. **Traffic Classifier (DistilBERT Sequence Classifier)**  
   - A DistilBERT model classifies whether the logs indicate bot traffic.

5. **Bad Bot Attack Detected?**  
   - If no bot activity is detected, return a response: `"Allow"`.
   - If bot activity is detected, proceed to rule generation.

6. **Bad Bot Mitigation Rule Generator (GPT-4o)**  
   - GPT-4o generates one or more mitigation rules based on the classified log data.

7. **Return JSON Response**  
   - The generated rules are returned to the client in a structured JSON format.

---

## 🧰 Technologies Used

| Component               | Description                        |
|------------------------|------------------------------------|
| **Flask**              | REST API Server                    |
| **DistilBERT**         | Lightweight transformer classifier |
| **GPT-4o**             | Rule generation based on logs      |
| **JSON**               | Input/output data format           |

---
