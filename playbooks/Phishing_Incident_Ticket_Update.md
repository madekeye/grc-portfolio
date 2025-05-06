
# Phishing Incident Ticket Update

## Ticket Details

- **Alert Severity**: High
- **Sender Details**: Suspicious mismatch between sender’s display name and email address (displayed as “HR Department” <hr-department@fake-domain.com>)
- **Message Body**: Included grammatical mistakes and urged user to download and open an attachment claiming to be a revised benefits policy.
- **Attachments or Links**: Email contained a PDF file attachment. File hash: `e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855`

## 5 Ws of the Incident

- **Who caused the incident?** Unknown external actor spoofing the organization’s HR department.
- **What happened?** A phishing email was received by an employee, containing a malicious PDF file that was verified as malware.
- **When did the incident take place?** April 30, 2025, 10:18 AM EDT.
- **Where did the incident occur?** On the user’s workstation within the corporate network.
- **Why did it happen?** The attacker attempted to gain a foothold in the environment via social engineering and malware delivery.

## Final Assessment

### Ticket Status: Escalated

### Ticket Comments:

After evaluating the phishing alert, the attachment was verified as malicious by hash analysis. The sender’s email address mismatched the display name, and the message included common indicators of phishing (urgency and grammar mistakes). The file hash matched a known malicious signature. As per the Phishing Incident Response Playbook (Step 3.2), the alert is escalated to the IR team for further containment and remediation.

**Reasons for Escalation**:

1. The file attachment is confirmed to be malicious.
2. The email exhibits clear signs of social engineering.
3. The alert severity is high and may indicate targeted phishing (spear phishing).
