# Module 3: Information Gathering and Vulnerability Scanning

## Q1
**Question:** Which two tools could be used to gather DNS information passively? (Choose two.)
**Type:** multi
**Options:**
- Recon-ng
- Dig
- Wireshark
- Nmap
- ExifTool
**Answer:** Recon-ng; Dig
**Explanation:** Recon-ng and Dig can perform passive reconnaissance based on DNS data. Wireshark is packet capture software, ExifTool extracts metadata from files, and Nmap is an active reconnaissance tool.

## Q2
**Question:** When performing passive reconnaissance, which Linux command can be used to identify the technical and administrative contacts of a given domain?
**Type:** single
**Options:**
- netstat
- dig
- whois
- nmap
**Answer:** whois
**Explanation:** The whois command identifies domain technical and administrative contacts, though many organizations keep registration details private via domain registrar contacts. Nmap is active reconnaissance, dig performs passive DNS reconnaissance, and netstat displays active network connections on a host.

## Q3
**Question:** Which specification defines the format used by image and sound files to capture metadata?
**Type:** single
**Options:**
- Exchangeable Image File Format (Exif)
- Extensible Image File Format (Exif)
- Exchangeable File Format (EFF)
- Interchangeable File Format (IFF)
**Answer:** Exchangeable Image File Format (Exif)
**Explanation:** Exif defines the formats for images, sound, and supplementary tags used by digital devices and systems that process image and sound files.

## Q4
**Question:** Why would a penetration tester perform a passive reconnaissance scan instead of an active one?
**Type:** single
**Options:**
- To collect information about a network without being detected
- Because the time to perform the scan is limited
- Because the root-level SSH credentials to a target have been compromised
- To test whether specific services or protocols are available on the network
**Answer:** To collect information about a network without being detected
**Explanation:** Passive reconnaissance is used when information must be collected without alerting security measures on the network. Any scan that injects traffic or elicits service responses is active and can be detected.

## Q5
**Question:** What type of server is a penetration tester enumerating when they enter the nmap -sU command?
**Type:** single
**Options:**
- DNS, SNMP, or DHCP server
- HTTP or HTTPS server
- POP3, IMAP, or SMTP server
- FTP server
**Answer:** DNS, SNMP, or DHCP server
**Explanation:** A UDP scan (-sU) enumerates servers running protocols that use UDP, such as DNS, SNMP, or DHCP.

## Q6
**Question:** What is the disadvantage of conducting an unauthenticated scan of a target when performing a penetration test?
**Type:** single
**Options:**
- Vulnerability of services running inside the target may not be detected.
- The scanner will report the port as open whether or not the service on that network segment is listening or not.
- Unauthenticated scans are more likely to provide a lower rate of false positives than authenticated scans.
- Unauthenticated scans are a form of passive reconnaissance that return little useful information.
**Answer:** Vulnerability of services running inside the target may not be detected.
**Explanation:** If a service isn't listening on that network segment, or is firewalled, an unauthenticated scan will report the port as closed and move on — meaning vulnerabilities may be missed.

## Q7
**Question:** What is required for a penetration tester to conduct a comprehensive authenticated scan against a Linux host?
**Type:** single
**Options:**
- User credentials with root-level access to the target system
- System user credentials
- Physical on-premises access to the target system
- Backdoor access to the target system
**Answer:** User credentials with root-level access to the target system
**Explanation:** Many commands an authenticated scanner runs require root-level access to gather complete information. System user credentials would only provide access to resources that user has privilege for, and remote SSH access is typically used rather than requiring on-premises access.

## Q8
**Question:** In which circumstance would a penetration tester perform an unauthenticated scan of a target?
**Type:** single
**Options:**
- When user credentials were not provided
- When the number of false positive vulnerability reports is not required
- When time is limited and faster scans are required
- When only targets with UDP services are to be scanned
**Answer:** When user credentials were not provided
**Explanation:** Unauthenticated scans don't use credentials, so they're used when user or root-level credentials are unavailable or unknown.

## Q9
**Question:** Why would a penetration tester use the nmap -sF command?
**Type:** single
**Options:**
- When a TCP SYN scan is detected by a network filter or firewall
- When the tester wants to conclude the scan
- When a TCP SYN scan reports more than one open port
- When the tester needs to time stamp the scan
**Answer:** When a TCP SYN scan is detected by a network filter or firewall
**Explanation:** When a firewall or filter detects a TCP SYN scan, a TCP FIN scan (-sF) sends a FIN packet instead, which is typically allowed through firewalls and filters.

