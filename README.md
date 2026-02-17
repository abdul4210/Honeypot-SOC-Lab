# Honeypot SOC Lab

In this project, I build a cloud-based lab using Microsoft Azure and Sentinel to demonstrate security monitoring, log collection, and threat analysis. I deploy a Windows 11 virtual machine, configure logging and network access, and forward security events into a log analytics workspace. Using KQL, I analyze authentication logs, enrich event data with geographic information, and visualize attack patterns through a world map.

---

### Tools Used
 - Azure Virtual Machine
 - Microsoft Sentinel
<img width="956" height="543" alt="image" src="https://github.com/user-attachments/assets/976a8384-5f00-4027-8dad-9de50e4be1fa" />

---

### Lab Steps

**Honeypot Creation**:
   - A virtual machine is created in Azure that will act as the honeypot
   - The VM is configured to be easily discoverable over the internet by allowing any inbound traffic into its virtual network and disbaling its firewalls.
<img width="1168" height="562" alt="1) vm made" src="https://github.com/user-attachments/assets/58b2a2b1-9d4b-4214-8431-1c48c45b957f" />
<img width="1577" height="832" alt="2) allow trafic" src="https://github.com/user-attachments/assets/65e8e97f-1d2e-427f-9c6d-de20c7f684a0" />
<img width="1305" height="825" alt="3) disable firewall" src="https://github.com/user-attachments/assets/3ac44e06-ba69-4ca9-b17f-fbeffb1a62b2" />

---

**Log Repository**
 - A mock SOC is setup using Sentinel as the SIEM
 - A log analytics workspace is created in Azure which will be the central log repository
 - A Sentinel workspace is created and connected to log analytics
 - A data collection rule is created to feed the VM's logs into the workspace
<img width="1770" height="747" alt="4) law" src="https://github.com/user-attachments/assets/9e349e59-781c-480b-b64d-5ce458f3ec72" />
<img width="857" height="487" alt="5) sent workspace" src="https://github.com/user-attachments/assets/734b5c0d-f8e4-41f3-8791-521b51fa6260" />
<img width="768" height="737" alt="7) dcr" src="https://github.com/user-attachments/assets/edf4a47e-fc90-4b4e-bb84-fd73d91cb080" />

---

**Log Inspection**
 - After just a few hours of the VM being on, The query shows many failed log-in attempts coming from real attackers over the internet
<img width="1826" height="815" alt="8) query 1" src="https://github.com/user-attachments/assets/43cb34df-f474-4b54-918d-98fca97a5a1d" />

---

**Log Enrichment**
 - A watchlist is created in Sentinel with an imported CSV file containing geographical data
<img width="1477" height="626" alt="9) watchlist" src="https://github.com/user-attachments/assets/88604ecd-d6be-4b6c-b75f-ffe4d65668d1" />
<img width="667" height="936" alt="10) ip sheet" src="https://github.com/user-attachments/assets/e1b80715-6051-4574-b9f1-9ff087b9e8dd" />

---

**Query of enriched logs**
 - The logs can now be queried to show where attacks are coming from
<img width="1530" height="725" alt="11) query 2" src="https://github.com/user-attachments/assets/567c323b-a998-45a2-a9a5-23d384033110" />

---

**Attack Map**
 - A map is created to provide visualizion of attacker locations using a Sentinel workbook with JSON
<img width="917" height="672" alt="13) json" src="https://github.com/user-attachments/assets/9da9954a-cff9-43c0-bcca-85a11a443735" />
<img width="1538" height="733" alt="12) map" src="https://github.com/user-attachments/assets/341c712a-f48e-4acd-8aee-c430140dfe77" />
