#### Distributed Denial of Service
attackers attempt to make a computer unavailable
- Flood attack
	- Sending a lot of requests
	- PING flood - too many pings(ICMP packets)
	- SYN Flood - alot incomplete  TCP handshakes
	- Can use Flood guards
	- Timeouts
	- IPS
Permanent Denial of Service attack (PDOS)
Attack which exploits a security flaw by reflashing a firmware, permanently breaking networking device

Fork Bomb
- attacker creates large number of processes to take up computer's available processing power
DDOS
- multiple machines send request to the victim
DNS amplification attack
- flooding dns request to the website
- from multiple device
- part of a botnet
To protect, use:
Blackhole/sinkhole
- identifies IPs and redirects them to a null server
- but attacker can come up w new IP
IPS/IDS
Elastic infrastructure - but bill increases

#### Domain Name System Attacks
translates websites names into IP address
Attacks:
- DNS Cache poisoning
	- corrupting dns cache data with false info
	- to prevent use DNSSES to add digital signature to org's DNS data
	- protect dns servers w secure network
- DNS amplification attacks
	- attacker overloads the target with DNS response traffic by exploiting the DNS resolution process. He uses target's IP for the DNS query and DNS sends response to the target. kind of DOS
	- limit size of dns responses
- DNS tunneling
	-  DNS over port 53 to restrict non tunnel dns data.
	- But attackers can utilise this for their own advantage by sending malicious code in the tunnel
- Domain hijacking
	- altering domain name's registration without original registrant's consent.
- DNS zone transfer attacks
	- attacker mimics an authorized system to request and obtain the entire DNS zone data for a domain

#### Directory Traversal Attack
type of injection attack
Directory traversals may be used to access any file on a system with the right permissions.
../ might be encoded as %2e%2f
File inclusion
- attacker downloads files from an arbitrary location or uploads an executable or script file to open a backdoor
- Remote file inclusions occur when an attacker tries to execute a script to inject a remote file 
- Local file inclusion occurs when an attacker tries to add a file that already exists
- tips
- ../ think directory traversal

#### Execution and Escalation Attack
Arbitrary code execution
- allows an attacker to run a code or module that exploits a vulnerability 
Remote Code execution
- type of arbitrary code execution that allows an attacker to transmit code from a remote host
Privilege escalation
- attacker attempts to gain admin access
- Vertical 
	- from normal to admin access
- Horizontal
	- one user to other user on same level of access
Rootkits
- malware that modifies system files often at kernel level to conceal its presence.
- Kernel mode
	- Complete control over system
- User mode
	- might have admin or normal access

#### Replay Attacks
network based attacks
maliciously repeating or delaying valid data transmissions
Session hijack
- Attacker alters real-time data transmissions
Replay attack
- Attacker intercepts data and decides whether to retransmit it later.
Use session token to stop these.
Use WPA3
#### Session Hijacking
Session management
- fundamental security component that enables web apps to identify a user.
- info is stored in cookies to retain info about the session
- cookie is a text file
- sent in the http header
- session cookies and persistent cookies
Session hijacking
- spoofing attack where the host is disconnected and replaced by the attacker.
Session prediction
- attacker attempts to predict session token to hijack
Cookie poisoning
- modifies the contents of the cookie to be sent to a client's browser and exploit the vulnerabilities in an application.

#### On-Path Attacks
pentester puts workstation logically between two hosts during the communication.
ARP poisoning
DNS poisoning
Introducing a rogue access point
Introducing a rogue hover/switch
relay - attacker becomes proxy between two hosts - can also change not just intercept.
SSL Stripping
- tricking the encryption with an HTTP conn. instead of HTTPS
Downgrade attack
- attacker attempts to have a client or server abandon its higher security mode

#### Injection Attacks
LDAP injection
- an attack in which LDAP statements, typically created by user input, are fabricated.
- input validation and sanitation
Command injection
- attacker is able to execute arbitrary shell commands via vulnerable web app
- input validation
Process injection
- method of executing arbitrary code in the address space of a separate live process
Many ways to inject:
- Injection through DLLs
- Thread execution hijacking
- Process hollowing
- Process Doppel ganging
- Asynchronous procedure calls
- Portable execution injections
To mitigate, use:
- Endpoint security solutions
- security kernel module
- Practice of least privilege
#### Indicators of Compromise
Data pieces that detect potential malicious activity.
Some of them are:
- Account lockouts
- Concurrent session usage
- Blocked content
- Impossible travel
- Resource consumption
- Resource inaccessibility
- Out of cycle logging
- Articles or documents on security breach
- Missing logs