##### Tailgating 
Sneaking in behind somebody else who has access

##### VM escape 
runs on VM, allows the attacker to control a hypervisor and attack other VMs or the physical host

##### Evil Twins
 - a rogue access point with the same SSID as an authorized access point
 - an unknowing user connects to the evil twin, then all traffic goes through the evil twin instead of the legitimate access point

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
 - sends more data or unexpected data
 - many start with a series of no operation (NOOP) commands, called a NOOP sled or NOOP ramp

##### Pharming attack
attempts to redirect users from one web site to another web site

### DoS (Denial of Service)
###### SYN flood
###### DDos (Distributed DoS)
###### Smurf Attack
doesn't attempt to  connect to systems but instead sends pings
###### MAC Flood
flood a swich with tons of Ethernet frames, consuming the memory of the switch and forcing out legitimate entries on the switch's address table. Effectively turns a switch into a hub

### Worms
###### Stuxnet
 - a worm designed to attack a specific embedded system
 - used in one of Iran's nuclear enrichment facilities, causing centrifuges to spin fast enough to tear themselves apart
 - Process:
     1. **Infect:** Windows systems were infected through USB drives
     2. **Search:** look through the network for a specific system
     3. **Update:** download an updated version of the worm
     4. **Compromise:** use zero-day vulnerabilities
     5. **Control:** control the system and send commands as desired
     6. **Deceive and destroy:** Send false data to monitors indicating everything is fine

### Virus
tries to replicate itself

###### Armored Virus
uses techniques to resist reverse engineering