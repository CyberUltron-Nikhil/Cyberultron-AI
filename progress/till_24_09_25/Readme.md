# ZeroShield

<div align="center">
  <img src="logo.jpg" alt="ZeroShield Logo" width="200" height="auto" />
  
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

**ZeroShield** is an AI-powered platform for holistic threat modeling and vulnerability management. It empowers organizations to identify, visualize, and manage risks across classic applications, GenAI/LLM integrations, and codebases managed through MCP servers. ZeroShield brings together system diagram analysis, LLM security probing, and automated codebase scanning, providing actionable risk scores, compliance insights, and AI-driven remediation guidance—all within a unified dashboard and workflow.

---

## Core Mission

To make enterprise security risk analysis simple, automated, and actionable—no matter the technology stack. ZeroShield bridges the gap between identifying, understanding, and remediating risks, integrating with your SDLC to deliver automated threat modeling, vulnerability analytics, compliance mapping, and guided remediation. The platform enables teams to accelerate secure innovation with confidence.

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

🎥 *Coming soon!* — ZeroShield walkthrough.

---

## Feature Deep Dives

### 1. Threat Modeling of Normal Systems

#### In-Depth Explanation

ZeroShield enables fully automated threat modeling for traditional and cloud-native systems using user-provided Data Flow Diagrams (DFDs) and architecture details. Leveraging industry methodologies such as STRIDE, DREAD, and OWASP Top 10, the platform analyzes every component and data flow to identify potential threats, assign risk scores, and map vulnerabilities to specific areas of your application or infrastructure.

**How it works for different users:**

- **Security Engineers:**  
  - Receive comprehensive, up-to-date threat models for each architecture version or deployment.
  - Focus reviews on prioritized, risk-scored threats, facilitating more effective security operations and audits.
  - Maintain an auditable, versioned record of threat analysis and remediation progress.

- **Developers & DevOps:**  
  - Get visibility into security gaps as early as the design phase, minimizing costly fixes later.
  - Integrate threat modeling into CI/CD and code review processes—enabling shift-left security.
  - Access actionable, context-aware remediation guidance that’s mapped to your stack and workflows.

- **Cloud & Solution Architects:**  
  - Instantly see the security implications of architectural choices and design patterns.
  - Use visualizations like attack trees and heatmaps to communicate risk to technical and business stakeholders.
  - Experiment with different system designs and receive immediate, evidence-based feedback.

**Dashboard View:**  
Interactive cards, risk scores, unresolved/resolved threat lists, OWASP/STRIDE mapping, heatmaps, and compliance overlays make it easy for all stakeholders to understand and act on their risk posture.

---

### 2. LLM Vulnerability Testing

#### In-Depth Explanation

ZeroShield delivers specialized security analysis for LLM (Large Language Model) and GenAI integrations, which are increasingly a target for novel attacks. The platform performs automated, context-aware probing for AI-specific risks—such as prompt injection, data leakage, model abuse, and supply chain vulnerabilities.

**How it works for different users:**

- **AI/ML & Product Teams:**  
  - Test deployed LLMs and GenAI features for prompt attacks, output manipulation, and sensitive data exposure—both pre- and post-release.
  - Get tailored recommendations for securing prompt-handling logic, input validation, and model integration.
  - Demonstrate to leadership and partners that AI risks are actively managed.

- **Security Engineers:**  
  - Integrate LLM scans into overall risk dashboards and ongoing threat models.
  - Automate GenAI risk validation with every build, ensuring no new risks are introduced as models or prompts change.
  - Correlate LLM-specific vulnerabilities with broader application and infrastructure risk.

- **Compliance & Audit:**  
  - Map AI/LLM vulnerabilities and controls to regulatory requirements and organizational standards.
  - Maintain evidence of active monitoring and mitigation of emerging AI threats.

**Dashboard View:**  
Severity-ranked vulnerability lists, attack trees for GenAI, compliance mapping for AI use, and ongoing risk trend analytics provide all stakeholders with clear insight into AI risk posture.

---

### 3. MCP Server Vulnerability Scanning

#### In-Depth Explanation

ZeroShield’s MCP Server Vulnerability Scanning provides an advanced, automated approach to codebase security and compliance analysis. 

**How it works:**

- The platform **clones your MCP server repository temporarily** and scans it for vulnerability patterns using advanced static analysis tools such as semgrep.
- All detected issues are **flagged and then analyzed by an LLM** to generate clear explanations and actionable fixes. 
- **Phase 2:** Each finding is further processed to generate OWASP vulnerability mappings and identify which compliance controls (across standards like ISO 27001, PCI DSS, NIST, SOC2, and GDPR) are impacted by each finding.
- The entire workflow is seamless and hands-off: once triggered, ZeroShield orchestrates scanning, analysis, mapping, and compliance reporting.

**How it works for different users:**

- **Developers & DevOps:**  
  - Instantly receive feedback on code risks, secrets, and compliance violations before merging or deployment.
  - Improve code quality and reduce manual review effort by integrating continuous scanning into CI/CD.
  - Get LLM-generated explanations and remediation suggestions for each issue, making fixes straightforward.

- **Security Engineers:**  
  - Achieve organization-wide code scanning across all MCP-managed repositories from a central dashboard.
  - Prioritize remediation using risk and compliance impact, and track progress over time.
  - Maintain an auditable history of findings, fixes, and compliance status for every repo and branch.

- **Compliance & Audit:**  
  - Monitor live compliance status by mapping vulnerabilities to exact controls and standards.
  - Generate audit-ready reports demonstrating proactive codebase governance and remediation.
  - Rapidly identify and address gaps before they impact regulatory posture.

**Dashboard View:**  
Comprehensive findings by repo/branch, LLM explanations, remediation tracking, OWASP and compliance mapping—enabling both security and compliance teams to work from a single source of truth.

---

## Example Workflows

**Workflow 1: Threat Modeling a New Application**  
- Upload your system DFD and architecture details.
- Instantly receive a threat model with prioritized risks, OWASP mapping, and compliance insights.
- Take remediation or assign tasks; monitor and update statuses as issues are resolved.

**Workflow 2: LLM Security Scan**  
- Select or register your LLM/GenAI integration for security probing.
- Review vulnerabilities and AI-specific risk guidance.
- Iterate on prompt design or integration, then re-test for secure deployment.

**Workflow 3: MCP Server Codebase Scan**  
- Start the scan for one or more repositories/branches.
- Review LLM explanations, compliance mappings, and remediation advice in the dashboard.
- Track fixes and export compliance or audit reports as needed.

---

## Use Cases

- **Security Architecture Reviews:** Automated, updatable threat models for any system or update.
- **Continuous Compliance:** Demonstrate adherence to ISO, PCI, NIST, SOC2, GDPR, and more.
- **DevSecOps Integration:** Embed risk and compliance checks deep into CI/CD pipelines.
- **GenAI/LLM Security:** Continuously validate and secure AI-powered features.
- **Enterprise Codebase Security:** Unified scanning and compliance reporting for all managed code.

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

**ZeroShield** — Unified, automated threat modeling and vulnerability management for the next generation of enterprise security.

All rights reserved. This software and its documentation are the intellectual property of CyberUltron Consulting Private Limited.
