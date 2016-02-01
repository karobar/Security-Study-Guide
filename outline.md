# Glossary

###### BCP (Business Continuity Plan)
often contains a succession planning chart

###### ESD (ElectroStatic Discharge)



###### DRP (Disaster Recovery Plan)

###### AUP (Acceptable Use Policy)

###### SAML (Security Assertion Markup Language)
an XML-based data format
used for SSO on web browsers

###### 3DES (Triple Data Encryption Standard)
weaker than AES




###### PKI (Public Key Infrastructure)

###### PBKDF2 (password Based Key Derivation Function 2)
key stretching technique designed to protect against brute force attempts 
salts the password with additional bits
an alternative is _bcrypt_

###### CRL (Certification Revocation List) 
a list of certificates that a Certificate Authority (CA) has revoked

###### Sniffing
The practice of capturing traffic with a protocol analyzer. 

###### Salting
a method used to prevent brute force attacks to discover passwords

###### Failover cluster
provides fault tolerance for servers 
can increase data availability
expensive



###### UPS (Uninterruptible Power Supply)

###### Onboarding/Offboarding business partners
bring new/returning people up to speed on policies

###### SYN
short for SYNchronize packet, the first step of the three-way handshake

###### Orphan VM
VM without updates

###### Mantrap
 - highly  effective at preventing unauthorized entry
 - can prevent tailgating.

# SSL
security on each end (end-to-end)

###### Captive Portals
a portal on some wireless access points which require credentials before access

###### LDAP (Lightweight Directory Application Protocol)

###### Fuzzing
 - injects random or unexpected data into an application
 - tests the effectiveness of input validation

###### RTO (Recovery Time Objective)
measure of time it takes to recover a resource

###### RPO (Recovery Point Objective)
point in time where you recover to

###### DLP (Data-Loss Prevention) System
 - analyzes network traffic
 - detects if confidential company data is included
 - can limit documents copied to a USB drive using content filters

###### IaaS (Infrastructure as a Service)
a Cloud computing option

###### SFTP (Secure File Transfer Protocol)

###### TFTP (Trivial File Transfer Protocol)

###### PGP (Pretty Good Privacy) aka GPG (GNU Privacy Guard)
- primarily used to encrypt mail
- can also be used to encrypt data at rest

###### SMTP (Simple Mail Transfer Protocol)
transmits data in cleartext (unless combined a with encryption protocol), usually from server to server



###### SSID (Service Set IDentifier)

###### DHCP (Dynamic Host Configuration Protocol)

###### TPM (Trusted Platform Module)
 - included in many new laptops 
 - provides a mechanism for vendors to provide hard drive encryption.
 - doesn't require purchasing additional hardware

###### HSM
 - removable hardware device
 - performs hard drive encryption

###### Flood guards
Blocks SYN flood attacks

###### Anomaly/Heuristic/Behavior-based Detection System
compare current activity with a baseline

###### Signature-base System
uses signatures similar to antivirus software

###### Honeypot
a **server** designed to look valuable to attackers in order to divert attacks

###### PPTP (Point-to-point Tunneling Protocol)

###### Honeynet
a fake network designed to look valuable to attackers in order to divert attacks

###### MAC (Media Access Control) address

###### SCADA (Supervisory Control And Data Acquisition) Network

###### TOTP (Time-based One-Time Password)
Protocol used to create passwords that expire after 30 seconds.

##### RADIUS (Remote Authentication Dial-In User Service)
An AAA (Authentication, Authorization, and Accounting) protocol

# Site Survey
 - Moving a wireless access point around the room
 - formal and informal flavors

###### 802.1x
 - An 802.1x server is implemented as a RADIUS server
 - An 802.1x server provides port-based authentication
 - can prevent unauthorized devices from connecting to a network
 - you can configure an 802.1x server with a VLAN to redirect unauthorized devices
 
###### TACACS+ 
Proprietary to Cisco

###### WPS (Wi-Fi Protected Setup)
 - a standard designed to simplify the setup of a wireless network
 - does not implement usernames

