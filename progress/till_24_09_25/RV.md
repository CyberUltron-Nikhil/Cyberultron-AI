# Threat Shield

<div align="center">
   <img width="200" height="200" alt="Threat Shield (ZAPESIC) Logo" src="https://github.com/user-attachments/assets/03398106-6184-47b0-b1f4-403d375f2eba" />
   <br />
   <em>Threat Shield, a part of <a href="https://zeroshield.ai">ZeroShield</a></em>

   
</div>
  <div align="center">
    <img src="https://img.shields.io/badge/Launching_Publicly-October_8th-red?style=for-the-badge" alt="Launching October 8th" />
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
- [Feature Overview](#feature-overview)
  - [1. Threat Modeling of Normal Systems](#1-threat-modeling-of-normal-systems)
  - [2. LLM Vulnerability Testing (with Garak Probes)](#2-llm-vulnerability-testing-with-garak-probes)
  - [3. MCP Server Vulnerability Scanning](#3-mcp-server-vulnerability-scanning)
- [Compliance Mapping](#compliance-mapping)
- [Example Workflows & User Benefits](#example-workflows--user-benefits)
- [Use Cases](#use-cases)
- [Tech Stack](#tech-stack)
- [Case Studies & Research](#case-studies--research)
- [Support](#support)
- [Get Involved](#get-involved)

---

## About Threat Shield
**Threat Shield** is an advanced **threat modelling platform** within the **[ZeroShield](https://zeroshield.ai)** platform, designed to give organizations deep, actionable insight into risks across classic applications, codebases, and cutting-edge GenAI/LLM integrations.Threat Shield unifies real-time threat modeling, LLM security probing via Garak, and MCP codebase vulnerability scanning for a complete, compliance-ready view of your security posture.


---

## Core Mission

Empower teams to rapidly identify, understand, and remediate security risks—across all technologies—by automating threat analysis, vulnerability detection, and compliance mapping. **Threat Shield** bridges the gap between security, development, and compliance, enabling secure digital innovation.

---
## Why Threat Shield? 

> **Automate security. Accelerate compliance.**  
> Threat Shield transforms complex, manual security and compliance challenges into automated, actionable insights—empowering you to prevent incidents, pass audits, and build securely at speed.

---

## Key Capabilities

- Automated Threat Modeling for Classic and Cloud-Native Systems
- Advanced LLM Vulnerability Testing (with deep Garak Probe analysis)
- MCP Server-Based Vulnerability Scanning & Compliance (LLM analysis)
- Real-Time Compliance & OWASP Top 10 Mapping (ISO, PCI, SOC2, NIST, GDPR)
- Unified Risk Analytics & Visualizations

---

## Target Users

- **Security Engineers:** Automate threat modeling, vulnerability scanning, and compliance.
- **Developers & DevOps:** Integrate risk analysis into CI/CD and shift security left.
- **AI/ML & Product Teams:** Secure and validate LLM/GenAI features with real security probes.
- **Compliance & Audit:** Map vulnerabilities to compliance frameworks and track remediation.
- **Cloud & Solution Architects:** Design secure architectures with instant, actionable feedback.

---

## Feature Overview

### 1. Threat Modeling of Normal Systems

#### Demo Video

<div align="center">
  <a href="https://github.com/user-attachments/assets/10ec45b0-a35f-45a7-a03f-c11f754e11b8">
    <img src="https://img.shields.io/badge/🎥_Watch_Threat_Modeling_Demo-blueviolet" alt="Watch Threat Modeling Demo Video" />
  </a>
</div>

#### What Users See & How It Works

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

### Threat Modeling Project Dashboard

<img width="800" height="600" alt="Screenshot 2025-09-29 173615" src="https://github.com/user-attachments/assets/a1e67280-139d-4392-a8db-52b77ae312ae" />


**Description:** The main dashboard for a **Threat Modeling** project, showcasing the system's overall risk score (6.5), key metrics like **Total STRIDE Threats** (6 identified, 6 unresolved), and the high-level **DREAD Heat Map** for rapid risk prioritization.



#### What/Why of Each Visualization
- **Summary Cards:** Instantly see the scale and urgency of risk in the system.
- **DREAD Heatmap:** Pinpoints highest-impact threats for prioritization.
- **Failed Controls:** Shows direct compliance gaps (e.g., SOC2, PCI).
- **OWASP Tracker:** Maps findings to industry standards for external reporting.
- **Attack Trees:** Helps visualize possible attack paths and lateral movement.
- **Threat Table:** Enables fast triage, assignment, and remediation tracking.


### Threat Modeling Attack Tree and OWASP Tracker

<img width="800" height="600" alt="Screenshot 2025-09-29 173641" src="https://github.com/user-attachments/assets/8c002fc9-6bcb-44cd-b4f9-d83b1006568f" />


**Description:** An in-depth view of the **Threat Modeling** dashboard, displaying the **PASTA Attack Tree** visualization to map out potential attack paths and lateral movement. It also highlights the **OWASP Top 10 Tracker**, showing 3 of 10 categories triggered, including **Identification and Authentication Failures** (A07) and **Security Misconfiguration** (A05).




### Threat Modeling Finding Details

<img width="800" height="600" alt="Screenshot 2025-09-29 173717" src="https://github.com/user-attachments/assets/5676290d-9dcd-4cb3-835f-d0aced641e6f" />


**Description:** An expanded view of a Threat Modeling finding, detailing an **API Key Exposure** threat. It shows the impact across five major compliance frameworks (**ISO, NIST, PCI DSS, GDPR, SOC 2**), the associated **OWASP Broken Access Control** (A01:2021) vulnerability, and a comprehensive, actionable **Suggested Fix** for secure key management.



### Threat Modeling Finding Scoring and Compliance

<img width="800" height="600" alt="Screenshot 2025-09-29 173703" src="https://github.com/user-attachments/assets/a84bcd7b-2472-4962-9474-1b548e0ff671" />


**Description:** The top portion of the Threat Modeling finding details, clearly showing the threat's **High Severity**, the associated **STRIDE Categories** (S-Spoofing, I-Information Disclosure), **DREAD Scores** for risk calculation, and a comprehensive list of affected **Compliance Controls** across ISO, NIST, PCI DSS, GDPR, and SOC 2.


#### Deep-Dive: How It Works
- Upload system diagrams, code, and metadata.
- The engine analyzes flows, trust boundaries, and identifies threats using STRIDE, DREAD, and OWASP logic.
- Each threat is auto-mapped to compliance controls.
- Dashboard and report update in real-time as threats are resolved.

#### Hypothetical User Scenario

> **Alice**, a Security Engineer, is onboarding a new payments platform. She uploads the system’s DFDs and architecture, connects the GitHub repo, and sets data sensitivity. Threat Shield instantly generates a threat model showing 23 STRIDE threats, highlighting 7 unresolved high-risk issues and 2 failed PCI compliance controls. Using the heatmap and attack tree, Alice quickly triages which risks to escalate to DevOps for urgent fixes, and exports a report to satisfy the next audit.



### 2. LLM Vulnerability Testing (with Garak Probes)

#### Demo Video

<div align="center">
  <a href="https://github.com/user-attachments/assets/8dd9b7b6-4781-4b37-8a62-788bc274b79d">
    <img src="https://img.shields.io/badge/🎥_Watch_LLM_Scanning_Demo-blueviolet" alt="Watch LLM Scanning Demo Video" />
  </a>
</div>

#### What Users See & How It Works

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


#### In-Depth Garak Probe Coverage

- **Garak probes** test models for:  
  - ANSI escapes, attack generation, audio attacks, antivirus/spam bypass, data leakage, prompt injection, roleplay/jailbreaks, SQLi, XSS, hallucinated package names, adversarial suffixes, emotional manipulation, and more.
- **LLM Exposure Analysis:**  
  - Beyond probe results, Threat Shield analyzes the LLM's exposure and risk posture, surfaces all successful bypasses, and maps to OWASP Top 10 and failed compliance controls.

### LLM Probe Finding Details

<img width="800" height="600" alt="Screenshot 2025-09-29 173750" src="https://github.com/user-attachments/assets/cd7f2baf-b9ee-48fa-8492-1d30119877ca" />


**Description:** A deep-dive into an LLM security finding, showing the results of a **malwaregen.Evasion** Garak probe. The panel displays the **Medium Risk Level**, a **20.8% hit rate**, failed compliance controls like **Malware Detection and Prevention**, and the specific **LLM-generated remediation fix** to update detection rules.



#### Deep-Dive: Garak Probe System

Threat Shield leverages the **Garak** framework for LLM security, running dozens of real-world probe categories:

| Probe Category         | What It Tests                                                             | Why It Matters                        |
|-----------------------|--------------------------------------------------------------------------|---------------------------------------|
| ANSI Escape           | Model exposes terminal codes                                              | Downstream system compromise          |
| Attack Generation     | Can model be tricked into toxic/illegal output                            | Content moderation, brand risk        |
| Audio                 | Multimodal attacks bypassing text safety                                 | Jailbreaks on non-text input          |
| AV/Spam Scanning      | Will model output malware/spam test strings                              | Bypassing security scanning           |
| Continuation/Slurs    | Model completes offensive/inappropriate words                            | Social/ethical risk                   |
| Data Leakage          | Model repeats training data                                               | Confidentiality breach                |
| Doctor/Roleplay       | Policy puppetry to bypass safety                                         | Regulatory/safety risk                |
| Encoding/Jailbreak    | Can model decode/obfuscate harmful payloads                              | Filter bypass, prompt injection       |
| Exploitation (SQLi)   | Model can output exploitable code                                        | Direct app/system compromise          |
| Fileformats           | Model exposes details about underlying files                             | Environment leakage                   |
| Glitch Tokens         | Model misbehaves on edge tokens                                          | Model stability, DoS                  |
| Goodside/Malwaregen   | Known adversarial/prompt injection patterns                              | Real-world exploit research           |
| Grandma/Emotional     | Will model yield to emotional manipulation                               | Social engineering risk               |
| Hallucination         | Model invents fake package/library names                                 | Supply chain attack                   |
| Prompt Injection      | Model can be hijacked to output specific strings                         | LLM-powered app hijacking             |
| XSS/Visual Jailbreak  | Model outputs code/image links for data exfiltration                     | Web/visual AI security                |
| Latent Injection      | Model attacked through hidden instructions in data                        | RAG, document QA system risk          |

> **Further Analysis:**  
> Beyond these probes, Threat Shield analyzes all probe results for exposure patterns—automatically scoring LLM risk, mapping incidents to OWASP Top 10 and compliance controls, and surfacing which prompt/attack types are most dangerous in your use case.

#### How It Benefits Users

- **Real-world attack simulation** using the latest security probe techniques.
- **Immediate understanding of LLM weaknesses and exposure.**
- **Human-readable explanations and remediation steps** for every finding.
- **Continuous assessment** as models/prompts evolve.
- **Supports secure, compliant AI adoption** in any environment.

#### Hypothetical User Scenario

> **Raj**, an AI/ML Product Lead, is launching a GenAI-powered helpdesk. He runs a Threat Shield LLM scan, which executes 40+ Garak probes. The dashboard reveals a high hit rate for prompt injection and roleplay attacks, and a failed GDPR control. Raj reviews the suggested fixes, patches the prompt template, and re-runs the scan—dropping risk level to “Low” and passing all compliance checks before go-live.




### 3. MCP Server Vulnerability Scanning

#### Demo Video

<div align="center">
  <a href="https://github.com/user-attachments/assets/b41ce23a-b494-49ae-81d4-46ec39a3a7ef">
    <img src="https://img.shields.io/badge/🎥_Watch_MCP_Scanning_Demo-blueviolet" alt="Watch MCP Scanning Demo Video" />
  </a>
</div>

#### What Users See & How It Works


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

- **Scan Limits**: Supports repositories up to **[INSERT SIZE LIMIT HERE]** for GitHub/GitLab integration.


### MCP Scan Project Dashboard

<img width="800" height="600" alt="Screenshot 2025-09-29 173159" src="https://github.com/user-attachments/assets/3d041883-97bb-48b0-bbab-c5029d929e57" />


**Description:** The dashboard for an **MCP Server Vulnerability Scan**, providing an executive summary with **Total Findings** (5), **High Risk** items (5), and the primary development language (Python). It also displays a list of detected **OWASP Vulnerabilities** (A03, A06, A04, A01) and a visualization of **Failed Compliance Controls** over time.




### MCP Finding Details

<img width="800" height="600" alt="Screenshot 2025-09-29 173534" src="https://github.com/user-attachments/assets/9e787855-371a-45c5-8daa-855e9798819c" />


**Description:** A detailed view of a security finding from the MCP Server scan, specifically the **detect-command-execution** rule. The panel highlights the affected code snippet, relevant compliance controls (**NIST SP 800-53** and **PCI DSS**), the associated **OWASP Injection** vulnerability (A03:2021), and the **LLM-generated recommended fix** to prevent unauthorized command execution.


#### What/Why of Each Visualization
- **Summary Cards:** Snapshot of codebase health and urgency.
- **Failed Controls:** Highlights direct compliance impact.
- **OWASP Card:** Maps code issues to industry standards.
- **Threat Graph:** Visualizes risk over time or per category.
- **Result Table:** Drill down to every finding, fix, and compliance mapping.

  
#### Technical Workflow

- **Phase 1:**  
  - Repository is temporarily cloned and scanned for static code analysis.
  - The system flags all code patterns matching vulnerability rules.
- **Phase 2:**  
  - Each finding is analyzed by an LLM to generate explanations and actionable fixes.
  - Further mapped to **OWASP Top 10** vulnerabilities and failed compliance controls (ISO 27001, PCI DSS, NIST, SOC2, GDPR, etc.).
  - Compliance mapping is visualized per finding and overall scan.


### Code-Level Finding Explanation

<img width="800" height="600" alt="Screenshot 2025-09-29 173512" src="https://github.com/user-attachments/assets/445c5c0b-95bd-4cb7-9167-b0466bb3a638" />


**Description:** A close-up view of the code analysis within the MCP Scan, showing the exact file (**mcp_server.py**) and code snippet where the vulnerability was detected. The finding is given a **Medium** risk severity, accompanied by an LLM-generated **Explanation** of the command execution risk found in the code.


 

#### Deep-Dive: Analysis Pipeline

- **Step 1: Static Analysis**
    - When a scan is triggered, Threat Shield temporarily clones the selected MCP repository.
    - **The system** runs a suite of static analysis rules covering OWASP Top 10, common code smells, secrets, and insecure configurations.
    - **The analysis engine is chosen for its speed, accuracy, and extensibility (custom rules per project/language).**
- **Step 2: LLM-Powered Findings**
    - Each finding is passed to an LLM for further analysis, generating:
        - Human-readable explanation of risk
        - Contextual remediation steps
        - Mapping to compliance controls (ISO, PCI, SOC2, NIST, GDPR, etc.)
- **Step 3: Dashboard and Reporting**
    - All results are visualized in the MCP scan dashboard, showing severity, status, compliance impact, and suggested fixes.
    - Reports can be exported for audit/evidence.


#### How It Benefits Users

- **Automated, deep static analysis** on every codebase.
- **LLM-powered explanations** for fast triage and remediation.
- **Clear compliance gap visibility** for every finding.
- **Audit-ready reporting** and compliance evidence on demand.

#### Hypothetical User Scenario

> **Jane**, DevSecOps Lead, pushes a new release to the MCP repo. Threat Shield automatically kicks off a scan. Within minutes, Jane sees 13 new findings—two critical SQL injection issues, several failed PCI controls, and a high-risk secrets leak. The LLM-generated explanations help her prioritize fixes, and she exports a compliance report for the next audit.


---

## Compliance Mapping

| Vulnerability / Threat Type                | OWASP Top 10 | ISO 27001 | PCI DSS | SOC2 | NIST | GDPR |
|--------------------------------------------|:------------:|:---------:|:-------:|:----:|:----:|:----:|
| Insecure Authentication                    | A07          | ✓         | ✓       | ✓    | ✓    | ✓    |
| Injection (SQLi, Command, etc.)            | A03          | ✓         | ✓       | ✓    | ✓    |      |
| Data Exposure/Leakage                      | A01, A06     | ✓         | ✓       | ✓    | ✓    | ✓    |
| Security Misconfiguration                  | A05          | ✓         | ✓       | ✓    | ✓    |      |
| Vulnerable/Outdated Components             | A06          | ✓         | ✓       | ✓    | ✓    |      |
| Prompt Injection (LLM)                     | A01, A05     |           |         |      |      | ✓    |
| Malicious Code Generation                  | A06, A10     | ✓         |         |      |      |      |
| Compliance Control Failure (General)       | All          | ✓         | ✓       | ✓    | ✓    | ✓    |

*Each finding in the dashboard is automatically mapped to these standards using probe/static analysis metadata and logic. Compliance impact is shown per issue and in summary cards.*


## Example Workflows & User Benefits

**Threat Modeling Workflow:**  
- Upload system diagrams and architecture details, review generated threat model, prioritize/assign remediation, track resolution and compliance mapping.
- Dashboard instantly shows unresolved STRIDE threats, failed PCI controls, and actionable fixes.

**LLM Security Workflow:**  
- Register LLM/GenAI features for assessment, receive prioritized vulnerability reports with Garak probe detail, act on LLM-generated fix steps, monitor ongoing risk.
-  AI/ML lead tests a chatbot with Garak probes; dashboard highlights prompt injection risk and GDPR compliance issues; fixes are applied and risk drops.

**MCP Vulnerability Workflow:**  
- Trigger scan for MCP repositories, review findings and LLM explanations, analyze OWASP/compliance mapping, assign remediations, produce compliance-ready reports.
- DevSecOps lead triggers a code scan; the system finds vulnerabilities, LLM explains and maps them to OWASP and compliance, all results are reviewed and exported for audit.

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
- **Code Scanning:** Static Analysis Engine
- **Database:** Configurable (e.g., SQLite/Postgres)

---

## Case Studies & Research
A public repository of case studies, research papers, and technical deep-dives will be made available soon (from October 8th onwards).

---

## Support

- 📧 Contact: [vartul@zeroshield.ai](mailto:vartul@zeroshield.ai)
- 📧 Support Queries: [support@zeroshield.ai](mailto:support@zeroshield.ai)

---


> **Value Proposition:**  
> Unified, automated threat modeling and vulnerability management for the next generation of enterprise security
> "Thraet Shield turns complex, manual security and compliance challenges into automated, actionable insights—empowering teams to move faster, safer, and with confidence."
*Threat Shield, a part of [ZeroShield](https://zeroshield.ai), brings in-depth, practical security to every step of your development and deployment lifecycle.*

---

## Get Involved

We welcome contributions from the security community! Here's how you can get involved with Threat Shield:

### 🤝 Contributing

- **Report Issues**: Found a bug or have a feature request? Open an issue on our repository
- **Code Contributions**: Submit pull requests to help improve Threat Shield
- **Documentation**: Help improve our documentation and examples
- **Security Research**: Contribute new threat models, attack patterns, or vulnerability tests

### 🔗 Community

- **GitHub Discussions**: Join our community discussions and share ideas
- **Security Research**: Collaborate on new security analysis techniques
- **Feedback**: Share your experience using Threat Shield in your organization

### 📞 Contact

- **General Contact**: [vartul@zeroshield.ai](mailto:vartul@zeroshield.ai)
- **Support**: [support@zeroshield.ai](mailto:support@zeroshield.ai)
- **Partnerships**: [partnerships@zeroshield.ai](mailto:partnerships@zeroshield.ai)

---

All rights reserved. This software and its documentation are the intellectual property of [ZeroShield](https://zeroshield.ai).

---
