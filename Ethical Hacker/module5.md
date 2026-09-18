# Module 5: Exploiting Wired and Wireless Networks Answers

## Q1
**Question:** Which NetBIOS service is used for connection-oriented communication?
**Type:** single
**Options:**
- NetBIOS-NS
- NetBIOS-DGM
- NetBIOS-SSN
- LLMNR
**Answer:** NetBIOS-SSN
**Explanation:** NetBIOS provides three services: NetBIOS-NS (name registration/resolution), NetBIOS-DGM (connectionless communication), and NetBIOS-SSN (connection-oriented communication).

## Q2
**Question:** Match the port type and number with the respective NetBIOS protocol service.
**Type:** matching
**Pairs:**
- UDP port 138 -> NetBIOS Datagram Service
- UDP port 137 -> NetBIOS Name Service
- TCP port 445 -> SMB protocol
- TCP port 139 -> NetBIOS Session Service
- TCP port 135 -> Microsoft Remote Procedure Call (MS-RPC)
**Explanation:** Each NetBIOS-related service and related protocol operates over a specific, well-known port used for identification during scanning and enumeration.

## Q3
**Question:** What two features are present on DNS servers using BIND 9.5.0 and higher that help mitigate DNS cache poisoning attacks? (Choose two.)
**Type:** multi
**Options:**
- Randomization of ports
- Provision of cryptographically secure DNS transaction identifiers
- Exclusion of any trust relationships between DNS servers
- Secure DNS data authentication
- Prevention of any recursive DNS queries
**Answer:** Randomization of ports; Provision of cryptographically secure DNS transaction identifiers
**Explanation:** BIND 9.5.0 and higher mitigate DNS cache poisoning through port randomization and cryptographically secure transaction identifiers. DNSSEC (a separate IETF technology) provides secure DNS data authentication and additional protection against cache poisoning.

## Q4
**Question:** What UDP port number is used by SNMP protocol?
**Type:** single
**Options:**
- 161
- 182
- 128
- 176
**Answer:** 161
**Explanation:** Simple Network Management Protocol (SNMP), used to manage network devices, operates over UDP port 161.

## Q5
**Question:** Which is a characteristic of a DNS poisoning attack?
**Type:** single
**Options:**
- The DNS server forward lookup zone is cleared.
- The DNS server reverse lookup zone is cleared.
- The DNS resolver cache is manipulated.
- The DNS server IP address is changed.
**Answer:** The DNS resolver cache is manipulated.
**Explanation:** DNS cache poisoning manipulates the DNS resolver cache by injecting corrupted DNS data, forcing the server to send a victim the wrong IP address and redirect them to the attacker's system.

## Q6
**Question:** Which Kali Linux tool or script can gather information on devices configured for SNMP?
**Type:** single
**Options:**
- snmp-check
- nslookup
- snmp-brute.nse
- snmp-netstat.nse
**Answer:** snmp-check
**Explanation:** The Kali Linux snmp-check tool performs an SNMP walk to gather information on devices configured for SNMP.

## Q7
**Question:** Match the SMTP command with the respective description.
**Type:** matching
**Pairs:**
- MAIL -> Used to denote the email address of the sender
- RSET -> Used to cancel an email transaction
- EHELO -> Used to initiate a conversation with an Extended Simple Mail Transport Protocol server
- DATA -> Used to initiate the transfer of the contents of an email message
- STARTTLS -> Used to start a Transport Layer Security connection to an email server
- HELO -> Used to initiate an SMTP conversation with an email server
**Explanation:** Each SMTP command serves a distinct role in initiating, securing, or managing an email transaction session.

## Q8
**Question:** Which two best practices would help mitigate FTP server abuse and attacks? (Choose two.)
**Type:** multi
**Options:**
- Limit anonymous logins to a select group of people
- Edit the hosts file to limit the number of authorized DNS servers
- Use encryption at rest
- Consolidate all back-end databases on the FTP server
- Require re-authentication of inactive sessions
**Answer:** Limit anonymous logins to a select group of people; Require re-authentication of inactive sessions
**Explanation:** Additional FTP hardening best practices include strong passwords with MFA, file/folder permission restrictions, encryption at rest, locking down admin accounts, keeping server software updated, using FIPS 140-2 validated ciphers, keeping back-end databases on a separate server, and disabling anonymous logins.

## Q9
**Question:** Which is a characteristic of the pass-the-hash attack?
**Type:** single
**Options:**
- Capture of a password hash (as opposed to the password characters) and using the same hashed value for authentication and lateral access to other networked systems
- Reverse engineering of the captured hash password and using the unencrypted password for authentication and lateral access to other networked systems
- Compromise of a SAM file and extraction of the password characters to use for authentication and lateral access to other networked systems
- Capture of the Windows password before the Kerberos hashing function and use of the unencrypted password for authentication and lateral access to other networked systems
**Answer:** Capture of a password hash (as opposed to the password characters) and using the same hashed value for authentication and lateral access to other networked systems
**Explanation:** Windows stores only a password hash in the SAM database, and since these hashes generally can't be reversed, an attacker can reuse a captured hash directly to authenticate to other systems.

