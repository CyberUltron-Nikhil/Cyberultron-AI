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

**RiskPilot** is an AI-powered platform for holistic threat modeling and vulnerability management. It empowers organizations to identify, visualize, and manage risks across classic applications, GenAI/LLM integrations, and codebases managed through MCP servers. RiskPilot brings together system diagram analysis, LLM security probing, and automated codebase scanning, providing actionable risk scores, compliance insights, and AI-driven remediation guidance, all within a unified dashboard and API.

---

## Core Mission

To make enterprise security risk analysis simple, automated, and actionable—no matter the technology stack. RiskPilot bridges the gap between identifying, understanding, and remediating risks, integrating with your SDLC to deliver automated threat modeling, vulnerability analytics, compliance mapping, and guided remediation. The platform enables teams to accelerate secure innovation with confidence.

---

## Key Capabilities

- **Automated Threat Modeling for Normal Systems**
- **LLM (Large Language Model) Vulnerability Testing**
- **MCP Server-Based Codebase Vulnerability Scanning**
- **Compliance Tracking & Mapping**
- **Unified Risk Dashboards & Visualizations**
- **REST APIs for Integration & Automation**

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

#### What It Does

- Accepts Data Flow Diagrams (DFDs) and detailed system architecture inputs (technology stack, authentication, sensitive data, etc.).
- Runs automated threat modeling using STRIDE, DREAD, and OWASP Top 10 methodologies.
- Identifies and scores threats, maps them to the affected components, and highlights both resolved and unresolved vulnerabilities.
- Visualizes attack surfaces, produces risk heatmaps, and aligns findings with compliance frameworks.

#### End-User Value

- **Security Engineers:**  
  - Save time by automating comprehensive threat models for each release and infrastructure change.
  - Focus reviews on the highest-risk threats thanks to risk scoring and prioritization.
  - Maintain consistent documentation for audit and compliance processes.

- **Developers & DevOps:**  
  - Integrate threat modeling into CI/CD pipelines and PR reviews.
  - Detect issues before code reaches production or cloud environments.
  - Receive actionable, context-specific remediation suggestions.

- **Cloud & Solution Architects:**  
  - Experiment with architectural changes and instantly see security implications.
  - Ensure new designs meet both security and compliance requirements.
  - Gain visual feedback (attack trees, heatmaps) for technical and non-technical audiences.

#### Typical User Workflow

1. **Upload DFD** and enter system details via dashboard or API.
2. **Automatic threat model generation:** STRIDE/DREAD/OWASP analysis, risk scoring.
3. **Review results:** Threat cards, risk scores, compliance mapping, and detailed vulnerability list.
4. **Take action:** Assign, track, and resolve issues; download compliance-ready reports.

#### Example API Usage

```bash
curl -X POST http://localhost:8000/create/normal_system/pre_upload \
  -F "image_file=@/path/to/your_dfd.png"
curl -X POST http://localhost:8000/create/normal_system \
  -H "Content-Type: application/json" \
  -d '{ ... system details ... }'
curl http://localhost:8000/fetch/normal_system/2
```

---

### 2. LLM Vulnerability Testing

#### What It Does

- Enables security analysis of LLM (Large Language Model) and GenAI integrations.
- Performs automated probing for LLM-specific risks: prompt injection, output manipulation, data leakage, supply chain vulnerabilities, and model abuse.
- Assigns risk scores to each finding and generates actionable remediation advice.
- Visualizes LLM attack vectors and context-specific compliance risks (e.g., data privacy, misuse).

#### End-User Value

- **AI/ML & Product Teams:**  
  - Test LLMs for prompt injection, output hijacks, data exposure, and more before and after deployment.
  - Validate that GenAI-powered features meet security/privacy standards.
  - Continuously monitor for new, emerging threats in the LLM threat landscape.

- **Security Engineers:**  
  - Integrate LLM scanning into broader threat modeling and security dashboards.
  - Automate GenAI security validation for every release.
  - Correlate LLM risks with other system and codebase vulnerabilities.

- **Compliance & Audit:**  
  - Demonstrate ongoing due diligence for AI-related compliance and governance.
  - Export LLM vulnerability and remediation reports for stakeholders.

#### Typical User Workflow

