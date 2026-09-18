# Final Exam: Ethical Hacker Course

> Note: Four "match the term" questions in the original source (PCI SSC key terms, API documentation resources, programming language data structures, and Kali nmap commands) had headers but no actual answer pairs included in the scraped content, so they were omitted here rather than guessed. One exhibit-based question (Reflected XSS color order) also had no answer key text and could not be resolved without seeing the image — it's included below but flagged as unverified.

## Q1
**Question:** Which are two best practices used to secure APIs? (Choose two.)
**Type:** multi
**Options:**
- Use reputable and standard libraries to create the APIs
- Make internal API documentation mandatory
- Keep API implementation and API security into one tier allowing the API developer to work on both facets simultaneously
- Secure API services to provide HTTP endpoints only
- Discussing company API development (or any other application development) on public forums
**Answer:** Use reputable and standard libraries to create the APIs; Make internal API documentation mandatory
**Explanation:** Best practices for securing APIs include using HTTPS-only endpoints with strong TLS, validating/sanitizing input, using reputable libraries, segmenting API implementation and security into distinct tiers, requiring internal documentation, and avoiding public discussion of API development.

## Q2
**Question:** Which type of threat actors use cybercrime attacks to promote what they believe in?
**Type:** single
**Options:**
- Hacktivists
- Organized crime
- State-sponsored
- Insider threats
**Answer:** Hacktivists
**Explanation:** Hacktivists aren't money-motivated; they use cybercrime to make a point or promote a belief, often by stealing and publicly revealing sensitive data.

## Q3
**Question:** A company conducted a penetration test 6 months ago. However, they have acquired new firewalls and servers to strengthen the network and increase capacity. Why would an administrator request a new penetration test?
**Type:** single
**Options:**
- The core data has been moved to the cloud infrastructure.
- The servers require independent performance evaluation.
- New cloud-based applications have been implemented.
- The attack surface has changed with the new equipment added.
**Answer:** The attack surface has changed with the new equipment added.
**Explanation:** As networks and systems change, the attack surface changes too, requiring periodic reevaluation of security posture through a new penetration test.

## Q4
**Question:** A network administrator performs a penetration test for a company that sells computer parts through an online storefront. The first step is to discover who owns the domain name that the company is using. Which penetration testing tool can be used to do this?
**Type:** single
**Options:**
- Exif
- Maltego
- h8mail
- WHOIS
**Answer:** WHOIS
**Explanation:** The whois command gathers domain ownership information from public records.

## Q5
**Question:** A penetration tester wants to quickly discover all the live hosts on the 192.168.0.0/24 network. Which command can do the ping sweep using the nmap tool?
**Type:** single
**Options:**
- nmap -p 1-65535 localhost
- nmap -sP 192.168.0.0/24
- nmap -sn 192.168.0.0/24
- nmap 192.168.1.0/24 -open
- nmap -sV 192.168.0.255
**Answer:** nmap -sn 192.168.0.0/24
**Explanation:** `nmap -sn` performs a ping sweep (host discovery scan) across the specified subnet to determine which devices are live.

## Q6
**Question:** A penetration tester runs the command `nmap -sF -p 80 192.168.1.1` against a Windows host and receives a response RST packet. What conclusion can be drawn on the status of port 80?
**Type:** single
**Options:**
- Port 80 is open
- Port 80 is closed
- Undetermined as this is a default response on a Windows system
- Port 80 is open/filtered
**Answer:** Undetermined as this is a default response on a Windows system
**Explanation:** A TCP FIN scan isn't reliable against Windows hosts, since Windows responds with an RST packet regardless of the actual port state.

## Q7
**Question:** Which common tool is used by penetration testers to craft packets?
**Type:** single
**Options:**
- nmap
- scapy
- pip3
- h8mail
- Recon-ng
**Answer:** scapy
**Explanation:** Scapy is a comprehensive Python-based framework for packet generation and manipulation, typically run with root permissions.

## Q8
**Question:** Why should a tester use query throttling techniques when running an authorized penetration test on a live network?
**Type:** single
**Options:**
- To reduce the number of attack threads that are being sent to the target at the same time
- To limit bandwidth on real-time antivirus and malware scanners
- To create a larger attack surface on the target
- To limit bandwidth on resource heavy applications
**Answer:** To reduce the number of attack threads that are being sent to the target at the same time
**Explanation:** Query throttling slows down scanner traffic — often by reducing simultaneous attack threads — to work around bandwidth limitations during vulnerability scanning.

## Q9
**Question:** Why would an organization hire a red team?
**Type:** single
**Options:**
- To evaluate the work of the security team of the organization
- To install equipment to protect against physical intrusion
- To defend the organization against cybersecurity threats
- To play the role of a threat actor by exposing vulnerabilities regarding technology
**Answer:** To play the role of a threat actor by exposing vulnerabilities regarding technology
**Explanation:** A red team mimics a real threat actor, exposing vulnerabilities and risks across technology, people, and physical security.

