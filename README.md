# QRCE-QRadar-Community-Edition-Rules

## Hi 👋, I'm Bhargav
**SOC / Blue-Team Engineer @ Cyberlancers**

- 🔭 I’m currently working on **QRCE – QRadar Community Edition Rule Pack** (this repo)
- 🤝 I’m looking to collaborate on **MITRE ATT&CK mapping** and **QRadar/Wazuh detection content**
- 🙌 I’m looking for help with **test data & false-positive tuning** (AD, DNS, Proxy, SMB)
- 📝 I share updates in Issues/PRs and on **[LinkedIn](https://www.linkedin.com/in/uppalapatibhargav/)**
- 💬 Ask me about **QRadar**, **Wazuh**, **ICS/IoT (MQTT, Modbus)**
- 📫 How to reach me: **bhargavu720@gmail.com** | **[LinkedIn](https://www.linkedin.com/in/uppalapatibhargav/)**

---

## About the Project
This repository is a living catalog of high-signal **QRadar** content:
- 🧭 **MITRE-mapped** detections with tactics/techniques/sub-techniques for analyst context
- 🧱 Clear split between **Detections** (offense-creating) and **Building Blocks** (reusable logic)
- 🧪 **CI validation** (`.github/workflows/validate.yml`) to keep YAML and schema consistent
- 📚 **Docs-ready**: structure works with MkDocs or GitHub Pages for publishing rule catalogs
- 🧩 **Dependencies captured** (reference sets, building blocks) to make deployments predictable

> We’ll grow from a starter set to a hardened library—prioritizing detections that reduce MTTD/MTTR and false positives.

---

## Skills
- **Programming & DB:** Python, Java, MySQL
- **Web:** HTML, CSS, PHP
- **SIEM & Blue Team:** IBM QRadar, Wazuh
- **Network & Security Devices:** Sophos Firewall, Fortinet **FortiGate** (basic), Grandstream switches
- **Network Security / IDS:** Suricata, Zeek, Nmap
- **Traffic & App Security Tools:** Wireshark, Burp Suite, **VirusTotal API**
- **Elastic Stack:** Filebeat, **Elasticsearch**, Kibana
- **Editor/IDE:** Visual Studio Code

---

## Future Plan
- **Clustered SIEM at scale:** QRadar/Wazuh in HA/multi-zone to handle high EPS
- **Cut false positives:** Continuous tuning with reference sets, test data, and rule tests
- **Real-time playbooks:** Concise, MITRE-mapped runbooks for top SOC use cases
- Add **Kafka/OTel pipelines** for scalable log shipping and replay
- **AI-assisted logs:** Deduplication, similarity grouping, and quick offense summaries
- **Custom & IoT logs:** Synthetic generators for Windows/Linux/Proxy/Firewall and IoT/ICS (MQTT, Modbus)
- **Compliance-ready content:** Map rules/playbooks to NIST CSF/800-61, CIS Controls, ISO 27001, PCI-DSS & GDPR; include evidence (rule IDs, tuning notes, retention, audit trails)
