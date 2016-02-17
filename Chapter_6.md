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
