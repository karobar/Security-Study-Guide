# Hardening
###### Disable unnecessary services
###### eliminate unneeded Applications
###### disabling unnecessary accounts
###### disable admin tools where not necessary

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
 - **Acceptable Use Policy (AUP):**
