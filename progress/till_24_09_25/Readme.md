# RiskPilot

**License:** MIT  
**Languages:** Python, Node.js, Next.js, TypeScript, React  
**Frameworks:** FastAPI, Next.js, TailwindCSS, Lucide React

---

## Table of Contents

- [About](#about)
- [Core Mission](#core-mission)
- [Key Capabilities](#key-capabilities)
- [Target Users](#target-users)
- [Demo Video](#demo-video)
- [Features](#features)
- [Example Workflows](#example-workflows)
- [Use Cases](#use-cases)
- [Tech Stack](#tech-stack)
- [Quick Start](#quick-start)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Access](#access)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
- [Contributing](#contributing)
- [Support](#support)
- [Get Involved](#get-involved)

---

## About

**RiskPilot** is a full-stack, AI-powered platform for automated threat modeling and risk analysis. It enables teams to upload system diagrams, describe architecture, and instantly receive a comprehensive security assessment. RiskPilot maps threats, vulnerabilities, and compliance issues, and provides actionable remediation guidance, making security management efficient and proactive.

---

## Core Mission

Our mission is to **bridge the gap between identifying security threats and remediating them**, automating the process of risk analysis, compliance checks, and threat modeling. RiskPilot empowers developers and security professionals to understand and address security risks earlier and more effectively in the software lifecycle.

---

## Key Capabilities

- **Automated Threat Modeling:** Upload DFDs, describe your system, and get a full threat model (STRIDE, DREAD scoring, OWASP Top 10 mapping).
- **Compliance Tracking:** Maps threats to standards like ISO 27001, PCI DSS, NIST, SOC 2, and GDPR.
- **Risk Heatmaps & Dashboards:** Visualize threats, risk scores, and vulnerabilities.
- **Remediation Guidance:** AI-generated fixes and compliance recommendations.
- **LLM Security Scanning:** Analyze risks in large language model integrations.
- **Modern Web UI:** Interactive, responsive dashboard for security management.

---

## Target Users

- **Security Engineers:** Streamline threat analysis and compliance.
- **DevOps & Developers:** Integrate risk analysis into CI/CD and system design.
- **Compliance Officers:** Automated mapping to compliance frameworks.
- **Product Teams:** Assess and monitor risk throughout system evolution.

---

## Demo Video

🎥 *Coming soon* — See RiskPilot in action!

---

## Features

| Feature                | Description                                                | Benefits                                      |
|------------------------|------------------------------------------------------------|------------------------------------------------|
| 🔍 Threat Modeling     | Upload DFDs, describe architecture, generate threat models | Rapid, automated, and repeatable threat analysis |
| 🛡️ Compliance Tracking | Maps threats to compliance standards                       | Simplifies audits and reporting                |
| 📊 Dashboard           | Visualize risks, vulnerabilities, and compliance           | Real-time, actionable insights                 |
| 🤖 AI Remediation      | Automated fix recommendations for each threat              | Accelerates resolution and reduces expertise barrier |
| 🧩 LLM Scanning        | Analyze LLM integrations for risks                         | Secure AI-powered features                     |
| 🔄 Status Management   | Track threat status (Resolved/Unresolved)                  | Focus on active risk                           |
| 📁 Bulk Operations     | Manage multiple systems and threats at scale               | Enterprise-ready scalability                   |

---

## Example Workflows

### Workflow 1: Secure a New Application

1. **Upload DFD:** POST `/create/normal_system/pre_upload` with your system's Data Flow Diagram.
2. **Describe System:** Submit system details (architecture, dependencies, auth) via `/create/normal_system`.
3. **Analyze Risks:** View dashboard for risk scores, STRIDE/DREAD analysis, OWASP mapping, and compliance.
4. **Remediate:** Follow AI-generated fixes and compliance advice.
5. **Track:** Update threat statuses and monitor risk over time.

### Workflow 2: LLM Security Scan

1. **Submit LLM Model/Provider:** POST `/create/llm_scan` with provider and probes.
2. **Monitor Scan Status:** Poll `/fetch/llm_scan/{id}` for job status.
3. **Review Results:** Access vulnerabilities, risk scores, and suggested remediations.

---

## Use Cases

- **Architecture Risk Reviews:** Instantly model threats for new or evolving systems.
- **Compliance Readiness:** Map your system's risks to ISO, PCI, NIST, SOC2, GDPR, etc.
- **DevSecOps Integration:** Integrate threat modeling into CI/CD pipelines.
- **AI/LLM Security:** Assess risks unique to LLM and AI integrations.
- **Security Dashboards:** Give leadership and teams clear, up-to-date risk views.

---

## Tech Stack

- **Backend:** Python (FastAPI), JWT Auth, REST API
- **Frontend:** Next.js (TypeScript), Tailwind CSS, Lucide React
- **Components:** React, TypeScript, Tailwind UI
- **AI:** (Optional) Integrations for automated analysis and remediation
- **Database:** (configurable, e.g., SQLite, Postgres)

---

## Quick Start

### Docker Deployment (Recommended)

1. **Backend**
    ```bash
    cd backend
    docker build -t riskpilot-backend .
    docker run -p 8000:8000 riskpilot-backend
    ```

2. **Frontend**
    ```bash
    cd frontend
    npm install
    npm run dev
    ```

### Local Installation

See [Installation](#installation) for step-by-step instructions.

---

## Prerequisites

- **Python**: 3.8+
- **Node.js**: 18+
- **npm**: 8+
- **Git**
- **Modern browser**: Chrome, Firefox, Edge, or Safari

---

## Installation

1. **Clone Repo**
    ```bash
    git clone https://github.com/CyberUltron-Nikhil/RiskPilot.git
    cd RiskPilot
    ```

2. **Backend Setup**
    ```bash
    cd backend
    python -m venv venv
    source venv/bin/activate  # or venv\Scripts\activate on Windows
    pip install -r requirements.txt
    python -m backend.main
    ```

3. **Frontend Setup**
    ```bash
    cd ../frontend
    npm install
    npm run dev
    ```

---

## Access

- **Frontend URL:** http://localhost:3000
- **Backend API:** http://localhost:8000

---

## Usage

- **Register/Login:** Authenticate and access the dashboard.
- **Upload DFD:** Start a new threat model.
- **Input System Details:** Describe your architecture.
- **Review Risks:** Analyze risks, compliance, and remediation.
- **Manage Threats:** Resolve and update threat statuses.

---

## API Endpoints

Below are key endpoints (see backend API docs for full list):

- `GET /` — Health check
- `POST /send_code` — Email verification for signup
- `POST /signup` — User registration
- `POST /login` — User authentication
- `POST /create/normal_system/pre_upload` — Upload DFD image
- `POST /create/normal_system` — Create threat model
- `GET /fetch/normal_system/list` — List all threat models
- `GET /fetch/normal_system/{id}` — Get specific threat model results
- `POST /edit/normal_system/threat/{project_id}/{threat_id}` — Update threat status
- `DELETE /delete/normal_system/{id}` — Delete threat model

---

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit changes (`git commit -m 'Add amazing feature'`)
4. Push to branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---

## Support

- 🐛 Issues: [GitHub Issues](https://github.com/CyberUltron-Nikhil/RiskPilot/issues)
- 📧 Email: [nikhil@cyberultron.com](mailto:nikhil@cyberultron.com)

---

## Get Involved

- 💬 Start or join discussions
- 🐛 Report bugs and vulnerabilities
- ⭐ Request features and improvements
- 💻 Contribute code or documentation

---

**RiskPilot — Proactive, Automated Threat Modeling & Security Risk Management.**

All rights reserved. This software and its documentation are the intellectual property of CyberUltron Consulting Private Limited.
