# ZeroShield

<div align="center">
   <img width="200" height="100" alt="image" src="https://github.com/user-attachments/assets/03398106-6184-47b0-b1f4-403d375f2eba" />

  
  <br />
  
  <div align="center">
    <a href="https://opensource.org/licenses/MIT">
      <img src="https://img.shields.io/badge/License-MIT-yellow.svg" alt="License: MIT" />
    </a>
    <a href="https://www.python.org/downloads/">
      <img src="https://img.shields.io/badge/python-3.8+-blue.svg" alt="Python" />
    </a>
    <a href="https://nodejs.org/">
      <img src="https://img.shields.io/badge/node.js-18+-green.svg" alt="Node.js" />
    </a>
    <a href="https://nextjs.org/">
      <img src="https://img.shields.io/badge/Next.js-14-black.svg" alt="Next.js" />
    </a>
    <a href="https://www.typescriptlang.org/">
      <img src="https://img.shields.io/badge/TypeScript-5.0-blue.svg" alt="TypeScript" />
    </a>
    <a href="https://openai.com/">
      <img src="https://img.shields.io/badge/OpenAI-GPT--4-purple.svg" alt="OpenAI" />
    </a>
    <a href="https://fastapi.tiangolo.com/">
      <img src="https://img.shields.io/badge/FastAPI-0.110+-green.svg" alt="FastAPI" />
    </a>
    <a href="https://tailwindcss.com/">
      <img src="https://img.shields.io/badge/TailwindCSS-3.3+-blue.svg" alt="TailwindCSS" />
    </a>
    <a href="https://lucide.dev/">
      <img src="https://img.shields.io/badge/Lucide-React-orange.svg" alt="Lucide React" />
    </a>
    <a href="https://react.dev/">
      <img src="https://img.shields.io/badge/React-18+-blue.svg" alt="React" />
    </a>
  </div>
</div>

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

**ZeroShield** is an AI-powered platform for holistic threat modeling and vulnerability management, enabling organizations to identify, visualize, and manage risks across classic applications, GenAI/LLM integrations, and codebases managed through MCP servers. ZeroShield unifies system diagram analysis, LLM security probing, and advanced vulnerability scanning, providing actionable risk scores, compliance insights, and AI-driven remediation guidance, all within a seamless dashboard.

---

## Core Mission

To make enterprise security risk analysis simple, automated, and actionable—no matter the technology stack. ZeroShield bridges the gap between identifying, understanding, and remediating risks, integrating with your SDLC to deliver automated threat modeling, vulnerability analytics, compliance mapping, and guided remediation. The platform enables teams to accelerate secure innovation with confidence.

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

🎥 *Coming soon!* — ZeroShield walkthrough.

---

## Feature Deep Dives

### 1. Threat Modeling of Normal Systems

#### In-Depth Explanation

ZeroShield's Threat Modeling feature empowers organizations to proactively identify and mitigate risks throughout the software development lifecycle. Users can upload Data Flow Diagrams (DFDs) and detailed architecture information, which ZeroShield analyzes using industry-standard frameworks such as STRIDE, DREAD, and OWASP Top 10.

- **Automated Analysis:** The platform automatically detects and categorizes threats, maps them to affected components, and calculates risk scores based on likelihood and impact.
- **Vulnerability Mapping:** Each identified threat is mapped to security controls and compliance requirements, enabling teams to see which standards (e.g., ISO 27001, PCI DSS, NIST, SOC2, GDPR) are impacted.
- **Attack Surface Visualization:** ZeroShield visualizes attack surfaces, threat propagation, and high-risk zones, making it easy to prioritize remediation.
- **Continuous Updates:** As system diagrams or architecture evolve, ZeroShield can update the threat model, ensuring it always reflects the most current posture.

**Value to End Users:**
- **Security Engineers:** Rapidly generate comprehensive, up-to-date threat models and maintain a clear audit trail.
- **Developers & DevOps:** Receive actionable insights on security risks relevant to their code and components, integrated into CI/CD.
- **Compliance & Audit:** Instantly identify compliance gaps and generate evidence for audits.
- **Architects:** Validate new designs or changes with instant security feedback and recommendations.

---

### 2. LLM Vulnerability Testing

#### In-Depth Explanation

ZeroShield's LLM Vulnerability Testing module provides specialized security analysis for applications and services integrating Large Language Models (LLMs) and GenAI.

- **Automated Probing:** The platform performs automated and customizable probing for LLM-specific threats, including prompt injection, prompt leakage, data exfiltration, output manipulation, and model supply chain risks.
- **LLM-Aware Analysis:** Each detected vulnerability is analyzed by an LLM, which provides human-readable explanations of the risk, root cause, and practical remediation steps.
- **Vulnerability & Compliance Mapping:** All findings are mapped to relevant OWASP categories and compliance standards (e.g., data privacy, misuse, governance).
- **Continuous Monitoring:** ZeroShield supports both one-time and continuous assessment as LLM integrations or prompt templates evolve.

**Value to End Users:**
- **AI/ML & Product Teams:** Validate GenAI and LLM features before and after deployment, ensuring resilience against evolving threat vectors.
- **Security Engineers:** Integrate LLM security testing into broader enterprise threat modeling and dashboards, correlating AI risks with infrastructure/codebase findings.
- **Compliance & Audit:** Demonstrate due diligence in AI governance and data privacy by mapping LLM risks to regulatory standards.
- **Leadership:** Gain confidence in responsible and secure AI adoption, with continuous posture tracking.

---

### 3. MCP Server Vulnerability Scanning

#### In-Depth Explanation

ZeroShield's MCP Server Vulnerability Scanning feature is designed for environments that use Managed Compute Platform (MCP) servers and source code repositories. When triggered, ZeroShield temporarily clones the selected MCP server repository and scans it for vulnerability patterns using [Semgrep](https://semgrep.dev), a leading open-source static analysis tool. The platform identifies weaknesses, secrets, and insecure patterns within the code.

Once the initial scan is complete (Phase 1), each finding is analyzed by a Large Language Model (LLM), which generates clear explanations and actionable fixes tailored to your code and context. In Phase 2, ZeroShield further processes each finding to provide detailed mappings:
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

- **Backend:** Python (FastAPI), REST API, JWT Auth
- **Frontend:** Next.js (TypeScript), Tailwind CSS, Lucide React, React
- **AI Analysis:** LLM/AI-powered integrations
- **Code Scanning:** Semgrep
- **Database:** Configurable (e.g., SQLite/Postgres)

---

## Support

- 📧 Email: [nikhil@cyberultron.com](mailto:nikhil@cyberultron.com)

---

**ZeroShield** — Unified, automated threat modeling and vulnerability management for the next generation of enterprise security.

All rights reserved. This software and its documentation are the intellectual property of CyberUltron Consulting Private Limited.
