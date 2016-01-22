# Questions & Answers
 1. A security admin is implementing a security program that addresses confidentiality and availability. What else should the administrator include? _Ensure systems are not susceptible to unauthorized changes_
 2. You need to transmit PII (Personally Identifiable Information) by email confidentially. _Encrypt it before sending_
 3. Lisa manages networks and mantians copies of the conf files for all routers and switches. She regularly creates hashes for these files and compares them with the previous week. Which security goal is she pursuing? _Integrity_
 4. An organization wants to provide protection against malware. Admins have installed antivirus software on all computers. They also implemented a firewall and IDS (Intrusion Detection System) on the network. What identifies this principle? _Layered security_
 5. Someone forgot their password. What should help desk do? _**Verify the identity of the user, then create a temporary password that expires after first use.  This forces the user to create a new password.**_
 6. Which type of authentication does a hardware token provide? _**something you have**_
 7. Which type of authenication is a retina scan? _Biometric_
 8. Users are required to log on to their computers with a smart card and a PIN. What describes this? _Multifactor authentication_
 9. Organization wants remote access solution with support for different **vendors**. What's the best choice? _**RADIUS is an AAA (authentication, authorization and accounting) protocol and is the best choice**_
 10. Organization implements storing user credentials in a central database. Users log on once with credentials, then can access other systems without logging on again. What does this describe? _Single sign-on (SSO)_
 11. Organization issues a variety of mobile devices, but wants to reduce potential data losses if the devices are lost/stolen. How to achieve this goal? _**Disk Encryption is a strong technical control that can mitigate potential data losses if mobile devices are lost or stolen**_
 12. Your job is monitoring security logs, analyzing trend reports, and installing CCTVs. What best identifies your responsibilities? _**Detecting security incidents**_
 13. A security professional has reported an increase in the number of **tailgating** violations into a secure data center. What can prevent this? _**A mantrap is highly effective at preventing unauthorized entry and can prevent tailgating**_
 14. You are redesigning password policy. You want to ensure that users change their passwords regularly, but they are unable to reuse password. What settings should you configure? _Maximum password age, Password History, **and Minimum Password Age, which prevents users from changing their password repeatedly to get back to their original password**_
 15. A security auditor recently completed an in-depth audit on your network.  She found the following passwords used on the network: Pa$$, 1@W2k, and G7bT3. What should be changed to avoid the problem shown with these passwords? _Password Length_
 16. An audit discovered several apparently dormant user accounts. Although users could log on to the accounts, no one had logged on to them for more than 60 days. You later discovered that these accounts are for contractors who work approx. one week every quarter. What's the best response? _~~Reset~~ **Disable the accounts, and then enable them when needed by the contractors.  Ideally, the accounts would include an expiration date so that they would automatically expire when no longer needed. Because the contractors need to access the accounts periodically, It's better to disable them rather than deleting them. Resetting implies that you are changing the password.**_
 17. Organization routinely hires contractors to assist with different projects.  Admins are rarely notified when a project ends and contractors leave. What can ensure that contractors cannot log on with their account after they leave? _Enable ~~an account enablement policy~~ **account expiration, so that the accounts are automatically diabled at the end of their contract. 'Account enablement' is nonsense. Account recovery allows recovery of accounts and security keys from ex-employees. Don't use generic accounts.**_
 18. Developers are planning to develop an application using role-based access control. What would they most likely include in their planning? _~~A listing of owners~~**A matrix of functions, roles, or job titles matched with the required access privileges for each of the titles**_
 19. An organization has implemented an access control model that enforces permissions based on data labels assigned at different levels. What type of model is this? _**MAC (mandatory access control)**_
 20. Your organization's policy requires that PII at rest and PII in transit be encrypted. What would the organization use to achieve these objectives? _SSH, ~~SMTP~~**PGP(Pretty Good Privacy)/GPG(GNU Privacy Guard)**_
 21. Give examples of protocols that use TCP port 22 by default. _SSH,SCP,SFTP_
 22. Which port should you block to block access to all external web sites? _TCP 80_
 23. Which ports whould you open on the firewall between your system and a remote system to be able to manage the remote server? _You can manage a remote server using SSH on TCP port 22 **and RDP(Remote Desktop Protocol) on TCP port 3389**_
 24. While reviewing logs on a firewall you see several requests for the AAAA record of gcgapremium.com. What is the purpose of this request? _**An AAAA record identifies the IPv6 address of a given name**_
 25. Your organization has several switches used within the network. You need to implement a control to secure the switch from physical access. What do? _Disable unused ports_
 26. You are configuring a switch and need to ensure that only authorized devices can connect to it and access the network through this switch. What do? _**Implement 802.1x**_
 27. You need to configure a UTM (Unified Thread Management) security appliance to restrict access to peer-to-peer file sharing web sites. What should you configure? _~~Content inspection~~**Configure the URL filter, which would block access to peer-to-peer sites**_
 28. You have implement a network design that allows internal computers to share one public IP address. What did you implement? _~~DNAT~~**PAT(Port Address Translation) is a form of NAT that allows many internal devices to share one pubic IP addr.**_
 29. What would you configure on a Layer 3 device to allow FTP traffic to pass through? _Access Control List_
 30. What type of device would have the following entires used to define its operation:
     
    permit IP any any eq 80
    permit IP any any eq 443
    deny IP any any    
 _~~Web Server~~**firewall. A web server wouldn't use an ACL.**_
 31. You are preparing to deploy an anomaly-based detection system to monitor network activity. What would you create first? _Baseline_
 32. A company wants to gather intelligence about current methods attackers are using against its clients. What can it use? _**Honeynet**_
 33. You oversee and monitor processes at a water treatment plant using SCADA systems.  Admins recently discovered malware on your system that was connecting to the SCADA systems. Although they removed the malware, managment is still concerned.  You need to continue using your system and it's not possible to update the SCADA systems. What do? _**A network intrusion prevention system (NIPS) installed on the Supervisory Control and Data Acquisition (SCADA) network can intercept malicious traffic coming into the network**_
 34. Your organization mantains a separate wireless network for visitors in a conference room. However, you have recently noticed that people are connecting to this network even when there aren't any visitors in the conference room. You want to prevent these connections, while maintaining easy access for visitors in the conference room. What do? _~~Disable SSID broadcasting~~**Reduce antenna power**_
 35. What represents the best action to increase security in a wireless network? _~~Disable SSID broadcast~~**Use CCMP encryption**_
 36. Your organization is hosting a wireless network with an 802.1x server using **PEAP**. On Thursday, users report they can no longer access the wireless network.  Administrators verified the network configuration matches the baseline, there aren't any hardware outages, and the wired network is operational. What's the most likely cause? _**The RADIUS server certificate expired**_
 37. You are planning a wireless network for a business.  A core requirement is to ensure that the solution encrypts user credentials when users enter their usernames and passwords.  What can meet this requirement? _**WPA2 over EAP-TTLS**_
 38. A small business owner modified her wireless router with the following settings: 
      - PERMIT 1A:2B:3C:4D:5E:6F
      - DENY 6F:5E:4D:3C:2B:1A  