## Q10
**Question:** Match the healthcare sector term to the respective description.
**Type:** matching
**Pairs:**
- Healthcare provider -> A person or an organization that provides patient or medical services
- Health plan -> A government program that pays for healthcare
- Business associates -> A person or organization that performs certain functions involving the use of PHI on behalf of, or provides services to, a covered entity
- Healthcare clearinghouse -> An entity that processes nonstandard health information it receives from another entity into a standard format
**Explanation:** HIPAA defines these distinct healthcare sector roles for regulatory and compliance purposes.

## Q11
**Question:** Which two elements are typically on the front of a credit card? (Choose two.)
**Type:** multi
**Options:**
- Magnetic stripe
- Embedded microchip
- Date of birth
- Primary account number
- Card security code
**Answer:** Embedded microchip; Primary account number
**Explanation:** The front of a card typically shows the embedded microchip, PAN, expiration date, and cardholder name. The magnetic stripe and CAV2/CID/CVC2/CVV2 security codes are on the back.

## Q12
**Question:** What can be used to document the testing timeline in a rules of engagement document?
**Type:** single
**Options:**
- Gantt charts and work breakdown structures
- OWASP ZAP
- Recon-ng
- Burp Suite
**Answer:** Gantt charts and work breakdown structures
**Explanation:** Gantt charts and work breakdown structures (WBS) document and demonstrate the testing timeline within a rules of engagement document.

## Q13
**Question:** A cybersecurity firm has been hired by an organization to perform penetration tests. The tests require a secure method of transferring data over a network. Which two protocols could be used to accomplish this task? (Choose two.)
**Type:** multi
**Options:**
- SCP
- HTTPS
- SFTP
- PGP
- S/MIME
**Answer:** SCP; SFTP
**Explanation:** SCP and SFTP securely transfer files over a network. PGP and S/MIME are for encrypted email, and HTTPS secures browser-to-server communication.

## Q14
**Question:** Match penetration testing methodology and standard with the respective description.
**Type:** matching
**Pairs:**
- OWASP WSTG -> This is a compilation of high-level phases of web application security testing and digs deeper into the testing methods used. This is primarily used by penetration testers from the web application security testing perspective.
- OSSTMM -> This is a peer-reviewed security testing methodology maintained by the Institute for Security and Open Methodologies (ISECOM). It is an open security research community providing original resources, tools, and certifications in the security field. It uses a document that lays out repeatable and consistent security testing.
- MITRE ATT&CK -> This is a resource for learning about the tactics of an adversary, techniques, and procedures (TTPs). This framework is a collection of different matrices of tactics, techniques, and sub-techniques used by penetration testers for both offensive and defensive purposes.
- NIST -> This is a document created to provide organizations with guidelines on planning and conducting information security testing. It is considered an industry standard for penetration testing guidance and is called out in many other industry standards and documents.
**Explanation:** Each methodology or standard addresses a different aspect of penetration testing guidance, from web app testing specifics to broad TTP cataloging to general testing planning.

## Q15
**Question:** Which three practices are commonly adopted when setting up a penetration testing lab environment? (Choose three.)
**Type:** multi
**Options:**
- Use a honeypot for all tests run from the physical attack platforms
- Create the penetration testing environment using virtual machines and virtual switches
- Create the penetration testing environment using physical equipment and switches in order to route the packets freely
- Ensure that when something crashes, it can be determined how and why it happened
- Use an open environment to allow for free passage of attack packets to the target machines
- Use a closed environment for all testing purposes
**Answer:** Create the penetration testing environment using virtual machines and virtual switches; Ensure that when something crashes, it can be determined how and why it happened; Use a closed environment for all testing purposes
**Explanation:** Penetration test lab requirements include a closed network, a virtualized environment for easy deployment/recovery, health monitoring for crash diagnosis, sufficient hardware resources, multiple operating systems, duplicate tools, and practice targets.

## Q16
**Question:** An organization wants to test its vulnerability to an employee with network privileges accessing the network maliciously. Which type of penetration test should be used to test this vulnerability?
**Type:** single
**Options:**
- Blue-box
- White-box
- Gray-box
- Black-box
**Answer:** Gray-box
**Explanation:** Gray-box testing runs from within the internal network in a partially known environment, simulating an insider or a compromise that has already reached a client machine, then pivoting to assess impact.

## Q17
**Question:** A penetration is being prepared to run the EternalBlue exploit using Metasploit against a target with an IP address of 10.0.0.1/8 from the source PC with an IP address of 10.0.0.111/8. What two commands must be entered before the exploit command can be run? (Choose two.)
**Type:** multi
**Options:**
- set RHOST 10.0.0.1
- set LHOST 10.0.0.1
- set TARGET 10.0.0.111
- set RHOST 10.0.0.111
- set LHOST 10.0.0.111
- set TARGET 10.0.0.1
**Answer:** set RHOST 10.0.0.1; set LHOST 10.0.0.111
**Explanation:** RHOST is set to the target's IP (10.0.0.1) and LHOST to the source/attacker's IP (10.0.0.111) before running the exploit.

## Q18
**Question:** A penetration tester runs the Nmap NSE script `nmap –script smtp-open-relay.nse 10.0.0.1` command on a Kali Linux PC. What is the purpose of running this script?
**Type:** single
**Options:**
- To compromise any snmp community strings on the target PC
- To check open relay configurations on the target server
- To compromise any open relays on the target server
- To check whether the smtp authentication is compromised on the target server
**Answer:** To check open relay configurations on the target server
**Explanation:** This NSE script tests whether the target's SMTP server is configured as an open relay (accepting and relaying mail from any user).

