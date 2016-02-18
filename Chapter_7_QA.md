1. An IDS alerts on increased traffic. Upon investigation, you realize it's due to a spike in network traffic from several sources. What's a likely explanation? _A DDoS attack_
2. A network admin needs to ensure the company's network is protected against smurf attacks. What should the admin do? _~~Install flood guards~~ **Smurf attacks are blocked by preventing routers from passing directed broadcasts, especially border routers with direct access to the Internet. Flood guards protect against SYN flood attacks**_
3. Some protocols include timestamps and sequence numbers. These components help protect against what type of attacks? _Replay_
4. Whats a good method to protect against someone trying to guess the correct PIN to withdraw money from an ATM? _Account lockout_
5. An application stores user passwords in a hashed format. Which of the following can decrease the likelihood that attackers can discover these passwords? _~~Rainbow tables~~ **A password salt is additional random characters added to a pssword before hashing the password, and it decreases the success of password attacks. Rainbow tables are used by attackers and contain precomputed hashes**_
6. A user complains that his system is no longer able to access google. Instead his browser goes to a different site. After investigation, you notice his host file looks like this:
    
       127.0.0.1     localhost
       72.52.230.233 www.google.com
   What's going on? _A pharming attack_
7. Security analysts recently discovered that users in your organization are inadvertently installing malware on their systems after visiting the `comptai.org` website. Users have a ligitimate requirement to visit this site. What's caused this malware? _typo squatting_
8. An attacker recently attacked a web server hosted by your company. After investigation, security professionals determined that the attacker used a previously unkown application exploit. What is this attack called? _Zero-day attack_
9. Which of the following developer techniques results in significant security vulnerabilities for online website applications? _Poor input validation_
10. An attacker is bypassing client-side input validation by intercepting and modifying data within the HTTP POST command. What's this attack? _~~Command injection~~ **An attacker can use a web proxy to intercept the HTTP POST command. The attacker then modifies the data in the command and sents it to the web site. Command injection is a type of client-side injection attack that input validation thwarts**_
11. Web developers are implementing error and exception handling in a web site application. What's a good practice for this? _Displaying a generic error message but logging detailed information on the error_
12. While reviewing logs for a web app, a developer notices that it has crashed several times reporting a memory error. Shortly after it crashes, the logs show malicious code that isn't part of a known application. What's going on? _Buffer overflow_
13. An app on one of your database servers has crashed several times recently. Examining detailed debugging logs, you discover that just prior to crashing, the database app is receiving a long series of x90 characters. What's going on? _Buffer overflow_
14. Attackers have attacked an online web server using a SQL injection attack. What describes this best? _The attacker is attempting to pass commands to a back-end database server to access data_
15. While creating a web app, a developer adds code to limit data provided by users. The code prevents users from entering special characters. What kind of attack will this code likely prevent? _XSS_
16. Homer recently received an email thanking him for a purchase that he didn't make. He asked an admin about it and the admin noticed a pop-up window, which included the following code: 
    
        <body onload="document.getElementByID('myform').submmit()">
          <form id="myForm" action=gcgapremium.com/purchase.php" method="post">
            <input name="Buy Now" value="Buy Now" />
          </form>
        </body>
    What's the most likely explanation? _XRSF_
17. Which of the following is an attack against servers hosting a directory service? _LDAP_
18. Your organization hosts a website within a DMZ and the site accesses a database server in the internal network. ACLs on firewalls prevent any connections to the database server except from the web server. Database fields holding customer data are encrypted and all data in transit between the website server and the database server. Which of the following represents the greatest risk to the data on the server? _SQL injection_
19. A security tester is sending random data to a program. What's going on? _Fuzzing_
20. Your organization is preparing to deploy a web app, which will accept user input. What will test the reliability of this application to maintain availability and data integrity? _~~Input validation~~ **Fuzzing can test the application's ability to maintain availabiliy and data integrity for some scenarios.  Input validation protects applications but doesn't test them**_
