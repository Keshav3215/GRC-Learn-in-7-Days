# 🛡️ Day 01 — GRC Foundations + CIA Triad

> **7-Day GRC Interview Prep Series** | Beginner → Interview-Ready  
> 📍 By: Keshav Yadav | Cybersecurity Graduate → GRC Analyst  
> 🗓️ Goal: Learn GRC from scratch with real-world examples and clear every fresher interview question

---

## 📌 Table of Contents

- [What is GRC?](#-what-is-grc)
- [G — Governance](#g--governance)
- [R — Risk Management](#r--risk-management)
- [C — Compliance](#c--compliance)
- [CIA Triad](#-cia-triad)
- [Key Terms: Vulnerability vs Threat vs Risk](#-key-terms-vulnerability-vs-threat-vs-risk)
- [What is an ISMS?](#-what-is-an-isms)
- [Day 01 Interview Questions](#-day-01-interview-questions)
- [Quick Revision Cheat Sheet](#-quick-revision-cheat-sheet)

---

## 🔷 What is GRC?

**GRC** stands for **Governance, Risk Management, and Compliance.**

It is a structured way for organizations to:
- Set rules and responsibilities (Governance)
- Identify and manage what can go wrong (Risk)
- Follow laws, regulations, and standards (Compliance)

> 💡 **Simple Definition:**  
> GRC is how a company stays **secure**, **legal**, and **accountable** — all at the same time.

### 🏢 Real-World Analogy

Think of a hospital:
| GRC Area | Hospital Example |
|---|---|
| **Governance** | Hospital policies — who can access patient records, who approves treatments |
| **Risk Management** | Identifying that a power cut could stop life-support machines and installing backup generators |
| **Compliance** | Following HIPAA (US) or health data laws so patient data is legally protected |

Without GRC → hospitals could leak patient data, operate illegally, and have no plan for emergencies.

---

## G — Governance

**Governance** = The rules, policies, and accountability structure of an organization.

It answers:
- Who is responsible for what?
- What are employees allowed to do?
- What decisions need management approval?

### 📄 Examples of Governance Documents

| Document | Purpose |
|---|---|
| Information Security Policy | Rules for protecting all company data |
| Acceptable Use Policy (AUP) | Rules for using company devices and internet |
| Access Control Policy | Who gets access to which systems |
| BYOD Policy | Rules for using personal phones/laptops for work |
| Password Policy | Minimum length, complexity, expiry rules |

### 🏢 Real Example

> A company like **Infosys** has an Information Security Policy that says:  
> *"All employees must use a VPN when accessing company systems from outside the office."*  
> That is governance — a rule that applies to everyone.

---

## R — Risk Management

**Risk Management** = Identifying what can go wrong, how likely it is, how much damage it can cause, and deciding what to do about it.

### 🔄 Risk Management Process (4 Steps)

```
Step 1: IDENTIFY   → What risks exist? (e.g., phishing emails, unpatched servers)
Step 2: ASSESS     → How likely? How bad? Score it on a 5×5 matrix
Step 3: TREAT      → Mitigate / Accept / Transfer / Avoid
Step 4: MONITOR    → Track risks regularly in a Risk Register
```

### 📊 Risk Scoring Matrix (5×5)

```
Impact →        1-Low    2-Minor   3-Moderate  4-Major   5-Critical
Likelihood ↓
5 - Almost Sure    5       10         15         20         25  ← HIGH RISK
4 - Likely         4        8         12         16         20
3 - Possible       3        6          9         12         15
2 - Unlikely       2        4          6          8         10
1 - Rare           1        2          3          4          5  ← LOW RISK
```

> 🟥 Score 15–25 = High Risk → Must act immediately  
> 🟨 Score 8–12 = Medium Risk → Plan to address  
> 🟩 Score 1–6  = Low Risk → Monitor only

### 🛠️ 4 Ways to TREAT a Risk (MATA)

| Treatment | Meaning | Example |
|---|---|---|
| **M**itigate | Reduce the risk by adding controls | Install antivirus to reduce malware risk |
| **A**ccept | Consciously accept the risk (low impact, low cost) | Accept that the office printer might occasionally jam |
| **T**ransfer | Move the risk to a third party | Buy cyber insurance |
| **A**void | Stop doing the activity that causes the risk | Shut down an old unpatched server |

> 💡 Mnemonic: **MATA** — Mitigate, Accept, Transfer, Avoid

---

## C — Compliance

**Compliance** = Following external laws, regulations, and industry standards.

If a company fails compliance → **fines, legal action, loss of business, reputational damage.**

### 🌍 Common Compliance Frameworks

| Framework | Who Needs It | What It Covers |
|---|---|---|
| **ISO 27001** | Any organization globally | Information security management |
| **GDPR** | Companies handling EU citizen data | Personal data privacy |
| **DPDP Act 2023** | Companies in India | Indian personal data protection |
| **PCI-DSS** | Any company processing card payments | Payment card data security |
| **SOC 2** | SaaS / cloud companies | Customer data security & availability |
| **HIPAA** | US healthcare companies | Patient health information |

### 🏢 Real Example

> A Mumbai-based startup builds a software product and gets clients in Germany.  
> Because they process EU citizens' data → they **must comply with GDPR**.  
> If they don't and there's a data breach → fine up to **€20 million or 4% of global revenue.**

---

## 🔐 CIA Triad

The **CIA Triad** is the foundation of all information security. Every security control, policy, and risk assessment ties back to protecting one or more of these three pillars.

```
        ┌─────────────────┐
        │  CONFIDENTIALITY │   Only authorized people can access data
        └────────┬────────┘
                 │
    ┌────────────┼────────────┐
    │                         │
┌───┴──────┐          ┌───────┴────┐
│ INTEGRITY │          │AVAILABILITY│
│ Data is   │          │Systems are │
│ accurate  │          │accessible  │
│& unchanged│          │when needed │
└───────────┘          └────────────┘
```

---

### 🔒 C — Confidentiality

**Definition:** Data is accessible only to people who are authorized to see it.

**How it's protected:**
- Encryption (AES-256, TLS)
- Access Control (Role-Based Access)
- Multi-Factor Authentication (MFA)
- Data Classification

**Real-World Examples:**

| Scenario | Confidentiality Protection |
|---|---|
| Your bank PIN | Encrypted in the bank's database — even bank employees can't see it |
| Company salary data | Only HR and Finance can access payroll systems |
| Patient medical records | Doctor-patient confidentiality + HIPAA encryption |
| WhatsApp messages | End-to-end encryption — only sender and receiver can read |

> ❌ **Confidentiality Breach Example:**  
> In 2021, Facebook leaked 533 million users' phone numbers and personal details.  
> Confidentiality was broken — unauthorized parties accessed private user data.

---

### 🔏 I — Integrity

**Definition:** Data is accurate, complete, and has not been tampered with.

**How it's protected:**
- Hashing (MD5, SHA-256) — detect if data was changed
- Digital Signatures
- Version Control
- Audit Logs / Change Management

**Real-World Examples:**

| Scenario | Integrity Protection |
|---|---|
| Software downloads | SHA-256 hash published — you verify the file wasn't modified |
| Bank transactions | Every transaction logged and immutable — amount can't be secretly changed |
| Legal documents | Digital signatures prove documents weren't altered after signing |
| Exam results | University systems log who made changes and when |

> ❌ **Integrity Breach Example:**  
> An attacker intercepts a bank transfer and changes the destination account number before it reaches the bank.  
> This is a **Man-in-the-Middle attack** breaking Integrity.

---

### 🌐 A — Availability

**Definition:** Systems, data, and services are accessible when authorized users need them.

**How it's protected:**
- DDoS Protection (Cloudflare, AWS Shield)
- Redundancy and Backups
- Load Balancing
- Business Continuity Plan (BCP)
- Disaster Recovery Plan (DRP)

**Real-World Examples:**

| Scenario | Availability Protection |
|---|---|
| E-commerce site during a sale | Load balancers distribute traffic so site doesn't crash |
| Hospital systems | Backup power generators ensure systems stay on during power cuts |
| Bank ATMs | Redundant networks so ATMs work even if one server fails |
| Cloud data backup | Daily backups to AWS S3 ensure data isn't lost if server crashes |

> ❌ **Availability Breach Example:**  
> In 2016, a massive DDoS attack on Dyn (a DNS provider) took down Twitter, Netflix, Reddit, and Spotify for hours.  
> Availability was destroyed — legitimate users couldn't access services.

---

### 🔗 CIA Triad — How They Interact

| Attack Type | CIA Pillar Broken |
|---|---|
| Data leak / unauthorized access | Confidentiality |
| Man-in-the-Middle, data tampering | Integrity |
| DDoS attack, ransomware locking files | Availability |
| Ransomware (encrypts files, demands payment) | All three — Confidentiality + Integrity + Availability |

> 💡 **GRC Connection:**  
> Every security policy you write in GRC must protect at least one of C, I, or A.  
> Example: *"Password Policy"* → protects **Confidentiality**  
> Example: *"Change Management Policy"* → protects **Integrity**  
> Example: *"Backup Policy"* → protects **Availability**

---

## 🎯 Key Terms: Vulnerability vs Threat vs Risk

These three terms are often confused. Know the difference perfectly.

### 📖 Definitions

| Term | Definition | Simple Example |
|---|---|---|
| **Vulnerability** | A weakness in a system or process | Unpatched Windows OS, weak password "admin123", no MFA |
| **Threat** | A potential cause of harm | Hacker, ransomware, insider employee, flood, power outage |
| **Risk** | Probability that a threat exploits a vulnerability and causes harm | Hacker (threat) + unpatched server (vulnerability) = high risk of breach |

### 🧮 Risk Formula

```
RISK = THREAT × VULNERABILITY × IMPACT
```

### 🔍 Real Scenarios

**Scenario 1 — High Risk:**
```
Vulnerability:  Company uses default admin password "admin/admin" on their router
Threat:         Automated bot scanning the internet for default credentials
Impact:         Attacker gains full network access → data breach, ransomware
Risk Score:     Likelihood = 5 (Almost Certain) × Impact = 5 (Critical) = 25/25 → CRITICAL
```

**Scenario 2 — Medium Risk:**
```
Vulnerability:  Old employee's account not deleted after they left
Threat:         Disgruntled ex-employee tries to log in
Impact:         Unauthorized access to internal files
Risk Score:     Likelihood = 3 (Possible) × Impact = 4 (Major) = 12/25 → MEDIUM
Treatment:      Mitigate → Implement offboarding checklist to disable accounts immediately
```

**Scenario 3 — Low Risk:**
```
Vulnerability:  Office printer has no PIN protection
Threat:         Employee accidentally prints someone else's document
Impact:         Minor internal document exposure
Risk Score:     Likelihood = 2 × Impact = 2 = 4/25 → LOW
Treatment:      Accept → Cost of PIN setup not worth the low risk
```

---

## 📋 What is an ISMS?

**ISMS = Information Security Management System**

An ISMS is a **systematic, organized approach** to managing an organization's information security. It is a framework of policies, processes, and controls — not just an IT system.

> 🏠 **Analogy:**  
> If your house is the "organization" and "security" means protecting it from theft:  
> - Buying a lock = one security control  
> - An ISMS = the complete system: locks + alarm + CCTV + insurance + emergency plan + rules for family members

### 🏗️ What an ISMS Covers

```
ISMS Framework
├── People        → Security awareness training, roles & responsibilities
├── Processes     → Risk management, incident response, change management
└── Technology    → Firewalls, encryption, access control, backups
```

### 📜 Standard That Defines ISMS: ISO/IEC 27001

- ISO 27001 is the **international standard** for building and certifying an ISMS
- Organizations get officially **certified** by a third-party auditor (BSI, Bureau Veritas)
- Certification proves to customers, regulators, and partners that your security is properly managed

### 🔄 ISMS Lifecycle (PDCA Model)

```
PLAN  →  DO  →  CHECK  →  ACT
  ↑                           ↓
  └───────────────────────────┘
         Continuous Improvement

PLAN:   Define security objectives, conduct risk assessment
DO:     Implement controls and security policies
CHECK:  Audit, monitor, review — are controls working?
ACT:    Fix gaps, improve, update policies
```

### 🏢 Real-World Example

> **Scenario:** A fintech startup in Pune wants to sell their product to a large UK bank.  
> The UK bank says: *"We only work with vendors who are ISO 27001 certified."*  
>
> **What the startup must do:**  
> 1. Build an ISMS — create policies, assess risks, implement controls  
> 2. Get audited by a certification body (like BSI Group)  
> 3. Receive ISO 27001 certificate (valid 3 years, with annual surveillance audits)  
> 4. Show the certificate to the UK bank → deal is possible

---

## ❓ Day 01 Interview Questions

Practice these aloud. Cover the answer first, speak from memory.

---

### Q1. What does GRC stand for and why is it important?

<details>
<summary>📝 Click to reveal answer</summary>

**GRC = Governance, Risk Management, Compliance.**

- **Governance** = Rules, policies, accountability — who does what
- **Risk Management** = Identify, assess, treat risks before they cause harm
- **Compliance** = Follow laws and standards (ISO 27001, GDPR, PCI-DSS)

**Why important:**  
Without GRC, companies face data breaches (poor governance), financial losses (unmanaged risks), and legal fines for non-compliance (GDPR fines up to €20M).

> 💬 Interview line: *"GRC connects business strategy to security, legal obligations, and operational risk in a structured way."*

</details>

---

### Q2. Explain the CIA Triad with one real example for each.

<details>
<summary>📝 Click to reveal answer</summary>

| Pillar | Definition | Real Example |
|---|---|---|
| **Confidentiality** | Only authorized users access data | WhatsApp end-to-end encryption — only you and the receiver see messages |
| **Integrity** | Data is accurate, not tampered with | SHA-256 hash verification of software downloads — proves file wasn't modified |
| **Availability** | Systems accessible when needed | Cloudflare DDoS protection keeps websites online during attacks |

> 💬 Interview line: *"Every security control I implement in GRC is designed to protect one or more of Confidentiality, Integrity, and Availability."*

</details>

---

### Q3. What is the difference between a Vulnerability, a Threat, and a Risk?

<details>
<summary>📝 Click to reveal answer</summary>

| Term | Definition | Example |
|---|---|---|
| **Vulnerability** | Weakness in a system | Unpatched software, no MFA, default passwords |
| **Threat** | Potential cause of harm | Hacker, ransomware, insider employee, flood |
| **Risk** | Probability threat exploits vulnerability | Hacker + unpatched server = risk of breach |

**Formula:** `Risk = Threat × Vulnerability × Impact`

**Example answer:**  
*"An unpatched VPN software is a vulnerability. An attacker scanning the internet for that vulnerability is a threat. The risk is the probability that the attacker successfully exploits it and gains access to our network."*

</details>

---

### Q4. What is an ISMS and which standard defines it?

<details>
<summary>📝 Click to reveal answer</summary>

An **ISMS (Information Security Management System)** is a systematic framework of policies, processes, and controls for managing information security risks across people, processes, and technology.

It is defined and certified under **ISO/IEC 27001**.

Key points:
- ISMS is not just IT — it covers people and processes too
- Uses the PDCA cycle: Plan → Do → Check → Act (continuous improvement)
- Organizations get ISO 27001 certified by a third-party auditor
- Certification tells customers: *"Our information security is properly managed."*

</details>

---

### Q5. How does GRC protect the CIA Triad?

<details>
<summary>📝 Click to reveal answer</summary>

| GRC Activity | CIA Pillar Protected |
|---|---|
| Writing a Password Policy | Confidentiality — prevents unauthorized access |
| Change Management Process | Integrity — ensures only authorized changes to systems |
| Backup and BCP Policy | Availability — ensures systems can be restored after failure |
| VAPT + Risk Register | All three — identifies and treats risks to C, I, and A |
| Incident Response Policy | All three — contains breaches that affect C, I, A |

> 💬 *"GRC operationalizes the CIA Triad through policies, controls, and continuous risk management."*

</details>

---

## 📌 Quick Revision Cheat Sheet

```
╔══════════════════════════════════════════════════════╗
║              DAY 01 — CHEAT SHEET                    ║
╠══════════════════════════════════════════════════════╣
║  GRC = Governance + Risk Management + Compliance     ║
║                                                      ║
║  CIA TRIAD:                                          ║
║  C = Confidentiality → Only authorized access        ║
║  I = Integrity       → Data not tampered with        ║
║  A = Availability    → Systems accessible when needed║
║                                                      ║
║  VULNERABILITY = Weakness (unpatched software)       ║
║  THREAT        = Actor/event (hacker, malware)       ║
║  RISK          = Threat × Vulnerability × Impact     ║
║                                                      ║
║  ISMS = Framework to manage info security            ║
║         Standard = ISO/IEC 27001                     ║
║         Model = PDCA (Plan→Do→Check→Act)             ║
║                                                      ║
║  RISK TREATMENT = MATA                               ║
║  M = Mitigate  A = Accept  T = Transfer  A = Avoid   ║
╚══════════════════════════════════════════════════════╝
```

---

## 📚 Resources for Day 01

| Resource | Link | Type |
|---|---|---|
| NIST Cybersecurity Framework | https://www.nist.gov/cyberframework | Free PDF |
| CIS Controls v8 | https://www.cisecurity.org/controls | Free Download |
| Simply Cyber (YouTube) | Search "Simply Cyber GRC" on YouTube | Free Videos |
| ISO 27001 Overview | https://www.iso.org/isoiec-27001-information-security | Official |

---

## ➡️ What's Coming Next

| Day | Topic |
|---|---|
| **Day 01** | ✅ GRC Foundations + CIA Triad ← You are here |
| **Day 02** | ISO 27001 Deep Dive + NIST CSF |
| **Day 03** | Risk Management + Build a Risk Register |
| **Day 04** | Compliance Laws — GDPR, DPDP Act, SOC 2, PCI-DSS |
| **Day 05** | Security Policies + Gap Analysis + BCP vs DRP |
| **Day 06** | Incident Management + TPRM + VAPT in GRC |
| **Day 07** | Mock Interview — 25 Questions Full Practice |

---

> 🏆 **Built by Keshav Yadav** — Cybersecurity Graduate | CEH v13 | SIH 2024 Winner  
> 📧 keshavy573@gmail.com | 🔗 linkedin.com/in/Keshav | 💻 github.com/Keshav

*Star ⭐ this repo if it helped you. Follow for Day 02 →*
