#### Wireless Infrastructure Security
Wireless access point placement - follows 802.11 WiFi standards and protocols.
Range
Coverage
Signal Strength
But make sure the signal is not accessible from outside.
Unidirectional access points
High location
Centre of the room
Extended Service Set configuration - ESS
- Involves multiple wireless access points working together to create a unified and extended coverage area for users in a large building or facility
Consider interference between different wireless access points.
- Co-channel
	- 2 channels overlapping using same frequency bands in the same area
	- Signals collide
	- Data is retransmitted until they are sent successfully
- Adjacent
	- Occurs when the channels selected for adjacent wireless access points do not have enough space between the channels.
	- loss of bandwidth
Always select channels 1,6 and 11 when operating in the 2.4 GHz wireless frequency band.

to figure out if interference use site survey:
Site survey is the process of planning and designing a wireless network to provide a solution for:
- wireless coverage
- Data rates
- Network capacity
- Roaming capability
- Quality of Service Levels
Heat map is created with site survey.
Heat maps are a graphical representation of the wireless coverage, the signal strength and frequency utilization data at different locations on a map.
Useful while trouble shooting

#### Wireless security settings
Common forms of wireless encryption.
- WEP
- WPA
- WPA 2
- WPA 3 (most secure)
Wired equivalent privacy - WEP
- Outdated 1999 wireless security standard - protected wired LANs
- used fixed encryption keys
- 64 bit and 128 bit
- RC4 encryption algorithm was used, was insecure and weak
WPA - WiFi Protected Access
- since 2003
- Used TKIP - temporal key integrity protocol
- generated 128 bit key for each packet, eliminating key reuse vulnerabilities
- insecure because of lack of sufficient data integrity checks in the TKIP implementation.
WPA2
- replaced TKIP with AES protocol
- adopted CCMP for stronger encryption
- CCMP - Counter cipher mode with block chaining message authentication code protocol
- New integrity check called MIC - Message integrity code was used in wpa2
WPA3
- Uses AES
- New features
	- SAE - Simultaneous authentication of equals
		- offers a key establishment protocol to guard against offline dictionary attacks
	- Enhanced open
		- Networks using open authentication had improved security.
		- improves user privacy and security by guarding against eavesdropping attacks in public WiFi settings
	- updated cryptographic protocols
		- uses AESGCMP instead of AES
		- GCMP - Galois Counter Mode
			- Supports 128 bit AES for personal networks and 192 bit AES for enterprise networks with WPA3
	- Management protection frames
		- Required to protect network from key recovery attacks
		- Stops
			- Eavesdropping
			- Forging
			- Tampering
Authentication, Authorization and Accounting (AAA protocol)
 - Centralizes user authentication to permit only authorized users to access network resources
 - Remote Authentication Dial-In user Service (RADIUS)
	 - used to secure network access, confirming user identities via central server that enforces predefined access
	 - aids in monitoring user activity to ensure accountability
- Terminal Access Controller Access-Control System Plus (TACACS+)
	- Separates functions of AAA to allow for a more granular control over processes
	- uses TCP and encrypts authentication over older AAA protocols
Authentication protocols
- confirm user identity for network security and authorized access
- EAP - Extensible Authentication Protocol
	- Authentication framework that supports multiple authentication methods
- PEAP - Protected Extensible Authentication Protocol
	- Authentication protocol that secures EAP within an encrypted and authenticated TLS tunnel.
	- Requires both client and server certificates for authentication
- EAP-TTLS  -  Extensible Authentication Protocol - Tunneled Transport Layer Security
	- Authentication protocol that extends TLS support across multiple platforms
	- Requires only Server certificate for authentication
- EAP-FAST - Extensible Authentication Protocol-Flexible Authentication via Secure Tunneling
	- Developed by CISCO, it enables secure re-authentication while roaming within a network without full authentication each time
#### Application Security
Input Validation
- authenticate, clean and secure data inputs 
- Validation Rules
	- These rules delineate acceptable and unacceptable inputs
Defense in depth is always advised.
Cookies
- data is stored in them
- secure cookies should be used instead
- refrain from using persistent cooking
Static Application Security Testing - SAST
- scanning the code before deployment
- Automated tools are available
- Manual code can also be done
DAST - Dynamic Security Application Testing
- testing method that analyzes an application while its running
- Two common methods of conducting DAST are:
	- Fuzzing
		- finding flaws by bombarding it with random data to trigger crashes and security vulnerabilities
	- Stress testing
		- Type of software testing that evaluates the stability and reliability of a system under extreme conditions
Attesting an application
- Code signing
	- Digital signature is used to identify and verify its integrity
	- Devs private key is used to generate a hash in the application, user uses the public key to verify