## Q19
**Question:** What is the penetration tester trying to achieve by running this exploit (FTP anonymous login check via `use auxiliary/scanner/ftp/anonymous`)?
**Type:** single
**Options:**
- To launch 220 packets of fragmented data to the FTP port on the target system
- To check if the target system will allow FTP anonymous login
- To enumerate FTP login on the target system
- To compromise the target system for a remote session
**Answer:** To check if the target system will allow FTP anonymous login
**Explanation:** The Metasploit auxiliary/scanner/ftp/anonymous module checks whether the target FTP server permits anonymous login.

## Q20
**Question:** A penetration tester deploys a rogue AP in the target wireless infrastructure. What is the first step that has to be taken to force wireless clients to connect to the rogue AP?
**Type:** single
**Options:**
- Send out false DNS beacons
- Spoof the MAC address of the rogue AP
- Set the PSK key to match the clients
- Send de-authentication frames to the clients
**Answer:** Send de-authentication frames to the clients
**Explanation:** Sending deauthentication frames disconnects clients from the legitimate AP, prompting them to reassociate — potentially with the rogue AP instead.

## Q21
**Question:** A cybersecurity student is learning about the Social-Engineer Toolkit (SET). Which two social engineering attacks can be launched using SET? (Choose two.)
**Type:** multi
**Options:**
- Google phishing
- Infectious media generator
- Create a payload and listener
- Simple hijacker
- Fake flash update
**Answer:** Infectious media generator; Create a payload and listener
**Explanation:** SET can launch attacks like infectious media generators and payload/listener creation. Google phishing, simple hijacker, and fake flash update are BeEF attacks, not SET.

## Q22
**Question:** A threat actor spoofed the phone number of the director of HR and called the IT help desk with a login problem. The threat actor claims to be the director and wants the help desk to change the password. What method of influence is this cybercriminal using?
**Type:** single
**Options:**
- Social proof
- Fear
- Authority
- Scarcity
**Answer:** Authority
**Explanation:** The attacker exploits the principle that people tend to comply with those in positions of authority — here, impersonating a company director.

## Q23
**Question:** Which statement correctly describes a type of physical social engineering attack?
**Type:** single
**Options:**
- Tailgating and piggybacking attacks can only be defeated through the use of control vestibules in conjunction with multifactor authentication.
- Social engineering techniques, software, and hardware can perform badge cloning attacks.
- Shoulder surfing attacks are performed only by a short distance between the threat actor and the victim.
- Dumpster phishing refers to a threat actor who scavenges for victims' private information in garbage and recycling containers.
**Answer:** Social engineering techniques, software, and hardware can perform badge cloning attacks.
**Explanation:** Badge cloning can use specialized software, hardware, and social engineering together. Piggybacking/tailgating can also be mitigated by turnstiles, double doors, or guards (not vestibules alone); shoulder surfing can occur from a distance with binoculars; and the garbage-scavenging attack is called dumpster diving, not dumpster phishing.

## Q24
**Question:** What is a characteristic of a pharming attack?
**Type:** single
**Options:**
- A type of attack in which a social engineer impersonates another person to have physical access to systems in an organization
- A threat actor redirects a victim from a valid website to a malicious legitimate looking site
- A social engineering attack carried out in a phone conversation
- A type of attack where the threat actor obtains confidential data of the victim using binoculars or even a telescope
**Answer:** A threat actor redirects a victim from a valid website to a malicious legitimate looking site
**Explanation:** Pharming redirects a victim from a valid site/resource to a malicious one designed to look legitimate, in order to extract information or install malware.

## Q25
**Question:** What kind of social engineering attack can be prevented by developing policies such as updating anti-malware applications regularly and using secure virtual browsers with little connectivity to the rest of the system and the rest of the network?
**Type:** single
**Options:**
- Watering hole
- SMS phishing
- Vishing
- Tailgating
**Answer:** Watering hole
**Explanation:** Since watering hole attacks target websites frequented by victims, regularly updated anti-malware and isolated/secure virtual browsing helps mitigate the risk.

## Q26
**Question:** An attacker enters the string `'John' or '1=1'` on a web form that is connected to a back-end SQL server causing the server to display all records in the database table. Which type of SQL injection attack was used in this scenario?
**Type:** single
**Options:**
- Inferential SQL injection
- Error-based SQL injection
- Boolean SQL injection
- Out-of-band SQL injection
**Answer:** Boolean SQL injection
**Explanation:** Since `'1=1'` always evaluates true, this Boolean condition causes the database to return all records.

## Q27
**Question:** What are two examples of immutable queries that should be used as mitigation for SQL injection vulnerabilities? (Choose two.)
**Type:** multi
**Options:**
- Time-delay queries
- Parameterized queries
- Static queries
- Stacked queries
- In-band queries
**Answer:** Parameterized queries; Static queries
**Explanation:** Immutable queries — static queries, parameterized queries, and non-dynamic stored procedures — best mitigate SQL injection vulnerabilities.