1. **Submit LLM provider/model and probes** for risk scanning.
2. **Automated vulnerability testing** is performed (e.g., prompt injection, prompt leaks).
3. **Review dashboard:** Severity-ranked vulnerabilities, attack trees, and remediation guidance.
4. **Mitigate:** Apply suggested fixes and re-test as needed.

#### Example API Usage

```bash
curl -X POST http://localhost:8000/create/llm_scan \
  -H "Content-Type: application/json" \
  -d '{ "provider": "OpenAI", "model": "gpt-4", "probes": ["ansiescape"] }'
curl http://localhost:8000/fetch/llm_scan/3
```

---

### 3. MCP Server Vulnerability Scanning

#### What It Does

- Integrates with MCP (Managed Code Pipeline) servers to automatically scan source code repositories for vulnerabilities, hardcoded secrets, misconfigurations, and compliance violations.
- Supports multi-repo, multi-language environments, providing centralized dashboards and unified reporting.
- Maps findings directly to compliance frameworks and allows for real-time tracking of remediation progress.

#### End-User Value

- **Developers & DevOps:**  
  - Get immediate, actionable feedback on code risks, secrets, and compliance issues before merge or deployment.
  - Automate codebase scanning as part of CI/CD to catch issues early.
  - Reduce manual review effort and improve code quality.

- **Security Engineers:**  
  - Orchestrate organization-wide code scanning across all MCP-managed repositories.
  - Focus on critical findings with risk-based prioritization.
  - Maintain an auditable record of codebase security posture and remediation history.

- **Compliance & Audit:**  
  - Monitor codebase compliance in real time, across all projects and teams.
  - Generate audit-ready reports and track regulatory adherence.
  - Ensure all code meets both security and compliance standards.

#### Typical User Workflow

1. **Trigger MCP scan** for one or more repositories and branches via dashboard or API.
2. **Automated scanning:** MCP analyzes code for vulnerabilities and compliance issues.
3. **Review findings:** Vulnerability list by repo/branch, secret exposures, misconfigurations, compliance status.
4. **Remediate:** Assign, track, and resolve issues; export compliance/audit reports.

#### Example API Usage

```bash
curl -X POST http://localhost:8000/create/mcp_scan \
  -H "Content-Type: application/json" \
  -d '{ "repo_url": "https://github.com/org/repo", "branch": "main" }'
curl http://localhost:8000/fetch/mcp_scan/42
```

---

## Example Workflows

**Workflow 1: Threat Model a New Application**  
1. Upload DFD and system details.
2. Review the generated threat model (risks, OWASP mapping, compliance links).
3. Act on remediation and compliance guidance.
4. Track threat and compliance resolution over time.

**Workflow 2: LLM Security Scan**  
1. Submit LLM provider/model for scanning.
2. Monitor scan and review vulnerabilities.
3. Apply recommendations to mitigate GenAI/LLM risks.

**Workflow 3: MCP Server Codebase Scan**  
1. Trigger MCP scan for one or more repositories and branches.
2. Review vulnerability and compliance findings in the dashboard.
3. Track remediation progress and export compliance reports as needed.

---

## Use Cases

- **Security Architecture Reviews:** Automated and updatable threat models for new or evolving systems.
- **Continuous Compliance:** Track and demonstrate compliance with ISO, PCI, NIST, SOC2, GDPR.
- **DevSecOps Integration:** Automated risk and compliance analysis in CI/CD.
- **GenAI/LLM Security:** Proactive testing and monitoring for AI-powered features.
- **Codebase Security:** Unified scanning and compliance reporting for all managed code.

---

## Tech Stack

- **Backend:** Python (FastAPI), JWT Auth, REST API
- **Frontend:** Next.js (TypeScript), Tailwind CSS, Lucide React
- **Database:** Configurable (e.g., SQLite/Postgres)
- **AI Analysis:** Integrations for LLM/AI-powered analysis
- **MCP Integration:** For scalable codebase scanning and orchestration

---

## Support

- 📧 Email: [nikhil@cyberultron.com](mailto:nikhil@cyberultron.com)

---

**RiskPilot** — Unified, automated threat modeling and vulnerability management for the next generation of enterprise security.

All rights reserved. This software and its documentation are the intellectual property of CyberUltron Consulting Private Limited.
