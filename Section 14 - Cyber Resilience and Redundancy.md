#### High Availability
Service is continuously available, low downtime
Uptime is the time a system remains online, expressed as a percentage.
Gold standard is 99.999% uptime.
Load balancing
- Distributing work on different systems
Clustering
- uses multiple computers, storage devices and redundant network connections
- work together as a single system
- provides high availability, reliability and scalability
- No single point of failure
- Continuity is maintained
- Can be combined with load balancing
Redundancy
- Duplication of resources
- to increase uptime.
- Having backup resources incase one fails

#### Data Redundancy
Effective way is to use RAIDs - Redundant array of independent disks.
combines multiple physical storage devices.
RAID 0 - striping - no fault tolerance - high performance
RAID 1- Mirrors data for redundancy in different drives - no downtime
RAID 5 - striping with 1 parity - atleast 3 storage devices - can hotswap with new one if old one fails
RAID 6 - 2 parity pieces - no downtime - resilient
RAID 10 - RAID 1 and RAID 0 combined - striped arrays of mirrored arrays
Categorization of RAIDS:
- Failure resistant
	- Redundant storage devices
	- RAID 1 and !)
	- even supports hardware malfunctions
- Fault tolerant
	- RAID 1,5,6 and 10 for uninterrupted operation during hardware failures
	- no downtime  -  resilient
- Disaster tolerant
	- Broad level of protection during catastrophic events
	- RAID 1 and RAID 10

#### Configuring a RAID


#### Capacity Planning
Strategic planning to meet future demands cost-effectively
People
- involves analyzing skills and comparing to future needs
Technology
- Assess current resources, utilization and gaps
Infrastructure
- Physical space and utilities to support operations
Process
- aims to optimize business processes to handle demand fluctuations by enhancing workflows, processes etc.



#### Powering Data Centers
Surge
- Small and unexpected increase in supplied power
Spike
- Short transient voltage caused by short circuit, tripped circuit breaker, a power outage or a lightning strike.
Sag
- small and unexpected decrease in voltage that is being provided 
Undervoltage event
- voltage is reduced for longer period of time
Power loss event
- total loss of power
- When power is restored, a power spike can also be caused.
How to protect:
Line conditioners
- Used to overcome any minor fluctuations in the power being received by the given system
- manages undervoltage and overvoltage and brings it to standard level
- not helpful during significant undervoltage or complete powerloss
UPS
- Provides emergency power when main power fails
- 15-60 minutes of power
Generator
- converts mechanical energy into electrical energy
- Takes over power supply for extended periods of time
- Types:
	- Portable gas-engine
		- Least expensive
		- small and portable
		- high maintenance
		- Small areas
	- Permanently installed
		- Rely on fossil fuels
		- Provide power for days
	- Battery-inverter
		- Quiet and less maintenance
		- Bridging the gap until other power source is online
	- Power Distribution Centre(PDC)
		- Central hub to receive and distribute power to systems in data centers

#### Data backups
Never keep all data on a single device or server
Backup
- process of creating duplicates
Onsite backup
- Using a hdd near your work environment 
Offsite backup
- Away from primary data source to overcome physical disasters
Frequency of backups
- Depends on org's Recovery point objective - RPO
- Depends on how often data is changed in org.
Encryption of backups
- Protect from unauthorized access
- Data at rest encryption
- Data in transit encryption
Snapshots
- Point in time copies of data
- Captures at a consistent state
- Used for rollbacks
Recovery
- Regaining access to data after a data loss or system failure
	- Steps:
		- Selection of backup
		- Initiating the recovery process
		- Data validation
		- Testing and validation
		- Documentation and reporting
		- Notification
Replication
- Near real time or real time copies of data
Journaling
- Recording each change to data

#### Continuity of Operations Plan
COOP has BCP and DRP
Business continuity plan - BCP
- responses to disruptive events
- involves preventive actions, recovery steps not limited to technical disruptions
Disaster recovery plan - DRP
- Subset of BCP
- focuses on how to resume operations swiftly after a disaster
- may include cloud based solutions
For a good BCP:
- Define the scope of the BCP/DRP to prevent scope creep
- Consider the org's risk appetite and tolerance
- Structure BCP/DRP by biz function or geographical area

#### Redundant Site Considerations
backup facility.
Hos site
- Fully equipped backup facility
- No downtime
- Expensive
- has One of everything
- Easier with cloud services
- only used for mission critical functions
Warm site
- partially equipped w backups
- Has power, phones, network connectivity
- Cheaper
- Has moderate response time
Cold site
- Cheaper
- No immediate backup
- Empty building etc.
Mobile site
- Can be hot/cold or warm site
- Depends on how you configure it
- Portable units - trailers or tents
- Self sufficient
Network redundancy options:
- Microwave link
- Local cable connection
- Cellular modem
Virtual site
- cloud based environment is utilized.
- can be hot, warm or cold.
- Scalable, cost effective and easy to maintain
Platform diversity
- vital aspect in redundant site design that uses different platforms to prevent single points of failure in disaster recovery
- Reliable


#### Resilience and Recovery Testing
Resilience testing
- assess the system's capacity to endure and adjust to disruptive occurrences
Recovery testing
- Evaluates system's ability to return to regular functioning following a disruptive incident
Tabletop exercises
- simulated discussion to improve crisis readiness without deploying resources
- team building
Failover test
- controlled experiment
- designed to check transition to a backup
- Needs more resources and time to conduct this
Simulation
- Computer generated representations of real world scenarios
Parallel processing
- Replicate data and processes onto a secondary system, running both in parallel
- checking reliability and stability of secondary setup
- Should make sure there is no disruption.