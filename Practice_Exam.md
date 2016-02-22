1. Lisa hid several plaintext documents within an image file. Which security goal is she pursuing? _Confidentiality_
2. You're the security admin in your organization. You want to ensure that a file maintains integrity. Which of the following choices is the best choice to meet your goal? _Hash_
3. An e-commerce web site doesn't currently have an account recovery process for customers who have forgotten their passwords. What are the best items to include if website designers add this process? _Create a web-based form that verifies customer identities using another method and set a temporary password that expires upon first use_
4. Your organization is planning to implement stronger authentication for remote access users. An updated security policy mandates the use of token-based authentication with a password that changes every 30 seconds. What's the best choice to meet this requirement? _TOTP_
5. Your organization issues laptops to mobile users. Admins configured these laptops with FDE, which requires users to enter a password when they first turn on the computer. After the OS loads, users are required to log on with a username and password. What best describes this? _Single-factor authentication_
6. Users at your organization currently use a combination of smart cards and passwords, but an updated security policy requires multifactor security using 3 different factors. What can you add to meet the new requirement? _Fingerprint readers_
7. A network includes a TGT server used for authentication. What authentication service does this network use? _Kerberos_
8. You're modifying a config file used to authenticate Unix accounts against an external server. The file includes phrases such as DC=Server1 and DC=Com. Which authentication service is the external server using? _LDAP_
9. What is an AAA protocol that uses shared secrets as a method of security? _RADIUS_
10. Your organization wants to reduce the amount of money it's losing due to thefts. What's the best example of an equipment theft deterrent? _cable locks_
11. A manager recently observed an unauthorized person in a secure area, which is protected with a cipher lock door access system. After investigation, he discovered that an authorized employee gave this person the cipher lock code. What's the best response to this issue at the minimum cost? _~~Place a guard at the entrance~~ **Securiy awareness training is often the best response to violations of security policies. If the individuals don't abide by the policies after training, management can take disciplinary action. Guards can prevent this issue by only allowing authorized personnel in based on facial recognition or identification badges. but at a much higher cost**_
12. Management recently rewrote the organization's security policy to strenghten passwords created by users. It now states that passwords should support special characters. What's the best setting to help the organization achieve this goal? _Complexity_
13. You've discovered that some users have been using the same passwords for months, even though the password policy requires users to change their password every 30 days. You want to ensure that users can't reuse the same password. Which settings should you configure? _~~Maximum password age~~ and minimum password age **The password history setting records previously used passwords to prevent users from reusing the same passwords. Using the password history setting combined with the minimum password age setting prevents users from changing their password repeatedly to get back to their original password. The maximum password age setting ensures users change their passwords regularly, but this is already set to 30 days in the scenario**_
14. A company recently hired you as a security admin. You notice that some former accounts used by temporary employees are currently enabled. What's the best response? _~~Set account expiration dates for all accounts when creating them~~ **Running a last logon script allows you to identify inactive accounts, such as accounts that haven't been logged on to in the last 30 days. Setting expiration dates for newly created accounts is a good step, but it doesn't address previously created accounts**_
15. An organization supports remote access, allowing user to work from home. However, management wants to ensure that personnel can't log on to work systems from home during weekends and holidays. What best supports this goal? _time-of-day restrictions_
16. You configure access control for users in your organization. Some departments have a high employee turnover, so you want to simplify account administration. What's the best choice? _Group-based privileges_
17. You're configuring a file server used to share files and folders among employees within your organization. However, employees shouldn't be able to access all folders on this server. What's the best method to manage security for these folders? _Use security groups with appropriate permissions_
18. The retirement castle uses groups for ease of administration and management. They recently hired Jasper as their new accountant. Jasper needs access to all the files and folders used by the accounting department. What should the admin do to give Jasper appropriate access? _Create an account for Jasper and add the account to the Accounting group_
19. Your organization recently updated its security policy and indicated that Telnet shouldn't be used within the network. What should be used instead of Telnet? _SSH_
20. One of  your web servers was recently attacked and you've been tasked with reviewing firewall logs to see if you can determine how an attacker accessed the system remotely. You identified the following port numbers in log entries: 21, 22, 25, 53, 80, 110, 443, and 3389. What protocol did the attacker most likely use? _RDP_
21. What provides the largest address space? _IPv6_
22. While analyzing a firewall log, you notice traffic going out of your network on UDP port 53. What does this indicate? _DNS traffic_
23. A team of users in your organization needs a dedicated subnet. For security reasons, other users shouldn't be able to connect to this subnet. What's the best solution? _~~Enable SNMP~~ **The best answer is to restrict traffic based on physical addresses. This is also known as MAC address filtering and is configured on a switch. SNMP monitors and manages network devices**_
24. An organization recently updated its security policy. A new requiement dictates a need to increase protection from rogue devices plugging into physical ports. What provides the best protection? _~~Disable unused ports~~ **IEEE 802.1x is a port-based authentication protocol and it requires systems to authentiate before they're granted access to the network. If an attacker plugged a rogue device into a physical port, the 802.1x server would block it from accessing the network. Disabling unused ports is a good practice, but it doesn't prevent an attacker from unplugging a system from a used port and plugging the rogue device into the port**_
25. What would admins typically place at the end of a firewall? _Implicit deny_
26. Your organization wants to protect its web server from cross-site scripting attacks. What provides the best protection? _~~IDS~~ **A WAF is an application-layer firewall designed specifically to protect web servers. An IDS can help prevent attacks, but it isn't as good as the WAV when protecting the web server**_
27. Management recently learned that several employees are using the company network to visit gambling and gaming web sites. They want to implement a security control to prevent this in the future. What would meet this need? _~~WAF~~ **A UTM device typically includes a URL filter and can block access to web sites, just as a proxy server can block access to web sites. A WAF protects a web server from incoming attacks**_
28. Which of the following protocols operates on Layer 7 of the OSI odel? _SCP_
29. What best describes a false negative? _An IDS doesn't detect a buffer overflow attack_
30. Company management suspects an employee is stealing critical project information and selling it to a competitor. They'd like to identify who is doing this, without compromising any live data. What's the best option to meet this goal? _Add fabricated project data on a honeypot_
31. Attackers frequently attacked your organization, and admins want to learn more about zero-day attacks on the network. What can they use? _Honeypot_
32. Security personnel recently noticed a successful exploit against an application used by many employees at their company. They notified the company that sold them the software and asked for a patch. However, they discovered that a patch wasn't available. What best describes this scenario? _Zero-day_
33. What type of encryption is used with WPA2 CCMP? _AES_
34. Admins in your organization are planning to implement a wireless network. Management has mandated that they use a RADIUS server and implement a secure wireless authentication method. What should they use? _~~WPA2-PSK~~ **Enterprise mode implements 802.1x as a RADIUS server and LEAP can secure the authentication channel. LEAP is a Cisco proprietary protocol, but other EAP variations can be used like PEAP, EAP-TLS, and EAP-TTLS WPA and WPA2 using a PSK don't use radius**_
35. Which of the following wireless security mechanisms is subject to a spoofing attack? _MAC address filtering_
36. What's the best description of why disabling SSID broadcast is not an effective security measure against attackers? _The network name is contained in wireless packets in plaintext_
37. You're reviewing logs from a wireless survey within your organization's network due to a suspected attack and you notice the following entries:

