# 🧠 Your Regex WAF Can’t Stop This: ZAPISEC vs API Recon Bots

Modern bots are no longer just brute-force scripts. They’re intelligent, stealthy, and often powered by the same LLMs we use to protect against them. Among the most dangerous is the **API Reconnaissance Bot** — bots that don’t attack directly but map your entire API surface to find vulnerabilities before launching a full-scale strike.

❗Traditional Web Application Firewalls (WAFs) using regex rules fail at this stage. Why? Because intent isn’t in the syntax — it’s in the sequence, timing, and behavior.

---

## ⚔️ The New Threat: Recon Bots Trained to Outsmart Regex

Modern recon bots are designed by developers using ChatGPT or GPT-4 to discover hidden API paths, test edge cases, and fingerprint backend behavior.

**What They Do:**
- Crawl `/swagger`, `/openapi`, `/internal`, `/debug`, and undocumented endpoints
- Try malformed requests to infer input validation logic
- Log response codes (403, 500, 200) to deduce protection layers
- Use headless browsers or real user-agents to bypass bot detection

> 💡 Recon bots are like silent burglars checking every window — they don’t break in yet, but they’re planning to.

---

## ❌ Why Regex Fails

Most WAFs rely on:
- Hardcoded rules like blocking `../`, `<script>`, or SQL keywords
- Rate limits that don’t apply to slow, timed probes
- Static IP bans, which are useless against proxy/VPN rotation

But these bots:
- Randomize request sequences
- Use LLM-generated payloads that pass regex rules
- Spread scans over days or weeks

> Regex sees one tree. ZAPISEC sees the whole forest.

---

## ✅ ZAPISEC’s LLM-Based Recon Detection Engine

ZAPISEC doesn’t just inspect the packet — it understands the **intent** behind it using a real-time Generative AI pipeline.

---

### 🧬 Core Modules

#### 🔍 Intent Extraction via LLMs
- Analyzes parameter names, payload structure, method sequences
- Identifies recon flows like auth-bypass trials, version sniffing, or input fuzzing

#### 🔁 Sequence Anomaly Modeling
- Tracks logical flow: `GET /login → POST /config → GET /debug`
- Flags illogical or suspicious access paths not seen in normal usage

#### 🧮 Entropy-Based Endpoint Scoring
- High-entropy endpoint paths (`/v1/%24config/9dZ`) usually signal automation
- Compared to typical user traffic, recon bot paths spike entropy scores

#### 🕸️ Behavior Graph Matching
- Connects the dots across sessions to model "probing trails"
- Uses graph AI to detect recon behaviors spanning 1000s of small requests

---

## 🔥 Real Case Study: Bot Trained via GPT-4

A recon bot, created using ChatGPT plugins, was used to crawl a fintech API.

**Observed:**
- Payloads looked clean
- Used curl, axios, python-requests, and fetch to rotate signatures
- Targeted `/transactions/preview`, `/internal/billing/test`, `/v2/config`

**ZAPISEC Detected:**
- Entropy score > 9.1 (vs normal ~3.2)
- API access flow violated application graph logic
- Bot fingerprint matched previous threat campaign variants

**→ Result:**
- Endpoint quarantined
- Traffic routed to deception service
- Attacker IP traced to bot marketplace logs

---

## 📈 Visuals to Include
![WhatsApp Image 2025-06-14 at 12 33 28_1bbedf43](https://github.com/user-attachments/assets/6de310f1-3d0c-404e-914e-f621d56986b4)
Stealth API Recon Bot mimics real traffic, slowly mapping endpoints without triggering alerts.



![WhatsApp Image 2025-06-14 at 12 34 29_78de07c1](https://github.com/user-attachments/assets/ee764253-410b-4459-87f0-477bea0f3cb7)
Recon bots show low entropy in API access patterns — spotted by ZAPISEC’s anomaly models.



### 1️⃣ Intent Extraction Heatmap  
_Visualizes which API calls were flagged as recon-like based on LLM interpretation._

```plaintext
+------------------------+--------------+
| Endpoint               | Recon Score  |
+------------------------+--------------+
| /v1/profile            | 0.2          |
| /v1/internal/debug     | 0.91 🔥      |
| /admin/logs/archive    | 0.88 🔥      |
| /v1/config-preview     | 0.79         |
+------------------------+--------------+

### 2️⃣ Behavior Flow Graph
Mermaid diagram showing a suspicious access trail.
graph TD
  A[GET /login] --> B[POST /v1/config-preview]
  B --> C[GET /internal/debug]
  C --> D[GET /admin/logs/archive]

### 3️⃣ Entropy Score Timeline
Shows an entropy spike as recon bot accessed high-variance paths.
| Time       | Avg Entropy |
|------------|-------------|
| 12:01:22   | 3.1         |
| 12:01:24   | 3.3         |
| 12:01:26   | 9.4 🚨      |
| 12:01:29   | 8.8 🚨      |
### 4️⃣ Regex WAF vs ZAPISEC Accuracy Table
| Feature                         | Regex WAF | ZAPISEC |
| ------------------------------- | --------- | ------- |
| Detects slow probe bots         | ❌         | ✅       |
| Understands intent in sequences | ❌         | ✅       |
| Learns over time                | ❌         | ✅       |
| Uses behavioral graphs          | ❌         | ✅       |
| Handles LLM-crafted payloads    | ❌         | ✅       |

