#### Ports and protocols
Port is a logical communication endpoint.
Inbound port : Logical comm. opening that is listening for a connection from a client
Outbound port: Logical comm. opening created on a client
Ports range 0 - 65535
Well-known ports - 0-1023 - IANA designated - Internet Assigned Numbers Authority
Registered ports - 1024 - 49151 - IANA designated - should be used by vendors
Dynamic and private ports - 49152 - 65535 - no IANA registration required - common in gaming and stuff
Protocol
- Rules governing the device comm. and data exchange
Well known ports: Should definitely understand and remember.

| S.no | Port Number   | Protocol Used                                         | TCP/UDP Support | Basic description                                                                                                                                          |
| ---- | ------------- | ----------------------------------------------------- | --------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1.   | 21            | FPT                                                   | Uses TCP        | Used for FPT - transfer files from host to host                                                                                                            |
| 2.   | 22            | SSh, SCP, SFTP                                        | Uses TCP        | - Provides secure remote terminal access and file transfer capabilities.<br><br>- Provides secure copy functions<br><br>- Provides secure file transfers   |
| 3.   | 23            | Telnet                                                | Uses TCP        | Provides insecure remote control of another machine using a text-based environment.                                                                        |
| 4.   | 25            | SMTP                                                  | Uses TCP        | Provides the ability to send emails over the network                                                                                                       |
| 5.   | 53            | DNS                                                   | TCP and UDP     | Translates domain names into IP addresses                                                                                                                  |
| 6.   | 69            | TFTP - Trivial File transfer protocol                 | UDP             | Used as a lightweight file transfer method for sending configuration files or network booting of an operating system                                       |
| 7.   | 80            | HTTP                                                  | TCP             | Used for insecure web browsing                                                                                                                             |
| 8.   | 88            | Kerberos                                              | UDP             | Network authentication protocol                                                                                                                            |
| 9.   | 110           | POP3 - post office protocol v3                        | TCP             | Responsible for retrieving email from a server                                                                                                             |
| 10.  | 119           | NNTP - Network News Transfer Protocol                 | TCP             | Used for accessing newsgroups                                                                                                                              |
| 11.  | 135           | RPC - Remote Procedure Call                           | TCP and UDP     | Facilitates communication between different system processes                                                                                               |
| 12.  | 137,138,139   | Netbios                                               | TCP and UDP     | Networking protocol suite                                                                                                                                  |
| 13.  | 143           | IMAP - Internet message access protocol               | TCP             | Allows access to email messages on a server                                                                                                                |
| 14.  | 161           | Simple Network Management Protocol - SNMP             | UDP             | Manages network devices                                                                                                                                    |
| 15.  | 162           | SNMP trap                                             | UDP             | Responsible for sending snmp TRAP messages                                                                                                                 |
| 16.  | 389           | LDAP - Lightweight Directory access protocol          | TCP             | Facilitates directory services                                                                                                                             |
| 17.  | 443           | HTTPS                                                 | TCP             | Provides secure web communication                                                                                                                          |
| 18.  | 445           | SMB - Server messages block                           | TCP             | Used for file and printer sharing over a network                                                                                                           |
| 19.  | 465, 587      | SMTP Secure - SMTPS                                   | TCP             | Provides secure SMTP comm.                                                                                                                                 |
| 20.  | 514           | Syslog                                                | UDP             | Used for sending log messages                                                                                                                              |
| 21.  | 636           | LDAP Secure - LDAPS                                   | TCP             | LDAP comm. over SSL/TLS                                                                                                                                    |
| 22.  | 993           | IMAPS - Internet message access protocol over ssl/tls | TCP             | Used for secure email retrieval                                                                                                                            |
| 23.  | 995           | Post office protocol version 3 over ssl/tls (POP3S)   | TCP             | Used for secure email retrieval                                                                                                                            |
| 24.  | 1433          | Microsoft SQL                                         | TCP             | Used to facilitate communication with microsoft SQL server                                                                                                 |
| 25.  | 1645, 1646    | RADIUS TCP                                            | TCP             | Used for remote authentication, authorization and accounting                                                                                               |
| 26.  | 1812 and 1813 | RADIUS UDP                                            | UDP             | Used for authentication and accounting as defined by the internet engineering task force (IEFT)                                                            |
| 27.  | 3389          | Remote desktop Protocol - RDP                         | TCP             | Enable remote desktop access                                                                                                                               |
| 28.  | 6514          | SYSLOG TLS                                            | TCP             | Used in a secure syslog that uses ssl/tls to encrypt the IP packets using a certificate before sending them across the IP network to the syslog collector. |

#### Firewalls
Monitors incoming and outgoing traffic using rules, block lists etc.
Segments the network.
Types:
- Packet filtering
	- checks packet headers for traffic allowance based on ip and port numbers
	- limited inspection capabilities.
