# Phishing Attack Simulation & Defensive Analysis

A comprehensive security project demonstrating the lifecycle of a social engineering attack, from credential harvesting to defensive detection. This project simulates real-world phishing campaigns using industry-standard tools and explores mitigation strategies for SOC environments.

> **⚠️ DISCLAIMER:** This project was conducted in a controlled, isolated laboratory environment for educational and defensive analysis purposes only. No real users were targeted. Unlawfully accessing systems or phishing without consent is illegal.

---

## 📄 Project Report
**[View Full Project Report (PDF)](./Phishing%20Attack%20Simulation%20and%20Defense.pdf)**

*Click the link above to view the complete documentation, including execution steps, screenshot evidence, and detailed analysis.*

---

## 📖 Project Overview
This project simulates a **Credential Harvesting Attack** to analyze how attackers clone legitimate websites and trick users into divulging sensitive information. It covers the full "Phishing Attack Life Cycle":
1.  **Preparation (Reconnaissance)**
2.  **Luring (Crafting Payload)**
3.  **Infection (Delivery)**
4.  **Collection (Credential Harvesting)**

The goal is to understand the attacker's methodology to build better defensive strategies (Blue Team) against Social Engineering.

## 🛠️ Tools & Technologies Used
* **Operating System:** Kali Linux
* **Attack Frameworks:**
    * **Zphisher** (Automated Phishing Tool)
    * **Social-Engineering Toolkit (SET)** (Website Attack Vectors)
* **AI Integration:** **ChatGPT** (Used to craft sophisticated "Pretexting" emails)
* **Defensive Tools:** Netcraft Extension, URL Analysis

---

## ⚔️ Attack Methodology (Red Team)

### 1. Attack Vector Selection
Used **SET** and **Zphisher** to deploy "Credential Harvester" modules.
* **Technique:** Website Cloning
* **Target Templates:** Google Login, Instagram Login
* **Port Forwarding:** Localhost / Cloudflared tunneling for delivery.

### 2. AI-Driven Pretexting (Social Engineering)
Leveraged Generative AI to craft high-trust phishing lures to bypass human suspicion.
* **Scenario:** "Netflix Premium Account Upgrade".
* **Technique:** Urgency ("Action Required") and Authority (Official Logo/Language).
* **AI Prompt:** *"give me email for netflix user about hisher netfilx free upgradation"*.

### 3. Execution & Capture
* Hosted the malicious landing page on a local server.
* Simulated victim traffic entering credentials.
* Intercepted and logged plain-text credentials (Username/Password) in real-time.

---

## 🛡️ Defensive Analysis (Blue Team)

As part of the SOC analysis, I documented how to detect and block these attacks:

### 1. Technical Detection
* **URL/Domain Analysis:** Checking for "Typosquatting" or mismatched domains (e.g., viewing the actual resolved URL vs. Anchor Text).
* **Netcraft Extension:** Using browser-based reputation tools to identify newly registered or malicious hosts.

### 2. Behavioral Testing
* **"Wrong Credentials" Test:** Intentionally entering fake data (e.g., `user: test / pass: 123`). If the site accepts it and redirects to the real page, it is likely a phishing collector.

---

## 🎓 Learning Outcomes
* **Social Engineering:** Understood the psychological manipulation behind "Pretexting" and "Baiting".
* **Tool Proficiency:** Gained hands-on experience with **SET** and **Zphisher** for penetration testing.
* **Defensive Posture:** Learned to identify IOCs (Indicators of Compromise) in email headers and URLs to improve organizational security awareness.

---

## 👤 Author
**Pranit Kalambate**
* **LinkedIn:** [linkedin.com/in/pranit-k](https://linkedin.com/in/pranit-k)
* **GitHub:** [github.com/pranitkalambate07](https://github.com/pranitkalambate07)

*This project is part of my portfolio for **Cybersecurity & SOC Analyst** roles.*
