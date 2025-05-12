# 🛡️ Home Lab SIEM: Suricata + ELK Stack

This project demonstrates a lightweight SIEM (Security Information and Event Management) setup using **Suricata**, **Filebeat**, **Elasticsearch**, and **Kibana** to monitor, detect, and visualize network traffic in a home lab environment.

## 🎯 Objectives
- Monitor traffic between two virtual machines.
- Detect suspicious behavior using Suricata rules.
- Centralize and visualize log data with the ELK Stack.
- Simulate real-world attack patterns.
- Provide actionable security recommendations.

---

## 🧰 Tools & Technologies
- **Suricata**: Network Intrusion Detection System
- **Filebeat**: Lightweight log shipper
- **Elasticsearch**: Log indexing and search engine
- **Kibana**: Log visualization and dashboard tool
- **Ubuntu** (VMs on VMware)

---

## 🏗️ Architecture Diagram

> *![image](https://github.com/user-attachments/assets/5664b1d4-8208-47ce-9c1d-f5149e62f13c)
> *

---

## 🔧 System Setup

| VM | Role | IP Address |
|----|------|------------|
| VM1 | Suricata Sensor + Filebeat + ELK | 192.168.1.10 |
| VM2 | Traffic Generator (attack simulation) | 192.168.1.11 |

---

## 📡 Log Flow

1. Suricata inspects network traffic and logs alerts in `eve.json`.
2. Filebeat reads the logs and forwards them to Elasticsearch.
3. Kibana visualizes logs and alerts for analysis.

---

## 📂 Configuration Files

Key config files are available in the `configs/` folder:
- `filebeat.yml`
- `suricata.yaml`
- `logstash-pipeline.conf`

---

## 🧪 Attack Simulations
Simulated common attacks to test detection:
- Port scanning using `nmap`
- Multicast scanning and service discovery
- Brute-force login attempts

---

## 🔍 Observations

- Majority of traffic was normal (HTTP, TCP/UDP).
- Suspicious behavior detected on high-numbered ports (e.g., 48000).
- Multicast activity flagged by Suricata as potential scan attempts.

---

## 🔐 Security Recommendations

- Harden firewall rules to block unnecessary ports.
- Regularly update Suricata rule sets.
- Segment internal network to prevent lateral movement.
- Encrypt traffic using TLS for sensitive services.

---

## 📄 Full Project Report

Read the full project documentation here:  
📎 ![image](https://github.com/user-attachments/assets/b97b1320-6d10-4013-97c6-539066abbc3c)


---

## ✅ What I Learned

- Building a functional SIEM using open-source tools.
- Deep understanding of traffic patterns and alerting logic.
- Parsing structured logs and creating actionable dashboards.

---

## 📌 Future Improvements

- Integrate Wazuh or Sigma rules for richer detection.
- Create real-time alerting via email or webhook.
- Expand to include Windows event log monitoring.

---

## 🧑‍💻 Author

**Geetansh Chawla**  
Aspiring Cybersecurity Analyst  
[LinkedIn](https://www.linkedin.com/in/getnsh/) • [Email](mailto:geetanshchawla2003@gmail.com)
