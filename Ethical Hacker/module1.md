# Module 1: Introduction to Ethical Hacking and Penetration Testing

## Q1
**Question:** Which statement best describes the term ethical hacker?
**Type:** single
**Options:**
- A person who uses different tools than nonethical hackers to find vulnerabilities and exploit targets
- A person that is financially motivated to find vulnerabilities and exploit targets
- A person that is looking to make a point or to promote what they believe
- A person who mimics an attacker to evaluate the security posture of a network
**Answer:** A person who mimics an attacker to evaluate the security posture of a network
**Explanation:** The term ethical hacker describes a person who acts as an attacker and evaluates the security posture of a computer network to minimize risk. Ethical hackers use the same tools to find vulnerabilities and exploit targets as nonethical hackers.

## Q2
**Question:** Which threat actor term describes a well-funded and motivated group that will use the latest attack techniques for financial gain?
**Type:** single
**Options:**
- Hacktivist
- State-sponsored attacker
- Organized crime
- Insider threat
**Answer:** Organized crime
**Explanation:** The cybercrime industry has become one of the most profitable illegal industries. Organized crime groups are well-funded and motivated, and they typically use the latest attack techniques to gain access to information systems.

## Q3
**Question:** Which type of threat actor uses cybercrime to steal sensitive data and reveal it publicly to embarrass a target?
**Type:** single
**Options:**
- Organized crime
- Hacktivist
- Insider threat
- State-sponsored attacker
**Answer:** Hacktivist
**Explanation:** Hacktivists are threat actors who are not motivated by money. They are looking to make a point, promoting a political agenda or social change, using cybercrime as the method of attack.

## Q4
**Question:** What is a state-sponsored attack?
**Type:** single
**Options:**
- An attack perpetrated by a well-funded and motivated group that will typically use the latest attack techniques for financial gain.
- An attack perpetrated by governments worldwide to disrupt or steal information from other nations.
- An attack perpetrated by disgruntled employees inside an organization.
- An attack perpetrated to steal sensitive data and then reveal it to the public to embarrass or financially affect a target.
**Answer:** An attack perpetrated by governments worldwide to disrupt or steal information from other nations.
**Explanation:** Cyber war and cyber espionage both fall under the category of state-sponsored attacks. Many governments worldwide use cyber attacks to steal information from opponents and cause disruption.

## Q5
**Question:** What is an insider threat attack?
**Type:** single
**Options:**
- An attack perpetrated by a well-funded and motivated group that will typically use the latest attack techniques for financial gain.
- An attack perpetrated by governments worldwide to disrupt or steal information from other nations.
- An attack perpetrated by disgruntled employees inside an organization.
- An attack perpetrated to steal sensitive data and then reveal it to the public to embarrass or financially affect a target.
**Answer:** An attack perpetrated by disgruntled employees inside an organization.
**Explanation:** An insider threat comes from inside an organization. Insider threats are often normal employees tricked into divulging sensitive information or mistakenly clicking malicious links, though they can also be malicious insiders motivated by revenge or money.

## Q6
**Question:** What kind of security weakness is evaluated by application-based penetration tests?
**Type:** single
**Options:**
- Firewall security
- Logic flaws
- Wireless deployment
- Data integrity between a client and a cloud provider
**Answer:** Logic flaws
**Explanation:** Application-based penetration tests focus on testing for security weaknesses in enterprise applications, including misconfigurations, input validation issues, injection issues, and logic flaws.

## Q7
**Question:** What two resources are evaluated by a network infrastructure penetration test? (Choose two.)
**Type:** multi
**Options:**
- AAA servers
- CSPs
- Web servers
- IPSs
- Back-end databases
**Answer:** AAA servers; IPSs
**Explanation:** Network infrastructure penetration tests evaluate the network infrastructure's security posture, including switches, routers, firewalls, AAA servers, and IPSs. Web servers and back-end databases are evaluated by application-based tests, while CSPs are evaluated by cloud-focused penetration testing.

## Q8
**Question:** When conducting an application-based penetration test on a web application, the assessment should also include testing access to which resources?
**Type:** single
**Options:**
- AAA servers
- Cloud services
- Switches, routers, and firewalls
- Back-end databases
**Answer:** Back-end databases
**Explanation:** Since a web application is typically built on a web server with a back-end database, the testing scope normally includes the database.

