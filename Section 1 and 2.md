
# Section 2 - Fundamentals of Security

## Section 1.2

### CIA TRIAD 
#### Confidentiality
- Protect personal privacy
- Maintain business advantage
- Achieve regulatory compliance(PII, PHI etc.)
To ensure, use:
- Encryption
- Access Controls
- Data masking(obscuring data)
- Physical security measures
- Training and awareness(reduce human errors)
#### Integrity
Data is accurate and unchanged.
Why critical?
- Ensure data accuracy
- Maintain trust
- Ensure system operability(if data format is altered)
To ensure, use:
- Hashing(Hash digest)
- Digital signatures
- Checksums
- Access Controls
- Regular Audits
#### Availability
Ensuring accessibility.
99.999% is the standard for uptime.
Important because:
- Ensuring business continuity
- Maintaining user trust
- Upholding an organization's reputation
To ensure, use:
- Redundancy(duplication)
	- Server Redundancy(Load balancer)
	- Data Redundancy(RAID etc.)
	- Network redundancy
	- Power redundancy(Generators, UPS etc.)
#### Non Repudiation
Can't deny any action.
Digital signatures are used to ensure non - repudiation.
Important because:
- Confirming the authenticity of Digital Transactions.
- Ensuring Integrity.
- Providing accountability.

AAA - Authentication - Authorization - Auditing
#### Authentication
Verifying individual identities.
5 authentication methods:
- Something you know(Knowledge factor)
- Something you have(Possession factor)
- Something you are(Inherence factor)
- Something you do(Action factor)
- Somewhere you are(Location factor)
2FA
MFA
Used to:
- Prevent unauthorized access.
- Protect user data and privacy
- Ensure resource validity
CIANA(Pentagon)
#### Authorization
 Right permissions for the right people.
 - Protect sensitive data - not everybody should have access to it.
 - Maintain system integrity in organization
 - Create more streamlined experiences(with only whats needed)
#### Accounting
Logging and tracking user activity.
Achieves:
- Transparency
- Security
- Accountability
Robust accounting system looks like:
1. Audit trail - Chronological record of all activity
2. Regulatory Compliance
3. Forensic analysis
4. Resource optimizations
5. User accountability.
 Performed using:
  - Syslog Servers
  - Network analyzers(wireshark etc.)
  - SIEM(realtime analysis)

Security Controls - categories and types
#### Categories
 - Technical Controls (tech/hardware/software)
	 - Firewalls
	 - Encryption processes
	 - Intrusion detection systems
 - Managerial controls (Strategic planning, governance)
	 - Risk assessments
 - Operational controls
	 - Day to day activities
	 - backup procedures
	 - account reviews
	 - user training programs
 - Physical controls
	 - Tangible real world security controls
	 - Shredding
	 - security guards
	 - CC
#### Types
- Preventive controls - before anything occurs
	- firewalls etc.
- Deterrent controls - makes it challenging for attackers
	- warning signs etc.
- Detective controls
	- Detection and notification (CCTV, IDS etc.)
- Corrective control - after the attack
	- Quarantining an infected file etc.
- Compensating controls - used when primary controls dont work
	- WAP2 along with firewall. 
	- Encryption and then VPN etc.
- Directive controls - policy
	- Behavior within organization.
	- Guiding processes.

#### ZERO TRUST - always verify
protects deperimeterized networks
"Trust nothing and Verify everything"
To create a zero trust network, we should use 2 different planes:
Control plane and Data Plane
Control plane lays out the policies and procedures.
Data planes makes sure they are properly executed.
Control plane encompasses several key elements:
- Adaptive identity
	- Realtime validation using location, behavior, device and more
- Threat scope reduction
	- Reduce user's access to unwanted stuff
- Policy-driven Access control
	- Access based on role and responsibilities
- Secured zones
	- Sensitive data only accessible to authorized people in isolated zones within the organization.
Control plane uses the following to make decision s about access:
- Policy engine
	- After identity verification, it cross references the access request with predefined policies.
- Policy Administrator
	- Used to establish and manage the access policies

Data plane consists of subject or system and the policy enforcement point
- Subject/system
	- Refers to individual or entity trying to access something
- Policy enforcement point
	- Allow of restrict access, acts as a gatekeeper

#### Gap Analysis
Difference between desired performance and current performance.
Steps:
1. Define the scope of the analysis
2. Gather data on the current state of the organization
3. Analyze the data to identify the gaps
4. Develop a plan to bridge the gap
Types:
5. Technical Gap Analysis
		Evaluate current technical infrastructure and identify weaknesses that stop it from fully utilizing the capabilities of security controls
6. Physical Gap Analysis
		Involves evaluating an organization's current business processes and identifying any areas where they fall short of the capabilities utilize cloud-based solutions.


