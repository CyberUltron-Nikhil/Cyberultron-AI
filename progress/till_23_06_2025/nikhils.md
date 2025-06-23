# Threat Modelling features

## SAST (Static Application Security Testing)
### Features:
- Source code scanning for vulnerabilities.
- AI-powered False Positive Reduction.
- Git integration (GitHub/GitLab).
- Actionable dashboard with highlighted vulnerable code and AI-generated fix suggestions.
### Open-Source Software:
- Engine: Semgrep
- https://github.com/semgrep/semgrep
- https://semgrep.dev/docs/getting-started/quickstart
## SCA (Software Composition Analysis)
### Features:
- Scanning of open-source dependencies for vulnerabilities.
- AI-powered Reachability Analysis to prioritize active risks.
- Generation of dependency lists with version, license, and vulnerability status.
### Open-Source Software:
- https://github.com/semgrep/semgrep
- https://semgrep.dev/docs/getting-started/quickstart
- https://trivy.dev/latest/docs/target/container_image/
- https://owasp.org/www-project-dependency-check/
- Engines: Trivy, OWASP Dependency-Check
- Data Sources: NVD (National Vulnerability Database), OSV.dev
## DAST (Dynamic Application Security Testing)
### Features:
- Dynamic scanning of running web applications and APIs.
- Isolated infrastructure to run scans securely.
- A unified dashboard to correlate DAST, SAST, and SCA findings.
- AI-enhanced Intelligent Crawling to prioritize critical user paths.
- AI-driven Adaptive Testing that adjusts attack patterns based on application responses.
### Open-Source Software:
- https://www.zaproxy.org/
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


## Github/GitLab integration 
| Feature | Requires Git Integration? | Primary Reason                                               |
| :------ | :------------------------ | :----------------------------------------------------------- |
| **SAST** | **Yes (Essential)** | Needs to access and read the application's source code.      |
| **SCA** | **Yes (Essential)** | Needs to access and read the project's dependency files.   |
| **DAST** | **No, but ca be done** | Core function only needs a URL, but integration enables CI/CD automation and better context. |