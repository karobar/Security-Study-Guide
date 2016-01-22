# Glossary
---
###### Tailgating 
Sneaking in behind somebody else who has access

---
###### Mantrap
 - highly  effective at preventing unauthorized entry
 - can prevvent tailgating.

---
###### Least Privilege
ensures users are granted only the access they need to perform their jobs, and no more.

---
###### SFTP (Secure Files Transfer Protocol)

---
###### TFTP (Trivial File Transfer Protocol)

---
###### PGP (Pretty Good Privacy) aka GPG (GNU Privacy Guard)
- primarily used to encrypt mail
- can also be used to encrypt data at rest

--- 
###### SMTP (Simple Mail Transfer Protocol)
transmits data in cleartext (unless combined a with encryption protocol)

---
##### STP (Spanning Tree Protocol)
prevent switching-loop problems 
###### RSTP (Rapid STP)
faster but doesn't authenticate

---
###### SSID (Service Set IDentifier)

---
###### DHCP (Dynamic Host Configuration Protocol)

---
###### Flood guards
Blocks SYN flood attacks

--- 
###### Anomaly/Heuristic/Behavior-based Detection System
compare current activity with a baseline

---
###### Signature-base System
uses signatures similar to antivirus software

---
###### Honeypot
a **server** designed to look valuable to attackers in order to divert attacks

---
###### PPTP (Point-to-point Tunneling Protocol)

--- 
###### Honeynet
a fake network designed to look valuable to attackers in order to divert attacks

---
###### MAC (Media Access Control) address

---
###### Evil Twin
a rogue access point with the same SSID as an authorized access point

---
###### SCADA (Supervisory Control And Data Acquisition) Network

---
###### TOTP (Time-based One-Time Password)
Protocol used to create passwords that expire after 30 seconds.

---
##### RADIUS (Remote Authentication Dial-In User Service)
An AAA (Authentication, Authorization, and Accounting) protocol
###### 802.1x
 - An 802.1x server is implemented as a RADIUS server
 - An 802.1x server provides port-based authentication
 - can prevent unauthorized devices from connecting to a network
 - you can configure an 802.1x server with a VLAN to redirect unauthorized devices
 
---
###### TACACS+ 
Proprietary to Cisco

--- 
###### WPS (Wi-Fi Protected Setup)
 - a standard designed to simplify the setup of a wireless network
 - does not implement usernames

---
#### EAP-TTLS
 - an 802.1x solution
##### EAP (Extensible Authentication Protocol)
###### PEAP (Protected EAP)
requires a certificate
###### LEAP (Lightweight EAP)
weaksauce
###### TTLS (Tunneled Transport Layer Security)

--- 
###### PSK (WPA2-preshared key)
does not authenticate users based on their usernames

--- 
###### RDP (Remote Desktop Protocol)

---
###### Stateless Inspection
packet filtering

---
###### Yagi antennas
directioinal antennas

---
# IPS (Intrusion Prevention System)
###### NIPS (Network IPS)
 - installed on networks
 - can intercept malicious traffic coming into the network
###### HIPS (Host-Based IPS)

--- 
# UTM (Unified Threat Management)
###### URL filter
can block access to types of sites
###### Content/Malware inspection
don't block access to sites

---
# Encryption
###### TLS (Transport Layer Security)
- Secures transmissions for data in transit
- Doesn't have a default port, use the port based on what it's encrypting
###### SSL 
Doesn't have a default port, use the port based on what it's encrypting
###### FTPS (File Transfer Protocol Secure)
uses either SSL or TLS 
###### HTTPS
uses SSL or TLS
###### CCMP (Counter mode cipher block Chaining Message authentication code Protocol)
provides stronger encryption than TKIP
###### TKIP (Temporal Key Integrity Protocol)
###### WEP (Wired Equivalent Privacy)
 - outdated wireless encryption
 - weak IVs (initialization vectors) used for key transmission
 - uses the RC4 stream cipher (which is strong)
###### WPA & WPA2 (Wi-Fi Protected Access)
wireless encryption

---
# Address Translation
### Port Address Translation (PAT)
allows many internal devices to share one public IP
### Dynamic Network Address Translation (DNAT) 
uses multiple public IP addresses instead of just one

---
# DNS
###### AAAA Record
identifies IPv6 address of a given name.
###### A record
identifies IPv4 address of a given name. 
###### MX record
identifies a mail server
###### CNAME record
identifies aliases

---
# Big List Of Ports
ID | #
--- | ---
 HTTP | TCP 80
 HTTPS | 443
 DNS | 53
 SSH (and therefore SCP, SFTP...) | TCP 22
 FTPS | 989 or 990
 TFTP | UDP 69
 RDP | TCP 3389
 Telnet | TCP 23
 SMTP | TCP 25
 FTP | TCP 21
 
---

 ---
# Firewalls
 - use ACLs as rules
 - implicit deny
---
# CIA
Confidentiality | Integrity | Availability
---|---|---
| protecting/securing data | ensure systems are not susceptible to unauthorized changes. | ensure critical systems provide uninterrupted service 
|encryption|hashes|RAID (Redundant Array of Inexpensive Disks)|
|access controls|||
|steganography|||
---
# Controls
### Technical Controls
###### Disk encryption
### Preventative Controls
Attempt to prevent incidents
###### Cable locks
###### Hardening Systems
 - Makes them more secure than their default configuration, but doesn't protect data after device is lost
 - Disabling unnecessary services
### Management Controls
###### Risk assessment 
### Monitoring Controls
###### CCTVs
### Access Controls
##### ACLs - Access Control List
Generally take the following format:  
Permission | Protocol | Source | Destination | Port
--- | --- | --- | --- | ---
DENY or ALLOW| TCP/UDP/IP, occasionally ICMP |  IP addr (or range,subnet,ANY) | IP addr (or range,subnet,ANY)| 
  
 - rules implemented on routers & firewalls
 - basic packet filtering
      - IP addr (and subnet ID)
      - ports 
 - identify what traffic is allowed or denied
 - can allow incoming and/or outgoing traffic
###### Implicit Deny
 - Last rule in an ACL
 - Sometimes automatic, sometimes manual
 - May look like "Deny Any Any" or "Deny All All"
##### Proximity Card
 - won't prevent tailgating
##### Cipher Lock
 - door access control
 - won't prevent tailgating
#### Access control models
###### Mandatory Access Control (MAC)
 - uses sensitivity labels and classification levels
 - effective at restricting access on a need-to-know basis
###### Discretionary Access Control (DAC)
 - specifies that every object has an owner
 - assigns permissions based on object ownership
 - might identify owners in a list
###### Role-based access control (role-BAC)
 - uses group-based privileges
###### Rule-base access control (rule-BAC)
 - uses rules that trigger in response to events

---
# Sign-On
### Single Sign-On (SSO)
Users only have to log on once
###### SAML
used with web-based applications
### Same Sign-On
Users can access multiple systems using the same credentials, but they have to enter their credentials again each time they access a new resource. 

---
# Authentication
Something you have | Something you are | Something you know 
---|---|---
|Hardware Tokens<br>Example: RSA tokens<br>uses a one-time password for authentication.| Biometrics | PIN 
|smart card|fingerprint|password|
||retina||
###### Do Not Require Hardware
 - PIN
 - password
###### Digital Signature
 - **non-repudiation**
 - integrity
  ---