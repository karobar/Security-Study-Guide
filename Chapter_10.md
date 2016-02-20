#### Certificates
 - digital document that specifies the following information on the owner:
    - serial number so the CA can validate
    - CA issuer
    - epiration date
    - owner
    - public key
 - used for encryption, authentication, and digital signatures

###### OCPS 
 - validates trust with certificates
 - only returns short responses such as good, unknown, or revoked

---
###### HTTPS
 - uses SSL or TLS
 - transmits a _symmetrical_ session key first with _asymmetrical_ encryption, then the rest of the session takes place with _symmetric_ encryption.

---
###### Key stretching
   - use salts among other methods to strengthen passwords
   - Examples: bcrypt and PBKDF2

---
###### PKI
requires a trust model between CAs

---
###### CSR
 1. Generate the RSA-based key pair
 2. include the public key in the CSR
 3. The CA will embed the public key in the certificate

---
###### Key escrow
placing a copy of a private key somewhere safe (give it to a trusted third party, copy and give to several key employees, etc.)

