#### Incident Response Process
Act of violating a security policy.
Commonly used IRP is produced by NIST.
7 phase model for the sec+ exam:
1. Preparation
	1. Involves strengthening systems and networks to resist attacks 
2. Detection
	1. Identifies security incidents
3. Analysis
	1. Involves a thorough examination and evaluation of the incident
4. Containment
	1. Limits the incident's impact by securing data and protecting business operations.
5. Eradication
	1. Starts after containment and aims to remove malicious activity from the system or network.
6. Recovery
	1. Restores systems and services to their secure state after an incident.
7. Post-incident activity/ Lessons learned
	1. Happens after containment, eradication and full system recovery.
Root Cause Analysis takes place
- Identifies the incident's source and how to prevent it in the future.
1. Define/scope the incident
2. Determine the causal relationships that led to the incident
3. Identify an effective solution
4. Implement and track the solutions
After action Report
- Collects formalized information about what occurred.

#### Threat Hunting
Finding hidden threats
- Establish a hypothesis
	- Combine hunting with threat intelligence
- Profiling threat actors and activities
- Threat hunting is used to:
	- Seek undetected issues
	- Focus on what bypasses existing rules
	- Explore cases where queries do not yield expected data
To keep themselves UpToDate, hunters focus on:
- Advisories and bulletins
- Intelligence fusion
- Threat data

#### Root Cause Analysis
Systematic process to identify the initial source of the incident and how to prevent it from occurring again.
- Define the scope 
- Determine causal relationships
- Identify an effective solution
- Implement and track the solution
No-blame approach


#### Incident Response Training and Testing
Training
- Ensure staff understands IRP
- End user training is important.
Testing
- Tabletop exercises
- Penetration test
- Simulation
They help in
-Identifying gaps in incident response plan
-Improving coordination between teams
-Ensuring roles for all during real incidents
#### Digital Forensic Procedures
- Process of investigating and analyzing digital devices and data to uncover evidence for legal purposes
- 4 main stages
	- Identification
		- Ensures safety of the scene, secures it to prevent any evidence contamination, and determines the scope of the evidence to be collected.
	- Collection
		- Refers to the process of gathering, preserving and documenting physical or digital evidence in various fields.
		- Follow proper acquisition procedures, order of volatility and chain of custody
			- Order of volatility
				- Dictates the sequence in which data sources should be collected and preserved based on their susceptibility to modification or loss.
					- NIST says
						- Collect system's memory data
						- Collect system state data
						- Collect storage device data
						- Capture network traffic and logs data
						- Collect remotely stored or archived data
			- Chain of custody
				- Documented and verifiable record that tracks the handling, transfer and preservation of digital evidence from the moment it is collected until it is presented in a court of law.
		- When collecting use one of the following 2 methods:
			- Disk imaging
				- bit by bit copy of storage device
				- includes deleted files and unallocated space
			- File carving
				- extracts files and data fragments from storage media without relying on the file system
	- Analysis
		- Systematically scrutinizing data
	- Reporting
		- Documenting findings, processes and methodologies used.
Legal hold
- Formal notification that instructs employees to preserve all potentially relevant electronic data, documents and records 
Preservation methods include:
- Making backup copies
- Isolating critical systems
- Implementing access controls
Electronic Discovery
- Process of identifying, collecting, and producing electronically stored information during potential legal proceedings
Must adhere to a code of ethics
- Avoiding bias
- Repeatable actions
- Preservation of evidence

#### Data Collection Principles
Always follow order of volatility
Review licensing and documentation of all systems
Data acquisition
- method of creating a forensically sound copy of data
- BYOD complicates this as privacy can be violated
Order of volatility
- CPU registers and cache memory
- RAM, routing tables, ARP caches, process table, temporary swap files
- HDD/SSD/Flash drive
- Remote logging and monitoring data
- Physical config and network topology
- Archival media
Some window registry keys require memory dump.

#### Disk Imaging and Analysis


