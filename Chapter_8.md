# Risk Calculations
###### MTTR (Mean Time to Repair)
 - time it takes to fix a device
 - given by manufacturer

###### MTBF (Mean Time Between Failure)
 - how long you can use a device before it fails
 - given by manufacturer

###### MTTF (Mean Time to Failure)
for devices you don't plan to replace
###### ALE (Annualized Loss Expectancy)
If an incident were to happen, how much do you expect to lose per year. ALE = SLE X ARO
###### SLE (Single Loss Expectancy)
If a single vulnerability were exploited, what could be lost. SLE = ALE / ARO
###### ARO (Annualized Rate of Occurence)
How many times a threat could compromise a vulnerability. ARO = ALE / SLE

---
##### Risk Response
 - Mitigate 
 - Transfer
 - Avoidance
 - Deterrence
 - Acceptance

---
###### Response Process
1. Incident Preparation
2. <INCIDENT!>
3. Incident Identification
4. Escalation and Notification
5. Incident Mitigation 

---
# Attackers, and how they work/think
  1. **recon phase:** identify IP addresses of targets
  2. **recon phase:** identify open ports with a port scanner
  3. **recon phase:** identify operating system
  4. **recon phase:** Banner grabbing: send a telnet request for an HTTP banner with server info
  5. **attack phase**

###### APT(Advanced Persistent Threat)
a group that has capability and intent to launch sophisticated and targeted attacks, and there is ample evidence to suggest that they actually exist

---
# Vulnerability scans
 - Vulnerability scanners use a database of known vulnerabilities; they test systems against this database.
 - For exapmle, the MITRE corporation maintains the CVE (Common Vulnerabilities and Exposures) list, which is a public list funded by the U.S. government
 - **NOT THE SAME AS A VULNERABILITY ASSESSMENT**
 - checks technical controls only

---
# Vulnerability Assessments
 - broader than **vulnerability scans**
 - checks technical **and** nontechnnical vulnerabilities

---
# Protocol Analyzers
 - a NIC must first be configured into _promiscuous mode_ in order to capture all traffic
 - example: Wireshark

---
# Routine Audits
#### User Access Reviews
 - verify users have the rights and permissions they need, but no more
 - reviews what users have accessed, and can detect accounts from ex-employees that are still enabled

#### User Rights and Permissions Reviews
 - also verifies that users have the rights and permissions they need, but no more
 - identifies the privileges granted to users, and compares these against what the users need

---
# Log Types
 - Operating System Event Logs
 - Firewall and Router Access Logs
 - Antivirus logs
 - Application logs
 - Performance logs
