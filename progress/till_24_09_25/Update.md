# Threat Shield (A module of ZeroShield)

<div align="center">
   <img width="200" height="200" alt="Threat Shield (ZAPISEC) Logo" src="https://github.com/user-attachments/assets/03398106-6184-47b0-b1f4-403d375f2eba" />
   <br />
   <em>Threat Shield is a core security module under the <b>ZeroShield</b> platform.</em>
</div>

---

## Table of Contents

- [About Threat Shield](#about-threat-shield)
- [Why Threat Shield? (Value Proposition)](#why-threat-shield-value-proposition)
- [Key Capabilities](#key-capabilities)
- [Target Users](#target-users)
- [Demo Video & Screenshots](#demo-video--screenshots)
- [Feature Deep Dives](#feature-deep-dives)
  - [1. Threat Modeling of Normal Systems](#1-threat-modeling-of-normal-systems)
  - [2. LLM Vulnerability Testing (Garak Probe Deep-dive)](#2-llm-vulnerability-testing-garak-probe-deep-dive)
  - [3. MCP Server Vulnerability Scanning (Semgrep Deep-dive)](#3-mcp-server-vulnerability-scanning-semgrep-deep-dive)
- [Compliance Mapping Table](#compliance-mapping-table)
- [Example User Scenarios](#example-user-scenarios)
- [Tech Stack](#tech-stack)
- [Support](#support)

---

## About Threat Shield

**Threat Shield** is an advanced security automation module within the **ZeroShield** platform, designed to give organizations deep, actionable insight into risks across classic applications, codebases, and cutting-edge GenAI/LLM integrations.  
Threat Shield unifies real-time threat modeling, LLM security probing via Garak, and MCP codebase vulnerability scanning for a complete, compliance-ready view of your security posture.

---

## Why Threat Shield? (Value Proposition)

> **Automate security. Accelerate compliance.**  
> Threat Shield transforms complex, manual security and compliance challenges into automated, actionable insights—empowering you to prevent incidents, pass audits, and build securely at speed.

---

## Key Capabilities

- Automated Threat Modeling for Classic & Cloud-Native Systems
- Deep LLM Vulnerability Testing with Garak (real adversarial probes)
- MCP Server-Based Code Scanning (Semgrep + LLM analysis)
- OWASP & Compliance Mapping (ISO, PCI, SOC2, NIST, GDPR)
- Unified, Interactive Risk Dashboards

---

## Target Users

- Security Engineers & Architects
- Developers & DevOps
- AI/ML Product Teams
- Compliance & Audit Professionals
- Cloud & Solution Architects

---

## Demo Video & Screenshots

> **Coming Soon:**  
> Screenshots and demo video will be added here as soon as they are available for each feature.

---

## Feature Deep Dives

---

### 1. Threat Modeling of Normal Systems

#### UI Breakdown (Figma Reference)
- **Project List Screen:**  
  - Table: [Name, Repo URL, Total Threats, Unresolved Threats, Total Non-Conformant, OWASP Found, Created At]
  - “Create Project” button to launch new assessment
- **Project Creation Dialog:**  
  - Tabs: Threat modeling / LLM Scanning / MCP Scanning  
  - Fields: System Name, Architecture Type, Description, Internet Facing (Y/N), Upload Architecture/DFD/UML, GitHub Repo connect, Auth Type, Data Sensitivity, Dependencies
- **Project Dashboard:**  
  - **Summary Cards:**  
      - Total STRIDE Threats Identified  
      - Threats Unresolved  
      - Threats Resolved  
      - Threat Score (overall risk indicator)
  - **DREAD Heatmap:** Visualizes risk by Damage, Reproducibility, Exploitability, Affected Users, Discoverability.
  - **Failed Controls Card:** Number of failed compliance controls.
  - **OWASP Top 10 Tracker:** Visual (circle graph) and list of which categories are triggered.
  - **Attack Trees:** Visual graph showing attack paths and relationships.
  - **Threat Details Table:**  
      - Columns: Threat, DREAD Score, Severity, Compliance, Location, STRIDE, Status, Suggested Fixes
      - Search & filter options
  - **Generate Report Button:** Exportable audit-ready report.

#### What/Why of Each Visualization
- **Summary Cards:** Instantly see the scale and urgency of risk in the system.
- **DREAD Heatmap:** Pinpoints highest-impact threats for prioritization.
- **Failed Controls:** Shows direct compliance gaps (e.g., SOC2, PCI).
- **OWASP Tracker:** Maps findings to industry standards for external reporting.
- **Attack Trees:** Helps visualize possible attack paths and lateral movement.
- **Threat Table:** Enables fast triage, assignment, and remediation tracking.

#### Deep-Dive: How It Works
- Upload system diagrams, code, and metadata.
- The engine analyzes flows, trust boundaries, and identifies threats using STRIDE, DREAD, and OWASP logic.
- Each threat is auto-mapped to compliance controls.
- Dashboard and report update in real-time as threats are resolved.

#### Hypothetical User Scenario

> **Alice**, a Security Engineer, is onboarding a new payments platform. She uploads the system’s DFDs and architecture, connects the GitHub repo, and sets data sensitivity. Threat Shield instantly generates a threat model showing 23 STRIDE threats, highlighting 7 unresolved high-risk issues and 2 failed PCI compliance controls. Using the heatmap and attack tree, Alice quickly triages which risks to escalate to DevOps for urgent fixes, and exports a report to satisfy the next audit.

---

### 2. LLM Vulnerability Testing (Garak Probe Deep-dive)

#### UI Breakdown (Figma Reference)
- **LLM Scans List:**  
  - Table: [Name, Total Tests, Total Hits, Hit Rate, Risk Level, Created At]
  - "Create Project" button to launch new scan
- **LLM Scanning Project Dashboard:**  
  - **Summary Cards:**  
      - Total Tests  
      - Total Hits  
      - Hit Rate  
      - Risk Level (visual/highlight)
  - **Failed Controls:** Number of non-conformant controls triggered by LLM findings.
  - **OWASP Vulnerabilities Card:** Number and list of OWASP Top 10 categories found.
  - **Threat Graph:** Distribution of exploit hits across probes.
  - **Probe Details Table:**  
      - Columns: Probe Name, Passed, Total, Hit Rate, Detector, Suggested Fixes
      - “View Suggestions” for every probe

#### What/Why of Each Visualization
- **Summary Cards:** High-level risk/weakness snapshot of LLM.
- **Failed Controls:** Links AI security to compliance posture.
- **OWASP Card:** Shows if LLM flaws could impact web/app security standards.
- **Probe Table:** Full transparency—see exactly which prompts/probes succeeded, failed, and why.

#### Deep-Dive: Garak Probe System

Threat Shield leverages the **Garak** framework for LLM security, running dozens of real-world probe categories:

| Probe Category         | What It Tests                                                             | Why It Matters                        |
|-----------------------|--------------------------------------------------------------------------|---------------------------------------|
| ANSI Escape           | Model exposes terminal codes                                              | Downstream system compromise          |
| Attack Generation     | Can model be tricked into toxic/illegal output                            | Content moderation, brand risk        |
| Audio                 | Multimodal attacks bypassing text safety                                 | Jailbreaks on non-text input          |
| AV/Spam Scanning      | Will model output malware/spam test strings                              | Bypassing security scanning           |
| Continuation/Slurs    | Model completes offensive/inappropriate words                            | Social/ethical risk                   |
| Data Leakage          | Model repeats training data                                               | Confidentiality breach                |
| Doctor/Roleplay       | Policy puppetry to bypass safety                                         | Regulatory/safety risk                |
| Encoding/Jailbreak    | Can model decode/obfuscate harmful payloads                              | Filter bypass, prompt injection       |
| Exploitation (SQLi)   | Model can output exploitable code                                        | Direct app/system compromise          |
| Fileformats           | Model exposes details about underlying files                             | Environment leakage                   |
| Glitch Tokens         | Model misbehaves on edge tokens                                          | Model stability, DoS                  |
| Goodside/Malwaregen   | Known adversarial/prompt injection patterns                              | Real-world exploit research           |
| Grandma/Emotional     | Will model yield to emotional manipulation                               | Social engineering risk               |
| Hallucination         | Model invents fake package/library names                                 | Supply chain attack                   |
| Prompt Injection      | Model can be hijacked to output specific strings                         | LLM-powered app hijacking             |
| XSS/Visual Jailbreak  | Model outputs code/image links for data exfiltration                     | Web/visual AI security                |
| Latent Injection      | Model attacked through hidden instructions in data                        | RAG, document QA system risk          |

> **Further Analysis:**  
> Beyond these probes, Threat Shield analyzes all probe results for exposure patterns—automatically scoring LLM risk, mapping incidents to OWASP Top 10 and compliance controls, and surfacing which prompt/attack types are most dangerous in your use case.

#### Hypothetical User Scenario

> **Raj**, an AI/ML Product Lead, is launching a GenAI-powered helpdesk. He runs a Threat Shield LLM scan, which executes 40+ Garak probes. The dashboard reveals a high hit rate for prompt injection and roleplay attacks, and a failed GDPR control. Raj reviews the suggested fixes, patches the prompt template, and re-runs the scan—dropping risk level to “Low” and passing all compliance checks before go-live.

---

### 3. MCP Server Vulnerability Scanning (Semgrep Deep-dive)

#### UI Breakdown (Figma Reference)
- **MCP Scans List:**  
  - Table: [Repository Name, Total Results, Language, Status, Created At]
  - “Create Project” for new scan
- **MCP Scanning Project Dashboard:**  
  - **Summary Cards:**  
      - Total Results  
      - Total Resolved  
      - Total High Risk
  - **Failed Controls:** Compliance controls failed by code issues.
  - **OWASP Vulnerabilities:** Number and list of Top 10 triggered.
  - **Threat Graph:** Shows trends/types/frequency across findings.
  - **Result Table:**  
      - Columns: Result Class, Severity, Rule Detected, Status, Suggested Fixes

#### What/Why of Each Visualization
- **Summary Cards:** Snapshot of codebase health and urgency.
- **Failed Controls:** Highlights direct compliance impact.
- **OWASP Card:** Maps code issues to industry standards.
- **Threat Graph:** Visualizes risk over time or per category.
- **Result Table:** Drill down to every finding, fix, and compliance mapping.

#### Deep-Dive: Semgrep & Analysis Pipeline

- **Step 1: Static Analysis with Semgrep**
    - When a scan is triggered, Threat Shield temporarily clones the selected MCP repository.
    - Semgrep runs a suite of static analysis rules covering OWASP Top 10, common code smells, secrets, and insecure configurations.
    - Semgrep is chosen for its speed, accuracy, and extensibility (custom rules per project/language).
- **Step 2: LLM-Powered Findings**
    - Each finding is passed to an LLM for further analysis, generating:
        - Human-readable explanation of risk
        - Contextual remediation steps
        - Mapping to compliance controls (ISO, PCI, SOC2, NIST, GDPR, etc.)
- **Step 3: Dashboard and Reporting**
    - All results are visualized in the MCP scan dashboard, showing severity, status, compliance impact, and suggested fixes.
    - Reports can be exported for audit/evidence.

#### Hypothetical User Scenario

> **Jane**, DevSecOps Lead, pushes a new release to the MCP repo. Threat Shield automatically kicks off a scan. Within minutes, Jane sees 13 new findings—two critical SQL injection issues, several failed PCI controls, and a high-risk secrets leak. The LLM-generated explanations help her prioritize fixes, and she exports a compliance report for the next audit.

---

## Compliance Mapping Table

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

*Each finding in the dashboard is automatically mapped to these standards using probe/static analysis metadata and logic. Compliance impact is shown per issue and in summary cards.*

---

## Example User Scenarios

1. **Threat Modeling**:  
   - Security engineer uploads system DFDs and architecture; dashboard instantly shows unresolved STRIDE threats, failed PCI controls, and actionable fixes.
2. **LLM Scanning**:  
   - AI/ML lead tests a chatbot with Garak probes; dashboard highlights prompt injection risk and GDPR compliance issues; fixes are applied and risk drops.
3. **MCP Scanning**:  
   - DevSecOps lead triggers a code scan; Semgrep finds vulnerabilities, LLM explains and maps them to OWASP and compliance, all results are reviewed and exported for audit.

---

## Tech Stack

- **Backend:** Python (FastAPI), REST API, JWT Auth
- **Frontend:** Next.js (TypeScript), Tailwind CSS, Lucide React, React
- **LLM Security:** Garak (probe framework)
- **Code Scanning:** Semgrep (static analysis)
- **Database:** Configurable (SQLite/Postgres)

---

## Support

- 📧 Email: [nikhil@cyberultron.com](mailto:nikhil@cyberultron.com)

---

**Threat Shield** — Automated, actionable security for every layer of your modern software stack.  
*Proudly a part of ZeroShield. All rights reserved.  
CyberUltron Consulting Private Limited.*
