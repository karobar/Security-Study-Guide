
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
 