After saving these settings, an employee reports that he cannot access the wireless network anymore.  Why? _Hardware/MAC address filtering_
 39. Homer recently implemented a wireless network in his home using WEP. He asks for advice. What do? _He should not use WEP because it is a weak encryption algorithm_
 40. What is an example of an attack against a mobile device? _**Bluejacking is the practice of sending unsolicited messages to other Bluetooth devices**_
 41. A network administrator needs to open a port on a firewall to support a VPN using PPTP. What port? _???_
 42. Attackers recently attacked a web server hosted by your organization.  Management has tasked admins with reducing the attack surface of this server to prevent future attacks.  What do? _Disabling unnecessary services_
 43. Network admins identified what appears to be malicious traffic from an internal computer, but only when nobody is logged onto the computer.  You suspect the system is infected with malware.  It periodically runs an application that attempts to connect to web sites over port 80 with Telnet.  After comparing the computer with a list of services from the standard image, you verify this application is very likely the problem. What process allowed you to make this determination? _Baselining_
 44. An updated security policy defines what applications users can install and run on company-issued mobile devices.  Which control enforces this policy? _Whitelisting_
 45. You want to test new security controls before deploying them. What provides flexibility to meet this goal? _Virtualiation technologies_
 46. An organization recently suffered an outage after a technician installed an application update on a vital server during peak hours.  The server remained down until administrators were able to install a previous version of the application on the server.  How to prevent this in the future? _Create a patch management policy_
 47. You are evaluating a critical industrial control system. You want to ensure the system has security controls to support availability.  Which meets your needs? _Implementing control redundancy and diversity_
 48. Of the following choices, what are valid security controls for mobile devices? _screen Locks, device encryption, and remote wipe_
 49. A new mobile device security policy has authorized the use of employee-owned devices, but mandates additional security controls to protect them if devices are lost or stolen.  What do? _Screen Locks and device encryption_
 50. You want to deter an attacker from using brute force to gain access to a mobile device. What do? _Account lockout settings_
 51. Management is considering allowing users to connect to the corporate network with their own devices. What represents a security concern? _Inability to ensure devices are up to date with current system patches_
 52. Your organization is planning to issue mobile devices to some employees, but they are concerned about protecting the confidentiality of data if the devices are lost or stolen.  Which is the best way to secure data at rest on a mobile device? _Full device encryption_
 53. Your organization recently purchased several new laptops for employees.  You're asked to encrypt the laptop's hard drives without purchasing additional hardware. What do you use? _???_
 54. Management within your organization wants to limit documents copied to USB flash drives.  What can be used to meet this goal? _???_
 55. You installed code designed to enable your account automatically, three days after anyone disables it.  What does this describe? _Logic bomb_
 56. Lisa recently completed an application used by the Personnel dept. to store PII and other employee info.  She programmed in the ability to access this application with credentials that only she knows, so that she can perform remote maintenance on the application if necessary. What does this describe? _backdoor_
 57. A recent change in an organization's security policy states that monitors need to be positioned so that they cannot be viewed from outside any windows. Why? _reduce success of shoulder surfing_
 58. You are troubleshooting an intermittent connectivity issue with a web server. After examining the logs, you identify repeated connection attempts from various IP addresses.  You realize these connection attempts are overloading the server, preventing it from responding to other connections.  What's happening? _DDoS attack_
 59. Your organization includes the following statement in the security policy: 
 >"Security controls need to protect against both online and offline password brute force attacks."       