## Q28
**Question:** An attacker enters the string `192.168.78.6;cat /etc/httpd/httpd.conf` on a web application hosted on a Linux server. Which type of attack occurred?
**Type:** single
**Options:**
- SQL injection
- Session hijacking
- Command injection
- Redirect attack
**Answer:** Command injection
**Explanation:** Command injection attempts to execute OS commands the attacker shouldn't be able to run — here, viewing the httpd configuration file.

## Q29
**Question:** Which two misconfigured cloud authentication methods could leverage a cloud asset? (Choose two.)
**Type:** multi
**Options:**
- Biometric authentication
- Identity and access management (IAM) implementations
- Local authentication
- Federated authentication
- Intelligent Platform Management Interface (IPMI)
**Answer:** Identity and access management (IAM) implementations; Federated authentication
**Explanation:** Misconfigured IAM implementations and federation misconfigurations are two common ways attackers leverage misconfigured cloud assets.

## Q30
**Question:** Match the cloud attack to the description.
**Type:** matching
**Pairs:**
- Credential Harvesting -> Act of gathering and stealing valid usernames, passwords, tokens, PINs, and any other types of credentials through infrastructure breaches
- Privilege Escalation -> Act of exploiting a bug or design flaw in a software or firmware application to gain access to resources that normally would have been protected from an application or a user
- Account Takeover -> When a threat actor gains access to a user or application account and uses it to then gain access to more accounts and information
**Explanation:** These three cloud attack types build on each other — from harvesting credentials, to escalating privileges, to taking over accounts entirely.

## Q31
**Question:** What is the purpose of using the `smtp-user-enum -M VRFY -u snp -t 10.0.0.1` command in Kali Linux?
**Type:** single
**Options:**
- To compromise SMTP open relay server 10.0.0.1
- To verify if a certain user exists on the SMTP server 10.0.0.1
- To start a Transport Layer Security (TLS) connection to an email server 10.0.0.1
- To initiate an SMTP conversation with an email server 10.0.0.1
**Answer:** To verify if a certain user exists on the SMTP server 10.0.0.1
**Explanation:** This command uses the SMTP VRFY method to check whether the user "snp" exists on the target SMTP server.

## Q32
**Question:** Match the mobile device security testing tool to the description.
**Type:** matching
**Pairs:**
- Burp Suite -> This can test mobile applications and determine how they communicate with web services and APIs.
- Drozer -> This Android testing platform and framework provides access to numerous exploits that can be used to attack Android platforms.
- Needle -> This open-source framework is used to test the security of iOS applications.
- ApkX -> This tool enables you to decompile Android application package files.
**Explanation:** Each tool targets a different part of mobile app testing — API communication, Android exploitation, iOS security, or APK decompilation.

## Q33
**Question:** Match the mobile device attack to the description.
**Type:** matching
**Pairs:**
- Sandbox analysis -> This can enable a threat actor to bypass the access control mechanisms implemented by Android, Apple iOS, and mobile app developers.
- Spamming -> This presents users with links to redirect them to malicious sites to steal sensitive information or install malware.
- Reverse engineering -> This is the process of analyzing a mobile app to extract information about the source code to understand the underlying architecture of a mobile application and potentially manipulate the mobile device.
**Explanation:** These represent three distinct mobile attack vectors — bypassing OS sandboxing, malicious link spam, and code-level reverse engineering.

## Q34
**Question:** Which two Bluetooth Low Energy (BLE) statements are true? (Choose two.)
**Type:** multi
**Options:**
- Threat actors can listen to BLE advertisements and leverage misconfigurations.
- BLE pairing is done by mobile apps.
- BLE involves a five-phase process to establish a connection.
- BLE advertisement can be intercepted using specialized antennas and equipment.
- All BLE-enabled devices implement cryptographic functions.
**Answer:** Threat actors can listen to BLE advertisements and leverage misconfigurations.; BLE advertisement can be intercepted using specialized antennas and equipment.
**Explanation:** BLE traffic can be intercepted with specialized antennas/equipment and attackers can exploit misconfigurations from listening to advertisements. BLE pairing occurs at the OS level (not by apps), uses a three-phase process, and not all devices implement BLE-layer encryption.

## Q35
**Question:** Match the insecure code practice to the description.
**Type:** matching
**Pairs:**
- Hard-coded credentials -> A catastrophic flaw that an attacker can leverage to completely compromise an application or the underlying system.
- Comments in source code -> Developers include information in source code that could provide too much information and might be leveraged by an attacker.
- Lack of error handling and overly verbose error handling -> A type of weakness and security malpractice that can provide information to help an attacker perform additional attacks on the targeted system.
- Unprotected APIs -> Many APIs lack adequate controls and are difficult to monitor. The breadth and complexity of APIs also make it difficult to automate effective security testing.
**Explanation:** Each insecure coding practice creates a different avenue of risk, from full compromise (hard-coded credentials) to incremental information leakage (comments, error handling) to poorly monitored attack surface (unprotected APIs).

## Q36
**Question:** Which C2 utility can be used to create multiple reverse shells?
**Type:** single
**Options:**
- Wsc2
- WMImplant
- Socat
- TrevorC2
**Answer:** Socat
**Explanation:** Socat is a C2 utility that can create multiple reverse shells. Wsc2 uses WebSockets, WMImplant leverages WMI, and TrevorC2 is a separate Python-based C2 utility.

