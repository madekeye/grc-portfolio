# 🌐 Case Study: DNS Tunneling Detection

## 📘 Scenario Overview
This study examines network traffic for signs of DNS tunneling, a technique often used to exfiltrate data or establish covert channels using DNS queries.

## 🎯 Objectives
- Detect patterns of DNS tunneling
- Identify abnormal domain lengths and entropy
- Extract potential data hidden in DNS queries

## 🛠 Tools Used
| Tool        | Purpose                     |
|-------------|-----------------------------|
| Wireshark   | DNS packet analysis         |
| Tshark      | Command-line DNS extraction |
| Python      | Entropy and regex analysis  |

## 🧪 Investigation Tasks & Findings
- High frequency of TXT/NULL DNS queries
- Long domain names with high entropy values
- Repeated query patterns consistent with tunneling tools

## 🔐 Security Insights
- DNS exfiltration channel identified
- Mitigation recommended: restrict external DNS access

## 📁 Files Included
- `dns_tunneling.pcap`
- `entropy_analysis.py`
- `dns-tunneling-analysis.md`

## 📌 Lessons Learned
- DNS is often overlooked as a covert channel
- Behavior-based analysis helps detect tunneling

## ✅ Skills Demonstrated
- DNS protocol inspection
- Data exfiltration detection
- Entropy analysis and scripting