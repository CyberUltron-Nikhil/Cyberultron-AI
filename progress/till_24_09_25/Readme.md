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

**RiskPilot** is an AI-powered threat modeling and security risk analysis platform. RiskPilot enables organizations to identify, visualize, and manage security threats across classic applications, GenAI/LLM integrations, and codebases managed via MCP servers. It brings together system diagram analysis, LLM vulnerability probing, and automated MCP code scanning into one seamless platform, delivering actionable risk scores, compliance insights, and AI-driven remediation guidance.

---

## Core Mission

Our mission is to make enterprise security risk analysis simple, automated, and actionable for all—from engineering and AI/ML to compliance and DevSecOps. RiskPilot bridges the gap between identifying risks and resolving them, integrating with your SDLC to deliver automated threat modeling, vulnerability tracking, compliance mapping, and guided remediation. The platform empowers teams to accelerate secure innovation with confidence.

---

## Key Capabilities

- **Normal System Threat Modeling:** Automated STRIDE/DREAD/OWASP Top 10 threat modeling from DFDs and architecture details.
- **LLM Vulnerability Testing:** AI-powered security analysis of LLM/GenAI integrations with risk scoring and remediation.
- **MCP Server Vulnerability Scanning:** Unified codebase scanning for vulnerabilities, secrets, and compliance issues via MCP.
- **Compliance Tracking:** Aligns findings with ISO 27001, PCI DSS, NIST, SOC 2, GDPR, and other frameworks.
- **Risk Dashboards:** Visualizes security posture, compliance gaps, and remediation progress.
- **REST APIs:** Supports automation and integration into existing workflows and CI/CD.

---

## Target Users

- **Security Engineers:** Automate threat modeling, vulnerability scanning, and compliance checks.
- **Developers & DevOps:** Integrate risk analysis into CI/CD, shift security left.
- **AI/ML & Product Teams:** Assess and secure LLM/GenAI features before and after deployment.
- **Compliance & Audit:** Access up-to-date mapping to standards and compliance status.
- **Cloud & Solution Architects:** Design secure architectures with instant feedback.

---

## Demo Video

🎥 *Coming soon!* — RiskPilot walkthrough.

---

## Feature Deep Dives

### 1. Threat Modeling of Normal Systems

#### What It Does
- Accepts Data Flow Diagrams (DFDs) and system architecture details.
- Uses STRIDE, DREAD, and OWASP Top 10 methodologies to generate threat models.
- Assigns risk scores, maps threats to components, and identifies unresolved/resolved threats.
- Visualizes attack surfaces, threat heatmaps, and compliance mapping.

#### Value for Users
- **Security Engineers:** Quickly generate and update threat models for every release and architecture change. Automate risk documentation and focus reviews on critical threats.
- **Developers & DevOps:** Integrate threat modeling into build and deploy pipelines. Identify security gaps before code leaves the dev environment.
- **Solution/Cloud Architects:** Get objective security feedback early in the design phase. Experiment with architecture alternatives and instantly see risk impact.

#### Example API Usage
```bash
curl -X POST http://localhost:8000/create/normal_system/pre_upload \
  -F "image_file=@/path/to/your_dfd.png"
curl -X POST http://localhost:8000/create/normal_system \
  -H "Content-Type: application/json" \
  -d '{ ... system details ... }'
curl http://localhost:8000/fetch/normal_system/2
```
#### Dashboard Output
- Threat summary cards, unresolved/resolved counts, risk scores, OWASP Top 10 and compliance mapping, attack trees and heatmaps.


---

### 2. LLM Vulnerability Testing

#### What It Does
- Scans LLM (Large Language Model) and GenAI integrations for security vulnerabilities such as prompt injection, data leakage, supply chain risks, and model abuse.
- Runs custom probes and AI-based tests against deployed models and APIs.
- Assigns risk scores and provides remediation advice for each detected issue.

#### Value for Users
- **AI/ML Engineers & Product Teams:** Secure LLM/GenAI deployments before and after launch. Proactively test for prompt injection, output manipulation, and other GenAI-specific threats.
- **Security Engineers:** Integrate LLM security checks into larger threat models and risk dashboards. Automate vulnerability testing for every release.
- **Compliance:** Demonstrate due diligence and active monitoring of emerging AI risks.

#### Example API Usage
```bash
curl -X POST http://localhost:8000/create/llm_scan \
  -H "Content-Type: application/json" \
  -d '{ "provider": "OpenAI", "model": "gpt-4", "probes": ["ansiescape"] }'
curl http://localhost:8000/fetch/llm_scan/3
```
#### Dashboard Output
- Vulnerability lists with severity, remediation advice, attack trees for GenAI threat paths, compliance mapping for AI use.


---

### 3. MCP Server Vulnerability Scanning

#### What It Does
- Integrates with MCP (Managed Code Pipeline) servers to scan codebases for vulnerabilities, secrets, misconfigurations, and compliance violations.
- Provides unified reporting and dashboards for multi-repo, multi-language codebases.
- Maps findings to compliance frameworks and tracks remediation progress.

#### Value for Users
- **DevOps & Developers:** Get immediate feedback on code risks, secret exposure, and compliance issues before merge or deployment. Automate scanning as part of CI/CD.
- **Security Engineers:** Orchestrate organization-wide code scanning across all MCP-managed repositories. Focus reviews on critical findings.
- **Compliance & Audit:** Monitor codebase compliance in real time, generate audit-ready reports, and ensure all code meets security standards.

#### Example API Usage
```bash
curl -X POST http://localhost:8000/create/mcp_scan \
  -H "Content-Type: application/json" \
  -d '{ "repo_url": "https://github.com/org/repo", "branch": "main" }'
curl http://localhost:8000/fetch/mcp_scan/42
```
#### Dashboard Output
- Vulnerability lists by repo and branch, secret findings, misconfigurations, compliance status and violations, remediation tracking.


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
