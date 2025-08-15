# 💥What is a DDoS Attack?

In today’s connected world, online services are expected to be **available 24/7**.  
However, **Distributed Denial of Service (DDoS) attacks** remain one of the most disruptive threats to internet infrastructure.

A **DDoS attack** works by overwhelming a server, network, or application with a massive flood of traffic from **multiple sources** — usually a botnet of compromised devices.  
This makes the targeted service **slow** or completely **unavailable** to legitimate users.

---

## 🌐 How Does a DDoS Attack Work?

1. **Infection Phase** – Attackers compromise thousands (or millions) of devices using malware.
2. **Control Phase** – These devices become part of a **botnet**, controlled remotely by the attacker.
3. **Attack Phase** – The botnet simultaneously sends massive traffic to the victim’s server.
4. **Impact Phase** – The target becomes overloaded, causing service disruption or downtime.

---

## 🛠️ Types of DDoS Attacks

<img width="1514" height="288" alt="image" src="https://github.com/user-attachments/assets/8b1ca19d-d637-476a-8fbd-55089349edd7" />


### 1️⃣ Volumetric Attacks
- **Goal:** Saturate available bandwidth.
- **How:** Sending high volumes of fake traffic to overwhelm the network.
- **Example:** A **UDP Flood** sends large packets to random ports, forcing the target to respond.

---

### 2️⃣ Protocol Attacks
- **Goal:** Exploit protocol weaknesses to exhaust server resources.
- **How:** Abuse handshake processes or malformed packets.
- **Example:** **SYN Flood** sends multiple SYN requests without completing the handshake, leaving connections half-open.

---

### 3️⃣ Application Layer Attacks
- **Goal:** Crash or slow down the actual application.
- **How:** Send legitimate-looking requests at high volume to overload server processing.
- **Example:** **Slowloris** sends partial HTTP requests very slowly, keeping connections open until the server can’t handle new requests.

---

## 🔍 Visual Representation

<img width="344" height="292" alt="image" src="https://github.com/user-attachments/assets/53bba0e4-b614-4886-a185-fc8f87d2e7dc" />


