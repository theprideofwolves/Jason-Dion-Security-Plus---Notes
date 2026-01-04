#### When to automate and orchestrate?
Complexity
Cost
Always do a cost benefit analysis.
Identify single points of failure while implementing automation or orchestration
Have a manual process ready incase orchestration or automation has failed
Dont accumulate technical dept - dont implement poorly - conduct regular assessments and reviews
Ongoing supportability
Automations depend on APIs and webhooks
Runbooks are automated versions of playbooks.
Runbooks include human interventions points in a automation process.
#### Benefits of Automation and Orchestration
1. Increasing efficiency and time savings
2. Enforcing baselines
3. Implementing standard infrastructure configurations
4. Scaling in a secure manner
5. Increasing employee retention
6. Increasing reaction times
7. Being a workforce multiplier

#### Automating support tickets
enhances efficiency of IT and customer service teams
Overwhelming volume can cause:
- Delays in issue resolution
- Increased workloads
- Decreased customer satisfaction scores
Automating can increase efficiency

Ticket creation
- automated generation of tickets when users or customers report issues or requests
- Follows six steps
	1. Users or customers will submit support requests through various channels
	2. An automation tool monitors and generates support tickets based on predefined criteria
	3. The automation system captures essential user submitted information
		1. Description
		2. Contact details
		3. Metadata
	4. Automation categorizes tickets based on content or source
	5. Tickets are prioritized based on predefined rules and criteria
	6. Automated notifications are sent to the relevant support team or technician
Ticket escalation
- ensures high priority issues are addressed promptly
- Follows a basic 5 step process
	1. criteria are defined based on nature of issue
	2. automation rules are created
	3. automation system starts taking actions
	4. automation will continuously monitor and track the progress of escalated tickets
	5. automation system triggers ticket closure and notifies the user or customer of the resolution
- Transparency and responsibility are crucial.
#### Automating Onboarding
crucial for scalability
- Creating documentation records
- Scheduled training 
- Provisioning equipment
- Managing access rights
- Distributing various checklists
- Collecting feedback
User and resource provisioning
User provisioning
- Create user's account
- assign the account the correct roles and access
- Send out the proper notifications and confirmations
- Conduct continuous synchronization and updates
Resource provisioning
- workstations
- software licenses
- communication tools
- Requirement analysis
- resource allocation
- configuration and customization
- verification and auditing
- gathering feedback
#### Automating Security
Guardrails
- automated safety controls to protect against insecure infrastructure configurations
Security groups
- Act as cloud-based server firewalls that control incoming and outgoing network traffic
1. Automation assigns instances to security groups with predefined rules
2. Systems adapt security groups to evolving threats
3. Automated traffic analysis ensures compliance with security settings
Service Access Management
- A crucial area to prioritize in security automation for risk reduction and operational efficiency
- Automatic access review
- Automatic monitoring of unusual activities for quick time response
- Automatic restriction of access when needed
- Automatic enabling/disabling of services for security
Managing permissions
Involves ensuring that individuals have the correct access level corresponding to designated role.
- Done using RBAC
- Manages user permissions for onboarding, transfers and departures
- Ensures protection of sensitive info
- Allows automated compliance checks and adjustments
#### Automating Application Development
to manage, test and deploy new apps or features with minimal human intervention.
CI/CD enhances efficiency, consistency and overall quality of software applications.
CI - Continuous integration
- practice in software development where developers merge code changes frequently in one place
- Release  - finalizing
- Deployment - pushing out releases
Continuous delivery 
- maintains deployable code with automation
- doesnt push automatically - allows manual control of deployment
Continuous deployment
- automates deployment after completion of build stage
Automated rollback features are essential.
#### Integrations and APIs
Integration
- Process of combining different subsystems or components
Application programming interface - API
- Set of rules and protocols that are used for building and integrating application software
APIS
- REST - Representational State Transfer
	- Architectural style that uses standard HTTP methods and status codes, uniform resource identifiers and MIME types - relies on JSON format - stateless
- SOAP - Simple Object Access Protocol
	- Protocol that defines a strict standard with a set structure for the message, usually in XML format
	- most robust
	- high security
CURL
- tool to transfer data - can be used to test api
- 