- Stateful
	- all inbound and outbound connections and requests are monitored.
- Proxy
	- intermediary between internal and external connections
	- makes connections on behalf of other endpoints
	- Types:
		- Circuit level
			- SOCKS layer
			- Operates on OSI layer 5(session layer)
		- Application level
			- operates on OSI layer 7(application)
			- conducts various proxy functions for each type of application.
			- Application proxies or layer 7 firewall
- Dynamic packet filtering
	- 
- Kernel proxy
	- has minimal impact on network performance
	- Inspects packets on all layers
Next generation firewall(NGFW)
- more aware of apps and their behaviors
- can conduct deep packet inspection for traffic
- Operates fast with minimal network performance impact
- Offers full-stack traffic visibility
- Integrates with various security products
- Single engine
Unified threat management firewall(UTM)
- ability to conduct multiple security functions in a single appliance.
- include functionalities of:
	- Network firewalls
	- network intrusion prevention system
	- gateway antivirus and antispam
	- vpn concentration
	- content filtering
	- load balancing
	- data loss prevention
- Single point of failure
- Advantages:
	- lower upfront costs, maintenance and power consumption
	- Simplified setup
	- full integration with multiple benefits
	- Separate individual engines
Web application firewall(WAF)
inspects http traffic or https
inline config
- between network firewall and web servers
out of band config
- receives mirrored copy of web traffic
- cant block live traffic
- like IDS
#### Configuring firewalls
ACL - rule set placed on firewalls, routers and other network infrastructure devices that permit or allow traffic through a particular interface.
Top down approach
Include a deny all rule at the end.
info in acl:
- Type of traffic
- source 
- destination
- action
- e.g.: access-list 100 permit tcp 192.168.0.0 0.0.0.255 any eq 22
Hardware based firewalls
- protects all devices on a subnet
Software based firewalls
- on individual system

#### IDS and IPS
IDP
- logs, alerts and Detects
IPS
- Logs, detects, alerts and Prevents
Network Intrusion detection system - NIDS
- Responsible for detecting unauthorized network access or attacks.
- can't stop but can alert
- installed in critical places

HIDS
- installed on a server or an endpoint
Wireless IDS
- detects attempts to cause a DOS on a wireless network
They detect using:
- Signature based algorithms
	- analyze based on defined signatures
	- need constant updates
	- not effective against zero day attacks
	- Pattern matching
		- focuses on specific steps
			- NIDS, WIDS
	- Stateful matching
		- known system baselines
			- WIDS
- Anomaly based algorithms
	- analyzes traffic and compares it to a normal baseline of traffic to determine whether a threat is occurring.
	- 5 types:
		- Statistical
		- Rule/Heuristic
		- Protocol
		- Application-based
		- Traffic
IPS
takes action to stop bad activity
Installed on the border of network, just beyond the firewall to analyze all traffic
NIPS
HIPS
WIPS
#### Network appliances
dedicated hardware device with pre installed software
main types:
Load balancers
- Crucial component in any high-availability network or system that is designed to distribute network or application traffic across multiple servers.
- if network fails, it redirects to working ones
	- During maintenance windows
	- system maintenance etc.
	- dynamic and transparent redirection ensures that services remain uninterrupted.
- Advance version is:
	- Application delivery controller
	- Functions
		- SSl termination
		- HTTP compression
		- Content caching
- In cloud environments they improve flexibility and scalability
- Used in:
	- High traffic websites
	- critical application systems
	- Extensive digital platforms
Proxy servers
- intermediary between client and server
- helpful in
	- content caching
	- request filtering
	- login management
- Can store copy of data, used next time when visited.
- security against ddos
- implementing user authentication protocols
- Providing secure tunnels
- routing traffic
Sensors
Designed to monitor, detect and analyze traffic and data flow across a network in order to identify any unusual activities, potential security breaches or performance issues.
- aiding in performance monitoring
- detecting performance anomalies
- triggering alerts
- first line of defense

Jump servers
dedicated gateway used by sys admins to securely access devices located in different security zones within the network
highly available
restrict direct access to systems
sensitive data is protected
centralized point of access, logs are generated
Streamlined management and maintenance

#### Port security
restricting which devices can connect to a specific port based on the network interface card's MAC address.
Network switches operate on layer 2.
They use intelligence to prevent collisions
Works in full duplex mode
Switch has a CAM table to store MAC address mapping - CAM stands for content addressable memory
MAC Flooding
To prevent 
MAC filtering
can restrict mac address
Sticky MAC - Persistent MAC learning
- Feature in network port security where the switch automatically learns and associates MAC addresses with specific interfaces
Defenses:
- 802.1x protocol
	- standardized framework 
	- uses
		- RADIUS
			- cross platform
			- doesn't support RAP, Netbios or x.25 PAD connections
		- TACACS+
			- cisco proprietary protocol  
			- slower as it uses TCP 
			- more secure
			- supports all networking protocols
	- To work, uses:
		- Supplicant
			- device of user
		- Authenticator
			- to which the request is made
			- switch, router etc.
		- Authentication service
			- centralized device that performs authentication
