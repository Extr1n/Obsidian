---
date: 12-19-2024
tags:
  - "#CSDS/CyberSec"
  - CSDS
---
# Header 1
# Topics
## Intro To Cyber Security
- CIA
	- Confidentiality
		- Only authorized ppl can access
	- Integrity
		- Unmodified data
	- Availability
		- Doesn’t go down
- Threat Vs Vulnerability vs Asset
	- Threat is smth that causes harm
	- Vulnerability is smth that is susceptible to harm
	- Asset is smth we're trying to protect
## Cryptography
- Asymmetric vs Symmetric Encryption
	- Asymmetric
		- Public and Private Keys
	- Symmetric
		- One key to encrypt and decrypt
- Process of Encrypting / Decrypting
	- Choose encryption type (Asymmetric vs Symmetric)
	- Generate Key (PBDKF2)
	- Choose encryption function (AES, RSA)
	- Choose hash function & salt
- What is a Salt
	- Adds sprinkle of randomness to the hashing function, can be stored alongside the encrypted info
- What is Encoding? Why is it important?
	- Encoding is a way of changing the format of your outputs. Used like functional programming
- PBDKF2 vs AES
	- PBDKF2 is used to generate the key
	- AES is to encrypt the string
- Should we use ECB and DES
	- No
- What is Hashing?
	- One way encryption, ensures data is not tampered with and defends against rainbow tables
- What is a Digital Signature
	- Hashes with asymmetric encryption and signs with private key. Used to ensure people are who they say they are
## Certificates
- What is a CA and Root CA
	- Certificate Authority signs certificates, Root CA is self signed and installed in OS
- How are certificates used in TLS
	- Used to authenticate the server with CA. Meant to keep you safe when browsing the internet
- What is the Lets Encrypt service?
	- Signs certificates for free, bc anyone should be able to host websites
- What type of encryption is used for TLS
	- Asymmetric encryption is used to exchange symmetric keys for the session
- Explain TLS Handshake
	- Exchange cipher settings, SSL versions, authenticates server, exchange symmetric key for session
- Why would your browser warn you about a website / certificate error?
	- Expired Cert
	- Cert hasn’t started yet
	- Cipher settings not supported
	- Untrusted CA
	- Revoked Cert
	- Domain name doesn’t match Cert
## Network
- How can protocols be attacked? (TCP SYN)
	- Spoofing IP address to create multiple connection requests without an endpoint and exhausting server resources
- What are TCP and IP protocols?
	- TCP is a protocol for sending packets ensuring integrity. One sender, one receiver
	- IP is determining the addresses of the sender and receiver
- How are IP and Port used together?
	- IP is the address of the machine, Port is the location of a particular service / application on the machine
- Understand differences in firewalls such as Packet filter and stateful
	- Packet filter looks at the type of packet, destination, source to determine if the packet should be let through
	- Stateful firewall looks at current connection / traffic to determine if packet should be sent through. Example is closed TCP connection so no more TCP packets
- Understand scanning network basics such as nmap and who is
	- nmap -sV scanme.org, tells you the version, -sp is a ping scan
	- whois is a website that tells you who owns the certificates of a website
- Understand what DNS is and the services it provides and it can be attacked
	- Domain Name Service, converts domain names into IP addresses and vice versa
	- Can be rerouted into malicious websites when intercepting web traffic
## OS Security
- How to harden an OS and core software such as Apache and SSH
- Apache
	- Remove server versions
	- Change Error Page
	- Don’t share file directory information
- SSH
	- RBAC
	- No password logins, only people in ssh file
	- How to add people to ssh file?
		- /etc/ssh/ssh_config
		- AllowUsers user1
		- /etc/shadow -> is the password file of users
## Malware and Threats
- Viruses
	- Spreads and self replicates
- Trojan
	- Conceals a virus as something legitimate so ppl click on it
- Spyware
	- Key logger, monitor user actions
- Malware
	- Damage to system
- Phishing
	- Pretend to be someone else in order to obtain information
## Application Testing + Pen testing
- Zed attack Proxy & Burp Suite
	- Used to intercept traffic
- Automated Scanner vs Manual Scanner
	- Automated goes through set checks
	- Manual is human done, typically more creative and nuanced
- Vulnerability assessment
	- Non intrusive way to detect risks
	- Focus more on discovery and not exploitation
		- Exploitations can lead to damage and unwanted consequences
- National Vulnerability Database
	- List of major vulnerabilities in history
- What are the phases of pen testing?
	- Scope - Recon - Discovery - Exploit - Report
- Different kinds of pen testing
	- Physical, network, application, social engineering
	- Static vs Dynamic Pen Testing
		- Static is code
		- Dynamic is live application
	- White vs Black Box
		- White box is all credentials
		- Black box is no access
	- Red vs Blue Team
		- Attack red
		- Blue defend
## Software Vulnerabilities
- Buffer Overflow
	- Hearbleed
- Race Conditions
	- Threading stuff
- Input Validation
- Authentication / Authorization attacks
- Client vs Server side attacks
- XSS Scripting
- SQL / Path Injection
- Is AI Generated code trustworthy?
## OWASP Top 10
- Broken Access Control
- Cryptographic Failures
- Injection
- Insecure Design
- Security Misconfiguration
- Note what the above vulnerabilities are and how to identify them in code
## Identity and Access Management
- Multifactor Authentication, What are the different types?
- What is mutual authentication?
- Authentication vs Authorization
- Out of Band Authentication **
- Password Policy in Linux
- What is RBAC give example in Linux
## Privacy
- Different approaches to protecting privacy
- How can you be tracked
- Browser Fingerprint
- Importance of mobile privacy
## Laws & Compliance
- What is an information security policy
- HIPAA
	- Health
- GDPR
	- Europe
- FERPA
	- Education
- PCI-DSS
	- Payments
## Mobile & IoT Security
- Top Vulnerabilities
- IoT Security
	- Weak Guessable or Hardcoded Passwords
	- Insecure Network Services
	- Insecure Ecosystem Interface
		- Consider being able to update a device without authentication
	- Insecure Random Number Generators
- Mobile Security
	- Improper Credential Usage
	- Hardcoding Credentials :(
	- Inadequate Supply Chain Security
	- Using a package with malicious code
	- Insecure Authorization/Authentication
- Process of Testing a mobile apps
	- Mobile Scavenger Hunt
	- Directing traffic through burp suite as an intentional man in the middle
## Forensics
- Deleted stuff is NOT deleted
- Different forensics tools
	- Autopsy - Used to browse and find data in system
	- Foremost - Find deleted files
	- Dumpzilla - Browsing history
	- Bulk Extractor - Credit Cards, GPS, email, from an image
## Academic & Organizations
- Different ways of getting involved