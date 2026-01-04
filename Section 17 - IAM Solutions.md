#### Identity and Access Management
Identification
- identifying if a user is legitimate
Authentication
- Verifying the ID
Authorization
 - after authenticating, giving the right person the right access
 Accounting
 - Logging everything
 Provisioning
 - Creating new user accounts and giving the right permissions
 Deprovisioning
 - Remove access when user no longer needs them
 Identity proofing
 - verifying identity of user before creating the account
 Interoperability
 - ability to work together and share information between different systems
 Attestation
 - validating access and everything else is correct
 
#### Multifactor Authentication
Security system that needs more than one method mode of authentication.
types
- Knowledge based - something you know
- possession based - something you have
- inherence based - something you are
- behavior based - something you do
- location based - somewhere you are
Single Factor authentication
Two factor authentication(combines 2 types of authentication)
Multi factor authentication(combines 2 or more)
The more the safer.
Passkeys are gold. They combine user id and passwords with fingerprints or face id. Very secure

#### Password Security
Measure of effectiveness of a password.
length : 12-16 characters
the more the better
Password complexity: mix uppercase, lowercase, numbers, special characters.
Shouldn't commit the crime of password reuse.
Change periodically
To reuse a password, they should change a certain number of passwords, the system remembers a set of old passwords and doesn't let the user set the recent ones just yet.
password expiration is also important.

Password managers are great tools.
Key features:
- Password generation
- Autofill
- Secure sharing
- Cross-platform access
Password-less authentication
- improved security
- user friendly
- biometrics, hardware tokens, otps, magic links, passkeys

#### Password attacks
Brute force attacks
- trying every possible combination
- time consuming
- needs alot of resources
Dictionary attack
- using a list with commonly used passwords
Password spraying
- a form of brute force attack that involves trying a small number of commonly used passwords against a large number of usernames or accounts
Hybrid attacks
- combines brute force and dictionary
- if format is knows, one can use this.
#### Single sign-on
auth process that allows a user to access multiple applications or websites by logging in only once with a single set of creds.
works based on trust between application and identity provider
Identity provider
- creates, maintains and manages id info.
- provides authentication services to relying applications within a federation or a distributed network
Step by step process:
- User logs in to idP
- User tries to log in to another app that uses the idp for auth purposes
- this new app sends your info to the idp, since u r already registered, the idp sends a token to you and the token is sent to the app and access is given to you
benefits
- improved user experience
- increased productivity
- reduced info tech support costs
- enhanced security
Protocols that enable single sign on are:
LDAP - Lightweight directory access protocol
- used to access and maintain distributed directory info services over an IP network
- LDAPS uses SSL/TLS
OAuth
- token based authentication and authorization
- allows user's info to be used by 3rd part services without exposing password
- common in restful apis
- Uses JSON to transfer data
SAML - Security Assertion Markup Language
- standard for logging users into applications based on their sessions in another context
- allows services to separate from IDPs and removes the need for direct user authentication

#### Federation
Process that allows for the linking of electronic IDs and attributes to store info across multiple distinct ID management systems.
Uses trust between diff systems.
Step by step take at how a federation works:
- Login initiation
- Redirection to an IDP
- Authenticating the user
- Generation of an assertion
- Returning to a service provider
- Verification and access
Benefits:
- Simplified user experience
- Reduced administrative overhead
- Increased security

#### Privileged Access Management

- restricts and monitors privileged access within an IT environment.
- key components
	- Just in time permission
		- giving high access only when needed and revoking them later
	- Password vaulting
		- stores critical creds 
	- Temporal accounts
		- temporary accounts that will be automatically deleted after the job is done.

#### Access Control Models
Mandatory Access Control
- uses labels and gives access
Discretionary Access Control
- the owner determines who has access
Role-based Access Control
- roles are assigned
- and roles are granted access
- enforces minimum privileges
Rule-Based Access Control
- enables admins to apply security policies to all users
Attribute-based Access Control
- uses object characteristics for access control decisions
- User attributes
	- user's name, role, org, ID or security clearance level
- Environment attributes
	- time of access, data location and current org's threat level
- Resource attributes
	- file creation date, resource owner, file name, and data sensitivity
Time of day restrictions
- Can limit access during a certain time
Principle of least privilege
- user is given the minimum access needed to finish their job.
Permission or authorization creep
- occurs when a user gains excessive rights during their career progression in the company.
#### Assigning Permissions
Administrator and User accounts
Local accounts
Microsoft accounts
Principle of least privilege
UAC - User account control
- mechanism designed to ensure that actions requiring administrative rights are explicitly authorized by the user.