###### PSK (WPA2-preshared key)
does not authenticate users based on their usernames

###### RDP (Remote Desktop Protocol)

###### Stateless Inspection
packet filtering

###### Yagi antennas
directioinal antennas

##### SNMP (Simple Network Management Protocol)
gathers/pushes configuration parameters from devices on a network

##### POP3 (Post Office Protocol v3)
only retrieves emails from servers
by default, sends a signal to server to delete

##### IMAP (Internet Message Access Protocol)
allows searching of inbox, creation of folders














---
# MAC (Message Authentication Code)
provides integrity similar to how a hash is used
###### HMAC (Hash-based Message Authentication Code)
hashing algorithm used with IPsec
RFC 4835 mandates the use of HMAC for authenticity and integrity

---
# Certificates
###### OCPS (Online Certificate Status Protocol)
validates trust with certificates
only returns short responses such as good, unknown, or revoked
###### CSR (Certificate Signing Request)


---
# Ciphers
### Block Cipher
encrypts data in specific-sized blocks, such as 64/128-bit blocks
###### AES (Advanced Encryption Standard)
###### DES (Data Encryption Standard)
###### MD5 (Message Digest 5)

---
# IPS (Intrusion Prevention System)
scans traffic coming into a network to block attacks
###### NIPS (Network IPS)
 - installed on networks
 - can intercept malicious traffic coming into the network

###### HIPS (Host-Based IPS)

# IDS (Intrusion Detection System)
###### NIDS (Network IDS)

---
# EAP-TTLS
 - an 802.1x solution

### EAP (Extensible Authentication Protocol)

###### PEAP (Protected EAP)
requires a certificate

###### LEAP (Lightweight EAP)
weaksauce

--- 
# UTM (Unified Threat Management)
use content filters
###### URL filter
can block access to types of sites

###### Content/Malware inspection
don't block access to sites

---


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
 SSL (and therefore HTTPS, ...) | 443
 DNS | 53
 SSH (and therefore SCP, SFTP...) | TCP 22
 FTPS | 989 or 990
 TFTP | UDP 69
 RDP | TCP 3389
 Telnet | TCP 23
 SMTP | TCP 25
 FTP | TCP 21
 VPN & PPTP | TCP 1723
 SNMP | 160,161,162
 POP3 | 110
 IMAP | 143
 ICMP | 
 
---
# Protocol IDs
Protocol | ID
--- | ---
IPsec | 50

 ---
# Firewalls
 - use ACLs as rules
 - implicit deny
 - software or hardware
 - network or host

---
# CIA
Confidentiality | Integrity | Availability
---|---|---
|Prevents the unauthorized disclosure of data| ensure systems/data are not susceptible to unauthorized changes.
| _authorized personnel_ **can** access the data | hashes | ensure critical systems provide uninterrupted service 
_unauthorized personnel_ **cannot** access the data| Message Authentication Code (MAC)|
|encryption||RAID (Redundant Array of Inexpensive Disks)|
|access controls|||
|steganography|||

## Confidentiality
### Encryption
##### TLS (Transport Layer Security)
- Secures transmissions for data in transit
- Doesn't have a default port, use the port based on what it's encrypting
###### TTLS (Tunneled Transport Layer Security)

##### SSL 
Doesn't have a default port, use the port based on what it's encrypting

##### FTPS (File Transfer Protocol Secure)
uses either SSL or TLS 

##### HTTPS
uses SSL or TLS

##### WEP (Wired Equivalent Privacy)
 - outdated wireless encryption
 - weak IVs (initialization vectors) used for key transmission
 - uses the RC4 stream cipher, which repeats keys

##### WPA & WPA2 (Wi-Fi Protected Access)
 - wireless encryption
 - WPA uses **TKIP (Temporal Key Integrity Protocol)**  
 - WPA2 uses **CCMP (Counter mode cipher block Chaining Message authentication code Protocol)**

