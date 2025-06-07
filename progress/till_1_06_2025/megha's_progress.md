# 🛡️ Detecting Bot Crawlers with Generative AI: A ZAPISEC Case Study

In today’s web-scale applications, distinguishing legitimate traffic from stealthy bots like **GoogleBot**, **BaiduBot**, **YahooBot**, or malicious crawlers is critical. These bots can silently flood your API, skew analytics, and even launch **Slowloris-style DDoS attacks** — all while bypassing traditional security rules.

ZAPISEC, a GenAI-powered API firewall, solves this with **real-time anomaly detection** fueled by **Generative AI, Isolation Forests, and LSTM Autoencoders**— even when data flows in **gigabytes to petabytes per day**.

---

## 🧨 Problem: Stealth Bot Crawlers & Layer 7 DDoS (e.g., Slowloris)

Bots often:

- Spoof headers & IPs (fake GoogleBot)
- Send slow, partial HTTP headers to hold sockets open (Slowloris)
- Exploit server thread exhaustion with minimal bandwidth

This makes them *invisible to traditional WAFs* that rely on regex rules or IP reputation.

---

## ⚙️ ZAPISEC’s Generative AI–Based Defense Strategy

### ✅ 1. **Real-Time Bot Fingerprinting**
ZAPISEC captures unique signals like:

- TCP/IP patterns (TTL, window size)
- TLS metadata (JA3 hashes)
- Browser JS behavior (headless checks)
- HTTP header anomalies (delayed or incomplete headers)

These are analyzed in <10ms at the edge.

---

### ✅ 2. **Generative AI Anomaly Detection Engine**

Using **Isolation Forest + LSTM Autoencoders**, ZAPISEC models:

- Normal request timings, header sequences, user-agent entropy
- Anomalies like prolonged socket life or slow POST/GET patterns
- Synthetic bot samples created via Generative Adversarial Networks (GANs)

---

### ✅ 3. **Multilayer Throttling & Response Logic**

- **Good bots** (verified GoogleBot) are allowed with trust scores.
- **Malicious bots** are:
  - Dropped
  - Served a synthetic 200 OK with no backend hit
  - Given CAPTCHA or JS challenges
- Adaptive thresholds change in real-time based on LLM insights.

---

## 📊 Generated Visualizations

### 📈 Anomaly Score Timeline
Shows sudden spikes in anomaly scores when bot-like behavior appears.

[Anomaly Score Timeline] ![image](https://github.com/user-attachments/assets/1ade7f07-66b7-4e30-a384-ec066c5ec9ba)
A dynamic time-series graph showing real-time anomaly scores spiking whenever bot-like behaviors are detected.
The X-axis represents request timestamps; the Y-axis shows anomaly confidence (0 to 1).
Legitimate traffic stays around ~0.1–0.2.
Sudden spikes up to 0.9+ highlight suspicious patterns like slow header delivery or high entropy in requests.
Marked events show GAN-generated synthetic bot traces matching real traffic anomalies.
Purpose:
Visualizes the exact moment ZAPISEC's Generative AI detects a deviation from baseline behavior — proving proactive detection.

---

### 🔥 Connection Age Heatmap
Visualizes long-lived connections (a Slowloris signature) across IPs.

[Connection Age Heatmap]![image](https://github.com/user-attachments/assets/426436ee-cb3e-4a5c-b4ff-7b63f45dacc7)
A heatmap where each cell represents an IP address and the intensity represents the average "open socket time".
Slowloris bots appear as deep red clusters (long-lived idle connections), while regular users are cool blue.
Time on X-axis; IPs on Y-axis.
You’ll notice persistent red zones indicating a botnet using distributed slow attacks.
Purpose:
Highlights the classic Layer 7 DoS pattern: bots holding sockets open to exhaust server threads. This heatmap shows the visibility ZAPISEC gives at a network level.


---

### ⏱️ Header Completion Delta Plot
Bots often trickle header bytes. This plot shows delay in full HTTP header delivery.

[Header Completion Delta Plot] ![image](https://github.com/user-attachments/assets/38c30014-5411-4f45-aefc-1cd1c97b5d50)
A scatter plot showing the delta (delay) between the TCP connection opening (SYN-ACK) and full header completion.
Legitimate browsers complete headers in <300ms.
Bots using trickle tactics stretch this to 2–5 seconds.
Plot shows clear outliers flagged by ZAPISEC, correlating with injected synthetic header sequences for detection benchmarking.
Purpose:
Proves how even advanced trickling bots (Slowloris-style) can't hide from ZAPISEC’s behavioral timing analysis.


---

### 📉 Socket Exhaustion Forecast
Predicts future server exhaustion probability due to idle, open sockets.

[Socket Exhaustion Forecast]![image](https://github.com/user-attachments/assets/7dea7915-3353-459e-8371-015d56d3fcb8)
A predictive line chart forecasting server resource usage over time based on current active connections, their age, and completion rate.
Projected exhaustion threshold is shown as a red line.
As bot activity increases, the forecast sharply approaches the threshold.
Annotations show exactly when ZAPISEC begins dropping, sandboxing, or redirecting traffic to synthetic backends.
Purpose:
Illustrates ZAPISEC's foresight — not only detecting bots but predicting impact and acting before service degradation occurs.




---

## 🧪 Feature Engineering Used in GenAI Model

| Feature Name            | Description |
|-------------------------|-------------|
| `header_completion_time` | Delay from SYN to first full header |
| `open_socket_duration`  | Time connection remains open without completion |
| `header_entropy`        | Randomness in header order/values |
| `request_body_delay`    | Delay between headers and body |
| `tcp_retransmission_count` | Signs of stalled connections |
| `anomaly_score`         | Output from AE or GAN models |

---

## 🛠️ Real-World Mitigation Flow

A ZAPISEC customer experienced slow API performance on `/checkout`. Here’s what happened:

1. GenAI detected **header trickling** from multiple regions.
2. Slowloris anomaly score > threshold.
3. ZAPISEC:
   - Dropped slow headers
   - Sent synthetic response to attacker
   - Activated Cloudflare rules via webhook
4. System retrained on attack pattern automatically.

---

## ✅ Why ZAPISEC Beats Traditional WAFs

| Feature | Traditional WAF | ZAPISEC GenAI |
|--------|------------------|----------------|
| Signature-based | ✅ | ❌ |
| Detects Low-Rate DoS | ❌ | ✅ |
| Dynamic Learning | ❌ | ✅ |
| Deep Traffic Modeling | ❌ | ✅ |
| Edge-Aware | ❌ | ✅ |

---

## 🔍 Conclusion

**ZAPISEC** combines **Generative AI, real-time detection, and adaptive policy enforcement** to stop both volumetric and stealth attacks like Slowloris.

In a world where bots evolve daily, ZAPISEC ensures your apps stay:

- Online ⚡
- Resilient 🔒
- Intelligent 🧠

> **ZAPISEC: Defend Smarter. Detect Sooner. Disrupt Threats.**

