
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