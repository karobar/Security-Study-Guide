
# Big List Of Ports
ID | #
--- | ---
 HTTP | TCP 80
 HTTPS | 443
 DNS | 53

# ACLs - Access Control List
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
 
# Firewalls
 - use ACLs as rules
 - implicit deny

# CIA
Confidentiality | Integrity | Availability
---|---|---
| protecting/securing data | ensure systems are not susceptible to unauthorized changes. | ensure critical systems provide uninterrupted service 
|encryption|hashes|RAID (Redundant Array of Inexpensive Disks)|
|access controls|||
|steganography|||

### Digital Signature
 - authentication
 - **non-repudiation**
 - integrity
### Least Privilege
ensures users are granted only the access they need to perform their jobs, and no more.
### Flood guards
blocks SYN flood attacks

# Authentication
Something you have | Something you are | Something you know | Do Not Require Hardware
---|---|---|---
|Hardware Tokens<br>Example: RSA tokens<br>uses a one-time password for authentication.| Biometric (ex: fingerprint | PIN ||
|||password||

