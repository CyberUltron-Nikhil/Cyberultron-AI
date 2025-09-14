# Threats Identified, Now What? Implementing Effective Security Mitigations 🛡️

So far, we've identified threats, vulnerabilities, and prioritized them based on risk. Now, it's time for the most crucial step: taking action. This week, we'll shift our focus from analysis to implementation by exploring mitigations, the security controls that reduce or eliminate risks.

---

## What are Mitigations (or Controls)?

A mitigation is a step, a process, or a security control that you implement to either prevent a threat from succeeding or to reduce its impact if it does. Think of them as the countermeasures you put in place to protect your system from the dangers you've identified.

There are different types of controls, but in threat modeling, we primarily focus on:

- **Preventative controls** → stop attacks before they happen  
- **Detective controls** → alert you to an attack in progress or after it has occurred  

---

## Common Mitigations and How They Work

Here are some of the most common and effective mitigations you can implement, directly related to the threats we've discussed:

- **Input Validation**  
  *Preventative control* that checks and sanitizes all user input to ensure it is in the correct format and doesn't contain malicious code.  
  **Threat Mitigated:** Prevents injection attacks like SQL Injection or Command Injection.

- **Multi-Factor Authentication (MFA)**  
  *Preventative control* that requires users to provide two or more verification factors to gain access.  
  **Threat Mitigated:** Reduces the risk of Spoofing Identity via stolen passwords.

- **Rate Limiting**  
  *Preventative control* that restricts the number of requests a user or IP address can make within a specific time frame.  
  **Threat Mitigated:** Prevents brute-force attacks and limits the impact of DoS attacks.

- **Web Application Firewall (WAF)**  
  *Preventative control* that monitors and filters traffic between a web application and the internet.  
  **Threat Mitigated:** Blocks SQL Injection, XSS, and other common attack vectors.

- **Logging and Monitoring**  
  *Detective control* that records system activity and raises alerts for suspicious behavior.  
  **Threat Mitigated:** Helps identify and respond to attacks like Repudiation and Tampering.

---

## Mapping Threats to Mitigations

The true value of this step is linking the specific threats you've found to the mitigations you plan to implement. This ensures your security efforts are purposeful and effective.

| Threat Identified       | Vulnerability              | Recommended Mitigation                    |
|--------------------------|----------------------------|-------------------------------------------|
| Spoofing Identity        | Weak password policy       | Multi-Factor Authentication (MFA)         |
| Tampering                | Unvalidated user input     | Robust input validation and sanitization  |
| Information Disclosure   | Verbose error messages     | Generic error messages; proper logging    |
| Denial of Service (DoS)  | Missing rate limiting      | Implement rate limiting on all APIs       |

---

## Export to Sheets  

By systematically implementing these controls, you can significantly reduce your system's overall risk posture.

---

## What’s Next?  

In our next blog post of the core series, we’ll talk about the importance of **documentation and maintaining your threat model**. A threat model is a living document, and keeping it up to date is key to long-term security.
