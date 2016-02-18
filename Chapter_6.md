# Malware
### Virus
 - attaches to a host application. executes when the host executes.
 - tries to replicate itself, then activates and delivers its payload. 
 - the payload may delete files, cause random reboots, join the computer to a botnet, or enable backdoors

###### Armored Virus
 - use techniques to resist reverse engineering
 - complex code can mask the virus's intent
 - the code can be encrypted
 - hide the location on the file system

### Worms
self-replicating malware that travels throughout a network **without** the assistance of a host application or user interaction. Resides in memory.
###### Stuxnet
 - a worm designed to attack a specific embedded system
 - used in one of Iran's nuclear enrichment facilities, causing centrifuges to spin fast enough to tear themselves apart
 - Process:
     1. **Infect:** Windows systems were infected through USB drives
     2. **Search:** look through the network for a specific system
     3. **Update:** download an updated version of the worm
     4. **Compromise:** use zero-day vulnerabilities
     5. **Control:** control the system and send commands as desired
     6. **Deceive and destroy:** Send false data to monitors indicating everything is fine

### Logic Bomb
### Backdoor
### Trojan
 - looks beneficial but includes a malicious component
 - most popular malware
 - frequently create backdoors
 - often delivered by **drive-by downloads**, which involve these steps:
    1. Attackers compromise a web site to gain control of it
    2. Attackers install a Trojan embedded in the website's code.
    3. Attackers attempt to trick users into visiting the site. Sometimes, they simply send the link to thousands of users via email hoping that some fo them click the link.
    4. When users visit, the web site attempts to download the Trojan onto the users' systems.

###### Rogueware/Scareware
 - masquerades as a free antivirus program, then states that it found a bunch of viruses
 - requests unlocking the full version of the program for a fee

###### Ransomware

### Botnets
 - computers in a botnet are called **zombies**
 - **bot herders** are criminals who manage botnets
 - used to send spam, launch DDoS attacks, download additional malware, keyloggers, adware, etc.

### Rootkits
 - a program or group of programs which hides the fact that the system has been infected
 - modifies the internal OS processes and registry files
 - has root-level or kernel-level access to a system
 - use **hooking**, which intercept calls to the operating system

### Spyware
 - installed without awareness
 - monitors the system
 - Ex: keyloggers

### Adware

---
# Social Engineering
 - flattery & conning
 - impersonation of authority or somebody else
 - encouragement
 - tailgating
 - dumpster diving

---
# Phishing
 - malicious spam with the purpose of tricking them into revealing personal info or clicking a link
 - often sends a user to a malicious website that appears like a legitimate site
 - cannot be prevented with input validation
 - a simple method used to validate email addresses is the use of **beacons**, which are links included in the email which links to an image stored on a server. The link includes unique code which identifies the receiver's email address. In order for the email application to display the image, it must retrieve the image from the Internet server. When the server hosting the image receives the request, it logs the user's email address, indicating it's valid. 

###### Whaling
a phishing attack which targets executives
###### Spear phishing
a targeted phishing attack

---
# Spim
spam through instand messaging

---
# Vishing
 - attacks VoIP system to give up PII
