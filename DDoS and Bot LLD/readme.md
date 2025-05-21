# 🛡️ Gen AI powered API Security Engine

This repository provides two independent Flask-based APIs for network security:

- **DDoS Sentry**: Detects DDoS attacks and generates mitigation rules.
- **Bot Sentry**: Detects bad bot traffic and generates mitigation rules.

Each module processes network logs, uses a lightweight finetuned deep learning model for classification, and utilizes LLMs to generate appropriate security rules.

---

## 📦 Modules

### 1. 🚨 DDoS Sentry

The **DDoS Sentry** module processes incoming network log data and determines whether a **DDoS attack** is occurring. If an attack is detected, it uses an LLM rule generator to produce mitigation strategies.

#### 🖼️ LLD

<img src="./DDoS Sentry.jpg" width="600" />



### 2. 🤖 Bot Sentry

The **Bot Sentry** module is responsible for detecting and mitigating bad bot activity. It follows a very similar architecture to the DDoS Sentry, with bot-specific logic and rule generation.

#### 🖼️ LLD

<img src="./Bot Sentry.jpg" width="600" />

