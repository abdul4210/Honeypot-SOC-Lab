# Honeypot SOC Lab

In this project, I build a cloud-based lab using Microsoft Azure and Sentinel to demonstrate security monitoring, log collection, and threat analysis. I deploy a Windows 11 virtual machine, configure logging and network access, and forward security events into a log analytics workspace. Using KQL, I analyze authentication logs, enrich event data with geographic information, and visualize attack patterns through a world map.

---

### Tools Used
 - Azure Virtual Machine
 - Microsoft Sentinel
<img width="956" height="543" alt="image" src="https://github.com/user-attachments/assets/976a8384-5f00-4027-8dad-9de50e4be1fa" />

---

### Lab Workflow

**Environment Setup**:
   - A virtual machine is created in Azure that will act as the honeypot
   - The VM is configured to be easily discoverable over the internet by allowing any inbound traffic into its virtual network and disbaling its firewalls.
<img width="1168" height="562" alt="1) vm made" src="https://github.com/user-attachments/assets/58b2a2b1-9d4b-4214-8431-1c48c45b957f" />
<img width="1577" height="832" alt="2) allow trafic" src="https://github.com/user-attachments/assets/65e8e97f-1d2e-427f-9c6d-de20c7f684a0" />
<img width="1305" height="825" alt="3) disable firewall" src="https://github.com/user-attachments/assets/3ac44e06-ba69-4ca9-b17f-fbeffb1a62b2" />

---
