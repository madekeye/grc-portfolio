# 🔍 Case Study: Network Traffic Analysis Using Wireshark

## 📘 Scenario Overview
You are a Security Analyst investigating unusual web traffic. A packet capture (`.pcap`) file contains session data between a user and a public website. Your objective is to identify key traffic patterns, protocols in use, and payload details to understand the communication flow.

## 🎯 Objectives
- Identify source and destination IP addresses
- Analyze protocols used in the session
- Drill down into packet layers and payload data
- Use Wireshark filters to isolate DNS, TCP, and UDP traffic

## 🛠 Tools Used
| Tool                     | Purpose                                  |
|--------------------------|------------------------------------------|
| Wireshark                | Network packet analysis                  |
| PCAP Files               | Captured network traffic                 |
| VirusTotal / URLScan     | For validating suspicious domains or IPs |
| WHOIS / IP Geolocation   | For tracing external communication       |
| Security Onion           | For advanced correlation                 |
| Python/Scapy             | For scripting analysis                   |

---

## 📁 Data Source

- **Filename**: `suspicious_traffic.pcap`
- **Size**: 2.4 MB
- **Capture Duration**: 7 minutes
- **Source**: Internal host in a corporate network showing abnormal communication patterns

---

## 🔍 Investigation Steps

### 1. **Initial Inspection**
- Opened the PCAP in Wireshark.
- Checked capture length, total number of packets, and average packet size.
- Applied initial filters:  

### 2. **Protocol Hierarchy**
- Noted heavy use of:
- HTTP (unusual for internal services)
- DNS (excessive queries)
- ICMP traffic to unknown destinations

### 3. **Top Talkers & Hosts**
- Identified frequent connections from:
- Internal host: `192.168.1.10`
- External IPs: `45.67.89.123`, `198.51.100.42`
- Suspicious domain: `maliciousupdate.net`

### 4. **Timeline Analysis**
- Created IO graph of packets/sec.
- Spikes every 60 seconds suggest beaconing behavior.

### 5. **DNS Query Inspection**
- Filter:
- Confirmed suspicious DNS tunneling indicators:
- Long subdomains
- Frequent TXT record use

### 6. **HTTP Traffic Review**
- Extracted HTTP objects.
- Found download attempts to executable files (`update.exe`).

---

## 🧩 Key Findings

| Finding                     | Description                                       | IOC                          |
|----------------------------|---------------------------------------------------|------------------------------|
| Malicious Domain           | Frequent contact to known bad domain              | `maliciousupdate.net`       |
| Suspicious External IP     | Receiving repeated ICMP traffic                   | `45.67.89.123`               |
| Downloaded Payload         | `.exe` file with unknown hash                     | `update.exe` (SHA256 hash)  |
| DNS Tunneling Behavior     | Long, frequent TXT record queries                 | Various subdomains           |

---

## 🚧 Recommendations

- Block domain `maliciousupdate.net` and associated IPs at the firewall.
- Quarantine host `192.168.1.10` for forensic review.
- Implement alerts for:
- Beaconing behavior
- Excessive DNS TXT queries
- Conduct full malware scan and memory analysis of affected host.
- Review egress filtering and DNS query logging policy.

---

## 📂 Artifacts

- 🗃️ PCAP File: `suspicious_traffic.pcap`
- 📎 Extracted IOCs: `ioc_report.txt`
- 📊 Graph: `traffic_beaconing_graph.png`
- 🔬 Malware sample (if safe): `update.exe`

---

## 📚 References

- [Wireshark Display Filters](https://wiki.wireshark.org/DisplayFilters)
- [VirusTotal IOC Check](https://www.virustotal.com/)
- [DNS Tunneling Techniques](https://attack.mitre.org/techniques/T1071/004/)

---

## 🧑‍💻 Analyst Notes

- First use of `Wireshark Follow TCP Stream` was instrumental in identifying encoded payloads.
- Consider incorporating `Suricata` in future to automatically flag known signatures.
- This case highlights the importance of DNS monitoring for early threat detection.