## Q37
**Question:** The attacking system has a listener (port open), and the victim initiates a connection back to the attacking system. Which two resources can create this type of malicious activity? (Choose two.)
**Type:** multi
**Options:**
- Empire
- Steghide
- Sysinternals
- BloodHound
- Netcat
**Answer:** Empire; Netcat
**Explanation:** This describes a reverse shell. Netcat and Metasploit's Meterpreter module are common reverse-shell tools, and Empire can also deploy reverse shells as part of its post-exploitation modules.

## Q38
**Question:** Match the PowerSploit module/script to the respective description.
**Type:** matching
**Pairs:**
- Invoke-Portscan -> Does a simple TCP port scan using regular sockets, based rather loosely on Nmap
- PowerUp -> Acts as clearinghouse of common privilege escalation checks, along with some weaponization vectors
- PowerView -> Performs network and Windows domain enumeration and exploitation
- Get-VaultCredential -> Displays Windows vault credential objects, including plaintext web credentials
- Set-CriticalProcess -> Causes the machine to blue screen upon exiting PowerShell
**Explanation:** Each PowerSploit module serves a specific post-exploitation function, from scanning to privilege escalation to credential extraction to destructive process manipulation.

## Q39
**Question:** Which two tools can create a remote connection with a compromised system? (Choose two.)
**Type:** multi
**Options:**
- Mimikatz
- Nmap
- Metasploit
- BloodHound
- Sysinternals
**Answer:** Metasploit; Sysinternals
**Explanation:** Metasploit can create an RDP connection via its RDP Post-Exploitation Module, and Sysinternals lets administrators control Windows machines remotely.

## Q40
**Question:** Which two options are PowerSploit modules/scripts? (Choose two.)
**Type:** multi
**Options:**
- Get-SecurityPackages
- Get-Keystrokes
- Get-ChildItem
- Get-HotFix
- Get-Process
**Answer:** Get-SecurityPackages; Get-Keystrokes
**Explanation:** Get-SecurityPackages and Get-Keystrokes are PowerSploit modules. Get-ChildItem, Get-Process, and Get-HotFix are native PowerShell cmdlets used for post-exploitation tasks.

## Q41
**Question:** Why is it important to use Common Vulnerability Scoring System (CVSS) to reference the ratings of vulnerabilities identified when preparing the final penetration testing report?
**Type:** single
**Options:**
- It is an international standard for listing publicly known vulnerabilities.
- It has been adopted by many tools, vendors, and organizations.
- It is authorized by governments around the world.
- It is easy to use.
**Answer:** It has been adopted by many tools, vendors, and organizations.
**Explanation:** CVSS's wide adoption across tools, vendors, and organizations increases the credibility and value of using it in a final penetration testing report.

## Q42
**Question:** A company hires a professional to perform penetration testing. The tester has identified and verified that one web application is vulnerable to SQL injection and cross-site scripting attacks. Which technical control measure should the tester recommend to the company?
**Type:** single
**Options:**
- User input sanitization
- Multifactor authentication
- Process-level remediation
- Role-based access control (RBAC)
**Answer:** User input sanitization
**Explanation:** Input validation/sanitization best practices mitigate SQL injection, XSS, CSRF, command injection, and similar vulnerabilities.

## Q43
**Question:** The IT security department of a company has developed an access policy for the datacenter. The policy specifies that the datacenter is locked between 5:30 pm through 7:45 am daily except for emergency access approved by the IT manager. What is the operational control implemented?
**Type:** single
**Options:**
- User training
- Mandatory vacations
- Job rotation
- Time-of-day restrictions
**Answer:** Time-of-day restrictions
**Explanation:** Time-of-day restrictions let an organization restrict user access based on the time of day — here, locking the datacenter during off-hours.

## Q44
**Question:** A security audit for a company recommends that the company implement multifactor authentication for the datacenter access. Which solution would achieve the goal?
**Type:** single
**Options:**
- Minimum password requirements
- Access control vestibule
- Video surveillance
- Biometric controls
**Answer:** Biometric controls
**Explanation:** Biometric controls (fingerprint, retinal scan, facial recognition) combined with a strong password provide effective multifactor authentication.

## Q45
**Question:** What are three examples of the items a penetration tester must clean from systems as part of the post-engagement cleanup process? (Choose three.)
**Type:** multi
**Options:**
- Tester-created credentials
- Network diagrams
- Shells
- Tools
- System patches
- Given passwords
**Answer:** Tester-created credentials; Shells; Tools
**Explanation:** Post-engagement cleanup includes removing tester-created accounts, shells spawned on exploited systems, and any tools installed or run during testing.

## Q46
**Question:** Which Python data structure is used, given the exhibit? (Referenced example uses key/value pairs.)
**Type:** single
**Options:**
- Tree
- Array
- Dictionary
- List
**Answer:** Dictionary
**Explanation:** A dictionary is a collection of data values ordered using key/value pairs.