## Q10
**Question:** What is a Kerberoasting attack?
**Type:** single
**Options:**
- It is an attempt to steal the hash value of a user credential and use it to create a new user session on the same network.
- It attempts to manipulate Kerberos tickets based on available hashes by compromising a vulnerable system and obtaining the local user credentials and password hashes.
- It is a post-exploitation attempt that is used to extract service account credential hashes from Active Directory for offline cracking.
- It attempts to manipulate data being transferred by performing data corruption or modification.
**Answer:** It is a post-exploitation attempt that is used to extract service account credential hashes from Active Directory for offline cracking.
**Explanation:** Kerberoasting is a post-exploitation activity used to extract service account credential hashes from Active Directory for offline cracking.

## Q11
**Question:** Match the attack type with the respective description.
**Type:** matching
**Pairs:**
- Reflected DOS -> This attack uses spoofed packets that appear to be from the victim. Then the sources become unwitting participants in the attack by sending the response traffic back to the intended victim.
- DNS Amplification -> This is an attack in which the attacker exploits vulnerabilities in target servers to initially turn small queries into much larger payloads, which are used to bring down the servers of the victim.
- Direct DOS -> This occurs when the source of the attack generates the packets, regardless of protocol, application, and so on, that are sent directly to the victim of the attack.
- DDOS -> This attack uses botnets that can be manipulated from a command and control (CnC, or C2) system.
**Explanation:** These four denial-of-service variants differ mainly in whether traffic is spoofed/reflected, amplified, sent directly, or coordinated through a botnet.

## Q12
**Question:** Match the attack type with the respective description.
**Type:** matching
**Pairs:**
- Route Manipulation attacks -> Typically a BGP hijacking attack by configuring or compromising an edge router to announce prefixes that have not been assigned to the organization
- Downgrade attacks -> The attacker forces a system to favor a weak encryption protocol or hashing algorithm that may be susceptible to other vulnerabilities
- DHCP Starvation attack -> An attacker floods a server with bogus DISCOVER packets until the server exhausts the supply of IP addresses
- VLAN Hopping attack -> An attacker bypasses any layer 2 restrictions built to divide hosts
- MAC address spoofing attack -> An attacker spoofs the physical address of the NIC device to match the address of another on a network in order to gain unauthorized access or launch a Man-in-the-Middle attack
**Explanation:** These attacks target different layers and mechanisms of network infrastructure, from routing (BGP) to encryption negotiation to DHCP/VLAN/MAC-layer manipulation.

## Q13
**Question:** Which tool can be used to perform a Disassociation attack?
**Type:** single
**Options:**
- Airmon-ng
- nmap
- POODLE
- EMPIRE
**Answer:** Airmon-ng
**Explanation:** Airmon-ng, part of the Aircrack-ng suite, can perform wireless reconnaissance and disassociation attacks.

## Q14
**Question:** Which is a characteristic of a Bluesnarfing attack?
**Type:** single
**Options:**
- An attack that is launched using common social engineering attacks, such as phishing attacks, can be performed by impersonating a wireless AP or a captive portal to convince a user to enter the user credentials.
- An attack that can be performed using Bluetooth with vulnerable devices in range. It is commonly performed as spam over Bluetooth connections using the OBEX protocol.
- An attack that can be performed using Bluetooth with vulnerable devices in range. This attack actually steals information from the device of the victim.
- An attack involves modifying BLE messages between systems that would lead them to believe that they are communicating with legitimate systems.
**Answer:** An attack that can be performed using Bluetooth with vulnerable devices in range. This attack actually steals information from the device of the victim.
**Explanation:** Bluesnarfing steals information from a victim's device over Bluetooth and can also be used to obtain a device's IMEI number.

## Q15
**Question:** Which Wi-Fi protocol is most vulnerable to a brute-force attack during a Wi-Fi network deployment?
**Type:** single
**Options:**
- WPA2-EAP
- WPS
- WPA3
- WPA2-TKIP
**Answer:** WPS
**Explanation:** Wi-Fi Protected Setup (WPS) simplifies wireless deployment, but most implementations don't limit repeated incorrect PIN attempts, making them highly susceptible to brute-force attacks.

## Q16
**Question:** What does the MFP feature in the 802.11w standard do to protect against wireless attacks?
**Type:** single
**Options:**
- It uses a PNL to maintain a list of trusted or preferred wireless networks.
- It uses a captive portal for all wireless associations.
- It inserts the 802.1q tag to protect the wireless frame.
- It helps defend against deauthentication attacks.
**Answer:** It helps defend against deauthentication attacks.
**Explanation:** Management Frame Protection (MFP), defined in 802.11w, protects wireless devices against spoofed management frames that could otherwise deauthenticate a valid user session.

