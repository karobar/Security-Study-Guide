# Questions & Answers
 1. A security admin is implementing a security program that addresses **confidentiality** and **availability**. What else should the administrator include? _Ensure systems are not susceptible to unauthorized changes_
 2. You need to transmit **PII (Personally Identifiable Information)** by email confidentially. _Encrypt it before sending_
 3. Lisa manages networks and mantians copies of the conf files for all routers and switches. She regularly creates hashes for these files and compares them with the previous week. Which security goal is she pursuing? _Integrity_
 4. An organization wants to provide protection against malware. Admins have installed antivirus software on all computers. They also implemented a firewall and **IDS (Intrusion Detection System)** on the network. What identifies this principle? _Layered security_
 5. Someone forgot their password. What should help desk do? _Verify the user's account exists_
 6. Which type of authentication does a hardware token provide? _???_
 7. Which type of authenication is a retina scan? _Biometric_
 8. Users are required to log on to their computers with a smart card and a PIN. What describes this? _Multifactor authentication_
 9. Organization wants remote access solution with support for different **vendors**. What's the best choice? _???_
 10. Organization implements storing user credentials in a central database. Users log on once with credentials, then can access other systems without logging on again. What does this describe? _Single sign-on_
 11. Organization issues a variety of mobile devices, but wants to reduce potential data losses if the devices are lost/stolen. How to achieve this goal? _Risk assessment_
 12. Your job is monitoring security logs, analyzing trend reports, and installing CCTVs. What best identifies your responsibilities? _Implementing monitoring controls_
 13. A security professional has reported an increase in the number of **tailgating** violations into a secure data center. What can prevent this? _???_
 14. You are redesigning password policy. You want to ensure that users change their passwords regularly, but they are unable to reuse password. What settings should you configure? _Maximum password age, Password History, Password Complexity_
 15. A security auditor recently completed an in-depth audit on your network.  She found the following passwords used on the network: Pa$$, 1@W2, and G7bT3. What should be changed to avoid the problem shown with these passwords? _Password Length_
 16. An audit discovered several apparently dormant user accounts. Although users could log on to the accounts, no one had logged on to them for more than 60 days. You later discovered that these accounts are for contractors who work approx. one week every quarter. What's the best response? _Reset the Accounts_
 17. Organization routinely hires contractors to assist with different projects.  Admins are rarely notified when a project ends and contractors leave. What can ensure that contractors cannot log on with their account after they leave? _Enable an account enablement policy_
 18. Developers are planning to develop an application using role-based access control. What would they most likely include in their planning? _A listing of owners_
 19. An organization has implemented an access control model that enforces permissions based on data labels assigned at different levels. What type of model is this? _???_
 20. Your organization's policy requires that PII at rest and PII in transit be encrypted. What would the organization use to achieve these objectives? _SSH, SMTP_
 21. Give examples of protocols that use TCP port 22 by default. _SSH,SCP,SFTP_
 22. Which port should you block to block access to all external web sites? _TCP 80_
 23. Which ports whould you open on the firewall between your system and a remote system to be able to manage the remote server? _???_
 24. While reviewing logs on a firewall you see several requests for the **AAAA** record of gcgapremium.com. What is the purpose of this request? _???_
 25. Your organization has several switches used within the network. You need to implement a control to secure the switch from physical access. What do? _Disable unused ports_
 26. You are configuring a switch and need to ensure that only authorized devices can connect to it and access the network through this switch. What do? _**Implement 802.1x**_
 27. You need to configure a **UTM** security appliance to restrict access to peer-to-peer file sharing web sites. What should you configure? _Content inspection_
 28. You have implement a network design that allows internal computers to share one public IP address. What did you implement? _**DNAT**_
 29. What would you configure on a Layer 3 device to allow FTP traffic to pass through? _Access Control List_
 30. What type of device would have the following entires used to define its operation:
     - permit IP any any eq 80
     - permit IP any any eq 443
     - deny IP any any    
 _Web Server_
 31. You are preparing to deploy an anomaly-based detectiion system to monitor network activity. What would you create first? _Baseline_
 32. A company wants to gather intelligence about current methods attackers are using against its clients. What can it use? _**Honeynet**_
 33. You oversee and monitor processes at a water treatment plant using **SCADA** systems.  Admins recently discovered malware on your system that was connecting to the SCADA systems. Although they removed the malware, managment is still concerned.  You need to continue using your system and it's not possible to update the SCADA systems. What do? _???_
 34. Your organization mantains a separate wireless network for visitors in a conference room.  However, you have recently noticed that people are connecting to this network even when there aren't any visitors in the conference room. You want to prevent these connections, while maintaining easy access for visitors in the conference room. What do? _Disable SSID broadcasting_
 35. What represents the best action to increase security in a wireless network? _Disable SSID broadcast & ???_
 36. Your organization is hosting a wireless network with an 802.1x server using **PEAP**. On Thursday, users report they can no longer access the wireless network.  Administrators verified the network configuration matches the baseline, there aren't any hardware outages, and the wired network is operational. What's the cause? _???_
 37. You are planning a wireless network for a business.  A core requirement is to ensure that the solution encrypts user credentials when users enter their usernames and passwords.  What can meet this requirement? _???_
 38. A small business owner modified her wireless router with the following settings: 
      - PERMIT 1A:2B:3C:4D:5E:6F
      - DENY 6F:5E:4D:3C:2B:1A  
After saving these settings, an employee reports that he cannot access the wireless network anymore.  Why? _Hardware address filtering_
 39. Homer recently implemented a wireless network in his home using WEP. He asks for advice. What do? _He should not use WEP because it is a weak encryption algorithm_
 40. What is an attack against a mobile device? _???_
 41. A network administrator needs to open a port on a firewall to support a VPN using **PPTP**. What port? _???_
 42. Attackers recently attacked a web server hosted by your organization.  Management has tasked admins with reducing the attack surface of this server to prevent future attacks.  What do? _Disabling unnecessary services_
 43. Network admins identified what appears to be malicious traffic from an internal computer, but only when nobody is logged onto the computer.  You suspect the system is infected with malware.  It periodically runs an application that attempts to connect to web sites over port 80 with Telnet.  After comparing the computer with a list of services from the standard image, you verify this application is very likely the problem. What process allowed you to make this determination? _Baselining_
 44. An updated security policy defines what applications users can install and run on company-issued mobile devices.  Which control enforces this policy? _Whitelisting_
 45. You want to test new security controls before deploying them. What provides flexibility to meet this goal? _Virtualiation technologies_
 46. An organization recently suffered an outage after a technician installed an application update on a vital server during peak hours.  The server remained down until administrators were able to install a previous version of the application on the server.  How to prevent this in the future? _Create a patch management policy_
 47. You are evaluating a critical industrial control system. You want to ensure the system has security controls to support availability.  Which meets your needs? _Implementing control redundancy and diversity_
 48. Of the following choices, what are valid security controls for mobile devices? _screen Locks, device encryption, and remote wipe_
 49. A new mobile device security policy has authorized the use of employee-owned devices, but mandates additional security controls to protect them if devi