## Q9
**Question:** What is the purpose of bug bounty programs used by companies?
**Type:** single
**Options:**
- Reward security professionals for finding vulnerabilities in the systems of the company
- Reward security professionals for discovering malicious activities by attackers in the systems of the company
- Reward security professionals for fixing vulnerabilities in the systems of the company
- Reward security professionals for breaking into a corporate facility to expose weaknesses in the physical perimeter
**Answer:** Reward security professionals for finding vulnerabilities in the systems of the company
**Explanation:** Companies and government institutions use bug bounty programs to reward security professionals for finding vulnerabilities in websites, applications, or systems, enabling the organization to fix them before threat actors exploit them.

## Q10
**Question:** What characterizes a partially known environment penetration test?
**Type:** single
**Options:**
- The tester must test the electrical grid supporting the infrastructure of the target.
- The tester is provided with a list of domain names and IP addresses in the scope of a particular target.
- The test is a hybrid approach between unknown and known environment tests.
- The tester should not have prior knowledge of the organization and infrastructure of the target.
**Answer:** The test is a hybrid approach between unknown and known environment tests.
**Explanation:** A partially known environment test (previously gray-box) is a hybrid approach between unknown- and known-environment tests. Testers may be provided credentials but not full network infrastructure documentation.

## Q11
**Question:** What characterizes a known environment penetration test?
**Type:** single
**Options:**
- The test is somewhat of a hybrid approach between unknown and known environment tests.
- The tester could be provided with network diagrams, IP addresses, configurations, and user credentials.
- The tester should not have prior knowledge of the organization and infrastructure of the target.
- The tester may be provided only the domain names and IP addresses in the scope of a particular target.
**Answer:** The tester could be provided with network diagrams, IP addresses, configurations, and user credentials.
**Explanation:** In a known-environment test (previously white-box), the tester starts with significant information about the organization and infrastructure, aiming to identify as many holes as possible.

## Q12
**Question:** Which type of penetration test would only provide the tester with limited information such as the domain names and IP addresses in the scope?
**Type:** single
**Options:**
- Known-environment test
- Partially known environment test
- Unknown-environment test
- OWASP Web Security Testing Guide
**Answer:** Unknown-environment test
**Explanation:** In an unknown-environment test (previously black-box), the tester typically has only a very limited amount of information, such as domain names and IP addresses in scope, with no prior knowledge of the organization or its infrastructure.

## Q13
**Question:** Match the penetration testing methodology to the description.
**Type:** matching
**Pairs:**
- MITRE ATT&CK -> Collection of different matrices of tactics and techniques that adversaries use while preparing for an attack
- OWASP WSTG -> Covers the high-level phases of web application security testing
- NIST SP 800-115 -> Provides organizations with guidelines on planning and conducting information security testing
- OSSTMM -> Lays out repeatable and consistent security testing
- PTES -> Provides information about types of attacks and methods
**Explanation:** Each methodology serves a distinct purpose in structuring penetration testing engagements, from tactic cataloging (MITRE ATT&CK) to web-specific testing (OWASP WSTG) to general security testing guidance (NIST SP 800-115, OSSTMM, PTES).

## Q14
**Question:** Which three options are phases in the Penetration Testing Execution Standard (PTES)? (Choose three.)
**Type:** multi
**Options:**
- Threat modeling
- Penetration
- Reporting
- Enumerating further
- Network mapping
- Exploitation
**Answer:** Threat modeling; Reporting; Exploitation
**Explanation:** PTES involves seven phases: Pre-engagement interactions, Intelligence gathering, Threat modeling, Vulnerability analysis, Exploitation, Post-exploitation, and Reporting.

## Q15
**Question:** Which two options are phases in the Information Systems Security Assessment Framework (ISSAF)? (Choose two.)
**Type:** multi
**Options:**
- Pre-engagement interactions
- Maintaining access
- Reporting
- Post-exploitation
- Vulnerability identification
**Answer:** Maintaining access; Vulnerability identification
**Explanation:** ISSAF phases are: Information gathering, Network mapping, Vulnerability identification, Penetration, Gaining access and privilege escalation, Enumerating further, Compromising remote users/sites, Maintaining access, and Covering the tracks.

## Q16
**Question:** Which two options are phases in the Open Source Security Testing Methodology Manual (OSSTMM)? (Choose two.)
**Type:** multi
**Options:**
- Vulnerability Analysis
- Maintaining Access
- Work Flow
- Network Mapping
- Trust Analysis
**Answer:** Work Flow; Trust Analysis
**Explanation:** OSSTMM's key sections include Operational Security Metrics, Trust Analysis, Workflow, Human security testing, Physical security testing, Wireless security testing, Telecommunications security testing, Data networks security testing, Compliance regulations, and Reporting (STAR).

