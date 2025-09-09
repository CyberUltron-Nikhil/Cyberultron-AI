---
title: "What to Fix First? Mastering Risk Assessment with the DREAD Model 📊"
description: "Learn how to use the DREAD model for risk assessment in threat modeling. Prioritize vulnerabilities with a structured scoring system and fix what matters most first."
author: "Megha SD"
date: 2025-09-09
tags: ["Threat Modeling", "Risk Assessment", "DREAD", "Cybersecurity", "STRIDE"]
---

# What to Fix First? Mastering Risk Assessment with the DREAD Model 📊

By now, we've identified our system's assets, mapped its attack surfaces, and used frameworks like STRIDE to uncover threats and vulnerabilities. But not all risks are created equal. The final, critical step in threat modeling is risk assessment: deciding which issues are the most urgent and dangerous. This week, we'll introduce the DREAD model, a simple yet powerful way to prioritize your security efforts.

---

## What is Risk Assessment?

Risk assessment is the process of evaluating the potential impact and likelihood of each identified threat. It helps you answer a fundamental question:  

**"How dangerous is this vulnerability, and how likely is it to be exploited?"**

Without a structured way to assess risk, you might waste time and resources fixing low-priority issues while leaving critical ones exposed. The DREAD model provides a quantifiable method to avoid this pitfall.

---

## The DREAD Model: A Quantitative Approach to Risk

The DREAD model is a risk scoring system used to prioritize threats. Each threat is evaluated based on five criteria, with each criterion typically scored on a scale from 1 (low) to 10 (high).

### Here's what each letter in DREAD stands for:

| **Criterion**     | **Description**                                                                 | **Example Score (1-10)**                    |
|-------------------|---------------------------------------------------------------------------------|---------------------------------------------|
| **Damage**        | How bad would the attack be? The total impact or damage if the threat is exploited. | 10: Total data loss; 1: Minor inconvenience. |
| **Reproducibility** | How easy is it for an attacker to reproduce the attack?                        | 10: Extremely easy, one-click script; 1: Very difficult, requires special tools. |
| **Exploitability** | How easy is it to exploit the vulnerability?                                   | 10: Trivial, no technical skill; 1: Requires a deep understanding of the system. |
| **Affected Users** | How many users would be impacted by the attack?                                | 10: All users; 1: A single, non-critical user. |
| **Discoverability**| How likely is it that an attacker will find the vulnerability?                 | 10: Publicly known; 1: Very difficult to find. |

---

## Calculating the DREAD Score

The total risk score is typically calculated as the average of the five criteria:

\[
\text{Total Risk Score} = \frac{D + R + E + A + D}{5}
\]

A higher average score indicates a more critical risk that should be addressed with greater urgency.

---

## DREAD in Practice: A Real-World Example

Let's apply the DREAD model to a common threat we've discussed: **SQL Injection in a login form.**

| **DREAD Criterion** | **Our Assessment**                                                                                   | **Score** |
|----------------------|-----------------------------------------------------------------------------------------------------|-----------|
| **Damage**           | An attacker could steal all user credentials, including hashed passwords and other personal information. This is a severe breach. | 9 |
| **Reproducibility**  | A simple SQL injection payload can be found online and is easy to use.                              | 10 |
| **Exploitability**   | This requires some basic technical knowledge, but is not difficult for a skilled attacker.          | 8 |
| **Affected Users**   | Every user account is at risk if the attacker gains full access to the database.                    | 10 |
| **Discoverability**  | This vulnerability is easy to find by entering simple test strings into the login form.             | 9 |

---

### Now, let's calculate the average score:

\[
\text{Score} = \frac{9 + 10 + 8 + 10 + 9}{5} = \frac{46}{5} = 9.2
\]

With a DREAD score of **9.2**, this is clearly a high-risk issue that requires **immediate attention**. By using a quantitative model, you can now justify why this needs to be fixed before other, lower-scoring issues.

---

## What's Next?

In our next blog post, we'll shift from identifying and prioritizing risks to actually fixing them. We'll explore the various mitigations and security controls you can implement to protect your system from the threats you've uncovered.