## Access Controls
Ensure that only authorized personnel can access data.   
Identification|Authentication|Authorization
---|---|---
Users claim an identity (i.e. with a username) | users prove their identity (i.e. with a password) | grant or restrict access to resources (i.e. permissions)
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

###### Discretionary Access Control (DAC)
 - specifies that every object has an owner
 - assigns permissions based on object ownership
 - might identify owners in a list

###### Mandatory Access Control (MAC)
 - uses sensitivity labels and classification levels
 - effective at restricting access on a need-to-know basis
 - strongest access control method available

###### Network Access Control (NAC)
 - dictate a baseline on a _health-check_ server
 - any system attempting to log on has to meet the baseline (programs, versions, etc.)
 - can also involve a _remediation_ server to work through issues on the connecting system

###### Role-based access control (role-BAC)
 - uses group-based privileges
###### Rule-base access control (rule-BAC)
 - uses rules that trigger in response to events

## Hashing
###### SHA-1 (Secure Hash Algorithm 1)


---
# Security Controls
impementation and enforcement

Technical | Management | Operational
---|---|---
Encryption | Risk assessment | Procedures
Passwords | Policies | Standards
|smart cards|Privacy Policy| Change Management
|least privilege|Acceptable Use Policy: _using resources_|
||Security Policy: _password length, etc_|
||Mandatory Vacations|
||Job Rotation|
||Separation of duties|
||Least Privilege: _ensures users are granted only the access they need to perform their jobs, and no more_

Deterrent | Preventative | Detective | Compensating 
---|---|---|---
||Cable locks||original control is too expensive
||Hardening: _disabling unnecessary services_||

~~### Monitoring Controls~~
~~###### CCTVs~~



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
# Attacks
##### Tailgating 
Sneaking in behind somebody else who has access

##### VM escape 
runs on VM, allows the attacker to control a hypervisor and attack other VMs or the physical host

##### Evil Twin
a rogue access point with the same SSID as an authorized access point

##### Logic Bomb
code that exectes in respose to an event

##### Rootkit
includes hidden processes

##### Trojan
looks beneficial but includes a malicious componenet

##### Phishing
 - sends unwanted email to users
 - cannot be prevented with input validation
###### Whaling
a phishing attack which targets  executives
###### Spear phishing
a targeted phishing attack

##### XSRF (cross-Site Request Forgery)

##### XSS (cross-site scripting)
inserting HTML or JavaScript code into a web site or email

##### LDAP injection
injecting LDAP commands to query a directory service database

##### Buffer Overflow
sends more data or unexpeceted data

##### Pharming attack
attempts to redirect users from one web site to another web site

### DoS (Denial of Service)
###### SYN flood
###### DDos (Distributed DoS)
###### Smurf Attack
doesn't attempt to  connect to systems but instead sends pings

### Virus
tries to replicate itself

###### Armored Virus
uses techniques to resist reverse engineering

---
# IPv4
### Classes 
determine the class by looking at the first octet
###### Class A (1-126)
###### Class B (128-191)
###### Class C (191-223)
### Private Addresses
can only be used within a private network for configuration
###### Class A (10.0.0.0-10.255.255.255)
###### Class B (172.16.0.0-172.16.255.255)
###### Class C (192.168.0.0-192.168.255.255)
### Reservation
A set of addresses to request from the DHCP server so that specific hosts can have specific addresses
### APIPA (Automatic Private IP Addressing)
 - 169.254.0.1-169.254.255.255
 - Not internet-routable
 - assigned if a device can't get an address (or one requested by reservation)

---
# Risk
### Risk Calculations
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

### Risk Response
###### Mitigate 
###### Transfer
###### Avoidance
###### Deterrence
###### Acceptance

---
##### STP (Spanning Tree Protocol)
prevent switching-loop problems 

###### RSTP (Rapid STP)
faster but doesn't authenticate

---
###### Response Process
1. Incident Preparation
2. <INCIDENT!>
3. Incident Identification
4. Escalation and Notification
5. Incident Mitigation 