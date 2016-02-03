# IDS & IPS
 - **Signature-based/definition-based** 
   - monitoring detects attacks based on known attack patterns
   - often use vulnerabilities listed in the **CVE (Common Vulnerabilities and Exposures list)**
 - **Anomaly-based/behavior-based/heuristic-based** 
   - monitoring detects attacks by first identifying normal operation through a baseline. It then compares current operations against the baseline to detect abnormal behavior
   - effective against zero-day exploits
 - a **passive IDS** logs an alert an may inform personnel
 - an **active IDS** takes action to change the environment

## IPS (Intrusion Prevention System)
 - scans traffic coming into a network to block attacks
 - All traffic passes through the IPS

###### NIPS (Network IPS)
 - installed on networks
 - can intercept malicious traffic coming into the network

###### HIPS (Host-Based IPS)

## IDS (Intrusion Detection System)
###### Packet Sniffing aka Protocol analyzing
###### NIDS (Network IDS)
###### HIDS (Host-based IDS)

---
# WAPs (Wireless Access Points)
  - Some WAPs connect the wireless clients to the wired network
  - Many WAPs also act as routers (All wireless routers are WAPs, not all WAPs are wireless routers)
  - the client and the WAP negotiate the highest throughput they can achieve without errors.
  - Isotropic, Omnidirectional/Dipole, Yagi/Directional

## Antenna Power
###### dBi
_Decibels-isotropic_ identifies the gain of an antenna and is commonly used with omni antennas
###### dBd
_Decibels-dipole_ identifies the gain of an antenna compared with a type of dipole antenna
###### dBm
_Decibels-milliwatt_ identifies the power level of the WAP

## Security Protocols
### EAP (Extensible Authentication Protocol)
provides a method for two systems to create a secure encryption key, also known as a PMK (Pairwise Master Key)

#### EAP-TLS
 - one of the most secure EAP standards
 - similar to PEAP, but requires certificates on the 802.1x server and each wireless clients

#### PEAP (Protected EAP)
 - requires a certificate
 - encapsulates and encrypts the EAP conversation in a TLS tunnel

###### EAP-TTLS (EAP-Tunneled TLS)
 - requires a certificate on the 802.1x server but not the clients
 - an extension of PEAP which allows systems to use some older authenticatoin methods such as PAP (Password Authentication Protocol)

#### LEAP (Lightweight EAP)
weaksauce

### WTLS and ECC
provide protection for smaller devices without a significant amount of processor power required by advanced security protocols such as WPA2
### WTLS (Wireless Transport Layer Security)
an implementation of TLS
### ECC (Elliptic Curve Cryptography)

## Captive Portals
a portal on some wireless access points which require credentials before access
## Isolation Mode
prevent wireless clients from connecting with each other

---
# WPS (Wi-Fi Protected Setup) 
 - allows users to configure a wireless network without typing in a passphrase
 - devices are configured by pressing buttons or by entering a PIN
 - recommended to turn off

##### WPS Brute Force
different PINs are tried until succeeding

--- 
# NFC (Near Field Communication) 
a group of standards used on mobile devices that allow them to communicate with other mobile devices when they are close to them.
### Bluetooth Wireless
uses MAC addresses
###### Discovery Mode
 - default bluetooth mode
 - MAC address is broadcasted
 - should be turned off

###### Bluejacking
sending unsolicited messages to nearby Bluetoooth devices, mostly harmless
###### Bluesnarfing
unauthorized access to or theft of information from a Bluetooth connection
###### Bluebugging
allow an attacker to take over a mobile phone

---
# Remote Access
the group of technologies that allow users to access an internal network from remote location
### RAS (remote access service)
provides access through dial-up or VPNs
### Telephony
the use of telephone technologies to connect computers
###### Dial-Up RAS
 - both the client and server need access to phone lines, and each must have a modem
 - allows access to a remote network over phone wires
 - typically PPP is used

### VPNs and VPN Concentrators
##### IPsec Tunneling
###### L2TP (Layer 2 Tunneling Protocol)
 - created by Cisco and Microsoft
 - creates a tunnel between devices
 - doesn't provide encryption
  - can be combined with IPsec, which is called L2TP/IPsec

###### NAT
breaks IPsec
##### SSL and TLS
can secure a VPN channel
##### PPTP 
secures a VPN channel, but is vulnerable
##### Site-to-Site VPNs
include two VPN servers that act as gateways for two networks separated geographically. Mostly transparent to the end user
##### VPN over Open Wireless
 - data should be encrypted.  HTTPS connections can be used

---
# Network Access Control (NAC)
 - dictate a baseline on a _health-check_ server
 - continuous security monitoring
 - any system attempting to log on has to meet the baseline (programs, versions, etc.)
 - can also involve a _remediation/quarantine_ server to work through issues on the connecting system
 - Usually includes checking the following:
   - Up-to-date antivirus software, and updated signature definitions
   - Up-to-date OS, and patches
   - Firewall enabled