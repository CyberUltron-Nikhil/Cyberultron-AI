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

<img width="1535" height="468" alt="image" src="https://github.com/user-attachments/assets/c9b65a5c-1af2-469e-913c-12f2073cf375" />


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

<img width="1568" height="440" alt="image" src="https://github.com/user-attachments/assets/10683f3c-fd15-48f4-adcc-416a859b2f51" />


---

### Now, let's calculate the average score:

\[
\text{Score} = \frac{9 + 10 + 8 + 10 + 9}{5} = \frac{46}{5} = 9.2
\]

With a DREAD score of **9.2**, this is clearly a high-risk issue that requires **immediate attention**. By using a quantitative model, you can now justify why this needs to be fixed before other, lower-scoring issues.

---

## What's Next?

In our next blog post, we'll shift from identifying and prioritizing risks to actually fixing them. We'll explore the various mitigations and security controls you can implement to protect your system from the threats you've uncovered.