Sandboxing
- Security mechanism that is used to isolate running programs by limiting the resources they can access and the changes they can make to a system.
#### Network Access Control - NAC
- Used to protect network from known and unknown devices by scanning any devices to determine its current state of security prior to being allowed access to your network.
- device is put in hold before receiving access
NAC can use either persistent or non persistent agents
Persistent Agent
- a software installed on a device requesting network access
Non persistent agent
- User connects to wifi, access a web portal and click a link for login in these solutions.
NAC can be a hardware or a software solution.
Most commonly used NAC is IEEE Standard 802.1x , used in a port based NAC.
- time based factors are considered for entry into network
- Location based factors too
- Role based factors reassess a device's authorization during its use
	- rule based factors apply a series of rules through a detailed admission policy

#### Web and DNS Filtering
Web filtering
- restricting content a user views by:
	- Agent based web filtering
		- Installing a small piece of software known as an agent on each device that will require web filtering.
	- Content categorization
		- Websites are categorized into - Social media, adult content, or gambling
	- Centralized Proxies
		- Server that acts as an intermediary between an org's end users and internet.
	- Block Rules
		- Specific guidelines set by an org to prevent access to certain websites or categories of websites 
	- URL Scanning
		- Used to analyze a website's URL to determine if its is safe or not to access. 
	- Reputation-based Filtering
		- Blocking or allowing websites based on their reputation score
DNS Filtering
- Technique used to block access to certain websites by preventing the translation of specific domain names to their corresponding IP addresses.
#### Email Security
DKIM - Domain keys Identified Mail
- Allows the receiver to check if the email was actually sent by the domain it claims to be sent from and if the content was tampered with during transit
- adds digital signature in email's header
- verified using public cryptographic key present in domain's DNS records.
- benefits
	- Email authentication
	- Protection against email spoofing
	- Improved Email deliverability
	- Enhanced Reputation Score
SPF - Sender Policy Framework
- Email authentication method designed to prevent forging sender addresses during email delivery
- verifies the IP of sender against list of authorized IPs
- benefits
	- Preventing spoofing
	- Improving email deliverability
	- Enhanced Domain's Reputation
DMARC - Domain-based Message Authentication, Reporting and Conformance
- An email validation system designed to detect and prevent email spoofing
- Used on top of DKIM or SPF
- Owner can make their own DMARC policy
- Protects against
	- Email compromise attacks
	- phishing emails
	- email scams
Email Gateway
- Server or system that serves as the entry and exit point for emails
- Help with
	- Email Routing
	- Email security
	- Policy enforcement
	- Encryption and Decryption
- Routes outgoing emails and directs incoming emails to user inboxes
- On premise gateways
- Cloud based gateways
- Hybrid gateways
Spam filtering
- Process of detecting unwanted and unsolicited emails and preventing them from reaching a user's email inbox.
- Uses techniques like:
	- Content analysis
	- Bayesian filtering(statistical)
	- DNS based sinkhole list
	- General email filtering rules
#### Endpoint Detection and Response
Endpoint detection and response - EDR
- Category of security tools that monitor endpoint and network events and record the information in a central database
- Analysis, detection, Investigation, Reporting and alerting takes place.
- Follows a six step process
	- Data collection
	- Data consolidation
	- Threat detection
	- Alerts and threats response
	- Threat investigation
	- Remediation
File Integrity Monitoring - FIM
- Used to validate the integrity of operating system and application software files using a verification method between the current file state and a known, good baseline
- Each file, even binary file, is hashed and stored and gets compared to a known good state.
Extended Detection and Response - XDR
- Security Strategy that integrates multiple protection technologies into a single platform to improve detection accuracy and simplify the incident response process
- Correlate data in all layers such as
	- Email
	- Endpoint
	- Server
	- Cloud workloads
	- Network
- Consolidated platform
#### User Behavior Analytics - UBA
Deploys big data and machine learning to analyze user behaviors for detecting security threats
User and Entity behavior Analytics (UEBA)
- Built upon the foundation of UBA with monitoring of entities(routers etc) as an additional function.
UBA aims to spot anomalies in established patterns, indicating potential threats.
UBA systems:
- Collect and analyze data from diverse sources
- Employ advanced analytics methods
- Create a baseline for normal user behavior
- Continuously monitor user activity to detect anomalies
Benefits
- Early detection of threats
- Insider threat detection
- Improved incident response

#### Selecting Secure Protocols
HTTP - HTTPS
FTP - SFTP
Telnet - SSH
IMAPS
POP3S
SMTPS
SNMPS
**Ports**
Logical construct that identifies specific processes or services in a given system
- Well known ports 0-1023
- Registered ports 1024 - 49151
- Dynamic or private ports 49152 - 65535
Transport Method
Way data is moved
- TCP
	- secure
	- 3 way handshake
	- a bit slow
	- no data loss
- UDP
	- doesnt guarantee data delivery
	- less secure