## Q17
**Question:** Which penetration testing methodology is a comprehensive guide focused on web application testing?
**Type:** single
**Options:**
- MITRE ATT&CK
- OWASP WSTG
- NIST SP 800-115
- OSSTMM
**Answer:** OWASP WSTG
**Explanation:** The OWASP Web Security Testing Guide (WSTG) is a comprehensive guide focused on web application testing, compiled over many years by OWASP members, covering high-level phases and detailed testing methods.

## Q18
**Question:** Which option is a Linux distribution that includes penetration testing tools and resources?
**Type:** single
**Options:**
- OWASP
- PTES
- SET
- BlackArch
**Answer:** BlackArch
**Explanation:** BlackArch (blackarch.org), Kali Linux (kali.org), and Parrot OS (parrotsec.org) are Linux distributions that include penetration testing tools and resources. SET is a social engineering testing tool, OWASP is a nonprofit securing-applications organization, and PTES is a testing standard.

## Q19
**Question:** Which option is a Linux distribution URL that provides a convenient learning environment about pen testing tools and methodologies?
**Type:** single
**Options:**
- vmware.com
- attack.mitre.org
- parrotsec.org
- virtualbox.org
**Answer:** parrotsec.org
**Explanation:** Linux distributions such as Kali Linux (kali.org), Parrot OS (parrotsec.org), and BlackArch (blackarch.org) provide convenient environments for learning pen testing tools and methodologies.

## Q20
**Question:** What does the "Health Monitoring" requirement mean when setting up a penetration test lab environment?
**Type:** single
**Options:**
- The tester needs to be sure that a lack of resources is not the cause of false results.
- The tester needs to be able to determine the causes when something crashes.
- The tester needs to ensure controlled access to and from the lab environment and restricted access to the internet.
- The tester validates a finding by running the same test with a different tool to see if the results are the same.
**Answer:** The tester needs to be able to determine the causes when something crashes.
**Explanation:** Penetration test lab requirements include a closed network (controlled/restricted access), health monitoring (determining causes of crashes), sufficient hardware resources (avoiding false results from resource shortages), and duplicate tools (validating findings with a second tool).

## Q21
**Question:** Which tool would be useful when performing a network infrastructure penetration test?
**Type:** single
**Options:**
- Vulnerability scanning tool
- Bypassing firewalls and IPSs tool
- Interception proxies tool
- Mobile application testing tool
**Answer:** Bypassing firewalls and IPSs tool
**Explanation:** Network infrastructure penetration tests might include tools for sniffing or manipulating traffic, flooding network devices, and bypassing firewalls and IPSs.

## Q22
**Question:** Which tool should be used to perform an application-based penetration test?
**Type:** single
**Options:**
- Sniffing traffic tool
- Bypassing firewalls and IPSs tool
- Interception proxies tool
- Cracking wireless encryption tool
**Answer:** Interception proxies tool
**Explanation:** Application-based penetration tests might use tools built for scanning and detecting web vulnerabilities, along with manual testing tools such as interception proxies.

## Q23
**Question:** Which tools should be used to perform a wireless infrastructure penetration test?
**Type:** single
**Options:**
- Web vulnerability detection tools
- Traffic manipulation tools
- Proxy interception tools
- De-authorizing network devices tools
**Answer:** De-authorizing network devices tools
**Explanation:** Wireless infrastructure penetration tests might use tools to crack wireless encryption, de-authorize network devices, and perform on-path (man-in-the-middle) attacks.

## Q24
**Question:** Which tools should be used for testing the server and client platforms in an environment?
**Type:** single
**Options:**
- Cracking wireless encryption tools
- Vulnerability scanning tools
- Interception proxies tools
- De-authorizing network devices tools
**Answer:** Vulnerability scanning tools
**Explanation:** For testing server and client platforms, automated vulnerability scanning tools can identify issues such as outdated software and misconfigurations. Fuzzing tools are typically used for testing protocol robustness.

## Q25
**Question:** Sometimes a tester cannot virtualize a system to do the proper penetration testing. What action should be taken if a system cannot be tested in a virtualized environment?
**Type:** single
**Options:**
- A full backup of the system
- Rebuild the system after any test is performed
- Adopt penetration test tools that will certainly not damage the system
- A complete report with recommended repairs
**Answer:** A full backup of the system
**Explanation:** Being able to recover the production environment is important, since penetration testing will break things regardless of the tools used. Virtual environments offer snapshots and restore features; if a system cannot be virtualized, a full backup is required instead.