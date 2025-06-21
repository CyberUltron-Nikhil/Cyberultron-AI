# List of features for SaaS

## SAST (Static Application Security Testing)
### Features:
- Source code scanning for vulnerabilities.
- AI-powered False Positive Reduction.
- Git integration (GitHub/GitLab).
- Actionable dashboard with highlighted vulnerable code and AI-generated fix suggestions.
### Open-Source Software:
- Engine: Semgrep
## SCA (Software Composition Analysis)
### Features:
- Scanning of open-source dependencies for vulnerabilities.
- AI-powered Reachability Analysis to prioritize active risks.
- Generation of dependency lists with version, license, and vulnerability status.
### Open-Source Software:
-Engines: Trivy, OWASP Dependency-Check
- Data Sources: NVD (National Vulnerability Database), OSV.dev
## DAST (Dynamic Application Security Testing)
### Features:
- Dynamic scanning of running web applications and APIs.
- Isolated infrastructure to run scans securely.
- A unified dashboard to correlate DAST, SAST, and SCA findings.
- AI-enhanced Intelligent Crawling to prioritize critical user paths.
- AI-driven Adaptive Testing that adjusts attack patterns based on application responses.
### Open-Source Software:
- Engine: OWASP ZAP (Zed Attack Proxy)

## LLM Red Teaming
### Features:

- Testing Large Language Models for bias, toxicity, data leakage, and resistance to prompt injection.
- A "Dual LLM System" architecture, featuring an "Attacker LLM" to generate adversarial prompts and a "Judge LLM" to evaluate the responses.
A library of pre-built attack prompt templates.
- Detailed reports that classify the risks found.
- A UI gallery to review each interaction (prompt, response, and the judge's verdict).
### Open-Source Software/Frameworks:

The document describes an architecture rather than a single, specific open-source engine like in the other categories. You would build this feature by integrating various open-source libraries (e.g., from Hugging Face) to create the "Attacker" and "Judge" LLM system and manage the library of prompt templates.