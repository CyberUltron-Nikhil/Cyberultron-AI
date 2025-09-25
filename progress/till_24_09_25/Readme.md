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
- [Feature Deep Dives](#feature-deep-dives)
  - [1. Threat Modeling of Normal Systems](#1-threat-modeling-of-normal-systems)
  - [2. LLM Vulnerability Testing](#2-llm-vulnerability-testing)
  - [3. MCP Server Vulnerability Scanning](#3-mcp-server-vulnerability-scanning)
- [Example Workflows](#example-workflows)
- [Use Cases](#use-cases)
- [Tech Stack](#tech-stack)
- [Support](#support)

---

## About

**RiskPilot** is an AI-powered platform for holistic threat modeling and vulnerability management. It empowers organizations to identify, visualize, and manage risks across classic applications, GenAI/LLM integrations, and codebases managed through MCP servers. RiskPilot brings together system diagram analysis, LLM security probing, and advanced vulnerability scanning, providing actionable risk scores, compliance insights, and AI-driven remediation guidance, all within a unified dashboard.

---

## Core Mission

To make enterprise security risk analysis simple, automated, and actionable—no matter the technology stack. RiskPilot bridges the gap between identifying, understanding, and remediating risks, integrating with your SDLC to deliver automated threat modeling, vulnerability analytics, compliance mapping, and guided remediation. The platform enables teams to accelerate secure innovation with confidence.

---

## Key Capabilities

- **Automated Threat Modeling for Normal Systems**
- **LLM (Large Language Model) Vulnerability Testing**
- **MCP Server-Based Vulnerability Scanning**
- **Compliance Tracking & Mapping**
- **Unified Risk Dashboards & Visualizations**

---

## Target Users

- **Security Engineers:** Automate threat modeling, vulnerability scanning, and compliance.
- **Developers & DevOps:** Integrate risk analysis into CI/CD, shift security left.
- **AI/ML & Product Teams:** Secure and validate LLM/GenAI features.
- **Compliance & Audit:** Map vulnerabilities to frameworks and track remediation.
- **Cloud & Solution Architects:** Design secure architectures with instant, actionable feedback.

---

## Demo Video

🎥 *Coming soon!* — RiskPilot walkthrough.

---

## Feature Deep Dives

### 1. Threat Modeling of Normal Systems

#### In-Depth Explanation

RiskPilot enables comprehensive threat modeling for traditional and modern application architectures. By analyzing uploaded data flow diagrams (DFDs) and detailed system architecture, it applies security frameworks such as STRIDE, DREAD, and OWASP Top 10 to automatically identify, categorize, and prioritize threats. The platform provides contextual risk scoring, highlights potential attack surfaces, and maps vulnerabilities to compliance requirements.

**Value to End Users:**
- **Security Engineers:** Automate and scale the creation and maintenance of threat models, reducing manual effort and human error.
- **Developers & DevOps:** Gain early visibility into security risks, enabling proactive remediation before deployment and smoother security reviews.
- **Architects:** Validate new designs and proposed changes to system architecture with instant feedback on potential security implications.
- **Compliance Teams:** Ensure that every threat is mapped to corresponding compliance controls, streamlining audit preparation.

---

### 2. LLM Vulnerability Testing

#### In-Depth Explanation

RiskPilot provides a specialized security assessment module for applications leveraging Large Language Models (LLMs) and GenAI. It evaluates integrations for risks such as prompt injection, data leakage, unintended behaviors, and supply chain exposures unique to AI-driven features. The system uses advanced probes and heuristic analysis to surface vulnerabilities and provides prioritized remediation recommendations. All findings are contextualized within broader application risk and compliance posture.

**Value to End Users:**
- **AI/ML & Product Teams:** Validate the security of LLM-powered features against both known and emerging threat vectors, reducing time-to-market for secure AI.
- **Security Engineers:** Integrate LLM risk analysis into enterprise security dashboards, ensuring that GenAI risks are not siloed or overlooked.
- **Compliance Teams:** Monitor privacy and AI governance requirements, and ensure that LLM features comply with data protection and regulatory standards.
- **Leadership:** Gain confidence in responsible AI adoption and risk management at scale.

---

### 3. MCP Server Vulnerability Scanning

#### In-Depth Explanation

RiskPilot’s MCP Server Vulnerability Scanning feature is designed for environments that use Managed Compute Platform (MCP) servers and source code repositories. When triggered, RiskPilot temporarily clones the selected MCP server repository and scans it for vulnerability patterns using [Semgrep](https://semgrep.dev), a leading open-source static analysis tool. The platform identifies weaknesses, secrets, and insecure patterns within the code.

Once the initial scan is complete (Phase 1), each finding is analyzed by a Large Language Model (LLM), which generates clear explanations and actionable fixes tailored to your code and context. In Phase 2, RiskPilot further processes each finding to provide detailed mappings:  
- Each vulnerability is mapped to the relevant OWASP category.
- Associated compliance controls are flagged, showing which compliance requirements (e.g., ISO 27001, PCI DSS, NIST, SOC2, GDPR) are affected for every issue.

All results are visualized in the unified dashboard, enabling teams to triage, assign, and resolve findings efficiently.

**Value to End Users:**
- **DevOps & Infrastructure Teams:** Receive comprehensive reports on workload risks, insecure configurations, and exposed secrets directly mapped to MCP environments and codebases, with actionable guidance.
- **Security Engineers:** Orchestrate vulnerability management across all MCP-managed repositories, focusing on the most critical findings and leveraging LLM explanations for rapid triage.
- **Compliance & Audit:** Monitor for regulatory and policy violations at a granular, per-finding level and produce detailed, compliance-ready evidence for audits.
- **Cloud & Solution Architects:** Make informed decisions on workload placement and architecture, guided by real-time risk and compliance visibility.

---

## Example Workflows

- **Threat Modeling Workflow:** Upload system diagrams and architecture details, review the generated threat model, prioritize and assign remediation, and track resolution and compliance mapping over time.
- **LLM Security Workflow:** Register LLM/GenAI features for security assessment, receive prioritized vulnerability reports and remediation actions, and monitor ongoing risk as models and integrations evolve.
- **MCP Vulnerability Workflow:** Trigger a scan for MCP-hosted repositories, review findings and LLM explanations, analyze OWASP/compliance mapping for each issue, assign remediations, and produce compliance-ready reports.

---

## Use Cases

- **Security Architecture Reviews:** Automated, updatable threat models for new or evolving systems.
- **Continuous Compliance:** Track and demonstrate compliance with ISO, PCI, NIST, SOC2, GDPR.
- **DevSecOps Integration:** Automated risk and compliance analysis in CI/CD.
- **GenAI/LLM Security:** Proactive testing and monitoring for AI-powered features.
- **MCP Workload Security:** Centralized vulnerability and compliance management for MCP environments.

---

## Tech Stack

- **Backend:** Python (FastAPI), JWT Auth, REST API
- **Frontend:** Next.js (TypeScript), Tailwind CSS, Lucide React
- **Database:** Configurable (e.g., SQLite/Postgres)
- **AI Analysis:** Integrations for LLM/AI-powered analysis
- **MCP Integration:** Semgrep-based scanning for MCP code repositories

---

## Support

- 📧 Email: [nikhil@cyberultron.com](mailto:nikhil@cyberultron.com)

---

**RiskPilot** — Unified, automated threat modeling and vulnerability management for the next generation of enterprise security.

All rights reserved. This software and its documentation are the intellectual property of CyberUltron Consulting Private Limited.