What is least helpful to meet these goals? _Password complexity_
 60. A code review of a web application discovered that the application is not performing boundary checking.  What should the web developer add to theis application to resolve this issue? _???_
 61. A web developer is using methods to validate user input in a web site application.  WHich attack isn't prevented by validating user input? _???_  62. Checking the logs of a web server, you see the following entry:
     
         198.252.69.169--[1/Sep/2013:05:20]"GET/index.php?username=ZZZZZZZZZZZZZZZZZZZZZZZBBBBBBBBCCCCCCCHTTP/1.1" "http://gcgapremiu.com/security/" "Chrome31"
What's going on here? _a buffer overflow attack_
 63. Looking a logs for an online web app, you see that someone has entered the following prhase into several queries:
     ' or '1'='1' -- 
    What's going on here _An XSS attack_
 64. A security tester is using **fuzzing** techniques to test an app. What does fuzzing use to test the app? _???_
 65. An organization has purchased fire insurance to manage the risk of a potential fire. What method are they using? _Risk acceptance_
 66. You are asked to identify the number of times a specific type of incident occurs per year. What is another name for this? _???_
 67. Lisa needs to calculate the total ALE for a group of servers used in the network.  During the past two years, five of the servers failed.  The hardware cost to replace each server $3,500, and the downtime has resulted in $2,500 of additional losses. What's the ALE? _???_
 68. Security experts at your organization have determined that your network has been repeatedly attacked from multiple entities in a foreign country.  Research indicates these are coordinated and sophisticated attacks.  What's going on? _advanced persistent threat_
 69. You're performing a vulnerability assessment. Whats your goal? _Determine if vulnerabilities can be exploited_
 70. You need to ensure that several systems have all appropriate security controls and patches. However, you are not to attack or compromise any of these systems. What do? _Vulnerability scan_
 71. What is a particularly invasive type of testing? _penetration test_
 72. A security professional is testing the functionality of an application, but doesn't have any knowledge about the internal code of an application. What type of test is this? _black box_
 73. Testers are analyzing a web app your organizaiton is planning to deploy.  They have full access to product documentation, including the code and data structures used by the application. What kind of test should they perform? _white box_
 74. A network admin is attempting to identify all traffic on an internal network. What tool is a good choice? _protocol analyzer_
 75. Your organization security policy requires that personnel notify security administrators if an incident occurs.  However, this is not occuring consistently.  Which of the following could the organization implement to ensure security admins are notified in a timely manner? _Incident response team_
 76. A security admin is reviewing an organization's security policy and notices that the policy doesn't define a time frame for reviewing user rights and permissions.  What is the minimum time frame she should recommend? _at least once a year_
 77. Security personnel recently performed a security audit.  They identified several employees who had permissions for previously held jobs within the company.  What should the organization do to prevent this in the future? _account management controls_
 78. You are a technician at a small organization.  You need to add fault-tolerance capabilities within the business to increase the availability of data.  However, you need to keep costs low. What meets your need? _???_
 79. An organization needs to identify a continuity of operations plan that will allow it to provide temporary IT supprot during a disaster.  The organization doesn't want a dedicated site.  What do? _**cold site**_
 80. Monty Burns is the CEO of a nuclear power plant. What should the company have in case something happens to him? _sucession planning_
 81. A continuity of operations plan for an organization includes the use of a **warm site**.  The **BCP** coordinator wants to verify that the organization's backup data center is prepared to implement the warm site if necessary. What do? _perform a disaster recovery exercise_
 82. Users are complaining of intermittent connectivity issues.  You investigate and discover that new network cables for these user systems run over fluorescent lights. What do? _**EMI shielding**_
 83. A software company occasionally provides application updates and patches via its web site.  It also provides a checksum for each update and patch.  Which of the following describes the purpose of the checksum? _Integrity of the application_
 84. A function converts data into a string of characters which cannot be reversed to re-create the original data. What type of encryption is this? _asymmetric encryption_
 85. Which of the following is a symmetric encryption algorithm that encrypts data one bit at a time? _stream cipher_
 86. A supply company has several legacy systems connected together within a warehouse.  An external security audit discovered the company is using **DES** and mandated the company upgrade DES to meet minimum security requirements.  The company plans to replace the legacy systems next year, but needs to meet the requirements from the audit.  What's likely the most simple upgrade for these systems? _**3DES**_
 87. Network admins in your organization need to administrator firewalls, security appliances, and other network devices.  These devices are protected with strong passwords, and the passwords are stored in a file. How to protect this password list? _file encryption_
 88. An employee at your organization is suspected of leaking data to a competitor. Investigations indicate he sent several email messages containing pictures of his dog.  Investigators have not been able to identify any other suspicious activity.  What's going on? _He's leaking data using steganography_
 89. You are planning to encrypt data in transit with **IPsec**. What is likely to be used with IPsec? _???_
 90. Bart wants to send a secure email to Lisa, so he decides to encrypt it.  He wants to ensure that only Lisa can decrypt it. What does Lisa need to meet this requirement? _Lisa's private key_
 91. An organization requested bids for a contract and asked companies to submit their bids via email.  After winning the bid, Acme realized it couldn't meet the requirements of the contract.  Acme instead stated that it never submitted the bid.  What would prove to the organization that Acme did submit the bid? _Digital signature_
 92. Application developers are creating an application that requires users to log on with strong passwords.  The developers want to store the passwords in such a way that it will thwart brute force attacks. What do? _???_
 93. A web site is using a certificate.  Users have recently been receiving errors from the web sit indidcating that the site's certificate is revoked.  Which includes a list of certificates that have been revoked? _???_
 94. Give an example of a managment control. _change management_
 95. security personnel recently identified potential fraud committed by a network admin. Investigators discovered this admin performs several job functions within the organization, including database administration and app development. How to reduce risk associated with this activity? _???_
 96. Security experts want to reduce risks associated with updating critical operating systems.  What meets this goal? _change management_
 97. Your company is considering implementing **SSO** capabilities to company applications and linking them to a social media site.  When implemented, users can log onto Facebook and then access company applications without logging on again. What is a potential risk related to this plan? _a data breach exposing passwords on the social media site will affect the company application_
 98. You work as a help-desk professional in a large organization.  You have begun to receive an extraordinary number of calls from employees related to malware. What should be your first response. _mitigation_
 99. A technician confiscated an employee's computer after management learned the employee had unauthorized material on his system. Later, a security expert captured a forensic image of the system disk. However, the security expert reported the computer was left unattended for several hours before he captured the image. What's a potential issue if this incident goes to court? _chain of custody_
 100. Social engineers have launched several successful phone-based attacks against your organization resulting in several data leaks.  What would be effective at reducing the success of these attacks? _???_
 