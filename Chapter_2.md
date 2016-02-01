# Access control models
there are _objects_, such as files, folders, shares, and printers, and _subjects_, which are typically users/groups which access objects
### Discretionary Access Control (DAC)
 - specifies that every object has an owner
 - assigns permissions based on object ownership
 - might identify owners in a list
 - Microsoft-specific
     - identifies users with Security Identifiers (SIDs), which are long strings of characters
     - Every _object_ includes a discretionary access control list (DACL) 
         - identifes who can access the object
         - This is a list of Access Control Entries (ACEs)
           - a SID and the permissions granted to the SID 

### Mandatory Access Control (MAC)
 - uses sensitivity labels and classification levels
 - effective at restricting access on a need-to-know basis
 - strongest access control method available
 - admins assign labels to _subjects_ and _objects_; when these match, the subject is granted access
 - Example: Top Secret, Secret, Confidential

### Network Access Control (NAC)
 - dictate a baseline on a _health-check_ server
 - any system attempting to log on has to meet the baseline (programs, versions, etc.)
 - can also involve a _remediation_ server to work through issues on the connecting system

### Role-based access control (role-BAC/RBAC)
uses group-based privileges

An example is Microsoft Project Server, which uses the following role-BAC matrix:
Role | Server privileges | Project Privileges
---|---|---
Administrators|All|All
Executives|None|All
Project Managers|None|All on assigned projects, none on unassigned projects
Team Members|None|Access for assigned tasks, limited views within scope of their assigned tasks, no views outside the scope of their assigned tasks

### Rule-base access control (rule-BAC/RBAC)
##### ACLs - Access Control Lists
Generally take the following format:  
Permission | Protocol | Source | Destination | Port
--- | --- | --- | --- | ---
DENY or ALLOW| TCP/UDP/IP, occasionally ICMP |  IP addr (or range,subnet,ANY) | IP addr (or range,subnet,ANY)|  #
  
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

---
# Security Controls
impementation and enforcement

## Implementation Methods
like Goals, one way of classifying security controls
Technical | Management/Administrative | Operational
---|---|---
|technology|management methods|implemented by people|
Encryption | Risk assessments (quantitative/qualitative) | Procedures
Passwords | Policies | Standards
|smart cards|Privacy Policy| Configuration & Change Management
|least privilege|Acceptable Use Policy: _using resources_| Awareness & Training
|antivirus|Security Policy: _password length, etc_|Contingency Planning
|IDSs|Mandatory Vacations|Media Protection
|firewalls|Job Rotation|Physical and environmental protection (cameras, door locks, heating, ventilaiton)
|fire suppression systems|Separation of duties|
|motion detectors|Least Privilege: _ensures users are granted only the access they need to perform their jobs, and no more_|
||vulnerability assessments|
||penetration tests

## Goals
Deterrent | Preventative | Detective | Compensating | Corrective
---|---|---|---|---
|cable locks|Cable locks|Log monitoring|original control is too expensive|Active IDS
|hardware locks|Hardening: making a system or application more secure than its default configuration|Trend analysis||Backups and system recovery
||Security awareness and training|security audit||
||guards (as in dudes)|Video surveillance
||Change Management|motion detection
||Account Disablement

## Physical Security Controls
 - Perimeter: fence, guards, gates, barricades
 - Building: guards, locked doors, lighting, video cameras 
 - secure work areas: escorts, restricted access
 - server and network rooms: designated server/wiring rooms
 - hardware: locked cabinets, cable locks, safes

###### Mantrap
 - controlling access to a secure area through a _buffer zone_
 - allows only one person through
 - turnstile

###### Bollards
 - short, vertical posts composed of reinforced concrete and/or steel
 - usually placed in front of entrances

# Logical Access Controls
implemented through technologies such as Group Policy and account management tools.