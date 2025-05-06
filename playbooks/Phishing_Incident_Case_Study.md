# 🚨 Phishing Alert Incident Case Study

## 📘 Case Study Summary: Phishing Alert Investigation in a Financial Services Organization
Scenario Summary:

As a Security Analyst at a financial services firm, you received an alert related to a suspicious email and file download. Upon further investigation, the email contained a malicious attachment confirmed by its hash value. Following your organization’s phishing response playbook and flowchart, you evaluated the alert, reviewed the sender’s details, message content, and malicious attachment. You recorded findings in the incident handler’s journal and completed the alert ticket update, deciding to escalate the incident due to the confirmed threat.

## 📌 Incident Summary

**Role:** Security Analyst  
**Organization Type:** Financial Services  
**Incident Type:** Phishing email with a malicious attachment  
**Severity:** High  
**Date of Incident:** [Insert Date]  
**Status:** Escalated

---

## 🧾 Alert Details

- **Alert Source:** Internal phishing alert system  
- **Alert Severity:** High  
- **Sender Email:** support@secure-payments.net (spoofed domain)  
- **Employee Targeted:** Jane.Doe@company.com  
- **Email Subject:** "Urgent: Payroll Update Required"  
- **Attachment Name:** Payroll_Update_2025.pdf.exe  
- **Attachment Hash:** Verified malicious (VirusTotal)  
- **Detection Method:** Hash match from threat intel feed  

---

## 🔍 Investigation Steps

1. **Alert Ticket Review:**
   - Confirmed alert severity was set to *High*.
   - Sender address spoofed to appear legitimate.
   - Email body contained grammatical errors and urgency tactics.
   - Attached file disguised as a PDF but had a `.exe` extension.
   - Hash matched known malware.

2. **5 W’s Analysis:**
   - **Who:** External attacker spoofing a payroll domain.
   - **What:** Sent a phishing email with a malicious attachment.
   - **When:** Received on [Insert Date].
   - **Where:** Targeted Jane.Doe@company.com at the endpoint.
   - **Why:** Attempted credential theft or malware execution.

3. **Attachment Analysis:**
   - File hash: *Confirmed malicious*.
   - Behavior: Designed to execute remote access trojan (RAT).
   - Impact: Could result in unauthorized access to payroll system.

---

## ✅ Ticket Update

- **Ticket Status:** Escalated  
- **Ticket Comments:**
   - Investigated high-severity phishing alert involving a spoofed sender and a malicious attachment.
   - Confirmed the executable file was disguised as a PDF and matched a known malware hash.
   - Due to the confirmed malicious nature and risk to payroll systems, the alert has been escalated to Tier 2 SOC for further containment and remediation.

---

## 🧠 Lessons Learned

- Email filtering systems flagged the message, but attachment-based phishing remains a significant risk.
- Continuous employee training is vital to detect spoofed emails.
- Rapid verification of file hashes is an effective method to confirm threats.

---

## 📎 Attachments

- [VirusTotal hash analysis link or screenshot]
- Alert ticket screenshot (if applicable)
- Email headers (optional for deeper analysis)

---

## 🛠️ Tools Used

- Wireshark (for potential network packet inspection)  
- VirusTotal (hash verification)  
- Email header analyzer  
- Organization’s phishing playbook

---

## 🔐 Recommendations

- Quarantine the user’s endpoint.
- Conduct full malware scan on user’s machine.
- Block domain and similar spoofed variants.
- Educate staff on detecting disguised file types.

---

