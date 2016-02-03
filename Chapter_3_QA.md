1. What protocol does IPv6 use for hardware address resolution? _NDP_
2. What is the default port for SSH? _22_
3. You are configuring a host-based firewall so that it will allow SFTP connections. What is required? _Allow TCP 22_
4. You need to send several large files containing proprietary data to a business partner. What's the best choice for this task? _SFTP_
5. Your organization is planning to establish a secure link between one of your mail servers and a business partner's mail server. The connection will use the internet. What protocol should you use? _~~SSH~~ **TLS is a good choice to create a secure connection between two systems over the internet. Although SSH creates a secure connection, it isn't used with SMTP**_
6. You recently learned that a network router has TCP ports 22 and 80 open, but the organization's security policy mandates that these should not be accessible. What do? _Disable SSH and HTTP on the router_
7. You need to prevent the use of TFTP through your firewall. what block? _UDP 69_
8. You need to enable the use of NetBIOS through a firewall. What ports should you open? _137 through 139_
9. Lisa wants to manage and monitor the switches and routers in her network. Which protocol should she use? _SNMP_
10. You need to deivide a single Class B IP address range into several ranges. What do? _Subnet the Class B IP address range_
11. You need to reboot your DNS server.  Which type of server are you most likely to reboot? _~~Unix Server~~ **BIND is a type of DNS software commonly used on the internet. BIND runs on Unix servers, but not all Unix servers are BIND servers**_
12. Your organization is increasing security and wants to prevent attackers from mapping out the IP addresses used on your internal network. What do? _~~Block outgoing traffic on UDP port 53~~ **By implementing secure zone transfers on internal DNS servers, it prevents attackers from downloading zone data and mapping out IP addresses and devices. Blocking outgoing traffic on UDP port 53 would prevent internal users from using DNS on the internet**_
13. A network technician incorrectly wired switch connections in you organization's network. It effectively disabled the switch as though it was a victim of a DoS attack. What should be done to prevent this in the future? _Implement STP or RSTP_
14. Your organization frequently has guests visiting in various conference rooms throughout the building. These guests need access to the Internet via wall jacks, but should not be able to access internal network resources. Employees need access to both the internal network and the internet. What would meet this need? _VLANs and 802.1x_
15. Your network currently has a dedicated firewall protecting access to a web server.  It is currently configured with the following two rules in the ACL along with an implicit allow rule at the end.  
   ```
      PERMIT TCP ANY ANY 443
      PERMIT ANY ANY 80
   ```  
You have detected DNS requests and zone transfer requests coming through the firewall and you need to block them. What can meet this goal? _add  `DENY IP ALL ALL 53` or change the implicit allow rule to implicit deny_
16. Your organization wants to prevent users from accessing file sharing web sites. What can meet this need? _~~Content inspection~~ **A URL filter blocks access o specific web sites based on their URLs**_
17. Your organiztion wants to combine some of the security controls used on the network. What could your organization imlement to meet this goal? _UTM_
18. Your organiation hosts a web server and wants to increase its security. You need to separate all web-facing traffic from internal network traffic. What's the best solution? _DMZ_
19. Network admins connect to a legacy server using Telnet. They want to secure these transmissions using encryption at a lower layer of the OSI model. What could they use? _~~SSH~~ **IPv6 includes the use of IPsec, which operates on Layer 3. Although you can use SSH instead of Telnet, they both operate on Layer 7**_
20. Which of the following operates on the HIGHEST layer of the OSI model, and is the most effective at blocking application attacks? _~Stateless firewall~~ **A WAF operates on multiple layers up to Layer 7 and blocks attacks against a web server. A stateless firewall only performs packet filtering and isn't effective against Application layer attacks**_