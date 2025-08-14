# 🛡️ Week 1: WAFs vs. Network Firewalls – Understanding the Difference

In modern cybersecurity, **firewalls** are often seen as the first line of defense.  
However, not all firewalls are created equal — especially when we compare **Web Application Firewalls (WAFs)** with **Network Firewalls**.  

While both aim to filter and monitor traffic, their **operating layers, inspection depth, and threat coverage** differ significantly.

---

## 🌐 What is a Web Application Firewall (WAF)?
A **Web Application Firewall** operates at the **Application Layer (Layer 7)** of the OSI model.  
It inspects **HTTP/HTTPS requests** to detect and block malicious activities targeting web applications.

A WAF focuses on **application-level threats** such as:
- **SQL Injection (SQLi)**
- **Cross-Site Scripting (XSS)**
- **Cross-Site Request Forgery (CSRF)**
- **Remote File Inclusion (RFI)**
- **Zero-Day web exploits**

**Example:**  
If an attacker tries to inject `UNION SELECT * FROM users` into a login form, the WAF can detect the malicious SQL pattern and block the request.

---

## 🔐 What is a Network Firewall?
A **Network Firewall** operates at the **Network (Layer 3)** and **Transport (Layer 4)** layers of the OSI model.  
It inspects **IP addresses, protocols, and ports** to control traffic flow between networks.

A Network Firewall focuses on **network-level threats** such as:
- Unauthorized IP access
- Port scanning
- Basic Denial-of-Service (DoS) attacks
- Protocol misuse

**Example:**  
If an attacker tries to send packets from an unauthorized IP address or uses an open port to exploit a service, the network firewall can block it.

---

## 📊 WAF vs. Network Firewall – Key Differences

| Feature | WAF | Network Firewall |
|---------|-----|------------------|
| **OSI Layer** | Layer 7 (Application) | Layers 3 & 4 (Network & Transport) |
| **Traffic Inspected** | HTTP/HTTPS content | IP, TCP, UDP packets |
| **Primary Threats** | SQLi, XSS, CSRF, RFI, Zero-Day exploits | Unauthorized access, port scanning, DoS attacks |
| **Granularity** | Deep inspection of web requests/responses | Broad filtering based on IP and port rules |
| **Protection Scope** | Web applications and APIs | Entire network perimeter |
| **Encryption Handling** | Can decrypt and inspect HTTPS traffic | Usually does not inspect encrypted payloads |
| **Adaptability** | Often uses machine learning for new threats | Mostly rule-based packet filtering |

---

## 📌 Visual Representation

```plaintext
       INTERNET
          |
    [ Network Firewall ]
          |
   ---------------
   |             |
[WAF]        Other Services
   |
Web Application
