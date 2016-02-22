Confidentiality | Integrity | Availability
---|---|---
|Prevents the unauthorized disclosure of data| ensure systems/data are not susceptible to unauthorized changes. | ensure critical systems provide uninterrupted service 
| _authorized personnel_ **can** access the data | hashes | Disk redundancy (RAID)
_unauthorized personnel_ **cannot** access the data| Message Authentication Code (MAC)| Server Redundancy
|encryption| Digital Signatures | Failover Clusters | 
|access controls||virtualization|
|steganography|| load balancing |
|||site redundancy (cold/warm/hot)
|||backups
|||alternate power/UPSs
|||cooling systems
|||patching

--- 
# Confidentiality
### Encryption 
#### Symmetric/Secret-key/Session-key encryption
using the same key to encrypt and decrypt
Algorithm | cipher type | Block Size (bits) | Key Size (bits) |Comments
---|---|---|---|---
AES | block | 128 | 128, 192, or 256-bit | fast, efficient, and strong. 
DES | block | 64 | 56 | very old and broken
3DES | block | 64 | 56, 112, or 168 | uses multiple passes of DES. weaker than AES. 
RC4 | stream | N/A| 40-2048 | used in WEP, SSL, and TLS
Blowfish | block | 64 | 32-448 | DES replacement
Twofish | block | 128 | 128, 192, or 256 |
One-Time pad||||very old, used by spies

###### Diffie-Hellman
an algorithm used to privately shared symmetric keys between parties

#### Asymmetric encryption
 - uses a matched pair of keys
 - require a certificate and a PKI
 - resource intensive

Method | Comments 
---|---
RSA | widely used. a minimum of 1024 bit keys, but should probably use 2048
ECC | doesn't take much processing power

Static Keys | Ephemeral Keys
---|---
used by RSA | used for a single session
can be validated | comply with **perfect forward secrecy**, which means that given the _same_ input, the algorithm produces _different_ public keys

#### Ciphers
###### Stream Ciphers
- encrypt data one bit at a time
- example: RC4

###### Block ciphers
encrypts data in specific-sized blocks, such as 64/128-bit blocks

#### File and Folder-Level Encryption
###### GPG (GNU Privacy Guard) aka PGP (Pretty Good Privacy) [Linux] 
can encrypt mail, files, and folders
###### EFS (Encrypting File System) [Windows]
#### Hardware-Based Encryption
much quicker than software encryption
characteristic|(TPM) Trusted Platform Module | (HSM) Hardware Security Module
---|---|---
Hardware|chip in motherboard, usually included by deault | Removable/external hardware device purchased separate 
Uses|provides full disk encryption | High-end mission-critical servers
Authentication|verifies the drive has not moved | application authentication
Encryption Keys|Includes an RSA key burned into the chip. When activated, generates a storage root key, which is used to generate other keys | stores RSA keys used in asymmetric encryption and can generate keys

#### Transport encryption
Method | comments
---|---
TLS | Replacement for SSL. requires certificates issued by CAs. 
SSL | requires certificates issued by CAs. uses asymmetric encryption to share session keys, and symmetric encryption to encrypt data transmitted. 
IPsec | uses HMAC. can use AES or 3DES for encryption with ESP. When IPsec uses ESP, it encrypts the entire packet (including the header), then slaps another IP header on
SSH | 

#### FTPS (File Transfer Protocol Secure)
uses either SSL or TLS 

#### Wireless Encryption
##### WEP (Wired Equivalent Privacy)
 - outdated wireless encryption
 - weak IVs (initialization vectors) used for key transmission
 - uses the RC4 stream cipher, which repeats keys

##### WPA & WPA2 (Wi-Fi Protected Access)
 - wireless encryption
 - can operate in either **Personal** or **Enterprise** modes
   - when using personal mode, users access the wireless network anonymously with a PSK or passphrase. also known as WPA-PSK or WPA2-PSK
   - when using enterprise mode, users must authenticate with unique credentials before access to the wireless network. Uses an 802.1x server.
 - WPA 
     - uses **TKIP (Temporal Key Integrity Protocol)**.
        - encrypts each packet with a new key  
     - When first released, WPA used RC4 (Rivest Cipher 4) stream encryption with TKIP
 - WPA2 uses **CCMP (Counter mode cipher block Chaining Message authentication code Protocol)**

###### WPA Cracking Attacks
1. Use a wireless sniffer to capture packets
2. Wait for a wireless client to authenticate.
3. Once you have the encrypted passphrase from the four-way handshake, they can launch a brute-force attack

##### IVs (Initialization Vectors)
 - the encryption keys used in WEP are derived from the WEB key entered into the WEP and the wireless devices
 - WEP then uses an initialization vector (IV) to create the kys used for RC4.
   - An IV is a 24-bit number 
 - WEP combines a password with an IV to create a key, and then encrypts the packet with this key

###### IV attack
the attacker uses packet injection techniques to add additional packets into the data stream. The WAP responds with more packets, which increases the probability that it will reuse a key. 

## Access Controls
Ensure that only authorized personnel can access data.   

