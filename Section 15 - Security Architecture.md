#### On-premise vs cloud
Cloud computing is delivery of services over internet, such as:
- Servers
- Storage
- Databases
- Networking
- Software analytics
- Intelligence
Responsibility matrix
- outlines division of responsibilities between cloud service provider and customer 
Third part vendors
- provide specialized services such as management tools
Hybrid solution
- combine on premise with cloud services
- Ensure
	- Sensitive data is protected
	- Regulatory requirements are met
	- Systems can communicate with each other
	- The solution is cost-effective
On-premise solution
- the biz maintains everything 
- complete control over data
Things to keep in mind when moving to a cloud based service:
- Availability
- Resilience
- Cost
- Responsiveness
- Scalability
- Ease of deployment
- Risk transference
- Patch availability
- Inability to patch
- Power
- Compute

#### Cloud security
Different vulnerabilities can include:
- Shared Physical server vulnerabilities
	- can lead to vulnerabilities if one user's data is compromised.
- Inadequate virtual environmental security
	- can lead to unauthorized access, data breaches and other incidents
- User access management
	-  Use mfa
- Lack of UpToDate security measures
- Single point of failure
	- Increase redundancy
- Weak authentication and encryption practices
- Unclear policies
	- Lack of clear guidelines
-  Data remnants
	- Residual data must be taken care of

#### Virtualization and containerization
Virtualization : Technology that emulates servers or systems
Containerization : Light weight alternative to full machine virtualization
Virtual machines
- run on hypervisors
	- Type 1 - bare metal. Runs directly on host hardware
	- Type 2 - standard os is needed - Kali on win is an example - Oracle VirtualBox
	- Type 1 is faster
Containerization
encapsulates the system in an environment suitable for it to run without worrying about dependencies.
Isolated.
Efficient, Quick.
Virtualization Vulnerabilities:
- VM escape
	- attacker is able to break out of the isolated environment
- Privilege escalation
	- gains higher level access
- Live VM migration
	- adversary in the middle attack
- Resource reuse
	- When resources are used for other tasks without first clearing details of the task it performed earlier.
Fix:
- Update OS
- Antivirus in each VM
- Strong passwords and group policies
Update hypervisors regularly.
Limit Connections between VM and physical machines
Beware of virtualization sprawl, mind the VMs being deployed.
#### Serverless
developers dont have the headache of maintaining servers
Cloud services take care of it
e.g: AWS Lambda, Google cloud functions
Less operational costs.
Automatic scaling.
Risks:
- Vendor lock-in
	- Limits to one vendor, switching is difficult

#### Microservices
collection of small autonomous services 
large apps are broken down into smaller independent services.
each runs a unique process to serve a business goal.
self contained, each service runs independently from others.
Advantages over monolithic services
- Scalability
- flexibility
- Resilience
- Faster deployment and updates
Challenges:
- Complexity
- Data management
- Network latency
- Security
#### Network infrastructure
Most important is Separation of network components:
- Physical separation - air gapping
	- Physically isolating a network
	- Most secure
- Logical separation
	- Firewalls
	- VLANS
	- Rules and policies
	- Flexible


#### Software defined network
Enables efficient network configuration to improve performance and monitoring.
Provides centralized view of the entire network.
Underlying architecture is abstract:
Data plane
- Forwarding plane
- Handles packets
- IP and ethernet are used for decision making
Control plane
- brain of the network
- Decides where traffic is sent
Application plane
- place where all apps that interact with SDN controller reside
e.g : google's B4 project

#### Infrastructure as code
Method in which IT infrastructures are defined in code files that can be versioned, tested and audited.
Idempotence.
- ability of an operation to produce same results every time.
Benefits
- Speed and efficiency
- Consistency and standardization
- Scalability
- Cost savings
- Auditability and compliance
Challenges:
- Leaning curve
- Complexity
- Security risks if not properly managed
#### Centralized vs decentralized
Centralized architecture
- all computing functions are operated from a single location
	- Server etc.
	- Efficiency and control
	- Consistency and accuracy
	- Cost and effectiveness
	- Risks
		- Single point of failure
		- Scalability issues
		- Security risks
Decentralized architecture
Computing functions are distributed across multiple systems or locations
- Resilient
- Scalable
- Flexibility
- Risks
	- Security risks
	- Management challenges
	- Data inconsistency

#### Internet of things
Network of physical items embedded with systems and network connectivity.
Key components:
Hub
- Central point
- collects, analyzes data from all connected components
Smart devices
- objects with computing capabilities and network connectivity
Wearables
- subset of smart devices
- worn on the body
Sensors
- Detect changes in environment and transform into digital data
Risks
- Weak defaults
- Poorly configured network services
#### ICS and SCADA
Industrial control systems(ICS)
- Control systems used to monitor and control industrial processes ranging from simple systems to complex systems
- Examples
	- Distributed control systems - DCS
	- Programmable Logic Controllers (PLCs)
Supervisory control and data acquisition(SCADA)
- type of ICS used to monitor and control geographically dispersed industrial processes
 Risks
- Unauthorized access
- Malware attacks
- Lack of updates
- Physical threats
Fixes
- Strong access controls
- Regular updates and system patches
- Firewall and intrusion detection systems
- Regular security audits
- Employee training
#### Embedded Systems
Real time operating systems run in embedded systems
Ensures data processing in real time
risks
- hardware failures
- Software bugs
- Security vulnerabilities
- Outdated systems
To secure:
- Network segmentation
	- Divide network into segments
- Wrappers
	- Show only entry and exit points not the data
- Firmware code control
	- Managing code that deals with low level processes
- Inability to patch(Most challenging)
	- Over the air updates must be used
