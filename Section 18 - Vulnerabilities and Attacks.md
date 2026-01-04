#### Hardware vulnerabilities
Weaknesses in physical components of a system/device
Firmware
- special software providing low level control of the hardware behavior
End of life systems
- No longer updates are rolled out by manufacturer
Unpatched systems
- not updated with latest updated
- oversight or negligence
Hardware misconfigurations
- set up is not optimal
- may open up vulnerabilities
- performance decreases
- unintended behavior
- automate and conduct regular audits to fix
to mitigate
- Hardening
	- tighten security
- patching
	- fix known vulnerabilities
- Configuration environment
	- all systems should adhere to a standard secure configuration
- Decommissioning
	- system is removed from network
- Isolation
	- limit potential damage
- Segmentation
	- Even if one system is affected, it doesn't spread to the rest of the network

#### Bluetooth Vulnerabilities and Attacks
used for exchanging data between fixed and mobile devices over short distances without the need for an internet connection.
Vulns
- Insecure device pairing
	- weak authentication
- device spoofing
	- attacker spoofing a legit device
- On path attacks
	- communication between devices is intercepted and altered.
Attacks
- Bluejacking
	- attacker can send messages to bluetooth enabled devices
	- no serious harm
- Bluesnarfing 
	- used to steal info like contacts, call logs and text messages
- Bluesmack
	- attacker sends lot of info causing the device to crash(like DOS)
- Blueborne
	- can infect numerous devices within seconds
	- no intervention needed
Best practices
- turn off bluetooth when not in use
- use non-discoverable mode
- Regularly update devices
- only pair with known devices
- always use unique PINs or passkeys when pairing
- be cautious of unsolicited messages or requests
- use encryption for sensitive data transfers

#### Mobile vulnerabilities and attacks
Sideloading
- installing apps from other sources
- apps not scanned
- always download from official sources
Jailbreaking/rooting
- gives user escalated privileges
Insecure connection methods
- don't use public Wi-Fi
Mobile device management(MDM)
- can regularly push security patches
- can see if all devices of the org are UpToDate
- can disable a device's ability to sideload programs
- detect if a device has been jailbroken or rooted
- Force each device to use a VPN connection

#### Zero day vulnerabilities
vulnerability with no patch.
Attackers use it to their advantage.
No one can stop it, most can't even detect it.
Zero day vulnerability
Zero day exploit
Zero day attack

#### Operating system vulnerabilities
Unpatched systems
- regularly update the system
Zero day vulnerabilities
- unknown to developers
- they cant fix it
- Use Host based IPS
Misconfigurations
- System settings are not properly configured
Data exfiltration
- unauthorized data transfers from org to an external location
Malicious Updates
- malicious update to a well known program crafted by the attacker
- always verify authenticity.

#### SQL and XML injections
Injections attacks occur when attackers sends malicious data into a system.
SQL injection
- insertion of injection queries into an data input form
- use input validation
- sanitize input
XML injections - Extensible Markup Language
- XML is used by web apps for authentication, authorization and other types of data exchange
- To protect, always send XML data in an encrypted tunnel such as TLS tunnel
- input validation and input sanitization
- If not, prone to:
	- Snooping
	- Spoofing
	- Request forgery
	- Injection of arbitrary code
- XML bomb - Billion laughs attack
	- XML encodes entities that expand to exponential sizes, consuming memory on the host and potentially crashing it.
	- consumes all resources, DOS
- XML external entity(XXE)
	- attack that embeds a request for a local resource.
To know if its an XML code, see if it has ID fields.
#### Conducting an SQL injection


#### XSS and XSRF
XSS - Cross site scripting
- Injects a malicious script into a trusted site to compromise the site's visitors
- input validation is important
- steps
	- attacker identifies missing input validation
	- attacker crafts a script and injects it
	- trusted site runs the code in a user's session
	- runs in the user's browser 
- Defaces a trusted website
- stealing user's data
- intercepting data or comm.
- installing malware on client's system
- breaks browser's security and trust model
- Non persistent XSS
	- Happens once when link is loaded 
- Persistent XSS
	- attacker inserts code in the backend
	- happens every time page in loaded
- DOM XSS
	- client's web browser is exploited
	- page content and layout is modified
TIPS for the exam
document.cookie
document.write/right then its a DOM based attacks
if u see javascript ..its an XSS attack
Session management
- enables web apps to uniquely identify user across different actions and requests
Cookie
- File containing ID data of a user when they visit a site
- Non Persistent
	- session cookies
	- reside in memory
	- alive for a short period of time
- Persistent
	- stored in browser cache until explicitly deleted or till they expire
Session hijacking
- a spoofing attack where attacker disconnects a host and then replaces it with his or her won machine by spoofing the original host IP
Session prediction
- attacker attempts to predict the session token in order to hijack the session
Cross site request Forgery (CSRF/XSRF)
1. Victims logs into bank account
2. bank assigns victim a validation token
3. Hacker sends forged request disguised as legitimate communication from the bank.
4. Victim unknowingly forwards request to bank.
5. Forged request is executed by the bank using previously assigned validation token.
to secure:
- Use user specific tokens in all form submissions
- add randomness and prompt for additional information
- Require users to enter their current password when changing their password

#### Buffer overflow
occurs when data exceeds allocated memory, potentially enabling unauthorized access or code execution
buffer is a temporary storage area
smashing the stack
- Occurs when an attacker can execute their malicious coed by overwriting the return address.
ASLR - Address Space layout randomization
- security measure that randomizes memory addresses, making buffer overflow attacks harder for attackers
Side channel attacks can bypass ASLR

#### Race Conditions
Software vulnerability where the outcome depends on the timing of events not matching the developer's intended order

occur when multiple threads write to the same variable or object in the same memory location simultaneously.

This can happen when dereferencing is exploited
Dereferencing is a fundamental operation in programing, and the vulns arise from unsafe or concurrent usage, particularly in scenarios involving race conditions
Dirty COW - COPY ON WRITE
Time of check vulnerability
- attacker can alter a system resource after an application checks its state but before the operation is performed.
Time of Use vulnerability
- attacker can change the state of a system resource between the time it is checked and the time it is used
TOC and TOU are two critical moments within the same vulnerability, which is categorized as a race condition.
Time of evaluation vulnerability - TOE
- involves manipulation of data or resources during the time window when a system is making a decision or evaluation
To protect against race conditions, use:
- Mutex
	- mutually exclusive flag that acts as a gatekeeper to a section of code so that only one thread can be processed at a time
	- might cause deadlocks sometimes