## Q17
**Question:** What is a DNS resolver cache on a Windows system?
**Type:** single
**Options:**
- It is a database of all WINS records.
- It is a static database entry of all forward and reverse lookup zones.
- It is a temporary database that contains records of all the recent visits and attempted visits to websites and other internet domains.
- It is a collective database of all Domain Name Service records of static and cached entries.
**Answer:** It is a temporary database that contains records of all the recent visits and attempted visits to websites and other internet domains.
**Explanation:** A DNS resolver cache is a temporary database Windows maintains to track recent website and domain visit attempts, sped up for future lookups.

## Q18
**Question:** Match the TCP port number with the respective email protocol that uses it.
**Type:** matching
**Pairs:**
- 465 -> The port registered by the Internet Assigned Numbers Authority (IANA) for SMTP over SSL (SMTPS).
- 587 -> The Secure SMTP (SSMTP) protocol for encrypted communications, as defined in RFC 2487, using STARTTLS.
- 143 -> The default port used by the IMAP protocol in non-encrypted communications.
- 995 -> The default port used by the POP3 protocol in encrypted communications.
- 993 -> The default port used by the IMAP protocol in encrypted (SSL/TLS) communications.
**Explanation:** Each email protocol/port pairing reflects whether the port is used for encrypted or non-encrypted SMTP, POP3, or IMAP traffic.

## Q19
**Question:** Which is the default TCP port used in SMTP for non-encrypted communications?
**Type:** single
**Options:**
- 25
- 110
- 143
- 993
**Answer:** 25
**Explanation:** TCP port 25 is the default for non-encrypted SMTP. Other common email ports: 465 (SMTPS), 587 (STARTTLS/SSMTP), 110 (POP3 non-encrypted), 995 (POP3 encrypted), 143 (IMAP non-encrypted), and 993 (IMAP encrypted).

## Q20
**Question:** What is a characteristic of a Kerberos silver ticket attack?
**Type:** single
**Options:**
- It uses forged service tickets for a given service on a particular server.
- It mimics the authentication hash on a particular server.
- It acts as the LDAP directory for authentication on a target server.
- It converts the hashed value to the unencrypted value for an authentication attack on a particular server.
**Answer:** It uses forged service tickets for a given service on a particular server.
**Explanation:** A Kerberos silver ticket attack forges service tickets for a specific service on a specific server, rather than a full domain-wide golden ticket.

## Q21
**Question:** Which attack is a post-exploitation activity that an attacker uses to extract service account credential hashes from Active Directory for offline cracking?
**Type:** single
**Options:**
- MITM
- On-Path attack
- MAC spoofing
- Kerberoasting
**Answer:** Kerberoasting
**Explanation:** Kerberoasting extracts service account credential hashes from Active Directory for offline cracking, exploiting weak encryption implementations and improper password practices.

## Q22
**Question:** Which four items are needed by an attacker to create a silver ticket for a Kerberos silver ticket attack? (Choose four.)
**Type:** multi
**Options:**
- Hash value
- System account
- SID
- FQDN
- Target service
- DNS forward lookup zone
- DNS resolver cache
- DNS reverse lookup zone
**Answer:** System account; SID; FQDN; Target service
**Explanation:** Creating a silver ticket requires the system account (ending in $), the domain's security identifier (SID), the fully qualified domain name (FQDN), and the target service (e.g., CIFS, HOST).

## Q23
**Question:** Which kind of attack is an IP spoofing attack?
**Type:** single
**Options:**
- On-path
- DDoS
- Pass-the-Hash
- Evil-Twin
**Answer:** On-path
**Explanation:** An on-path attack intercepts communications between two systems, splitting the original connection into two new ones (client-to-attacker and attacker-to-server), often using IP spoofing to trick the victim into connecting to the attacker.

## Q24
**Question:** What is a common mitigation practice for ARP cache poisoning attacks on switches to prevent spoofing of Layer 2 addresses?
**Type:** single
**Options:**
- DHCP snooping
- DNSSEC
- DAI
- BIND 9.5
**Answer:** DAI
**Explanation:** Dynamic ARP Inspection (DAI) on switches is a common mitigation for ARP cache poisoning attacks, preventing spoofing of Layer 2 addresses.

## Q25
**Question:** An attacker is launching a reflected DDoS attack in which the response traffic is made up of packets that are much larger than those that the attacker initially sent. Which type of attack is this?
**Type:** single
**Options:**
- Downgrade
- Amplification
- On-path
- DNS cache poisoning
**Answer:** Amplification
**Explanation:** An amplification attack is a form of reflected DoS attack where the response traffic sent by the unwitting participant is much larger than what the attacker originally sent (while spoofing the victim), flooding the victim with unsolicited large packets.