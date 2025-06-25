#  Phishing Email Analysis - Cyber Security Internship Task 2
-------------
## Objective
-------------

To analyze a suspicious email sample and identify key phishing characteristics using basic cyber security analysis techniques and tools.

---



---
-------------------------
## Sample Email Analyzed
-------------------------
From:support@paypaypal[.]net
To:john[.]doe@mybusiness[.]com
Subject: Update your account
Sender: PayPal (spoofed)
Reference ID: PP-563D-1E36-4997-92D1

"Dear John,
We detected unusual activity on your PayPal account. Log into PayPal to verify your identity and update your password and security questions.
...
Verify your identity now."
---
----------------------------------
## ANALYSIS OF PHISHING INDICATORS
----------------------------------
### Indicator 1: Sender Email Address (Spoofing)

- **Observation:** The sender's email address is `service-update@paypal-secure-alert.com`.
- **Analysis:** This is a classic example of domain spoofing. Although the domain includes “paypal,” it is **not** the official `paypal.com` domain. Instead, it uses **paypal-secure-alert.com**, which is misleading. Legitimate companies like PayPal send messages from their primary domain (`@paypal.com`). This makes it a significant red flag.

---

### Indicator 2: Email Header Discrepancies *(Hypothetical)*

**Objective:** To check the email's origin and authenticity using tools like MXToolbox or Google Admin Toolbox.

- **Received Path:** In a phishing email, the path would likely show the message originated from a **foreign or unrelated mail server**, not PayPal’s official infrastructure.
- **Return-Path:** Often differs from the "From" address and points back to the attacker’s fake server.
- **Authentication Results:**
  - **SPF (Sender Policy Framework)**
  - **DKIM (DomainKeys Identified Mail)**
  - **DMARC (Domain-based Message Authentication, Reporting, and Conformance)**
  
  In most phishing emails, these checks **fail or return a SOFTFAIL**, indicating the email is not authorized by the domain it claims to be from.

---

### Indicator 3: Suspicious Links (URL Mismatch)

- **Observation:** The email contains a call-to-action link in the form of a button: **"Verify your identity now"**.
- **Analysis:** Hovering over the button reveals a **different destination URL** than what is visually shown.
- **Displayed Text:** Verify your identity now
- **Actual Destination (Hypothetical):** `http://secure-paypal-login.info/account/verify`
- **Discrepancy:** This domain is not owned by PayPal and is structured to deceive. It mimics PayPal’s brand to lure users to a fake login portal designed to **harvest credentials**.

---

### Indicator 4: Urgent and Threatening Language

- **Observation:** The email body includes multiple urgent phrases:
  - “We detected unusual activity on your PayPal account.”
  - “Log into PayPal to verify your identity…”
  - “You won't be able to send money or withdraw money…”
  - “Failure to do so will result in…”
- **Analysis:** These statements are crafted to create **fear and urgency**, pressuring the recipient into quick action before evaluating the legitimacy of the message. This is a **classic social engineering technique**.

---

### Indicator 5: Spelling and Grammar Errors / Unprofessional Tone

- **Observation:** The email contains a **generic greeting**, such as **“Dear John”** (or in other phishing cases, “Dear Customer”).
- **Analysis:** While this version uses a name, it's still potentially forged. Real emails from PayPal often contain precise, personalized account references and include security footers. Also, the tone is **overly formal and robotic**, often with slight awkward phrasing—something that typically differs from real corporate communication.

---
----------------------
## SUMMARY OF FINDINGS
----------------------
This email is **definitively a phishing attempt**. It exhibits multiple high-risk indicators and social engineering tactics designed to manipulate the user into clicking a malicious link and surrendering personal account credentials.

**Key Phishing Traits Found:**

- [x] **Spoofed Sender Address** – uses a deceptive domain name.
- [x] **(Hypothetical) Failed SPF/DKIM/DMARC Authentication** – sender is not verified.
- [x] **Mismatched URL** – destination link does not belong to PayPal.
- [x] **Urgent/Threatening Tone** – invokes fear and prompts quick action.
- [x] **Generic or Forged Greeting** – no strong personalization, potentially mass-sent.

---
-------------
## TOOLS USED
-------------
- **Email Client / Text Viewer** – to examine email content
- **Online Header Analyzer (e.g., MXToolbox)** – to inspect technical origin and authentication
- **Web Browser Hover Technique** – to detect mismatched URL destinations

---
----------
## Outcome
----------
- Demonstrated ability to identify phishing patterns.
- Understood psychological manipulation (social engineering) used in phishing.
- Learned best practices in verifying emails via header and link inspection.
