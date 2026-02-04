# SOC Homelab Project – Security Onion, Wazuh, Kali, OpenVAS

## Overview
This project is a hands-on SOC homelab designed to simulate real-world attack, detection, and incident response workflows.

The lab focuses on **detection, investigation, and response**, not just tool installation or exploitation.

## Architecture
- Hypervisor: VMware
- Isolated NAT network: `cyberlab (192.168.100.0/24)`
- No access to home network
- Controlled internet access (optional)

### Systems
- Security Onion SIEM – `192.168.100.10`
- Windows Server 2019/2022 (AD + victim) – `192.168.100.20`
- Kali Linux (attacker) – `192.168.100.50`
- Wazuh EDR (manager on Security Onion)
- OpenVAS / Greenbone vulnerability scanner

## Tools Used
- Security Onion (Suricata, Zeek, Elastic, Kibana)
- Wazuh EDR
- Sysmon
- Winlogbeat
- Kali Linux (Nmap, Metasploit, Responder, Empire, CrackMapExec)
- OpenVAS (Greenbone)

## Project Goals
- Detect attacker activity using SIEM and EDR
- Correlate logs across network and endpoint sources
- Simulate realistic attack scenarios
- Perform SOC-style investigation and incident response
- Document detections and findings like a real SOC analyst

## Status
- [x] SIEM deployed and stable
- [x] Windows logs ingested into Security Onion
- [x] Sysmon telemetry active
- [ ] SOC detections and dashboards
- [ ] Attack simulation and validation
- [ ] Incident response documentation

## Disclaimer
This lab is for **educational purposes only**.  
All attacks are performed in an isolated environment intentionally built for defensive learning.