## Q47
**Question:** Which statement describes the concept of Bash shell in operating systems?
**Type:** single
**Options:**
- Bash shell is a Linux GUI.
- Bash shell is a command shell that supports interactive command execution only.
- Bash shell is a GUI that can be used in operating systems.
- Bash shell is a command shell and language interpreter for an operating system.
**Answer:** Bash shell is a command shell and language interpreter for an operating system.
**Explanation:** Bash is a command shell and language interpreter available on Linux, macOS, and Windows, supporting both interactive and non-interactive command execution.

## Q48
**Question:** Which three tools can be used to perform passive reconnaissance? (Choose three.)
**Type:** multi
**Options:**
- Dig
- Nmap
- Nslookup
- Enum4linux
- Host
- Zenmap
**Answer:** Dig; Nslookup; Host
**Explanation:** Dig, Nslookup, and Host are DNS-based tools used for passive reconnaissance. Nmap, Zenmap, and Enum4linux are active reconnaissance tools.

## Q49
**Question:** An attacker uses John the Ripper to crack a password file. The attacker issued the `~$ john –list=formats` command in Kali Linux. Which information is the attacker trying to find?
**Type:** single
**Options:**
- The password file format
- The ciphertext formats supported by the current version
- The command line format to crack a password file
- The output format supported by the current version
**Answer:** The ciphertext formats supported by the current version
**Explanation:** The `--list=formats` option lists the ciphertext formats supported by the installed version of John the Ripper.

## Q50
**Question:** What are two exploitation frameworks? (Choose two.)
**Type:** multi
**Options:**
- Proxychains
- BeEF
- Metasploit
- Tor
- Encryption
**Answer:** BeEF; Metasploit
**Explanation:** Metasploit and BeEF are both exploitation frameworks (general and web-application-focused, respectively). Tor, Proxychains, and encryption are used for evasion, not exploitation.

## Q51
**Question:** A customer uses Infrastructure as a Service (IaaS) as a cloud implementation. Therefore, the cloud customer is responsible for data, applications, runtime, middleware, virtual machines (VMs), containers, and operating systems in VMs hosted in the cloud. What should the cloud customer do before testing the security of the hosted cloud services?
**Type:** single
**Options:**
- Run the penetration test in off-peak hours and report the results to the cloud provider
- Run the stress test prior to the penetration test and report the results to the cloud provider
- Obtain detailed guidelines on how to perform security assessments and penetration testing from the cloud provider
- Disable end-to-end encryption in order to conduct the penetration test
**Answer:** Obtain detailed guidelines on how to perform security assessments and penetration testing from the cloud provider
**Explanation:** Before testing security in a cloud environment, the customer must get the cloud provider's guidelines/authorization for security assessments and penetration testing, since shared infrastructure has provider-specific rules of engagement.

## Q52
**Question:** A penetration tester wants to stealthily scan a firewall for open ports. Which two nmap commands are the best approaches for the task? (Choose two.)
**Type:** multi
**Options:**
- nmap 192.168.1.1 -f
- nmap 192.168.1.1 -O
- nmap 192.168.1.1 -A
- nmap 192.168.1.1 -F
- nmap 192.168.1.1 -n
- nmap 192.168.1.1 mtu 32
**Answer:** nmap 192.168.1.1 -f; nmap 192.168.1.1 mtu 32
**Explanation:** Both `-f` (fragment packets) and custom `--mtu` fragmentation are classic nmap techniques for evading firewall/IDS inspection by splitting packets into smaller pieces, making the scan stealthier.

## Q53
**Question:** Risk management involves risk appetite and tolerance, risk assessment, risk acceptance, and risk mitigation. Which statement correctly describes the risk management term?
**Type:** single
**Options:**
- Risk appetite and tolerance is the calculation of the current risk level.
- Risk acceptance is the risk level that an organization is willing to take.
- Risk assessment includes the steps to reduce the risk.
- Risk mitigation is the process of determining an acceptable risk level.
**Answer:** Risk acceptance is the risk level that an organization is willing to take.
**Explanation:** Risk acceptance defines the level of risk an organization is willing to tolerate. Risk assessment calculates the current risk level, risk mitigation involves steps to reduce risk, and risk appetite/tolerance defines acceptable risk levels.

## Q54
**Question:** What is the advantage of setting up a penetration environment as an isolated virtual lab where VMs can attack each other without packets leaving the physical system?
**Type:** single
**Options:**
- It is an open environment that permits packets to flow freely between devices.
- It is a closed environment that routes the packets over a physical switch.
- It is a closed environment that allows you to perform different attacks and send IP packets between VMs without those packets leaving the physical system.
- It is an open environment that allows for deployment and recovery of devices being tested through quick backup recovery methods.
**Answer:** It is a closed environment that allows you to perform different attacks and send IP packets between VMs without those packets leaving the physical system.
**Explanation:** A closed virtual lab environment contains all attack traffic within the physical host, preventing packets from reaching production networks while still allowing realistic testing between VMs.

