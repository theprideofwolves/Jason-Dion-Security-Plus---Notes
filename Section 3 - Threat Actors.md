#### Threat Actors
Entity responsible for threat
Motivations of threat actors include:
- Data exfiltration - stealing data 
	- Selling on dark web
	- Identity theft
	- Competitive advantage
- Espionage
	- Spying to gain sensitive data
	- Nation state or rival organizations
	- For strategic advantages
- Financial gain
	- Most common
	- ransomware
	- financial trojans
- Ethical Reasons
	- To improve security
	- bug bounty hunters and white hat hackers
- Disruption or chaos
	- For the thrill of it
	- Some men just want to watch the world burn
- Blackmail
	- Ransomware
	- sextortion
- Service disruption
	- DOS
	- DDOS
- Philosophical or political beliefs
	- Hacktivists
- Revenge
	- employee who is fired or laid off.
- War
	- Disrupt infrastructure
	- compromise security
	- economic damage
	- geopolitical objectives
Attributes of a threat actor:
- Internal vs External
	- Internal 
		- Insiders
	- External
		- Hacktivists
		- Rival company hackers
- Resources and Funding
	- Tools skills and personnel at the disposal of a given threat actor.
- Level of sophistication and capability
	- Technical skills, complexity of attacks and level of expertise of the threat actors.
	- Custom malwares etc.
Threat Actor attributes based on characteristics or properties such as motivations and funding levels:
- Unskilled attackers
	- Script kiddies
		- Cant develop own programs or tools, uses tools made by others
		- Motivated by desire for recognition or curiosity
		- DDOS of most common attack using tools and readily available payloads
- Hacktivists
	- Driven by social change
	- Techniques used:
		- Website defacement
			- Electronic graffiti
		- DDOS Attacks
			- Overwhelm resources of the system
		- Doxing
			- public release of personal information to support a victim
		- Leaking of sensitive data
			- Stealing and releasing sensitive data to public
	- Motivated by belief.
	- Anonymous or LULZSEC
- Organized crime
	- Sophisticated and well - structured.
	- Members have specific roles
	- High level of technical ability.
	- Use new tech such as crypto or cellular tech
	- Target MSBs or high net worth.
	- Can be hired by rival companies or nation-state to act on their behalf.
	- FIN7 or CARBANAK
- Nation-state actors
	- Sponsored by governments
	- Part of military or sometimes
	- Mostly operate as independent entities so the nation  can deny any attack.
	- Attempt false flag attacks - meaning they make it look like attack originated from someone else. to deviate the victim, mislead investigators.
	- Advanced persistent threat - prolonged targeted cyberattack. Most dangerous
	- Motivated to achieve strategic goals. 
	- Stuxnet worm
- Insider threats
	- Threats within the organization
	- Has alot of knowledge as the actor is inside the organization.
	- Capabilities are based on the role. But skill plays a role too.
- Shadow IT
	- Use of personal devices for work purposes without the employer's or organization's knowledge
	- Installation of unapproved software
	- Use of cloud services that have not been approved by the organization.
	- sometimes, as it takes alot of time for the organization to approve for a new device such as a monitor, the person buys a monitor on his own, even this is shadow IT..What if its a USB?
#### Threat Vectors and Attack Surfaces
Pathway by which an attacker can gain unauthorized access to a computer or network to deliver a malicious payload or carry out an unwanted action.

**Attack point** encompasses all the various points where an unauthorized user can try to enter data to or extract data from an environment.

Attack surface can be reduced:
- Reducing access
- Removing unnecessary software
- Disabling unused protocols

Threat vectors include:
- Messages
	- Phishing campaigns
- Images
	- Embedding malicious code in the image file
	- Stegano attacks
- Files
	- Malicious files disguised as legit files
- Voice calls
	- Social engineering by impersonation
- Removable devices
	- USB or HDD/SDD
	- Baiting by dropping these in public places.
- Unsecure Networks
	- Wireless networks lacking security(public wifi)
	- Rogue access points
	- Bluetooth attacks - BlueBorne and BlueSmack
#### Outsmarting threat actors
Proactive process using deceptive and disruptive technologies.
Deceptive and disruptive technologies are designed to mislead, confuse and divert attackers from critical assets while simultaneously detecting and neutralizing threats. Can delay or deter. Most commonly used are:

- Honeypots
	- Used to mimic real systems
	- Focus on gathering info like the attackers techniques
	- Detect insider threats, internal fraud, snooping and malpractice
	- Simulation basically
	- Can log everything
	- To install a honeypot in an enterprise network, place it within a screened subnet or isolated segment that is easily accessed by potential attackers
	- Double edged sword coz attacker might learn how your internal systems work.
- honeynets
	- Network of honeypots
	- More complex
	- Includes servers, routers and switches
	- Logs everything
	- Double edged sword coz attacker might learn how your internal systems work.
- Honeyfiles
	- Decoy file to lure attackers in a system.
	- Fake data, trap.
	- When accessed an alert is generated.
	- can be created in any formats such as:
		- Word processing documents
		- Spreadsheets
		- Presentation files
		- images
		- database files
		- executables
	- Embedded with unique identifiers or watermarks
	- Placed deliberately under loose defenses
- Honeytokens
	- Data with no legit value.
	- Only monitored for access.
	- Useful for detecting insider threats.
Some disruption technologies include:
- Using bogus DNS entries
	- Fake DNS entries to mislead and waste attacker's time.
	- Non existent domains
- Creating decoy directories
	- fake files/folders within storage of a system. 
	- Alerts are generated when accessed.
- Generating dynamic page
	- Used in websites to present ever-changing content to web crawlers to confuse and slow down the threat actor.
- Using port triggering
	- Security mechanism where specific services or ports on a network device remain closed until a specific outbound traffic pattern is detected.
- Spoofing fake telemetry data
	- Responding to scans by sending out fake data.
**TTPs - Tactics, Techniques and Procedures.**
Refer to specific methods and patterns of activities or behaviors associated with a particular threat actor or group of threat actors.

Cyber professionals learn these TTPs of the attackers by implementing deceptive and disruptive technologies discussed above.

