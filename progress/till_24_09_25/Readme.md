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
- [Core Features & Value](#core-features--value)
- [Example Workflows](#example-workflows)
- [Use Cases](#use-cases)
- [Tech Stack](#tech-stack)
- [Support](#support)

---

## About

**RiskPilot** is an AI-powered threat modeling and security risk analysis platform. It enables organizations and development teams to rapidly identify, visualize, and manage security threats in their applications and cloud architectures. By uploading system diagrams and describing technical details, users get actionable threat models, risk scores, vulnerability mappings (OWASP Top 10), compliance status, and AI-generated remediation advice—all in a modern dashboard interface or via REST API.

---

## Core Mission

Our mission is to make security risk analysis simple, automated, and actionable for all—from engineering to compliance. RiskPilot closes the gap between identifying risks and resolving them, integrating with your SDLC to deliver automated threat modeling, real-time vulnerability tracking, compliance mapping, and guided remediation. The platform empowers teams to move from security discovery to rapid resolution, enabling secure innovation at scale.

---

## Key Capabilities

- **Automated Threat Modeling:** Generate comprehensive threat models (STRIDE/DREAD scoring, OWASP Top 10 mapping) from Data Flow Diagrams (DFDs) and architectural data.
- **Compliance Tracking:** Map threats to industry frameworks (ISO 27001, PCI DSS, NIST, SOC 2, GDPR) and highlight compliance violations.
- **AI-Powered Remediation:** Get clear, actionable fixes and compliance recommendations for every threat.
- **Risk Dashboards:** Visualizations including heatmaps, metrics cards, attack tree diagrams (PASTA/MAESTRO).
- **LLM Security Scanning:** Specialized jobs for Large Language Model (LLM) integrations, including vulnerability checks and attack surface analysis.
- **Status Management:** Track threat and compliance resolution over time.
- **Developer-Friendly APIs:** REST endpoints for system integration and automation.

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

## Core Features & Value

### 1. Automated Threat Modeling

**What it does:**  
- Accepts Data Flow Diagrams (DFDs) and detailed architecture input.
- Uses STRIDE/DREAD and OWASP Top 10 methodologies to generate instant threat models.
- Assigns risk scores, tracks resolved/unresolved threats, and visualizes attack surfaces.

**Value for End Users:**  
- *Security Engineers*: Fast, repeatable threat models for every system iteration.
- *Developers/DevOps*: Immediate visibility into risks before deployment; integrate with CI/CD.
- *Architects*: Objective, comprehensive security analysis for design decisions.

**Sample API Usage:**
```bash
curl -X POST http://localhost:8000/create/normal_system/pre_upload \
  -F "image_file=@/path/to/your_dfd.png"
curl -X POST http://localhost:8000/create/normal_system \
  -H "Content-Type: application/json" \
  -d '{ ... system details ... }'
```
**Sample Dashboard Output:**  
- Threat summary cards
- Unresolved/resolved threat counts
- OWASP Top 10 vulnerabilities mapped to your architecture

---

### 2. Compliance Tracking & Mapping

**What it does:**  
- Analyzes the threat landscape against industry standards (ISO, PCI, NIST, SOC2, GDPR).
- Maps discovered threats to specific compliance requirements.
- Tracks compliance status and generates audit-ready summaries.

**Value for End Users:**  
- *Compliance Officers*: Automated compliance posture and violation reports.
- *Security/Engineering*: Know exactly which threats impact compliance and why.
- *Leadership*: Real-time organizational compliance dashboard.

**Sample Dashboard Output:**  
- Compliance heatmaps
- Violation lists mapped to control IDs
- Exportable compliance summaries

---

### 3. LLM Security Scanning

**What it does:**  
- Scans LLM integrations for prompt injection, misuse, and supply chain risks.
- Runs custom probes against AI/GenAI features and tracks LLM-specific threats.
- Visualizes potential attack paths unique to LLM use cases.

**Value for End Users:**  
- *AI/ML Teams*: Secure LLM deployment and prevent model abuse.
- *Security/DevOps*: Integrate AI risk scanning into new and existing products.
- *Product Managers*: Confidence in the security of AI-powered features.

**Sample API Usage:**
```bash
curl -X POST http://localhost:8000/create/llm_scan \
  -H "Content-Type: application/json" \
  -d '{ "provider": "OpenAI", "model": "gpt-4", "probes": ["ansiescape"] }'
curl http://localhost:8000/fetch/llm_scan/3
```
**Sample Dashboard Output:**  
- LLM vulnerability lists with severity
- Remediation advice for each detected risk
- Attack tree diagrams for LLM threat paths

---

## Example Workflows

**Workflow 1: Threat Model a New Application**  
1. Upload DFD and system details via API or dashboard.
2. Review instant threat model (risks, OWASP, compliance mapping).
3. Act on remediation and compliance guidance.
4. Update threat statuses as issues are addressed.

**Workflow 2: LLM Security Scan**  
1. Submit LLM provider/model for risk scanning.
2. Monitor scan status and review vulnerabilities.
3. Apply AI-generated recommendations to mitigate risks.

---

## Use Cases

- **Security Architecture Reviews:** Generate and update threat models for new or changing systems.
- **Continuous Compliance:** Maintain and demonstrate compliance with ISO, PCI, NIST, SOC2, GDPR.
- **DevSecOps Integration:** Automate risk analysis and compliance assessment in CI/CD.
- **GenAI/LLM Security:** Proactively address emerging threats in AI-powered features.
- **Executive Dashboards:** Provide leadership with real-time risk, compliance, and remediation status.

---

## Tech Stack

- **Backend:** Python (FastAPI), JWT Auth, REST API.
- **Frontend:** Next.js (TypeScript), Tailwind CSS, Lucide React.
- **UI Components:** React, TypeScript, Tailwind CSS, Lucide React.
- **AI Analysis:** (Supports integration points for LLM/AI-powered analysis.)
- **Database:** (Configurable; e.g., SQLite/Postgres for backend storage.)

---

## Support

- 📧 Email: [nikhil@cyberultron.com](mailto:nikhil@cyberultron.com)

---

**RiskPilot** — Making threat modeling and risk management simple, automated, and actionable.

All rights reserved. This software and its documentation are the intellectual property of CyberUltron Consulting Private Limited.