Identification|Authentication|Authorization
---|---|---
Users claim an identity (i.e. with a username) | users prove their identity (i.e. with a password) | grant or restrict access to resources (i.e. permissions)
||**something you know** (password,PIN) least secure||
||**something you have** (smart card,key fob/token, HOTP and TOTP)
||**something you are** (biometrics, fingerprint, retina) most secure
||**somewhere you are** (geolocation)
||**something you do** (touch screen gestures, behavioral biometrics, keystroke dynamics)
||Kerberos
||LDAP

##### Identity Proofing
 - the process of verifying that people are who they claim to be prior to issuing them credentials, or if they lose their credentials
 - security questions
 - password recovery

##### Proximity Card
 - won't prevent tailgating

##### Cipher Lock
 - door access control
 - won't prevent tailgating

### Authentication
###### Do Not Require Hardware
 - PIN
 - password

###### Digital Signature
 - provides non-repudiation 
 - also provide integrity
 - an **encrypted hash** of a message

##### Authentication Services
###### Kerberos
 - network auth. protocol within a MS Windows Active Directory domain or Unix 'realm'
 - uses a database of subjects or users (in MS windows, this is Active Directory)
 - Key Distribution Center (KDC) 
    - also known as a Ticket-Granting Tickets(TGT) server
    - issues timestamped tickets which expire after a certain time period

###### LDAP and Secure LDAP
 - LDAP (Lightweight Directory Application Protocol)
    - specifies formats and methods to query **directories** (a database of objects that provides a centrall access point to manage users, computers, and other directory objects)
    - an extension of the X.500 standard
    - Windows = Active Directory domains, Unix = LDAP
    - **Example**: A user _Homer_ in the _Users_ container within the _example.com_ domain is identified with the following LDAP string: `LDAP://CN=Homer,CN=Users,DC=example,DC=com`
    - CN is short for _common name_ or _container_,  depending on context; DC is short for _domain component_
    - Secure LDAP uses TLS or SSL to encryption to protect LDAP


###### Sign-On
**Single Sign-On (SSO):** 
 - Users only have to log on once
 - Creates _transitive trust_ relationships    
 - Federation: connecting authentication mechanisms from different environments (OSes,networks,etc.)
   - _Federated identity management system_
        - can be implemented with a _federated database_, which provides central authentication
        - can be implemented with SAML (Security Assertion Markup Language)
            - an XML-based data format used form SSO on web browsers
            - defines three roles
              - **Principal**: Typically the user
              - **Identity Provider**: creates, maintains, and manages identity information for principals
              - **Service Provider**: an entity that provides services to principals. redirects principals to obtain identities.

**Same Sign-On:** Users can access multiple systems using the same credentials, but they have to enter their credentials again each time they access a new resource. 

###### Authenticating RAS Clients
 - provide access to a network from an outside source

RAS client| comments
---|---
PAP | sends passwrds in cleartext, so is susceptible to sniffing. uses PPP
CHAP | Server challenges client for authentication information. uses PPP.
MS-CHAP | 
RADIUS | provides a centralized method of authentication for multiple remote access servers. Encrypts password packets **using symmetric encryption**. An AAA protocol
Diameter | an improvement over RADIUS. Supports Extensible Authentication Protocol (EAP).
XTACACS | proprietary Cisco. Improvement over TACACS.
TACACS | alternative to RADIUS. Proprietary Cisco. Can interact with Kerberos. encrypts the entire process


##### Something you have
###### Smart Cards
 - credit card-sized cards that have an embedded microchip and a certificate
 - contains an embedded certificate, which holds a user's private key
 - Common Access Card (CAC): issued by the DoD
 - Personal Identity Verification (PIV): issued by US federal agencies

###### Tokens/Key Fobs
 - electronic device about the size of a remote key for a car
 - contain an LCD which displays a number that changes periodically
 - RSA Secure ID: a popular token product
 - USB tokens include a USB connector and a smart chip, which stores a certificate

###### HOTP (HMAC-based One-Time Password)
 - algorithm combines a secret key and an incrementing counter, then creates a hash of the results
 - 6 to 8 digits
 - user requests a new HOTP number using a token/key fob or software app. 
 - if a HOTP number is given but not used, it's usable forever
 - open-source

###### TOTP (Time-based One-Time Password)
 open source protocol used to create passwords that expire after 30 seconds.
 
##### Something you are
###### Biometrics
Errors: 
  - **False acceptance:** incorrectly identifies an _unauthorized_ user as an _authorized_ user. **FAR** (False Acceptance Rate/Type 2 error)
  - **False rejection:** **FRR/type 1 error**

---
# Integrity
### Hashing 
Algorithm | Type | Comments
---|---|---
MD5 | Hash + Integrity | 128-bit hashes
SHA-1 | Hash + Integrity | 160-bit hashes
SHA-2 | Hash + Integrity | 224,256,384, and 512-bit 
SHA-3 | Hash + Integrity | like SHA2 but uses a different method
HMAC | Integrity/Authenticity | 'extends' MD5 or SHA1. used with IPsec. uses a 'shared secret'
---|---|---
RIPEMD | Hash + Integrity | 128, 160, 256, and 320
LANMAN | Hash + Integrity | very old and bad Microsoft
NTLM | Hash + Integrity | improved microsoft

---
# Availability
#### Redundancy
###### Site Redundancy
 - Hot site (ready and available 24/7)
 - cold site (a location where personnel, equipment, and data can be moved to when needed)
 - warm site (somewhere between hot & cold)

#### Fault Tolerance
