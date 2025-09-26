# ZeroShield

<div align="center">
   <img width="200" height="200" alt="ZeroShield (ZAPESIC) Logo" src="https://github.com/user-attachments/assets/03398106-6184-47b0-b1f4-403d375f2eba" />
   <br />
   <em>Threat Shield is a part of ZeroShield</em>

   
</div>
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


## Table of Contents

- [About](#about)
- [Core Mission](#core-mission)
- [Key Capabilities](#key-capabilities)
- [Target Users](#target-users)
- [Demo Video & Screenshots](#demo-video--screenshots)
- [Feature Overview](#feature-overview)
  - [1. Threat Modeling of Normal Systems](#1-threat-modeling-of-normal-systems)
  - [2. LLM Vulnerability Testing (with Garak Probes)](#2-llm-vulnerability-testing-with-garak-probes)
  - [3. MCP Server Vulnerability Scanning](#3-mcp-server-vulnerability-scanning)
- [Compliance Mapping](#compliance-mapping)
- [Example Workflows & User Benefits](#example-workflows--user-benefits)
- [Use Cases](#use-cases)
- [Tech Stack](#tech-stack)
- [Support](#support)

---

## About

**ZeroShield** is an AI-powered platform for holistic threat modeling and vulnerability management. It enables organizations to identify, visualize, and manage risks across classical applications, GenAI/LLM integrations, and codebases managed through MCP servers. Threat Shield, a core module of ZeroShield, provides advanced threat modeling, LLM vulnerability testing (with in-depth Garak probe analysis), and MCP server vulnerability scanning—all in a unified, actionable dashboard.

---

## Core Mission

Empower teams to rapidly identify, understand, and remediate security risks—across all technologies—by automating threat analysis, vulnerability detection, and compliance mapping. **ZeroShield** bridges the gap between security, development, and compliance, enabling secure digital innovation.

---

## Key Capabilities

- Automated Threat Modeling for Classic and Cloud-Native Systems
- Advanced LLM Vulnerability Testing (with deep Garak Probe analysis)
- MCP Server-Based Vulnerability Scanning & Compliance
- Real-Time Compliance & OWASP Top 10 Mapping
- Unified Risk Analytics & Visualizations

---

## Target Users

- **Security Engineers:** Automate threat modeling, vulnerability scanning, and compliance.
- **Developers & DevOps:** Integrate risk analysis into CI/CD and shift security left.
- **AI/ML & Product Teams:** Secure and validate LLM/GenAI features with real security probes.
- **Compliance & Audit:** Map vulnerabilities to compliance frameworks and track remediation.
- **Cloud & Solution Architects:** Design secure architectures with instant, actionable feedback.

---

## Demo Video & Screenshots

> **Screenshots and demo video coming soon!**  
> (This section will be updated as soon as assets are available.)

---

## Feature Overview

### 1. Threat Modeling of Normal Systems

#### What Users See & How It Works

- **Dashboard View:**  
  - Project table showing Name, Repo URL, Total Threats, Unresolved Threats, Non-Conformant Issues, OWASP Found, and Created At.
  - System detail dialog: Enter system name, architecture, description, internet exposure, upload architecture/DFD diagrams, link GitHub repos, set authentication/data sensitivity, add dependencies.
  - Interactive dashboard:  
    - Summary cards for STRIDE threats, unresolved/resolved threats, threat score.
    - DREAD heatmap, attack trees, failed controls, OWASP Top 10 vulnerability tracker.
    - Detailed threat table with DREAD score, severity, location, compliance, STRIDE tags, status, suggested fixes.
    - One-click report generation.

#### How It Benefits Users

- **Proactive risk identification** before incidents can occur.
- **Automated, up-to-date threat models**—no manual upkeep.
- **Instant visibility into unresolved threats and compliance gaps.**
- **Actionable remediation** for each threat with mapped compliance impact.
- **Visual analytics** for technical and business audiences.

---

### 2. LLM Vulnerability Testing (with Garak Probes)

#### What Users See & How It Works

- **LLM Scan Dashboard:**  
  - Table of all LLM scans with totals, hits, hit rate, risk level, and timestamps.
  - Each scan: summary cards for total tests, hits, hit rate, risk level; failed controls; OWASP mapping.
  - Probe details table: Each probe run (e.g., ansiescape, atkgen, etc.), status, detector, suggestions.
  - Generate report button.

#### In-Depth Garak Probe Coverage

- **Garak probes** test models for:  
  - ANSI escapes, attack generation, audio attacks, antivirus/spam bypass, data leakage, prompt injection, roleplay/jailbreaks, SQLi, XSS, hallucinated package names, adversarial suffixes, emotional manipulation, and more.
- **LLM Exposure Analysis:**  
  - Beyond probe results, Threat Shield analyzes the LLM's exposure and risk posture, surfaces all successful bypasses, and maps to OWASP Top 10 and failed compliance controls.

#### How It Benefits Users

- **Real-world attack simulation** using the latest security probe techniques.
- **Immediate understanding of LLM weaknesses and exposure.**
- **Human-readable explanations and remediation steps** for every finding.
- **Continuous assessment** as models/prompts evolve.
- **Supports secure, compliant AI adoption** in any environment.

---

### 3. MCP Server Vulnerability Scanning

#### What Users See & How It Works

- **MCP Scan Dashboard:**  
  - Table of MCP scans: repo name, results, language, status, created at.
  - Scan detail: summary cards (total results, resolved, high risk), failed controls, OWASP vulnerabilities found, threat graph.
  - Result table: Rule detected (from semgrep), severity, compliance mapping, status, suggested fixes.
  - Report export.

#### Technical Workflow

- **Phase 1:**  
  - Repository is temporarily cloned and scanned with **Semgrep** for static code analysis.
  - Semgrep flags all code patterns matching vulnerability rules.
- **Phase 2:**  
  - Each finding is analyzed by an LLM to generate explanations and actionable fixes.
  - Further mapped to **OWASP Top 10** vulnerabilities and failed compliance controls (ISO 27001, PCI DSS, NIST, SOC2, GDPR, etc.).
  - Compliance mapping is visualized per finding and overall scan.

#### How It Benefits Users

- **Automated, deep static analysis** (Semgrep) on every codebase.
- **LLM-powered explanations** for fast triage and remediation.
- **Clear compliance gap visibility** for every finding.
- **Audit-ready reporting** and compliance evidence on demand.

---

## Compliance Mapping

| Vulnerability / Threat Type                | OWASP Top 10 | ISO 27001 | PCI DSS | SOC2 | NIST | GDPR |
|--------------------------------------------|:------------:|:---------:|:-------:|:----:|:----:|:----:|
| Insecure Authentication                    | A07          | ✓         | ✓       | ✓    | ✓    | ✓    |
| Injection (SQLi, Command, etc.)            | A03          | ✓         | ✓       | ✓    | ✓    |      |
| Data Exposure/Leakage                      | A01, A06     | ✓         | ✓       | ✓    | ✓    | ✓    |
| Security Misconfiguration                  | A05          | ✓         | ✓       | ✓    | ✓    |      |
| Vulnerable/Outdated Components             | A06          | ✓         | ✓       | ✓    | ✓    |      |
| Prompt Injection (LLM)                     | A01, A05     |           |         |      |      | ✓    |
| Malicious Code Generation                  | A06, A10     | ✓         |         |      |      |      |
| Compliance Control Failure (General)       | All          | ✓         | ✓       | ✓    | ✓    | ✓    |

> **Note:** Each finding in the dashboard is mapped to these standards and visualized at both summary and per-issue level.

---

## Example Workflows & User Benefits

**Threat Modeling Workflow:**  
- Upload system diagrams and architecture details, review generated threat model, prioritize/assign remediation, track resolution and compliance mapping.

**LLM Security Workflow:**  
- Register LLM/GenAI features for assessment, receive prioritized vulnerability reports (with Garak probe detail), act on LLM-generated fix steps, monitor ongoing risk.

**MCP Vulnerability Workflow:**  
- Trigger scan for MCP repositories, review findings and LLM explanations, analyze OWASP/compliance mapping, assign remediations, produce compliance-ready reports.

**Benefits:**  
- Prevent real-world security incidents and compliance failures before they happen.
- Save time with automation and actionable guidance.
- Communicate risk and progress clearly to all stakeholders.

---

## Use Cases

- Security architecture reviews for new/evolving systems
- Continuous compliance (ISO, PCI, NIST, SOC2, GDPR)
- DevSecOps integration into CI/CD
- GenAI/LLM security validation and monitoring
- MCP workload/codebase security

---

## Tech Stack

- **Backend:** Python (FastAPI), REST API, JWT Auth
- **Frontend:** Next.js (TypeScript), Tailwind CSS, Lucide React, React
- **AI Analysis:** LLM/AI-powered integrations, Garak
- **Code Scanning:** Semgrep
- **Database:** Configurable (e.g., SQLite/Postgres)

---

## Support

- 📧 Email: [nikhil@cyberultron.com](mailto:nikhil@cyberultron.com)

---

**ZeroShield** — Unified, automated threat modeling and vulnerability management for the next generation of enterprise security.  
*Threat Shield, a part of ZeroShield, brings in-depth, practical security to every step of your development and deployment lifecycle.*

All rights reserved. This software and its documentation are the intellectual property of CyberUltron Consulting Private Limited.

---

> **Value Proposition:**  
> "ZeroShield turns complex, manual security and compliance challenges into automated, actionable insights—empowering teams to move faster, safer, and with confidence."
