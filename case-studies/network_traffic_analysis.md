# 🔍 Case Study: Network Traffic Analysis Using Wireshark

## 📘 Scenario Overview
You are a Security Analyst investigating unusual web traffic. A packet capture (`.pcap`) file contains session data between a user and a public website. Your objective is to identify key traffic patterns, protocols in use, and payload details to understand the communication flow.

## 🎯 Objectives
- Identify source and destination IP addresses
- Analyze protocols used in the session
- Drill down into packet layers and payload data
- Use Wireshark filters to isolate DNS, TCP, and UDP traffic

## 🛠 Tools Used
| Tool        | Purpose                  |
|-------------|--------------------------|
| Wireshark   | Network packet analysis  |
| PCAP Files  | Captured network traffic |

## 🧪 Investigation Tasks & Findings
- Explored packets using filters like `ip.addr`, `tcp.port`, `udp.port`, `eth.addr`
- Identified DNS queries and HTTP traffic
- Determined IP addresses, TTL values, frame sizes, and TCP flags

## 🔐 Security Insights
- Normal DNS and HTTP behavior observed
- No malicious patterns detected

## 📁 Files Included
- `sample.pcap`
- `network-traffic-analysis.md`

## 📌 Lessons Learned
- Filtering is crucial for effective analysis
- Header inspection reveals traffic intent

## ✅ Skills Demonstrated
- Protocol identification
- Wireshark analysis
- Network forensics