## Q55
**Question:** What is the penetration tester trying to achieve when manipulating Kerberos tickets based on available hashes after compromising a vulnerable system and obtaining local user credentials and password hashes?
**Type:** single
**Options:**
- To steal the hash value of a user credential and use it to create a new user session on the same network
- To manipulate the data being transferred by performing data corruption or data modification
- To spoof an authorized MAC address and bypass a NAC configuration
- To manipulate Kerberos tickets based on available hashes by compromising a vulnerable system and obtaining the local user credentials and password hashes
**Answer:** To manipulate Kerberos tickets based on available hashes by compromising a vulnerable system and obtaining the local user credentials and password hashes
**Explanation:** This describes a Kerberos ticket attack (such as a silver or golden ticket attack), using compromised local credentials and hashes to forge tickets.

## Q56
**Question:** A black-box penetration testing is being performed on the network of a client. The penetration tester does not have physical access to the client network but is parked outside. Which Kali Linux tool can the penetration tester use to compromise the Wi-Fi network and break the encryption keys?
**Type:** single
**Options:**
- aircrack-ng
- scapy
- wireshark
- nmap
**Answer:** aircrack-ng
**Explanation:** Aircrack-ng is a Kali Linux suite for wireless network auditing, including breaking WEP/WPA encryption keys.

## Q57
**Question:** Which three tools can be used in a vishing attack? (Choose three.)
**Type:** multi
**Options:**
- BeEF
- Asterisk
- Nikto
- SET
- SpoofApp
- Nessus
- SpoofCard
**Answer:** Asterisk; SpoofApp; SpoofCard
**Explanation:** Asterisk, SpoofApp, and SpoofCard are voice/caller-ID spoofing tools directly usable in vishing attacks. BeEF targets XSS victims, and Nikto/Nessus are vulnerability scanners unrelated to vishing.

## Q58
**Question:** Which method of influence is a psychological phenomenon in which an individual cannot determine the appropriate mode of behavior?
**Type:** single
**Options:**
- Likeness
- Authority
- Fear
- Social proof
**Answer:** Social proof
**Explanation:** Social proof occurs when an individual, unsure of appropriate behavior, follows what others appear to be doing.

## Q59
**Question:** Why is it important to validate and filter out invalid session ID values in a web application?
**Type:** single
**Options:**
- To prevent on-path attacks
- To prevent session sniffing by attackers
- To prevent predicting session IDs by attackers
- To prevent further exploitation of other web application vulnerabilities
**Answer:** To prevent further exploitation of other web application vulnerabilities
**Explanation:** Validating and filtering session ID input (like any user input) helps prevent it from being leveraged to exploit other application vulnerabilities.

## Q60
**Question:** Which two items can be investigated to help detect a cloud account takeover attack? (Choose two.)
**Type:** multi
**Options:**
- Login location
- Failed login attempts
- User emails
- Normal file sharing patterns
- Incoming VPN connections
**Answer:** Login location; Failed login attempts
**Explanation:** Unusual login locations and spikes in failed login attempts are common indicators investigated to detect account takeover attempts.

## Q61
**Question:** Which C2 utility is Python-based and uses WebSockets?
**Type:** single
**Options:**
- WMImplant
- Socat
- Wsc2
- Twittor
**Answer:** Wsc2
**Explanation:** Wsc2 is a Python-based C2 utility that uses WebSockets. WMImplant leverages WMI, Socat creates reverse shells, and Twittor uses Twitter DMs for C2.

## Q62
**Question:** Which two options are PowerShell commands? (Choose two.)
**Type:** multi
**Options:**
- Get-Location
- Get-Service
- Get-TimedScreenshot
- Get-GPPPassword
- Get-VolumeShadowCopy
**Answer:** Get-Location; Get-Service
**Explanation:** Get-Location and Get-Service are native PowerShell cmdlets. Get-TimedScreenshot, Get-GPPPassword, and Get-VolumeShadowCopy are PowerSploit-specific post-exploitation modules.

## Q63
**Question:** What Windows-based command-line interface suite of tools can run commands to reveal information about running processes and kill or stop services?
**Type:** single
**Options:**
- Sysinternals
- BloodHound
- Empire
- WinRM
**Answer:** Sysinternals
**Explanation:** Sysinternals is a suite of tools letting administrators (or attackers) reveal information about running processes and control (kill/stop) services remotely.

## Q64
**Question:** Which tool can be used to enumerate SMB shares and vulnerable Samba implementations?
**Type:** single
**Options:**
- Dig
- Censys
- Recon-ng
- Enum4linux
**Answer:** Enum4linux
**Explanation:** Enum4linux enumerates SMB shares and identifies vulnerable Samba implementations on target systems.

## Q65
**Question:** A cybercriminal uses a valid user account and launches an attack to extract service account credential hashes without sending additional IP packets to the victim and without having domain admin credentials. Which post-exploit attack is being launched?
**Type:** single
**Options:**
- On-path
- MAC spoofing
- Kerberoasting
- ARP cache poisoning
**Answer:** Kerberoasting
**Explanation:** Kerberoasting extracts service account credential hashes from Active Directory (via legitimate Kerberos ticket requests) for offline cracking, without needing domain admin rights or generating extra network traffic to the victim.

## Q66 (Unverified — exhibit and answer key missing)
**Question:** A Reflected XSS attack is being conducted by an attacker on a vulnerable server. Each colored arrow is a step of this attack. What color order represents this attack in progress?
**Type:** single
**Options:**
- Green, black, yellow, blue, red
- Red, black, yellow, blue, green
- Blue, red, black, yellow, green
- Green, blue, red, black, yellow
**Answer:** Not determinable from provided source (no exhibit image or answer key text was included)
**Explanation:** This question depends on a diagram exhibit that wasn't included in the source text, and no explanation/answer was provided either. If you have the actual image or the confirmed answer, send it and I'll fill this in correctly rather than guess.