## Q10
**Question:** What is the purpose of host enumeration when beginning a penetration test?
**Type:** single
**Options:**
- To identify all active IP addresses within the scope of the test
- To count the total number of IP addresses within the scope of the test
- To identify all vulnerable hosts within the scope of the test
- To count the total number of vulnerable hosts within the scope of the test
**Answer:** To identify all active IP addresses within the scope of the test
**Explanation:** Host enumeration identifies all active IP addresses within scope and may provide limited information about those devices, such as type and OS version.

## Q11
**Question:** What can be deduced when a tester enters the nmap -sF command to perform a TCP FIN scan and the target host port does not respond?
**Type:** single
**Options:**
- That the port is open
- That the port is not responding to TCP traffic
- That the port is listening for UDP traffic
- That the port is not ready to close the TCP connection
**Answer:** That the port is open
**Explanation:** Normal behavior is to ignore a FIN packet on an open port, so no response implies the port is open. A closed port would send back an RST packet.

## Q12
**Question:** What is the disadvantage of running a TCP Connect scan compared to running a TCP SYN scan during a penetration test?
**Type:** single
**Options:**
- The extra packets required may trigger an IDS alarm.
- Both open and closed ports are detected.
- Indeterminate ICMP messages are generated.
- Hosts and addresses outside the scope of the test may be scanned.
**Answer:** The extra packets required may trigger an IDS alarm.
**Explanation:** Security tools are more likely to log the full TCP connection of a TCP Connect scan, and IDSs are more likely to trigger alarms on multiple TCP connections from the same host.

## Q13
**Question:** When a penetration test identifies a vulnerability, how should the vulnerability be further verified?
**Type:** single
**Options:**
- Determine if the vulnerability is exploitable
- Prioritize the vulnerability severity
- Assess the business risk associated with the vulnerability
- Mitigate the vulnerability
**Answer:** Determine if the vulnerability is exploitable
**Explanation:** If a detected vulnerability can be exploited, it is verified as valid. Only after verification should it be prioritized, risk-assessed, and mitigated.

## Q14
**Question:** Why is the Common Vulnerabilities and Exposures (CVE) resource useful when investigating vulnerabilities detected by a penetration test?
**Type:** single
**Options:**
- It is an international consolidation of cybersecurity tools and databases.
- It is a high level list of software weaknesses.
- It has three vulnerability score components.
- It is a dictionary of known attacks.
**Answer:** It is an international consolidation of cybersecurity tools and databases.
**Explanation:** CVE was created in 1999 to consolidate cybersecurity tools and databases internationally. CWE is a high-level list of software weaknesses, CVSS has base/temporal/environmental score components, and CAPEC is a dictionary of known real-world attacks.

## Q15
**Question:** What is the purpose of applying the Common Vulnerability Scoring System (CVSS) to a vulnerability detected by a penetration test?
**Type:** single
**Options:**
- To calculate the severity of the vulnerability
- To determine the priority of the vulnerability
- To determine the attack vector that applies to the vulnerability
- To accurately record how the vulnerability was detected
**Answer:** To calculate the severity of the vulnerability
**Explanation:** CVSS is a widely adopted standard for calculating vulnerability severity using base, temporal, and environmental score components.

## Q16
**Question:** A threat actor is looking at the IT and technical job postings of a target organization. What would be the most beneficial information to capture from these postings?
**Type:** single
**Options:**
- The type of hardware and software used
- The salaries of the positions listed
- The hours of work required by the roles listed
- The employment benefits offered by the company
**Answer:** The type of hardware and software used
**Explanation:** Job postings typically list the hardware and software skills required, giving an attacker helpful information about the platforms the business operates, useful for planning an attack.

## Q17
**Question:** How is open-source intelligence (OSINT) gathering typically implemented during a penetration test?
**Type:** single
**Options:**
- By using public internet searches
- By installing and running the OSINT API
- By sending phishing emails
- By using nmap for web page and web application enumerations
**Answer:** By using public internet searches
**Explanation:** OSINT gathering uses publicly available intelligence sources, such as internet searches, to collect and analyze information about a target.

