# RiskPilot

License: MIT  
Languages: Python, Node.js, Next.js, TypeScript, React, FastAPI  
Frameworks: FastAPI, Next.js, Tailwind CSS, Lucide React

---

## Table of Contents

- [About](#about)
- [Core Mission](#core-mission)
- [Key Capabilities](#key-capabilities)
- [Target Users](#target-users)
- [Demo Video](#demo-video)
- [Core Features & User Value](#core-features--user-value)
- [Example Workflows](#example-workflows)
- [Use Cases](#use-cases)
- [Tech Stack](#tech-stack)
- [Support](#support)

---

## About

**RiskPilot** is an AI-powered threat modeling and security risk analysis platform. It enables organizations to quickly identify, visualize, and manage security threats in applications and cloud environments. Upload system diagrams and architecture details to instantly receive actionable threat models, risk scores, vulnerability mappings (OWASP Top 10), compliance status, and AI-generated remediation advice. RiskPilot provides a seamless dashboard and REST API for enterprise security management.

---

## Core Mission

Our mission is to make security risk analysis simple, automated, and actionable for all—from engineering to compliance. RiskPilot bridges the gap between identifying risks and resolving them, integrating with your SDLC to deliver automated threat modeling, real-time vulnerability tracking, compliance mapping, and guided remediation. The platform empowers teams to move from security discovery to rapid resolution, enabling secure innovation at scale.

---

## Key Capabilities

- **Automated Threat Modeling**  
- **Compliance Tracking**  
- **LLM Security Scanning**  
- **Risk Dashboards and Visualizations**  
- **Status Management**  
- **REST APIs for Integration**

---

## Target Users

- **Security Engineers:** Automate threat modeling, risk scoring, and compliance checks.
- **DevOps & Developers:** Integrate risk analysis into CI/CD, shift security left.
- **Compliance & Audit Teams:** Access up-to-date mapping to standards and compliance status.
- **Product & Cloud Architects:** Design more secure architectures with instant feedback.

---

## Demo Video

🎥 *Coming soon!* — RiskPilot walkthrough.

---

## Core Features & User Value

### 1. Automated Threat Modeling

**How it works:**  
- Upload a Data Flow Diagram (DFD) and enter architecture details.  
- RiskPilot uses STRIDE/DREAD and OWASP Top 10 to generate a comprehensive threat model.
- Each threat is scored and mapped to affected assets and attack vectors.

**Value for Users:**  
- **Security Engineers:** Rapid, repeatable threat models for new systems or after every architectural change.
- **Developers & DevOps:** Early detection of security risks before deployment; integrate with CI/CD for continuous insight.
- **Architects:** Objective, comprehensive analysis for design and review phases.

**Sample API Usage:**
```bash
curl -X POST http://localhost:8000/create/normal_system/pre_upload \
  -F "image_file=@/path/to/your_dfd.png"
curl -X POST http://localhost:8000/create/normal_system \
  -H "Content-Type: application/json" \
  -d '{ ... system details ... }'
```
**Sample Dashboard Output:**  
- Threat summary cards, unresolved/resolved counts, OWASP Top 10 mapping, risk heatmaps.

---

### 2. Compliance Tracking

**How it works:**  
- RiskPilot analyzes discovered threats in the context of major frameworks (ISO 27001, PCI DSS, NIST, SOC2, GDPR).
- Maps each threat to specific compliance controls.
- Provides dashboards and reports on compliance posture and violation status.

**Value for Users:**  
- **Compliance & Audit Teams:** Automated compliance mapping and violation tracking with audit-ready summaries.
- **Security/Engineering:** Understand which threats impact compliance and how to prioritize remediation.
- **Leadership:** Get real-time visibility into compliance posture across projects.

**Sample Dashboard Output:**  
- Compliance heatmaps, control violation lists, exportable reports.

---

### 3. LLM Security Scanning

**How it works:**  
- Scan LLM (Large Language Model) integrations for prompt injection, supply chain, and AI-specific risks.
- Run custom probes against deployed models and services.
- Visualize unique attack paths for GenAI/LLM-based features.

**Value for Users:**  
- **AI/ML Teams:** Secure LLM deployments and prevent model abuse.
- **Security/DevOps:** Integrate AI risk scanning into existing and new products.
- **Product Managers:** Confidence in the security of AI-powered features.

**Sample API Usage:**
```bash
curl -X POST http://localhost:8000/create/llm_scan \
  -H "Content-Type: application/json" \
  -d '{ "provider": "OpenAI", "model": "gpt-4", "probes": ["ansiescape"] }'
curl http://localhost:8000/fetch/llm_scan/3
```
**Sample Dashboard Output:**  
- LLM vulnerability lists, severity ratings, remediation advice, attack trees.

---

## Example Workflows

**Workflow 1: Threat Model a New Application**  
1. Upload DFD and system details.
2. Review the instant threat model (risks, OWASP mapping, compliance links).
3. Take action on remediation and compliance guidance.
4. Track threat and compliance resolution over time.

**Workflow 2: LLM Security Scan**  
1. Submit LLM provider/model for scanning.
2. Monitor scan and review vulnerabilities.
3. Apply recommendations to mitigate risks.

---

## Use Cases

- **Security Architecture Reviews:** Automated and updatable threat models for new or evolving systems.
- **Continuous Compliance:** Maintain and demonstrate compliance with ISO, PCI, NIST, SOC2, GDPR.
- **DevSecOps Integration:** Automated risk analysis and compliance in CI/CD.
- **GenAI/LLM Security:** Address emerging threats in AI-powered features.
- **Executive Dashboards:** Real-time risk, compliance, and remediation status for leadership.

---

## Tech Stack

- **Backend:** Python (FastAPI), JWT Auth, REST API
- **Frontend:** Next.js (TypeScript), Tailwind CSS, Lucide React
- **Database:** Configurable (e.g., SQLite/Postgres)
- **AI Analysis:** Integrations for LLM/AI-powered analysis

---

## Support

- 📧 Email: [nikhil@cyberultron.com](mailto:nikhil@cyberultron.com)

---

**RiskPilot** — Making threat modeling and risk management simple, automated, and actionable.

All rights reserved. This software and its documentation are the intellectual property of CyberUltron Consulting Private Limited.