## Q67
**Question:** A security management system is preparing to push a new configuration to a firewall that involves rebuilding access control lists and security rules. An attacker has a very small time window to bypass the firewall security controls until the new firewall rules take effect. What kind of vulnerability is being exploited by the attacker?
**Type:** single
**Options:**
- Hard-coded credentials
- Improper error handling
- Remote file inclusion
- Race condition
**Answer:** Race condition
**Explanation:** A race condition vulnerability is exploited here — the attacker takes advantage of the narrow timing window between the old and new firewall configurations.

## Q68
**Question:** Which two social engineering attacks can be launched using BeEF? (Choose two.)
**Type:** multi
**Options:**
- Fake notification bar
- Arduino-based attack vector
- Create a payload and listener
- Powershell attack vectors
- Google phishing
**Answer:** Fake notification bar; Google phishing
**Explanation:** BeEF can launch fake browser notification bars and Google phishing attacks. Arduino-based attack vectors, payload/listener creation, and PowerShell attack vectors are SET features, not BeEF.

## Q69
**Question:** A penetration tester is preparing the final report after the tests are completed. One remediation recommended by the tester is to close unnecessary open ports and services, remove unnecessary software, and disable unused ports. Which type of cybersecurity control is being recommended?
**Type:** single
**Options:**
- Physical control
- Technical control
- Operational control
- Administrative control
**Answer:** Technical control
**Explanation:** Closing ports/services and removing unnecessary software are technology-based hardening actions — examples of technical controls.

## Q70
**Question:** A penetration tester is hired by a company to evaluate the security posture of the IT service department. In the final report, the tester recommends that the company implement role-based access control for the data center systems. Which type of control is recommended?
**Type:** single
**Options:**
- Physical
- Operational
- Technical
- Administrative
**Answer:** Administrative
**Explanation:** Role-based access control (RBAC) is categorized as an administrative control — a policy-based measure to reduce risk.

## Q71
**Question:** A penetration tester is hired by a company to perform web application vulnerability assessment. The tester has completed the required tests and cleaned the target systems. What next step should be done before closing the assignment?
**Type:** single
**Options:**
- Disable all testing tools.
- Remove shells spawned on exploited systems.
- Remove any user accounts that were created during tests.
- Ask the company personnel to validate that the cleanup efforts are sufficient.
**Answer:** Ask the company personnel to validate that the cleanup efforts are sufficient.
**Explanation:** After cleanup, having the client or system owner validate that the cleanup was sufficient is an important final step before closing the engagement.

## Q72
**Question:** Which three applications are used for cracking passwords? (Choose three.)
**Type:** multi
**Options:**
- Recon-ng
- Cain
- Shodan
- CeWL
- Hashcat
- John the Ripper
**Answer:** Cain; Hashcat; John the Ripper
**Explanation:** Cain (and Abel), Hashcat, and John the Ripper are password-cracking tools. Recon-ng and Shodan are reconnaissance tools, and CeWL is a wordlist-generation tool rather than a cracker itself.

## Q73
**Question:** A penetration tester is conducting a gray box penetration test for an organization. The tester wishes to assess vulnerabilities of an IoT device by sending an invalid packet to a proprietary service listening on TCP port 2984. What tool can the tester use in order to send a packet with customized fields to observe the response from the IoT device?
**Type:** single
**Options:**
- Scapy
- Recon-NG
- Shodan
- Nmap
**Answer:** Scapy
**Explanation:** Scapy allows crafting packets with fully customized fields, ideal for testing a proprietary service with non-standard packet formats.

## Q74
**Question:** A penetration tester is searching for a framework that provides a matrix of common tactics and techniques used by attackers, along with recommended mitigations. Which framework will be best suited to provide the requisite information?
**Type:** single
**Options:**
- MITRE
- OWASP WSTG
- NIST SP 800-15
- ISSAF
**Answer:** MITRE
**Explanation:** MITRE ATT&CK provides a matrix of adversary tactics, techniques, and sub-techniques, along with recommended mitigations.

## Q75
**Question:** A threat actor has stolen an iPhone and is attempting to jailbreak it to gain access to resources that normally would have been protected. Which type of attack is the threat actor performing?
**Type:** single
**Options:**
- Privilege escalation
- Metadata service attacks
- Side-channel attacks
- Credential harvesting
**Answer:** Privilege escalation
**Explanation:** Jailbreaking exploits vulnerabilities to gain access to protected resources beyond the device's intended permission model — a form of privilege escalation.

## Q76
**Question:** Which misconfiguration in IoT would allow threat actors to obtain sensitive information from the system and underlying network on IoT devices?
**Type:** single
**Options:**
- Error messages and debug handling
- Digital certificates
- Misconfigured metadata service
- Side-channels
**Answer:** Error messages and debug handling
**Explanation:** Poorly configured error messages and debug handling on IoT devices can leak sensitive system and network information to an attacker.