# 🛡️ Phishing Email Analysis - Cyber Security Internship Task 2

## 📌 Objective

To analyze a suspicious email sample and identify key phishing characteristics using basic cyber security analysis techniques and tools.

---

## 🧰 Tools Used

- 📨 Sample Phishing Email (Provided in Task)
- 🌐 [MxToolbox Email Header Analyzer](https://mxtoolbox.com/EmailHeaders.aspx)
- 🧠 Manual Link Inspection (hover-to-check)
- 🔍 Grammar and Style Review

---

## 📨 Sample Email Analyzed

Subject: Update your account
Sender: PayPal (spoofed)
Reference ID: PP-563D-1E36-4997-92D1

"Dear John,
We detected unusual activity on your PayPal account. Log into PayPal to verify your identity and update your password and security questions.
...
Verify your identity now."
---

## 🛠️ Analysis Process

### 1. **Sender Address Check**
- **Suspicious**: The sender claims to be PayPal, but actual phishing emails often use spoofed or lookalike domains.
- **Not Verified**: Missing full email headers in this case, but real analysis would check SPF/DKIM records.

### 2. **Urgent Language and Threats**
- Text includes phrases like:
  - “unusual activity”
  - “Log into your PayPal account as soon as possible”
  - “You won't be able to send or withdraw money”
- **Purpose**: To induce fear and prompt impulsive action (common social engineering tactic).

### 3. **Generic Greeting**
- **“Dear John”** appears here, but in real phishing emails it's often just “Dear Customer” or no greeting at all.
- If the email was truly personalized, it might still be spoofed.

### 4. **Call-to-Action Link**
- **“Verify your identity now”** is likely hyperlinked to a fake PayPal login page.
- If hovered (in actual email), the URL would typically **not match PayPal's domain**.

### 5. **Language and Grammar**
- Tone mimics official language well, but some formatting and sentence flow seem off or too repetitive.
- No major spelling errors, but **repetition** and **over-explanation** are red flags.

---

## 🚨 Phishing Indicators Detected

| Phishing Indicator                | Found | Notes |
|----------------------------------|-------|-------|
| Spoofed sender email             | ✅    | Likely (needs header to confirm) |
| Urgent/threatening language      | ✅    | Repeated warnings about account suspension |
| Generic or misleading greeting   | ✅    | Common tactic; personalization may be fake |
| Suspicious call-to-action links  | ✅    | Encourages immediate click without context |
| Poor grammar or redundancy       | ⚠️    | No errors, but structure is overly robotic |
| Misleading branding              | ✅    | Uses PayPal logo and reference ID to appear real |

---

## 📈 Outcome

- Demonstrated ability to identify phishing patterns.
- Understood psychological manipulation (social engineering) used in phishing.
- Learned best practices in verifying emails via header and link inspection.
