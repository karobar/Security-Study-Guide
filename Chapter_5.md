# Hardening
 - Disable unnecessary services
 - eliminate unneeded Applications
 - disabling unnecessary accounts
 - disable admin tools where not necessary

---
# Baselines
#### Security baselines
   - used to ensure systems start in a secure state
   - Microsoft domains use Group Policy to standardize the configuration of systems. An admin can create and apply a **GPO (Group Policy Object)**, which contain specific security settings such as password policies, system services, software restrictions

#### Configuration baselines 
###### Examples
   - The United States Government Configuration Baseline (USGCB), which include settings that are compliant with Security Content Automation Protocol (SCAP)
   - printer configuration
   - application settings 
   - TCP/IP settings

#### Application Configuration Baselines
similar to system configuration baselines, but only refer to a specific application, such as Microsoft SQL Server
#### Host software baselines 
are used to document software installed on host systems
#### Application configuration baselines 
used to document appropriate application settings
#### Performance baselines
used to identify when system performance is degrading
#### Image _(in the context of a baseline)_
a snapshot of a single system that admins deploy to multiple other systems

---
# VMs
easy to steal.
###### Sandbox
you can create a VM in a sandbox, which prevents the VM from interacting with anything else, be them VMs, the host, or other devices on the network
###### File types
 - **VHD (Virtual Hard Disk):** contain the contents of a C drive, for example.
 - **XML:** storing configuration details 
 - **AVHD (Automatic VHDs) aka 'Differencing Disks':** Hold the differences between the current disk and the configuration at that time
 - **VSV:** Hold the saved state for devices associated with the VM
 - **BIN:** hold the memory for VMs that are in a saved state

---
# Static Computing Environments
 - SCADA systems
 - Embedded systems
 - mobile systems
 - mainframes
 - game consoles
 - vehicle computing systems

## Protecting Static Systems

 - **Redundancy and diversity controls:** ensures a system continues to operate even after suffering a failure
 - **Network segmentation**
 - **Layered Security**
 - **Application firewalls**
 - **Manual Updates**
 - **Firmware Version Control**
 - **Wrappers:** Some *nix systems use TCP wrappers to filter traffic coming in and out of a system

#### Mobile Device Concerns
 - **Inventory Control:** Radio-Frequency IDentification (RFID) methods to track the movement of company-provided mobile devices
 - **Removable Storage:**
 - **Storage segmentation:** for example, users might be required to use external storage for any corporate data
 - **Screen locks:**
 - **Lockout**
 - **Remote Wiping**
 - **Disabling unused features**

##### BYOD Concerns
 - **Acceptable Use Policy (AUP)**
 - **Adherance to corporate policies**
 - **Privacy**
 - **User Acceptance**
 - **Data Ownership**
 - **Support Owernership:** Limiting the types of devices supported by an organization
 - **Architecture/infrastructure considerations:** Restrict all devices to a segmented network
 - **Forensics**
 - **Legal concerns**
 - **On-boarding/off-boarding**
 - **Onboard camera/video**

##### Mobile Device Management (MDM)
 - Example: Microsoft ConfigMgr 2012 R2
 - Patch management
 - Antivirus management
 - Application control

---
# Data Leakage 
### DLP (Data Loss/Leak Prevention)
 - Examines and inspects data, looking for unauthorized transmissions
 - Network-based (data-in-motion)
 - Storage-based (data-at-rest)
 - Endpoint-based (data-in-use)

---
# SANs (Storage Area Network) and Virtual SANs
 generally more efficient than a typical file server

###### FC (Fibre Channel)
 - instead of a TCP/IP network
 - very fast, but expensive
 - cheaper alternative without cabling = FCoE (FC over Ethernet)

###### iSCSI (Internet Small Computer System Interface)
 - transfers traditional SCSI commands over IP 
 - can be implemented within LANs


# Cloud Computing
### SaaS (Software as a Service)
 - any application provided to users over a network with a web browser
 - examples: gmail, google docs
 - **MaaS (Management as a Service):** Management is outsourced. For example a third party can review logs and provide reports

### PaaS (Platform as a Service)
 - Provides customers with a preconfigured computing platform/OS and applications

### IaaS (Infrastructure as a Service)
 - outsourcing hardware, support

### Hybrid Cloud
a combination of two or more clouds
### Community cloud
shared by two or more organizations
### Risks




