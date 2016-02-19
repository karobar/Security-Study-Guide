###### Smurf Attacks
 1. Smurf spoofs a target's IP address
 2. Smurf attacker sends a ping out as broadcast instead of unicast 
 3. target is flooded with ICMP replies

---
###### Xmas/Christmas Tree Attack
 - a type of port scan used to identify underlying details of an OS
 - has several bit flags set in the TCP packet header like the lights on a Christmas Tree
 - Different OSs respond to the flags differently

---
###### MitM (Man-in-the-Middle) Attacks
A computer that accepts traffic from each party in a conversation and forwards the traffic between the two

---
###### Replay Attacks
 - an attacker replays data that was already part of a communication session
 - a third party attempts to impersonate a client that is involved in the original session.

---
# Password Attacks
 - attempt to discover or bypass passwords 
 - the password hash can also be attacked!

###### Online Password Attack
attempting to discover a password from an online system. For example, an attacker trying to log on to an account by trying to guess a user's password
###### Offline Password Attack
attempts to discover passwords from a captured database or captured packet scan. For exapmle, during a data breach, hackers could download a copy of an entire database, then discover passwords within that copy.
###### Birthday Attacks
 - named after the birthday paradox
 - an attacker is able to create a password that produces the same hash as the user's actual password (hash collision)
 - md5 uses 128 bits and is susceptible to birthday attacks
 - SHA-2 uses up to 512 bits and isn't susceptible

###### Rainbow Table Attacks
 - attempting to discover a password from a hash using a **rainbow table**, which is a huge database of precomputed hashes.
 - Assume a hacker has a hash, they can use an application which follows this algorithm:
    1. guess a password (or use a dictionary)
    2. hash the guess
    3. compare the original hash with the guess-hash
    4. if not the same, repeat
 - **rainbow tables** speed up step 2 from the above process by storing passwords and their calculated hashes

---
###### Salting
 - a way to prevent dictionary and rainbow table attacks 
 - a set of random data, such as two additional characters, is added to a password before hashing

---
# DNS Attacks
###### DNS Poisoning
 - attempts to modify or corrupt DNS results
 - for example, a successful DNS poisoning attack can modify the IP address associated with google.com and replace it with the IP address of a malicious website

###### Pharming Attacks
 - corrupting the DNS _server_ or the cached addresses on a DNS _client_ 
 - for example, modification of the hosts file on Windows to the following:
     
       127.0.0.1      localhost
       204.79.197.200 google.com
 - (204.79.197.200 is Bing's address )

### ARP Poisoning Attacks
 - an attack which misleads computers or switches about the actual MAC address of a system
 - ARP resolves the IP addresses of systems to their MAC addresses and stores the result in an area of memory known as the **ARP cache**
 - ARP uses two primary messages:
    - **ARP request:** broadcasts the IP address and asks "Who has this IP address?"
    - **ARP reply:** The computer with the IP address in the ARP request responds with its MAC address. The computer that sent the ARP request caches the MAC address for the IP address. Computers that hear the ARP reply cache the MAC address.
 - Attackers can create ARP reply packets with spoofed or bogus MAC addresses

###### ARP MitM (Man-in-the-Middle) Attacks
Normal operation:   
             
    ☺ <- Switch -> (Router with IP:192.168.1.1 MAC:01-23-45-01-01-01)-Internet

After a hacker connects to the switch and poisons the ARP cache with the following:

    192.168.1.1, 01-23-45-66-66-66

This now happens:

    ☺ <- Switch -> (Router...)-Internet  
         v^
         ☻ (hacker with IP:192.168.1.66 MAC 01-23-45-66-66-66)
         
###### ARP DoS Attack
 - An attacker can send an ARP reply with a bogus MAC address for the **default gateway** (which is the IP address of a router connection which provides a path out of the network)
 - If all computers cache a bogus MAC address for the default gateway, none of them can reach it and the outgoing network halts

---
###### Typo Squatting/URL hijacking
when someone buys a domain name close to a ligitimate site

--- 
###### Watering Hole Attacks
attempting to discover which websites employees are likely to visit and then infecting those wesites with malware

---
# Web browser concerns
 - add-ons
 - cookies
    - **session hijacking attacks:** when a user logs onto a website, the website often returns a cookie with a session ID which remains on the user's system until logged off. In this attack, the attacker learns this session ID and impersonates the user.
    - **Flash Cookies and LSOs (Locally Shared Objects):** Flash cookies are stored in multiple locations, and cannot be deleted by normal means. As an example, when a user goes to a website A which uses a Flash cookie and a website B which doesn't use a Flash cookie, the Flash cookie can record activity on website B
 - attachments
 - **arbitrary code execution:** the ability of an attacker to execute _commands_ or programs on a target system
 - **remote code execution:** the ability of an attacker to execute code from a _remote system_

---
###### Header Manipulation Attacks
spoofing a users's session ID or other flags within the header

---
# Secure Coding
#### Input Validation
 - proper characters
 - boundary/range checking
 - block HTML

###### Client-Side Input Validation
 - quicker, but is vulnerable to attack
 - validation code is included in the HTML page sent to the client, and doesn't submit the form until the client enters the correct data
 - only works if JavaScript is enabled
 - a validated form can be interfered with on the way back

###### Server-Side Input Validation
 - slower but secure

#### Avoiding Race Conditions
when two or more modules or applications attempt to access a resource at the same time, it causes a conflict called a race condition
#### Error/Exception Handling
 - error messages should be general, not specific; so that attackers can't determine details about the system

---
###### NOP Sled/Slide
 - Used in buffer overflow attacks
 - Many Intel processors use hexadecimal 90 as a NOP (no-operation) command. 
 - When executing code from memory, a computer which encounters a NOP command just goes to the next location

---
###### XSRF oor CSRF (Cross-Site Request Forgery)
 - an attacker tricks a user into performing an action on a website, using a crafted HTML link
 - for an example, if you go to `google.com/search?q=Success`, it's just like if you went to google and searched for 'Success'
 - attackers manipulate the URL to do crazy stuff

---
# Transitive Access and Client-Side Attacks
 - an attacker can't access a database server, but they can access a web server which connects to a database server
 - if the web server is trusted, it can query the database server and retrieve data
 - if the web server doesn't use input validation, it can get SQL injected, then transfers malicious code to the database
