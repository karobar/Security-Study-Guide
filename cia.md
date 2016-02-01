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

# Confidentiality
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
||**something you know** (password,PIN) least secure||
||**something you have** (smart card,key fob/token, HOTP and TOTP)
||**something you are** (biometrics, fingerprint, retina) most secure
||**somewhere you are** (geolocation)
||**something you do** (touch screen gestures, behavioral biometrics, keystroke dynamics)
||Kerberos

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
 - **non-repudiation**
 - also provide integrity

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
    - **Example**: A user _Homer_ in the _Users_ container within the _example.com_ domain is identified with the following LDAP string: 
      ```LDAP://CN=Homer,CN=Users,DC=example,DC=com```
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

# Integrity
#### Hashing
###### SHA-1 (Secure Hash Algorithm 1)
#### Digital Signatures
Require the use of certificates and a PKI

# Availability
#### Redundancy
###### Site Redundancy
 - Hot site (ready and available 24/7)
 - cold site (a location where personnel, equipment, and data can be moved to when needed)
 - warm site (somewhere between hot & cold)

#### Fault Tolerance