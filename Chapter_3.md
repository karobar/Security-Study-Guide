# Connectivity Protocols
## IPv4
### Subnetting
 - isolates traffic
 - increases efficiency
 - CIDR notation uses the '/' followed by the number of 1s in the subnet mask
   - 255.255.255.0 becomes /24

### Classes 

Class | Range 
---|---
A  | [0-128)
B | [128-192)
C | [192-224)

### Private Addresses
can only be used within a private network for configuration

Class | Range 
---|---
A | [10-11)
B | [172.16-172.32)
C | [192.168-192.169)

### Reservation
A set of addresses to request from the DHCP server so that specific hosts can have specific addresses
### APIPA (Automatic Private IP Addressing)
 - 169.254.0.1-169.254.255.255
 - Not internet-routable
 - assigned if a device can't get an address (or one requested by reservation)

## TCP
three way hadnshake, SYN/ACKs
## UDP
DoS attack favorite
## ICMP
 - DoS attack favorite
 - common to block ICMP at firewalls and routers, which prevents discovering devices in a network with a _host enumeration sweep_

## ARP (Address Resolution Protocol)
 - resolves IPv4 addresses to MAC addresses
 - TCP/IP uses the IP address to get a packet to a destination network, but once it arrives on the destination network, it uses the MAC address to get it to the correct host. ARP is required once the packet reaches the destination subnet. 
 - ARP poisoning uses ARP packets to give clients false hardware address updates and attackers use it to redirct or interrupt network traffic

## NDP (Neighbor Discovery Protocol)
 - performs several functions for IPv6
 - performs address resolution similar to ARP
 - autoconfigures device IPv6 addresses
 - discovers other devices on the network

# Encryption Protocols
###### SSH
can encrypt:
 - 'TCP Wrappers', a type of ACL used on Linux and Unix to filter traffic
 - SFTP traffic
 - SCP traffic

###### FTPS
###### SFTP
###### SCP
###### SSL & TLS
 - TLS is a replacement for SSL
 - can encrypt other protocols like HTTPS, SMTP, and LDAP

###### IPsec
 - encapsulates and encrypts IP packets
 - native to IPv6, but works with IPv4
 - Two modes: **Tunnel** and **Transport**
   - Tunnel Mode encrypts entire IP packets, and is used in VPNs
   - Transport mode only encrypts the payload, used in private networks
 - Two main components:
   - Authentication Header (AH)
   - Encapsulating Security Payload (ESP)
 - provides authentication and encryption
 - uses IKE (Internet Key Exchange) to authenticate clients
   - creates security associations for the VP and then uses those associations to set up a secure channel between the client and the VPN server 

---
# Application Protocols
###### HTTP
###### HTTPS
###### FTP
###### SFTP
###### FTPS
###### TFTP (Trivial File Transfer Protocol)
 - uses UDP
 - used to transfer smaller amounts of data, such as when communicating with network devices
 - many attacks have used TFTP
 - not an essential protocol on most networks
 - usually disabled

###### Telnet
 - legacy protocol used to connect to remote systems or network devices
 - command-line interface
 - some admins use Telnet to connect to routers and make configuration changes
 - transmits data in cleartet
 - less-secure alternative to SSH

###### SNMP (Simple Network Management Protocol)
 - monitors and manages the configuration network devices
 - _SNMP agents_ are installed on devices and send status information to an SNMP manager via notifications known as _traps_ (often _device traps_)
 - SNMPv2 and SNMP3 are much more secure

###### NetBIOS
name resolution service for NetBIOS names on internal networks
###### LDAP
###### Kerberos
###### Microsoft SQL Server
###### RDP 

---
# Email Protocols
###### SMTP
###### POP3
###### IMAP4 (Internet Message Access Protocol)
 - used to store email on an email server
 - allows a user to organize and manage email in folders on the server

---
# DNS (Domain Name System)
 - most DNS servers on the net are Unix-like run BIND (Berkeley Internet Name Domain) software. Microsoft has alternatives
 - Occasionally, DNS servers share information/records with each other in a process known as a **zone transfer**
 - If attackers are able to access zone data on DNS server, they can map out an entire network

###### AAAA Record
identifies IPv6 address of a given name. Like A records. 
###### A record
 - also called a host record
 - identifies IPv4 address of a given name.  
 - Client ----name---> Server; Client <----address---- Server

###### MX record
identifies a mail server
###### CNAME record
identifies aliases
###### PTR (pointer) record
 - The opposite of an A record. 
 - Client ----address---> Server; Client <----name---- Server

###### MX (Mail Exchanger)
 - identifies a mail server
 - linked to an A or AAAA record of the mail server

###### CNAME (Canonical Name)
 - aka an alias
 - allows a single system to have multiple names associated with a single IP addr. 

---
# Ports
 - 65535 total TCP ports, 65535 total UDP ports
 - TCP/IP works with the client OS to maintain a table of client-side ports. This table associates port numbers with different applications that are expecting return traffic. Client-side ports start at port 49,152 and increment up to 64435. If all are used up, it wraps back around to 49,152

--- 
# Network Devices
### Hubs
between 4 and 32 physical ports
### Switch 
many have a console port that admins can use to monitor all traffic, which can be useful to an attacker
###### STP (Spanning Tree Protocol)
prevent switching-loop problems 
###### RSTP (Rapid STP)
faster but doesn't authenticate
###### VLAN
 - uses a switch to group computers into a virtual network
 - extra security due to isolation of traffic
 - separates based on _logical needs_ instead of _physical location_

###### 802.1x Port Security
a port-based authentication protocol
 - provides much stronger port security than simply disabling unused ports or using MAC address filgering
 - requires that users or devices authenticate when they connect to a specific access point, or a specific physical port
 - can be implemented in both wireless and wired networks
 - An 802.1x server is implemented as a RADIUS or Diameter server
 - you can configure an 802.1x server with a VLAN to redirect unauthorized devices

# Routers
###### Firewalls
 - use ACLs as rules
 - implicit deny
 - software or hardware
 - network or host
 - linux systems support **iptables** (and many additions such as ipv6tables, arptables, etc.), commonly referred to as xtables
 - can also be implemented as a WAF (Web Application Firewall) to protect a single web app, commonly hosted on a web server as an additional layer of security

---
# Address Translation
### NAT
a protocol that translates public IP addrs into private IP addrs and vice versa
 - not compatible with IPsec

###### Static NAT
single public IP addr one-to one with single private IP addr
###### Dynamic NAT
multiple public addresses in a one-to-many map, based on load
### Port Address Translation (PAT)
allows many internal devices to share one public IP
### Dynamic Network Address Translation (DNAT) 
uses multiple public IP addresses instead of just one

---
# UTM (Unified Threat Management)
###### URL filter
can block access to types of sites
###### Content/Malware inspection
don't block access to sites
###### Web Security Gateway
 - a type of UTM that can protect against multiple threats, including email attachments, embedded code in web pages, and spam
 - Strength in content filtering

---
# OSI model
Name|Devices|Protocols
---|---|---
physical | cables **hubs** | Ethernet, cable protocols
Data link| Switches | MAC, **ARP, NDP, VLANs**
Network | Routers, **Layer 3 Switches**| IP, **IPsec, ICMP** |
Transport||TCP,UDP| 
Session||
Presentation||
Application|Proxies, application-proxy firewalls, web app firewalls, web security gateways, UTM security appliances | **DNS, FTP, FTPS**, HTTP, HTTPS, **LDAP, POP3, RDP, SCP, SFTP, SMTP, SNMP, SSH, Telnet, and TFTP**
