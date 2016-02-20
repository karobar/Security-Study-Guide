# Interoperability Agreemements
Agreement Type | Definition | Parties | Example|  Comments
---|---|---|---|---
ISA | specified technical and security requirements for planning, establising, maintaining, and disconnecting a secure connection | 2+ entities |Ex: stipulation of certain types of encryption for all data in transit |  strict guidelines
SLA| stipulates performance expectations | a company and a vendor |Ex: minimum uptime and maximum downtime levels | Organizations use SLAs when contracting services from service providers (like ISPs). Many SLAs include a monetary penalty if the vendor is unable to meet the agreed-upon expectations
BPA | A written agreement that details a relationship | business partners | | includes obligations, shares of profits or losses each partner will take, their responsibilities to each other, and what to do if a partner chooses to leave the partnership. can help settle conflicts
MOU | expresses an understanding indicating intention to work together towards a common goal | 2+ parties | | similar to an SLA in that it defies the responsibilities of each of the parties.  Less formal than an SLA or ISA. Doesn't include monetary penalties.

# Forensics
#### Order of volatility
collect evidence starting with _least permanent_ to _most permanent_
 1. Cache memory, including the processor cache and hard drive cache
 2. RAM
 3. **swap file (extension of ram stored on the hdd, rebuilt when the system is booted)** or paging file
 4. data on local disk drives
 5. logs stored on remote systems
 6. archive media

###### Capture a System Image
###### Create a Hash of a captured forensic image