MAC | SSID | Encryption | Power
--- | --- | --- | ---
12:AB:34:CD:56:EF | GetCertifiedGetAhead | WPA2 | 47
12:AB:34:CD:56:EF | GetCertifiedGetAhead | WPA2 | 62
56:CD:34:EF:12:AB | GetCertifiedGetAhead | WPA2 | 20
12:AB:34:CD:56:EF | GetCertifiedGetAhead | WPA2 | 57 
12:AB:34:CD:56:EF | GetCertifiedGetAhead | WPA2 | 49

What's the most likely explanation? _An evil twin is in place_

38. Mobile users in your network report that they frequently lose connectivity with the wireless network on some days, but on other days they don't have any problems. What could cause this? _Wireless jamming_
39. Management within your organiztion wants some users to be able to access internal network resources from remote locations. What's the best choice to meet this need? _VPN_
40. You suspect that an executable file on a web server is malicious and includes a zero-day exploit. What steps can you take to verify your suspicions? _Perform an OS baseline comparison_
41. Lisa has scanned all the user computers in the organization as a part of a security audit. She's creating an inventory of these systems, including a list of applications running on each computer and the application versions. What's she most likely trying to identify? _~~Attack surface~~ **Admins create a list of apps installed on systems as part of an application baseline. THe attack surface looks at much more than just applications and includes protocols and services**_
42. An update security policy identifies authorized applications for company-issued mobile devices. What would prevent users from installing other applications on these devices? _Whitelisting_
43. A company is implementing a feature that allows multiple servers to operate on a single physical server. What is this? _Virtualization_
44. A software vendor recently developed a patch for one of its applications. Before releasing the patch to customers, the vendor needs to tesst it in different environments. What provides the best method to test the patch in different environments? _virtualized sandbox_
45. Your company has recently standardized servers using imaging technologies. However, a recent security audit verified that some servers were immune to known OS vulnerabilities, whereas other systems weren't immune to the same vulnerabilities. What would reduce these vulnerabilities? _Patch management_
46. Someone stole an executive's smartphone, and the phone includes sensitive data. What would you do to prevent the thief from reading the data? _Use remote wipe_
47. Your organization has issued mobile devices to several key personnel. These devices store sensitive information. What can admins implement to prevent data loss from these devices if they are stolen? _Full device encryption_
48. Homer wants to esure that other people can't view data on his mobile device if he leaves it unattended. What should he implement? _Screen lock_
49. Management wants to implement a system that will provide automatic notification when personnel remove devices from the building. Which security controls will meet this requirement? _RFID_
50. Your organization was recently attacked, resulting in a data breach, and attackers captured customer data. Management wants to take steps to better protect customer data. What would best support this goal? _Stronger access controls and encryption_
51. A business owner is preparing to decomission a server that has processed sensitive data. He plans to remove the hard drives and send them to a company that destroys them. However, he wants to be certain that personnel at that company can't access data on the drives. What's the best option? _Encrypt the drives using FDE_
52. Your organization is considering the purchase of new computers. A security professional stresses that these devices should include TPMs. What benefit does a TPM provide? _It uses hardware encryption, which is quicker than software encryption_
53. What functions does an HSM include? _~~Provides FDE~~ **A HSM is a removable device that can generate and store RSA keys used with servers for data encryption. A TPM provides full drive encryption and is included in many laptops**_
54. Homer installed code designed to enable his account automatically, three days after someone disables it. What did Homer create? _backdoor_
55. Your local library is planning to purchase new computers that patrons can use for internet research. Which of the following are the best choices to protect these computers? _Anti-malware software and cable locks_
56. Your organization has been recieving a signifant amount of spam with links to malicious web sites. You want to stop the spam. What do? _~~Add antivirus software~~ **You can block emails from a specific domain sending spam by adding the comaiin to a block list. While the question doesn't indicate that the spam is coming from a single domain, this is still the best answer. Antivirus software doesn't block spam**_
57. Attackers have launched an attack using multiple systems against a single target. What's this? _DDos_
58. Security admins are reviewing security controls and their usefulness.  Which attacks will account lockout controls prevent? _brute force and dictionary_
59. A web developer wants to reduce the chances of an attacker successfully launching XSRF attacks against a web site app. What provides the best protection? _Server-side input validation_
60. A web developer is input validation techniques to a web site app. What should the developer implement during this process? _Perform the validation on the server side_
61. An attacker is attempting to write more data into a web app's memory than it can handle. What type of attack is this? _Buffer overflow_
62. During a pentest, a tester injected extra input into an app causing the app to crash. What happend? _Fuzzing_
63. A security expert is attempting to identify the number of failures a web server has in a year. What is the expert most likely identifying? _ALE_
64. You're trying to add additional security controls for a database server that includes customer records and need to justify the cost of $1,000 for these controls. The database includes 2,500 records. Estimates indicate a cost of $300 for each record if an attacker successfully gains access to them. Research indicates that there is a 10% possibility of a data break in the next year. What's the ALE? _$75000_
65. A penetration tester is tasked with gaining info on one of your internal servers and he enters the following command `telnet server1 80`. What's the purpose of this command? _~~Use Telnet to remotely administer server1~~ **This command sends a query to server1 over port 80 and if the server is running a service on port 80, it will connect. This is a common beginning command for a banner grabbing attempt. If `80` was omitted, Telnet would attempt to connect using its default port of 23 and attempt to create a Telnet session**_
66. A recent vulnerability assessment identified several issues related to an organization's security posture. What is most likely to affect the organization on a day-to-day basis? _Lack of antivirus software_
67. Which of the following tools would a security admin use to identify misconfigured system within a network? _Vulnerability scan_
68. A security expert is running tests to identify the security posture of a network. However, these tests are not exploiting any weaknesses. What test is the security expert performing? _Vulnerability scan_
69. What is a tool that isn't invasive and can verify is security controls are in place? _vulnerability scan_
70. Your organization develops web app software, which it sells to other company for commercial use. To ensure the software is secure, your organiation uses a peer assessment to help identify potential security issues related to the software. What's the best term for this process? _Code review_
71. Your organization plans to deploy new systems within the network within the next six months. What should your organization implement to ensure these systems are developed properly? _design review_
72. You need to periodically check the configuration of a server and identify any changes. What are you performing? _Baseline review_
73. Your organization hired an external security expert to test a web app. The security expert isn't given any access to the application interfaces, code, or data. What type of test will the security expert perform? _black box_
74. A security admin needs to inspect protocol headers of traffic sent acrosss the network. WHat tool is the best choice for this task? _Protocol analyzer_
75. You're troubleshooting issues between two servers on your network and need to analyze the network traffic. What's the best tool to capture and analyze this traffic? _Protocol analyzer_
76. What is a low-cost solution for fault tolerance? _RAID_
77. You need to modify the network infrastructure to increase availability of web-based apps for internet clients. What provides the best solution? _Load balancing_
78. A security analyst is creating a document that includes the expected monetary loss from a major outage. She's calculating the potential lost sales, fines, and impact on the organization's customers. What document is she likely creating? _BIA_
79. Your organization is updating its business continuity documents. You're asked to review the communications plans for possible updates. What should you ensure is included in the communications plan? _~~A list of systems to recover in hierarchical order~~ **A communications plan will include methods used to respond to media requests, including basic templates. Although not available as a possible answer, it would also include methods used to communicate with response team members, employees, suppliers, and customers. None of the other answers aer part of a communications plan. A DRP includes a list of systems to recover in hierarchical order**_
80. What type of encryption does the RADIUS protocol use? _Symmetric_
81. Your organization is planning to implement VTC, but it wants to protect the confidentiality of the streaming video. What do? _RC4_
82. An organization is implementing a PKI and plans on using public and private keys. What can be used to create strong key pairs? _RSA_
83. Your organizatino is investigating possible methods of sharing encryption keys over a pubic network. What's the best choice? _ECDHE_
84. A user wants to hide confidential data within a jpg. What do? _Steganography_
85. You need to ensure data sent over an IP-based network remains confidential. What provides the best solution? _Transport encyrption_
86. Personnel within your company are assisting an external auditor perform a security audit. They frequently send documents to the auditor via email and some of these documents contain confidential information. Managment wants to implement a solution to reduce the possibility of unintentionally exposing this data. What do? _Encrypt all outbound email containing confidential information_
87. What two protocols provide strong security for the Internet with the use of certificates? _SSL and TLS_
88. Lenny and Carl work in an organization that includes a PKI. Carl needs to send a digitally signed file to Lenny. What does Carl use in this process? _Carl's private key_
89. Bart recently sent out confidential data via email to potential competitors. Management suspects he did so accidentally, but Bart denied sending the data. Management wants to implement a method that would prevent Bard from denying accountability in the future. What are you trying to enforce? _Non-repudiation_
90. An organization is planning to implement an internal PKI for smart cards. What should the organization do first? _~~Identify a recovery agent~~ **A PKI requires a CA, so a CA should be installed first. A recovery agent can be identified, but it isn't required to be done as a first step for a CA**_
91. Which of the following is a valid reason to use a wildcard certificate? _reduce the administrative burden of managing certificates_
92. Homer works as a contractor at a company on a one-year renewing contract. After reviewing his contract, the company issues him a new smart card. However, he's now having problems digitally signing email or opening encrypted email. What's the most likely solution? _~~copy his original private key to his new smart card~~ **He should publish the certificate in his new smart card in a global address list within the domain. It's not possible for users to copy a certificate, a public key, or a private key to a smart card**_
93. You need to request a certificate for web server. Which would you most likely use? _CSR_
94. An organization is implementing a data policy and wants to designate a recovery agent. What indicates what a recovery agent can do? _~~A recovery agent can restore a system from backups~~ **Recovery agents can decrypt data and messages if users lose their private key. Although backups are important, this isn't the role of a recovery agent**_
95. An organizational policy specifies that duties of app developers and admins must be separated. What's the most likely result of implementing this policy? _One group develops program code and the other group deploys the code_
96. App developers in your organization currently update apps on live production servers when needed. However, they don't follow any predefined procedures before applying the updates. What should the organization implement to prevent any risk associted with this process? _Change managment_
97. What is a type of media that allows the mass distribution of personal comments to specific groups of people?  _Social media_
98. Your organization wants to prevent damage from malware. Which stage of the common incident repsonse procedures is the best stage to address this? _Prepartion_
99. You're reviewing incident response procedures related to the order of volatility. What's less volatile? _Hard disk drive_
100. Security personnel confiscated a user's workstation after a security incident. Admins removed the hard drive for forensic analysis, but left it unattended for several hours before capturing an image. What could prevent the company from taking the employee to court over the incident? _A chain of custody wasn't maintained_