## Q18
**Question:** What initial information can be obtained when performing user enumeration in a penetration test?
**Type:** single
**Options:**
- A valid list of users
- The IP addresses of the target hosts
- The credentials of a specified user
**Answer:** A valid list of users
**Explanation:** Once access to the target internal network is achieved, user enumeration tools gather a valid list of users — the first step toward attempting to crack a set of credentials.

## Q19
**Question:** What useful information can be obtained by running a network share enumeration scan during a penetration test?
**Type:** single
**Options:**
- Systems on a network that are sharing files, folders, and printers
- The usernames and password credentials of users on the network
- All vulnerable hosts on the network
- Lists of the attack vectors that can exploit the network
**Answer:** Systems on a network that are sharing files, folders, and printers
**Explanation:** A network share enumeration scan identifies systems sharing files, folders, and printers, helping build out the internal network's attack surface.

## Q20
**Question:** A penetration tester must run a vulnerability scan against a target. What is the benefit of running an authenticated scan instead of an unauthenticated scan?
**Type:** single
**Options:**
- Authenticated scans can provide a more detailed picture of the target attack surface.
- Authenticated scans are a form of passive reconnaissance that does not trigger target security alarms.
- Authenticated scans are performed without user credentials.
- Authenticated scans are less complex and are quicker than unauthenticated scans.
**Answer:** Authenticated scans can provide a more detailed picture of the target attack surface.
**Explanation:** Authenticated scans require credentials with root-level access and can provide a complete picture of the target's attack surface.

## Q21
**Question:** What are three considerations when planning a vulnerability scan on a target production network during a penetration test? (Choose three.)
**Type:** multi
**Options:**
- The timing of the scan
- The available network bandwidth
- The network topology
- The available scanning tools
- The trained personnel available to analyze the scan results
- The scan reporting requirement
**Answer:** The timing of the scan; The available network bandwidth; The network topology
**Explanation:** To minimize disruption to a target production network, planning should consider timing, available bandwidth, and network topology. Available tools, trained personnel, and reporting requirements are procedural considerations for the tester and customer, not scan-target considerations.

## Q22
**Question:** When performing a vulnerability scan of a target, how can adverse impacts on traversed devices be minimized?
**Type:** single
**Options:**
- The scan should be performed as close to the target as possible.
- Unauthenticated vulnerability scans should be performed.
- Only passive reconnaissance scans should be performed.
- Scanning policy options should include query throttling.
**Answer:** The scan should be performed as close to the target as possible.
**Explanation:** Performing the scan as close to the target as possible eliminates impacting the intervening devices that scanner traffic would otherwise traverse, and ensures those devices don't affect scan results.

## Q23
**Question:** A company hires a cybersecurity consultant to conduct a penetration test to assess vulnerabilities in network systems. The consultant is preparing the final report to send to the company. What is an important feature of a final penetration test report?
**Type:** single
**Options:**
- It gives an accurate presentation of vulnerabilities.
- It follows expected report presentation standards and style.
- It is a summary of general information so non-technical managers can understand it.
- It is made publicly available to all interested parties.
**Answer:** It gives an accurate presentation of vulnerabilities.
**Explanation:** The most important feature of a final penetration test report is accuracy — all vulnerabilities verified, with no false positive results.

## Q24
**Question:** What is the advantage of using the target Wi-Fi network for reconnaissance packet inspection?
**Type:** single
**Options:**
- Physical access to the building may not be required.
- The packet scan takes less time wirelessly compared to using the target wired network.
- More information can be captured wirelessly compared to using the target wired network.
- Fewer false positive vulnerabilities are detected.
**Answer:** Physical access to the building may not be required.
**Explanation:** A target's wireless footprint can extend beyond building walls, meaning packet inspection over Wi-Fi often doesn't require physical internal building access, reducing the chance of detection.

## Q25
**Question:** What guidance does the NIST Cybersecurity Framework provide to help improve an organization's cybersecurity posture?
**Type:** single
**Options:**
- The framework outlines standards and industry best practices.
- The framework provides a global consolidation of cybersecurity tools and databases.
- The framework lists cyber attacks that have been seen in the real world.
- The framework provides a vulnerability scoring system.
**Answer:** The framework outlines standards and industry best practices.
**Explanation:** The NIST Cybersecurity Framework outlines standards and industry best practices used to improve organizations' cybersecurity posture.