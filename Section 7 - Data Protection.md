#### Data Classifications
Category based on value of the data.
- Sensitive Data
	- Data with personal identifiers.
Overclassifying isn't efficient.
Classify properly.
There are 4 classification schemes based on whether you are a COMMERCIAL BUSINESS or a GOVERNMENT.
 - Commercial Business
	 - Public
		 - No impact if released
	 - Sensitive
		 - Minimal impact if released
	 - Private
		 - Contains data that should only be used internally.
	 - Confidential
		 - Trade secrets, source codes etc.
- Government
	- Unclassified
		- Can be released to public
	- Secret
		- Could damage security
	- Sensitive but unclassified
		- No impact, but can impact those whose info is being released
	- Top secret
		- National security if threatened
	- Confidential
		- Serious effects
Data lifecycle
- Collect
- Retain
- Dispose
#### Data ownership
Process of identifying who's responsible for CIA and stuff.
Types of owners:
- Data owner
	- Ultimate responsibility - the senior executive - responsible for CIA
- Data Controller
	- Responsible for storage and management,
- Data processor
	- Hired by data controller.
	- Helps with storing and management
- Data custodian
	- Handling the storage systems.
	- Sys admins
- Data steward
	- Quality of data and associated metadata.
	- Labeling.
- Data privacy officer
	- Responsible for managing PII, PHI etc.
IT people should never be data owners.
#### Data states
- Data at rest
	- Stored.
	- Prime targets
	- Use encryption
		- Full disk encryption
			- Encrypts entire hard drive
			- System off - encrypted
			- System on - decrypted
		- Partition encryption
			- Encrypts specific partitions
		- File encryption
			- Encrypt individual file
		- Volume encryption
			- Set of selected files or directories
		- Database encryption
			- Encrypt column, row or tables
		- Record encryption
			- Encrypt specific fields within a database record
- Data in transit
	- Actively moving
	- Encyrptions used:
		- SSL/TLS
			- Cryptographic protocols to provide secure communication over a computer network
		- VPN
			- Create secure connections
		- IPSec
			- Protocol suite for authenticating and encrypting each IP packet in the data stream.
- Data in use
	- Actively being processed
	- Should be decrypted to be processed at different levels such as:
		- Application level
		- Access controls
		- Secure enclaves(isolated)
		- Intel software guards in memory.
#### Data types
- Regulated Data
	- Info controlled by laws, regulations or industry standards
	- Must comply to GDPR, HIPAA etc.
	- PHI, PII
- Trade secrets
	- Confidential business info
- Intellectual property
	- Creations of the mind
	- Artistic works etc.
- Legal information
	- Data related to legal proceedings, contracts, or regulatory compliance
- Financial information
	- Info regarding financial transactions, such as sales records, invoices, tax documents and bank statements.
- Human-readable vs Non human readable data
	- Text docs or spreadsheets.
#### Data sovereignty

Information is subject to laws of the nation in which it is located.
Geolocation has a lot of impact on businesses.

#### Securing Data
 - Geographic restrictions
	 - setting up virtual boundaries to restrict access based on location
 - Encryption
	 - Plaintext to ciphertext
 - Hashing
	 - Convert into fixed length of numbers of alphabets
 - Masking
	 - Partial obfuscation
 - Tokenization
	 - Replaces sensitive with non-sensitive
	 - Used in credit cards
 - Obfuscation
	 - Making data unclear
 - Segmentation
	 - Dividing network
 - Permission restrictions
	 - Define who has access to what
#### Data loss prevention
Used to monitor data in use, transit and at rest.
Limits amount of data that can be stolen
Software
- Endpoint DLP system
	- Installed on a system to monitor and alert any modifications to data thats in use in that system
-  Network DLP system
	- Software or hardware placed at the perimeter to detect data in transit
- Storage DLP
	- Installed in server
	- Protects data at rest
- Cloudbased DLP system.
	- SAAS. Part of the cloud service

#### Configuring a DLP
