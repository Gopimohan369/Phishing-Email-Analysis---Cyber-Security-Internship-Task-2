#  **Phishing Email Analysis – Cyber Security Internship (Task 2)**  

---

## 1. **Objective**

To analyze a suspicious email sample and identify key phishing characteristics using basic cyber-security analysis techniques and tools.

---

## 2.  **Sample Email Analyzed**

| Field | Value |
|-------|-------|
| **From** | `<support@paypaypal[.]net>` |
| **To** | `<john[.]doe@mybusiness[.]com>` |
| **Subject** | *Update your account* |
| **Sender (claimed)** | **PayPal** (spoofed) |
| **Reference ID** | PP-563D-1E36-4997-92D1 |

> **Email body excerpt**  
> ```
> Dear John,
> We detected unusual activity on your PayPal account. Log into PayPal to verify your identity and update your password and security questions.
> ...
> Verify your identity now.
> ```

---

## 3.  **Analysis of Phishing Indicators**

| # | Indicator | Findings |
|---|-----------|----------|
| **1** | **Sender Email Address (Spoofing)** | `service-update@paypal-secure-alert.com` <br> *Domain contains “paypal” but is not the official* **paypal.com** – clear spoof. |
| **2** | **Email Header Discrepancies** *(hypothetical)* | • **Received-Path:** originates from non-PayPal server <br> • **Return-Path:** attacker’s domain <br> • **SPF / DKIM / DMARC:** **FAIL / SOFTFAIL** |
| **3** | **Suspicious Links (URL Mismatch)** | **Displayed:** *Verify your identity now* <br> **Actual:** `http://secure-paypal-login.info/account/verify` <br> – malicious, non-PayPal domain. |
| **4** | **Urgent & Threatening Language** | Phrases such as “unusual activity”, “you won’t be able to send money”, “failure will result in…”. <br> Designed to induce fear and haste. |
| **5** | **Generic / Unprofessional Tone** | Uses **“Dear John”** but lacks other personalization; wording is robotic. |

---

## 4.  **Summary of Findings**

This email is **unequivocally a phishing attempt**, exhibiting multiple high-risk indicators and social-engineering tactics aimed at harvesting credentials.

|   Key Phishing Traits |
|-------------------------|
| Spoofed sender domain |
| (Hypothetical) failed SPF / DKIM / DMARC |
| Mismatched URL destination |
| Urgent, fear-based language |
| Generic or forged greeting |

---

## 5.  **Tools Used**

- **Email Client / Text Viewer** – inspect raw content  
- **Online Header Analyzers** (e.g., *MXToolbox*, *Google Admin Toolbox*) – validate SPF/DKIM/DMARC  
- **Browser Hover Technique** – reveal mismatched URLs  

---

## 6. **Outcome**

- Identified spoofed domains, mismatched URLs, and psychological manipulation tactics.  
- Reinforced best practices for verifying sender authenticity via header analysis.  
- Highlighted how urgency and generic salutations fuel mass phishing campaigns.  