802.1x is top notch defense against unauthorized access on the network
802.1x can also be used to encapsulate EAP
Extensible Authentication Protocol
Framework and series of protocols, offers various ways to conduct authentication:
- simple passwords
- digital certificates
- PKI
Variations of EAP:
- EAP MD5
	- UTILIZES SIMPLE PASSWORDS AND CHALLENEGE HANDSHAKE AUTHENTICATION to provide remote access authentication
	- one way authentication process
- EAP FAST
	- Flexible authentication vis secure tunneling
	- uses protected access credential instead of certificates
	- mutual authentication
- EAP TLS
	- Uses pki
	- digital certificate installed on both server and client for authentication
	- mutual authentication
- PEAP
	- protected EAP
	- mutual authentication
	- uses server certificate and Microsoft AD db for it to authenticate a password from the client
- EAP TTLS
	- digital certificate only on server
	- client uses passwords
- EAP LEAP
	- only works on cisco based devices
#### Securing network communications
To ensure data security on a network we rely on:
VPN
- extends private network over a public network
- users can securely send and receive data
- Types
	- Site to site
		- connects 2 sites securely over a public network
		- a bit slow
	- Client to site
		- connects client with a site
	- Fill tunnel in the above types
		- all traffic is encrypted.
		- entire network is accessible after headquarters network
	- Split tunnel in the above types
		- divides traffic and network requests 
		- sends them to appropriate networks
		- less secure
		- more performance
		- bypasses headquarters server
	- Clientless
		- secure remote access through browser based vpns
		
TLS
- protocol that provides cryptographic security for secure connections and is used for secure web browsing and data transfer
- slows
- DTLS
	- Datagram based version
	- a bit fast
IPSec
- most common
- provides authentication and encryption in IP networks
- CIAuthentication is ensured
- Anti replay
 5 steps of establishing a vpn over IPSEC
 1. Request to start internet Key exchange
	 - PC1 initiates traffic to PC2, triggering IPSEC tunnel creation by RTR1
 2. IKE phase 1
	 - RTR1 and RTR2 negotiate security associations for IPSec IKE phase 1 (ISAKMP) tunnel
 3. IKE phase 2
	 - IKE phase 2 establishes a tunnel within the tunnel
 4. Data transfer
	 - Data transfer between PC1 and PC2 takes place securely
	 - Two modes to choose from:
		 - Transport mode
			 - employs the original IP header, ideal for client to site VPNs, and is advantageous when dealing with MTU constraints
			 - most vpn has an MTU limit of 1500 bytes
		- Tunneling mode
			- employed for site to site VPNs and adds an extra header that can increase packet size and exceed the MTU
			- can go over 1500
 5. Tunnel termination
	 - Tunnel termination, including the deletion of IPSec security associations
Authentication header (AH)
- Offers connectionless data integrity and data origin authentication for IP datagrams using cryptographic hash as identification information
Encapsulation Security Payload (ESP)
- Employed for providing authentication, integrity, replay, protection and data confidentiality by encrypting the packet's payload.

 
#### SD-WAN and SASE
SD WAN software defined wide area network
- Virtualized approach to managing and optimizing wide area network connections to efficiently route traffic between remote sites, data centers and cloud environments
SASE - secure access service edge
- Used to consolidate numerous networking and security functions into a single cloud-native service to ensure that secure and access for end users can be achieved
- e.g:VPC in aws, azure virtual WAN, gcp interconnect

#### Infrastructure Considerations
include:
- Correct placement of devices
- Security zones and screened subnets(DMZ)
- Understanding attack surface
- Determining connectivity methods
- Understanding device attributes
- Configuring the failure mode
	Things to consider:
		Fail open
		- allows all traffic in the event of failure
		Fail closed
		- blocks all if failed
#### Selecting Infrastructure Controls
Control is a safeguard installed to minimize risks on assets
resource efficiency
Key principles while selecting infrastructure controls
- Principle of least privilege
- Defense in depth
- Risk based approach
- Lifecycle management
- Open design principle
Methodology
- Assessing the current state
- Conduct gap analysis
- Setting clear objectives
- benchmarking
- Conducting cost benefit analysis
- Ensuring stakeholder involvement
- Implementing monitoring and feedback loops
Best practices
- Conduct a comprehensive risk assessment
- Align control selection with established standards
- Customize framework controls
- Emphasize stakeholder engagement and training
Controls must be regularly reviewed.
