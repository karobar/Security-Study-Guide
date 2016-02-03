
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
###### Response Process
1. Incident Preparation
2. <INCIDENT!>
3. Incident Identification
4. Escalation and Notification
5. Incident Mitigation 