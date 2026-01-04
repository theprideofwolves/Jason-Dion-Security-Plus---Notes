#### Changing default configurations
Default configs are designed to make it easy for the user to use the application or service, such as:
- Default passwords
- Unneeded ports and protocols
- Extra open ports
- Change protocols to their secure counterparts
	- HTTP to HTTPS etc.

#### Restricting applications
Practice least functionality
- restrict or uninstall unnecessary applications
Use configuration management tools to manage installed apps on the device.
Secure baseline image
- Standardized workstation image, including OS, essential applications and strict policies in corporate networks
Allowlisting
- only apps on the list are allowed to run
- application level ACL
- secure but complex to manage
Blocklisting
- apps on this list are not allowed to run
- Easy and less secure

#### Unnecessary Services
Services are bg apps that operate within OS executing a range of tasks.
Disable malicious or unnecessary services.

#### Trusted Operating Systems
Designed to provide a secure computing env by enforcing stringent security policies that usually rely on mandatory access controls.
Evaluation Assurance Level 6 designated to certain OSs.
- Mandatory access control
- Security auditing
- Role based Access control
Trusted OS minimize trust base by utilizing micro kernels, attack surface is reduced
Balance sec requirements with:
- Usability
- Performance
- Functional Requirements
EAL 4:
- carefully designed, tested and reviewed offering good security assurance.

#### Updates and Patches
Bugs are fixed using updates and patches.
Patch management ways:
- Manual
- Automated
Types of patches
- Hotfixes
- Updates
- Service packs
Service Pack
- Includes all the hotfixes and updates since the release of the operating systems
Effective patch management system looks like:
- Assign a dedicated team to track vendor security patches
- Establish automated system-wide patching for OS and apps
- Include cloud resources in the patch management
- Categorize patches as urgent, important, or non-critical for prioritization.
- Create a test environment to verify critical patches before production deployment
- Maintain comprehensive patching logs for program evaluation and monitoring
- Establish a process for evaluating, testing, and deploying firmware updates
- Develop a technical process for deploying approved urgent patches to production
- Periodically assess non-critical patches for combined rollout

#### Patch management
Planning, testing, implementing, and auditing of software patches. 
Security fixes
Functionality updates
Planning
- Creating policies, procedures, and systems to track and verify patch compatibility.
Testing
- Test before deploying in your entire network
Implementation
- Manual or automated depending on the size of the network
Patch rings are also used. Limiting number of machines while rolling out updates to reassure and reverify the updates in live environments.

#### Group policies
Baselining
- Process of measuring changes in the network, hardware or software environment.

#### SELinux - Security enhanced Linux
Additional layer of security in linux distros
They come with Mandatory access control
Context based permissions
- Permission schemes that are defined by various properties for a given file or process.
	- SELinux
	- AppArmor
- Different from DAC where owner controls anything
SELinux enforces MAC on processes and resources and enables information to be classified and protected.
Contexts defined by SELinux:
- USER
	- defines what users can access
		- Unconfined_u(All users)
		- User_u(Unprivileged users)
		- Sysdmin_u(System administrators)
		- Root(Root user)
- ROLE
	- defines what roles can access a given object
		- object_r applies to files and directories
- TYPE
	- groups objects together that have similar security requirements or characteristics
- LEVEL(Optional)
	- Used to describe the sensitivity level of a given file, directory or process
Three modes of SELinux:
- Disabled
	- SELinux is essentially turned off, and so MAC is not going to be implemented
- Enforcing
	- All the SELinux security poilicies are being enforced.
- Permissive
	- SELinux is enabled, but the security policies are not enforced.
Two types of policies are used by SELinux:
- Targeted
	- Default
	- targeted policies are run in a confined domain
	- Untargeted policies run in unconfined domains
- Strict
	- Enforces MAC on everything
	- Complicated to setup
Violations are recorded as logs.

SELinux is only as strong as the restricted profiles being created
#### Data Encryption
Process of converting data into a secret code to prevent unauthorized access
File disk encryption
- encrypts entire hard drive
	- Bitlocker, filevault etc.
Partition encryption
- only a partition is encrypted
	- Veracrypt etc.
File encryption
- individual files are encrypted
	- GNU Privacy guard - GPG - Provides cryptographic privacy and authentication for data communication.
Volume encryption
- Creates an encrypted container that of a set space on the storage medium, it can house various files and folders.
	- Veracrypt etc.
Database encryption
- secures entire database, extending to multiple storage devices or cloud storage, similar to full disk encryption.
- SQL Server Transparent Data encryption(TDE)
	- Auto encrypts the entire database without needing application changes, as the system handles encryption and decryption
Record encryption
- encrypts individual rows in a database
- flexible

#### Secure Baselines
Standard set of configs and controls that guarantee minimum security.
- Establish a secure baseline
	- thorough assessment of system is required
	- Monitor and validate group policies
- Deploy secure baselines across all of the org's digital assets
	- Configuring firewalls
	- Setting user permissions
	- implementing encryption protocols
	- Ensuring up-to-date antivirus and antimalware solutions across all devices
Always compare with known good config.
- Maintain all the secure baseline on all assets
Training and awareness.

