# CCST Networking Reviewer — Corrected Question Bank (78 questions)

> **Source basis:** `CCST_Networking_Reviewer.pdf` (99 slides, exported from PowerPoint), corrected for technical accuracy. Questions are not numbered in the PDF, so they are numbered Q1–Q86 in PDF order. Exact identical repeated question-text duplicates have been removed; non-identical near-duplicates are kept.
>
> **Correction rules used in this file**
> - Answer keys follow the technically correct networking/security concept, not the highlighted PDF reviewer key.
> - Obvious source wording errors are corrected directly.
> - If the PDF did not offer a technically correct option, a corrected option is added.
> - Where the PDF slide shows no written answer, the derived answer is used directly.
> - Every question that has a picture, topology, or command output keeps its **`Exhibit`** section. Where an extracted image file exists, it is named in `Image file` (found in the `exhibits/` folder alongside this file).

## How to use this file (for Codex / app generation)

Each question uses this structure:

```
## Q<n>
- PDF page: <slide number>
- Type: single | multiple | matching | true_false | command | image_single | image_multiple | image_matching | image_true_false | image_command
Question / Exhibit / Options (or Pairs, or Statements) / Answer / Explanation
```

- `single` = one correct option; `multiple` = "Choose 2" style (select all correct).
- `matching` = drag items on the left to targets on the right; the **Pairs** table is the answer key. Left items may be reused (see the question note).
- `true_false` = each statement is graded True/False separately; the answer line gives all of them in order.
- `command` / `image_command` = free-text answer (accept case-insensitive, trimmed matches and obvious equivalents).
- Build visual exhibits (topologies, CLI output) from the `Exhibit` text, or display the provided image file when available.

## Corrected-Version Notes

This version is the study/practice bank to use when you want the logically correct answer, including items where the original reviewer highlight was not technically accurate.

---

# Section 1 — Standard Concepts

*PDF pages 5–39 (Q1–Q35)*


## Q1

- **PDF page:** 5
- **Type:** single

**Question:**

> Given the IP address 172.16.199.25 and the subnet mask 255.255.252.0, what is the CIDR notation for this address?  

**Options:**

- A. 172.16.100.25/22
- B. 172.16.100.25/21
- C. 172.16.100.25/23
- D. 172.16.100.25/20

**Answer:** A. 172.16.100.25/22

**Explanation:** The subnet mask 255.255.252.0 is `11111111.11111111.11111100.00000000`, which has 22 network bits. Therefore the CIDR prefix is `/22`. The IP address text and options disagree on `172.16.199.25` versus `172.16.100.25`, but among the provided choices the technically correct prefix is option A.

---

## Q2

- **PDF page:** 6
- **Type:** single

**Question:**

> How is the following IP address written when using CIDR notation?  
> IP Address: 192.168.0.16  
> Subnet Mask: 255.255.255.240  

**Options:**

- A. 192.168.0.16/30
- B. 192.168.0.16/15
- C. 192.168.0.16/28
- D. 192.168.0.16/24

**Answer:** C. 192.168.0.16/28

**Explanation:** 255.255.255.240 has 28 consecutive 1-bits (24 + 4), so the prefix is /28.

---

## Q3

- **PDF page:** 7
- **Type:** single

**Question:**

> What is the CIDR prefix notation for a subnet mask of 255.255.0.0?  

**Options:**

- A. /24
- B. /8
- C. /16
- D. 32

**Answer:** C. /16

**Explanation:** 255.255.0.0 has 16 network bits, so the prefix is /16. (Option D is printed as "32" without a slash in the PDF.)

---

## Q4

- **PDF page:** 8
- **Type:** single

**Question:**

> A host is given the IP address 172.16.100.25 and the subnet mask 255.255.252.0. Which CIDR notation is correct?  

**Options:**

- A. 172.16.100.25/23
- B. 172.16.100.25/20
- C. 172.16.100.25/21
- D. 172.16.100.25/22

**Answer:** D. 172.16.100.25/22

**Explanation:** 255.255.252.0 = /22. The PDF prints no explicit question sentence after the mask; the options make clear the question asks for the CIDR notation (same as Q1).

---

## Q5

- **PDF page:** 9
- **Type:** single

**Question:**

> Which address is included in the 192.168.200.0/24 network?  

**Options:**

- A. 192.168.199.13
- B. 192.168.200.13
- C. 192.168.201.13
- D. 192.168.1.13

**Answer:** B. 192.168.200.13

**Explanation:** 192.168.200.0/24 covers 192.168.200.0 to 192.168.200.255 (usable hosts .1 to .254). Only 192.168.200.13 is inside it.

---

## Q6

- **PDF page:** 10
- **Type:** single

**Question:**

> What is the most compressed valid format of the IPv6 address 2001:0db8:0000:0016:0000:001b:2000:0056?  

**Options:**

- A. 2001:db8::16::1b:2:56
- B. 2001:db8::16::1b:2000:56
- C. 2001:db8:16::1b:2:56
- D. 2001:db8:0:16::1b:2000:56

**Answer:** D. 2001:db8:0:16::1b:2000:56

**Explanation:** IPv6 compression has two key rules: remove leading zeros inside each hextet, and use `::` only once to replace one contiguous run of all-zero hextets. A and B are invalid because they use `::` twice. C incorrectly shortens `2000` to `2`; leading zeros can be removed, but nonzero trailing digits must remain. D is the valid compressed form: `0db8` becomes `db8`, `0016` becomes `16`, `0000` can be represented by `::`, `001b` becomes `1b`, and `0056` becomes `56`.

---

## Q8

- **PDF page:** 12
- **Type:** single

**Question:**

> Which address is a link-local IPv6 address?  

**Options:**

- A. FDF8:F535:82EF::53
- B. FE80::261:2EFE:FE10:765
- C. 2001:0db8:85a3:0000:0000:8a2e:0370:7334
- D. 2401:db00:21:70e4:face:0:3:0

**Answer:** B. FE80::261:2EFE:FE10:765

**Explanation:** IPv6 link-local addresses are in FE80::/10. A is a unique local address (ULA); C and D are global unicast.

---

## Q9

- **PDF page:** 13
- **Type:** single

**Question:**

> At which OSI layer is the data stream broken up into segments that include source and destination port numbers?  

**Options:**

- A. Network
- B. Session
- C. Transport
- D. Data Link

**Answer:** C. Transport

**Explanation:** The Transport layer (Layer 4) segments data and adds source and destination port numbers (TCP or UDP).

---

## Q10

- **PDF page:** 14
- **Type:** single

**Question:**

> Which information is included in the header of a UDP segment?  

**Options:**

- A. Port Numbers
- B. IP Address
- C. Sequence Numbers
- D. MAC Address

**Answer:** A. Port Numbers

**Explanation:** A UDP header holds source port, destination port, length, and checksum. IP addresses are Layer 3, MAC addresses Layer 2, and sequence numbers are a TCP feature.

---

## Q11

- **PDF page:** 15
- **Type:** single

**Question:**

> During the data encapsulation process, which OSI layer adds a header that contains MAC addressing information and a trailer used for error checking?  

**Options:**

- A. Network
- B. Session
- C. Transport
- D. Data Link

**Answer:** D. Data Link

**Explanation:** The Data Link layer (Layer 2) builds frames: a header with source and destination MAC addresses and a trailer with the Frame Check Sequence (FCS) for error detection.

---

## Q12

- **PDF page:** 16
- **Type:** single

**Question:**

> Which protocol allows you to securely upload files to another computer on the internet?  

**Options:**

- A. SFTP
- B. HTTP
- C. NTP
- D. ICMP

**Answer:** A. SFTP

**Explanation:** SFTP transfers files over an SSH connection (TCP port 22). HTTP is unencrypted, NTP is time sync, ICMP is diagnostics.

---

## Q13

- **PDF page:** 17
- **Type:** matching

**Question:**

> Move each of the protocols on the left to its characteristics on the right.  

**Items (left):**

- SFTP
- TFTP
- DNS
- DHCP
- ICMP

**Targets (right):**

- Enables the use of SSH keys to prevent an impostor from connecting to the server.
- Ensures data integrity and data security for file transfers using port 22.
- Enables backup of network and router configuration files using UDP.
- Transfers small files within a LAN using port 69.
- Performs a query to translate companypro.net to an IP address.
- Assigns the reserved IP address 10.10.10.200 to a web server at your company.
- Performs a ping to ensure that a server is responding to network connections.

**Answer (pairs):**

| Item | Target |
|---|---|
| SFTP | Enables the use of SSH keys to prevent an impostor from connecting to the server. |
| SFTP | Ensures data integrity and data security for file transfers using port 22. |
| TFTP | Enables backup of network and router configuration files using UDP. |
| TFTP | Transfers small files within a LAN using port 69. |
| DNS | Performs a query to translate companypro.net to an IP address. |
| DHCP | Assigns the reserved IP address 10.10.10.200 to a web server at your company. |
| ICMP | Performs a ping to ensure that a server is responding to network connections. |

**Explanation:** Each protocol on the left can be used more than once: SFTP (SSH, port 22) matches two items, TFTP (UDP port 69) matches two items, and DNS, DHCP, ICMP match one each.

---

## Q14

- **PDF page:** 18
- **Type:** matching

**Question:**

> Move each protocol or device type from the list on the left to the correct OSI layer on the right.  

**Exhibit (exact description of the image / diagram / command output):**

Slide layout: the five OSI layers (Physical, Data Link, Network, Application, Transport) are listed in a left column as drag targets. The original slide grouped Cable, Hub, and NIC together; this corrected version separates NIC because a NIC is normally associated with Data Link behavior through its MAC address.  

**Items (left):**

- SMTP, FTP
- TCP, UDP
- Cable, Hub
- NIC
- Switch
- Router

**Targets (right):**

- Physical
- Data Link
- Network
- Application
- Transport

**Answer (pairs):**

| Item | Target |
|---|---|
| SMTP, FTP | Application |
| TCP, UDP | Transport |
| Cable, Hub | Physical |
| NIC | Data Link |
| Switch | Data Link |
| Router | Network |

**Explanation:** SMTP and FTP are Application layer protocols. TCP and UDP are Transport layer protocols. Cables and hubs operate at the Physical layer. A NIC touches Layer 1 physically, but it is normally taught with Data Link because it has and uses a MAC address. Switches are Data Link devices, and routers operate at the Network layer.

---

## Q15

- **PDF page:** 19
- **Type:** matching

**Question:**

> Move each protocol from the list on the left to the correct TCP/IP model layer on the right.  

**Items (left):**

- TCP
- IP
- FTP
- Ethernet

**Targets (right):**

- Internetwork
- Application
- Transport
- Network Access

**Answer (pairs):**

| Item | Target |
|---|---|
| TCP | Transport |
| IP | Internetwork |
| FTP | Application |
| Ethernet | Network Access |

**Explanation:** In the TCP/IP model, TCP belongs to Transport, IP belongs to the Internet/Internetwork layer, and FTP is an Application layer protocol. Ethernet belongs to the bottom Network Access layer, also called the Link layer in some references.

---

## Q16

- **PDF page:** 20
- **Type:** matching

**Question:**

> Move each category on the left to its correct definition on the right.  

**Items (left):**

- LAN
- PAN
- WAN

**Targets (right):**

- Connects devices such as computers, telephones, tablets, and printers within a range of about 10 meters.
- Spans a small area such as a room, home, office building, or small group of buildings.
- Spans a large geographical distance and connects smaller networks over leased lines and VPNs or tunnels.

**Answer (pairs):**

| Item | Target |
|---|---|
| PAN | Connects devices such as computers, telephones, tablets, and printers within a range of about 10 meters. |
| LAN | Spans a small area such as a room, home, office building, or small group of buildings. |
| WAN | Spans a large geographical distance and connects smaller networks over leased lines and VPNs or tunnels. |

**Explanation:** PAN ≈ 10 meters (for example Bluetooth); LAN = small site; WAN = large geographic distance.

---

## Q17

- **PDF page:** 21
- **Type:** single

**Question:**

> Which command will display all the current operational settings configured on a Cisco router?  

**Options:**

- A. show protocols
- B. show startup-config
- C. show version
- D. show running-config

**Answer:** D. show running-config

**Explanation:** show running-config displays the active configuration in RAM. show startup-config shows the saved configuration in NVRAM; show version shows hardware/software information.

---

## Q18

- **PDF page:** 22
- **Type:** true_false

**Question:**

> For each statement about bandwidth and throughput, select True or False.  

**Statements:**

- 1. High levels of network latency decreases network bandwidth.
- 2. Low bandwidth can increase network latency.
- 3. You can increase throughput by decreasing network [word missing in PDF].

**Answer:** 1 — False; 2 — True; 3 — True

**Explanation:** Bandwidth is capacity, usually measured in bits per second; latency is delay, usually measured in milliseconds. (1) High latency does not reduce the configured bandwidth of a link, so it is False. (2) Low bandwidth can cause queues to form when there is more traffic than the link can carry, which increases delay, so it is True. (3) If the missing word is "latency", then reducing latency can improve real user-perceived throughput and responsiveness, so True is the logical answer.

---

## Q19

- **PDF page:** 23
- **Type:** matching

**Question:**

> Move each cloud computing service model from the list on the left to the correct example on the right.  

**Items (left):**

- IaaS
- SaaS
- PaaS

**Targets (right):**

- A company develops an application using cloud-based resources and tools.
- These virtual machines are connected by a virtual network in the cloud.
- A user accesses a web-based graphics design application in the cloud for a monthly fee.

**Answer (pairs):**

| Item | Target |
|---|---|
| PaaS | A company develops an application using cloud-based resources and tools. |
| IaaS | These virtual machines are connected by a virtual network in the cloud. |
| SaaS | A user accesses a web-based graphics design application in the cloud for a monthly fee. |

**Explanation:** Read the examples by asking how much the customer manages. PaaS gives developers a managed platform and tools for building applications. IaaS gives raw infrastructure such as virtual machines, storage, and virtual networks. SaaS is a finished application consumed over the internet, such as a web-based design app.

---

## Q20

- **PDF page:** 24
- **Type:** matching

**Question:**

> Move each cloud service model on the left to its correct description on the right.  

**Items (left):**

- IaaS
- SaaS
- PaaS

**Targets (right):**

- Provides the hardware and software needed for developing, running, and managing applications.
- Provides pay-as-you-go access to resources provided on virtual machines and virtual storage.
- Provides on-demand access to applications delivered remotely over the internet.

**Answer (pairs):**

| Item | Target |
|---|---|
| PaaS | Provides the hardware and software needed for developing, running, and managing applications. |
| IaaS | Provides pay-as-you-go access to resources provided on virtual machines and virtual storage. |
| SaaS | Provides on-demand access to applications delivered remotely over the internet. |

**Explanation:** PaaS is the managed application platform: runtime, tools, and services for developing and running apps. IaaS is pay-as-you-go infrastructure: virtual machines, storage, and networking. SaaS is a ready-to-use application delivered remotely.

---

## Q21

- **PDF page:** 25
- **Type:** single

**Question:**

> Which protocol does an IPv6 host use to resolve the MAC address associated with a destination IPv6 address?  

**Options:**

- A. Address Resolution Protocol (ARP)
- B. Cisco Discovery Protocol (CDP)
- C. Neighbor Discovery Protocol (NDP)
- D. Dynamic Host Configuration Protocol (DHCP)

**Answer:** C. Neighbor Discovery Protocol (NDP)

**Explanation:** IPv6 does not use ARP. NDP (carried in ICMPv6) resolves IPv6 addresses to MAC addresses.

---

## Q22

- **PDF page:** 26
- **Type:** single

**Question:**

> Which protocol is used by an IPv6-enabled host to perform automatic stateless address configuration?  

**Options:**

- A. DHCPv6
- B. ICMPv6
- C. TFTP
- D. DNS

**Answer:** B. ICMPv6

**Explanation:** Stateless Address Autoconfiguration uses ICMPv6 Neighbor Discovery, especially Router Solicitation and Router Advertisement messages, to learn prefix information and form an IPv6 address. TFTP is a file-transfer protocol and is unrelated to SLAAC.

---

## Q24

- **PDF page:** 28
- **Type:** single

**Question:**

> A user initiates a trouble ticket stating that an external web page is not loading. You determine that other resources, both internal and external, are still reachable. Which command can you use to help locate where the issue is in the network path to the external web page?  

**Options:**

- A. ping -t
- B. tracert
- C. ipconfig /all
- D. nslookup

**Answer:** B. tracert

**Explanation:** tracert shows the path hop by hop, so you can see where traffic stops on the way to the unreachable site.

---

## Q25

- **PDF page:** 29
- **Type:** multiple

**Question:**

> Which two statements are true about the IPv4 address of the default gateway configured on a host? (Choose 2.)  
> Note: You will receive partial credit for each correct response.  

**Options:**

- A. The IPv4 address of the default gateway must be the first host address in the subnet.
- B. The same default gateway IPv4 address is configured on each host on the local network.
- C. The default gateway is the Loopback0 interface IPv4 address of the router connected to the same local network as the host.
- D. The default gateway is the IPv4 address of the router interface connected to the same local network as the host.
- E. Hosts learn the default gateway IPv4 address through router advertisement.

**Answer:** B and D

**Explanation:** Every host on the local network uses the same gateway address, which is the router interface on that network. It need not be the first host address (A), is not a loopback address (C), and IPv4 hosts do not learn it through router advertisements (E; that is IPv6).

---

## Q27

- **PDF page:** 31
- **Type:** single

**Question:**

> An engineer configured a new VLAN named VLAN2 for the Data Center team. When the team tries to ping addresses outside VLAN2 from a computer in VLAN2, they are unable to reach them. What should the engineer configure?  

**Options:**

- A. Additional VLAN
- B. Default route
- C. Default gateway
- D. Static route

**Answer:** C. Default gateway

**Explanation:** A host needs a default gateway to reach destinations outside its own VLAN/subnet.

---

## Q29

- **PDF page:** 33
- **Type:** single

**Question:**

> What is the purpose of assigning an IP address to the management VLAN interface on a Layer 2 switch?  

**Options:**

- A. To enable access to the CLI on the switch through Telnet or SSH
- B. To enable the switch to provide DHCP services to other switches in the network
- C. To enable the switch to act as a default gateway for the attached devices
- D. To enable the switch to resolve URLs for the attached devices

**Answer:** A. To enable access to the CLI on the switch through Telnet or SSH

**Explanation:** The management SVI address lets administrators reach the switch remotely (Telnet/SSH). A Layer 2 switch does not route, resolve URLs, or act as a gateway.

---

## Q30

- **PDF page:** 34
- **Type:** single

**Question:**

> Which of the following is a characteristic of the Spanning Tree Protocol (STP)?  

**Options:**

- A. Prevents loops in a network by blocking redundant links.
- B. Provides load balancing across multiple paths in a network.
- C. Prioritizes network traffic based on Quality of Service (QoS) settings.
- D. Allows for rapid convergence by eliminating the need for spanning tree.

**Answer:** A. Prevents loops in a network by blocking redundant links.

**Explanation:** STP prevents Layer 2 loops by placing redundant ports in a blocking state.

---

## Q31

- **PDF page:** 35
- **Type:** single

**Question:**

> What protocol is used by OSPF to form neighbor relationships and exchange routing information?  

**Options:**

- A. CP (Control Protocol)
- B. P (Protocol)
- C. MP (Multiprotocol)
- D. Llo (Link-Local Operations)
- E. IP protocol 89

**Answer:** E. IP protocol 89

**Explanation:** OSPF does not use TCP or UDP ports to form adjacencies. OSPF packets are carried directly inside IP using protocol number 89. OSPF routers send Hello packets to discover neighbors and maintain neighbor relationships.

---

## Q32

- **PDF page:** 36
- **Type:** single

**Question:**

> What information is contained in the MAC address table of a switch?  

**Options:**

- A. Dynamically learned Layer 2 and Layer 3 addresses of devices communicating on active ports on the switch
- B. The MAC addresses of devices communicating on active ports and static MAC addresses configured by the administrator
- C. All active ports on the switch and the host Layer 3 addresses that were dynamically learned on each port
- D. MAC addresses to IP address mappings learned through ARP requests or manually configured by the administrator

**Answer:** B. The MAC addresses of devices communicating on active ports and static MAC addresses configured by the administrator

**Explanation:** A MAC address table maps MAC addresses to ports (dynamic and static entries). Layer 3 data is not stored there; D describes an ARP table.

---

## Q33

- **PDF page:** 37
- **Type:** single

**Question:**

> What is the purpose of a subnet mask?  

**Options:**

- A. Determine the network portion of an IP address
- B. Determine the host portion of an IP address
- C. Determine the default gateway for a network
- D. Determine the DNS server for a network

**Answer:** A. Determine the network portion of an IP address

**Explanation:** A subnet mask separates an IPv4 address into network bits and host bits. The 1-bits identify the network portion; the remaining 0-bits identify the host portion. That is why option A is the best single answer, even though option B is related: once you know the network bits, you also know which bits remain for hosts.

---

## Q34

- **PDF page:** 38
- **Type:** single

**Question:**

> A user at your company cannot connect to a website on the internet. However, they can connect to network resources on the company LAN. You want to use the divide-and-conquer approach to troubleshoot the issue. What should you do first?  

**Options:**

- A. Run the Telnet command from the user's computer
- B. Ping the default gateway from the user's computer
- C. Check the computer's cable connections
- D. Check the computer's network adapter

**Answer:** B. Ping the default gateway from the user's computer

**Explanation:** Divide and conquer starts in the middle of the stack (Layer 3). Since the LAN works, pinging the default gateway tests Layer 3 and shows which direction to troubleshoot.

---

## Q35

- **PDF page:** 39
- **Type:** single

**Question:**

> Your company has 20 Cisco switches throughout its building. You need to view the configuration of each switch from the command line. Which protocol should you use?  

**Options:**

- A. FTP (File Transfer Protocol)
- B. RDP (Remote Desktop Protocol)
- C. SMTP (Simple Mail Transfer Protocol)
- D. SNMP (Simple Network Management Protocol)
- E. SSH (Secure Shell)

**Answer:** E. SSH (Secure Shell)

**Explanation:** To view the configuration of Cisco switches from a command-line session, administrators normally connect with SSH and then run commands such as `show running-config`. SNMP can monitor or retrieve management information, but it is not the usual interactive CLI protocol.

---

# Section 2 — Security

*PDF pages 42–52 (Q36–Q46)*


## Q36

- **PDF page:** 42
- **Type:** single

**Question:**

> Which device protects the network by permitting or denying traffic based on IP address, port number, or application?  

**Options:**

- A. Firewall
- B. Access point
- C. VPN gateway
- D. Intrusion detection system

**Answer:** A. Firewall

**Explanation:** A firewall permits or denies traffic by rules on addresses, ports, protocols, and applications.

---

## Q37

- **PDF page:** 43
- **Type:** single

**Question:**

> How does a firewall determine which traffic to block?  

**Options:**

- A. The firewall matches traffic based on the IP address in the ARP table
- B. The firewall performs a one-to-many network address translation
- C. The firewall matches the traffic based on source and destination IP address
- D. The firewall performs a one-to-one network address translation.

**Answer:** C. The firewall matches the traffic based on source and destination IP address

**Explanation:** Firewalls match traffic against rules (source/destination IP, and also ports/protocols). NAT is address translation, not filtering.

---

## Q38

- **PDF page:** 44
- **Type:** true_false

**Question:**

> You plan to use a network firewall to protect computers at a small office.  

**Statements:**

- 1. A firewall can block traffic to specific ports on internal computers.
- 2. A firewall can direct all web traffic to a specific IP address.
- 3. A firewall can prevent specific apps from running on a computer.

**Answer:** 1 — True; 2 — True; 3 — False

**Explanation:** A network firewall can filter by port and can redirect (port-forward) web traffic to a specific address, but it cannot stop applications from running on a computer (that is endpoint software).

---

## Q39

- **PDF page:** 45
- **Type:** single

**Question:**

> Which best describes confidentiality with regard to network security?  

**Options:**

- A. Ensures data is available for access by providing redundant systems.
- B. Ensures data is not changed during transit between systems.
- C. Ensures data is kept secret using safeguards to prevent unauthorized access.
- D. Ensures data is trusted and has not been tampered with or changed.

**Answer:** C. Ensures data is kept secret using safeguards to prevent unauthorized access.

**Explanation:** A describes availability; B and D describe integrity.

---

## Q40

- **PDF page:** 46
- **Type:** single

**Question:**

> Which component of the AAA service security model provides identity verification?  

**Options:**

- A. Authentication
- B. Accounting
- C. Auditing
- D. Authorization

**Answer:** A. Authentication

**Explanation:** Authentication answers "Who are you?" by verifying identity with something like a password, certificate, biometric factor, or one-time code. Authorization happens after authentication and answers "What are you allowed to do?" Accounting records what the user or device did.

---

## Q41

- **PDF page:** 47
- **Type:** single

**Question:**

> When setting up a wireless network, which security benefit is provided by enabling WPA3?  

**Options:**

- A. Limits network access to only specified devices
- B. Sends traffic through an encrypted tunnel
- C. Secures authentication between client and access point
- D. Makes it more difficult to discover wireless network

**Answer:** C. Secures authentication between client and access point

**Explanation:** WPA3 replaces the WPA2-PSK handshake with SAE, securing client-to-AP authentication against offline dictionary attacks.

---

## Q42

- **PDF page:** 48
- **Type:** matching

**Question:**

> Move the CIA security principles from the list on the left to their examples on the right.  

**Items (left):**

- Confidentiality
- Integrity
- Availability

**Targets (right):**

- You generate a digital signature and attach it to a message.
- You encrypt a sensitive email message.
- You configure three redundant web servers at your company.

**Answer (pairs):**

| Item | Target |
|---|---|
| Integrity | You generate a digital signature and attach it to a message. |
| Confidentiality | You encrypt a sensitive email message. |
| Availability | You configure three redundant web servers at your company. |

**Explanation:** Digital signature = integrity; encryption = confidentiality; redundant servers = availability.

---

## Q43

- **PDF page:** 49
- **Type:** matching

**Question:**

> Move the MFA factors from the list on the left to their correct examples on the right.  
> Factors: Possession, Inherence, Knowledge  

**Items (left):**

- Possession
- Inherence
- Knowledge

**Targets (right):**

- Specifying your name and password to log on to a service.
- Entering a one-time security code sent to your device after logging in.
- Holding your phone to your face to be recognized.

**Answer (pairs):**

| Item | Target |
|---|---|
| Knowledge | Specifying your name and password to log on to a service. |
| Possession | Entering a one-time security code sent to your device after logging in. |
| Inherence | Holding your phone to your face to be recognized. |

**Explanation:** MFA factors are categories of evidence. Knowledge is something you know, such as a username/password combination. Possession is something you have, such as a phone receiving a one-time code. Inherence is something you are, such as facial recognition or a fingerprint.

---

## Q44

- **PDF page:** 50
- **Type:** matching

**Question:**

> Move the security options from the list on the left to their characteristics on the right. You may use each security option once, more than once, or not at all.  

**Items (left):**

- WEP
- WPA2-Personal
- WPA-Enterprise

**Targets (right):**

- Uses a minimum of 40 bits for encryption.
- Uses a RADIUS server for authentication.
- Uses AES and a pre-shared key for authentication.

**Answer (pairs):**

| Item | Target |
|---|---|
| WEP | Uses a minimum of 40 bits for encryption. |
| WPA-Enterprise | Uses a RADIUS server for authentication. |
| WPA2-Personal | Uses AES and a pre-shared key for authentication. |

**Explanation:** WEP is the older and weak wireless security option; it originally used 40-bit keys, so it matches the minimum-40-bit clue. WPA-Enterprise uses 802.1X authentication with a RADIUS server, so it is used in managed business networks. WPA2-Personal is the home/small-office mode that uses AES with a pre-shared key.

---

## Q45

- **PDF page:** 51
- **Type:** matching

**Question:**

> You need to configure wireless settings for a home router. Move the actions from the list on the left to the correct scenarios on the right.  

**Exhibit (exact description of the image / diagram / command output):**

Slide layout: the three scenarios are listed on the left with three wireless security actions on the right. This corrected version pairs each scenario with the logically correct action.  

**Items (left):**

- Set the security mode to WPA2-PSK
- Disable SSID broadcasting
- Disable WPS

**Targets (right):**

- You want to prevent users from using the push-button method for accessing the network.
- You want devices to use a pre-shared key when connecting to the network.
- You want to prevent devices from discovering the name of the WiFi network.

**Answer (pairs):**

| Item | Target |
|---|---|
| Disable WPS | You want to prevent users from using the push-button method for accessing the network. |
| Set the security mode to WPA2-PSK | You want devices to use a pre-shared key when connecting to the network. |
| Disable SSID broadcasting | You want to prevent devices from discovering the name of the WiFi network. |

**Explanation:** WPS is the push-button/PIN onboarding feature, so disabling WPS prevents users from joining with that method. WPA2-PSK uses a pre-shared key. Disabling SSID broadcasting hides the Wi-Fi network name from ordinary discovery scans.

---

## Q47

- **PDF page:** 55
- **Type:** single

**Question:**

> Which wireless security option uses a pre-shared key to authenticate clients?  

**Options:**

- A. WPA2-Personal
- B. 802.1x
- C. 802.1q
- D. WPA2-Enterprise

**Answer:** A. WPA2-Personal

**Explanation:** WPA2-Personal (PSK) uses a shared key. WPA2-Enterprise and 802.1X use per-user authentication via RADIUS; 802.1Q is VLAN tagging.

---

## Q48

- **PDF page:** 56
- **Type:** single

**Question:**

> You need to connect a computer's network adapter to a switch using a 1000BASE-T cable. Which connector should you use?  

**Options:**

- A. Coax
- B. RJ-11
- C. OS2 LC
- D. RJ-45

**Answer:** D. RJ-45

**Explanation:** 1000BASE-T is Gigabit Ethernet over twisted-pair copper with RJ-45 connectors.

---

## Q49

- **PDF page:** 57
- **Type:** single

**Question:**

> Which type of connector should you use to terminate unshielded twisted pair (UTP) cable?  

**Options:**

- A. ST (Straight Tip)
- B. SC (Subscriber Connector)
- C. RJ-45 (Registered Jack 45)
- D. OS2 LC

**Answer:** C. RJ-45 (Registered Jack 45)

**Explanation:** UTP is terminated with RJ-45. ST, SC, and LC are fiber connectors.

---

## Q50

- **PDF page:** 58
- **Type:** single

**Question:**

> You want to store files that will be accessible by every user on your network. Which endpoint device do you need?  

**Options:**

- A. Access point
- B. Server
- C. Hub
- D. Switch

**Answer:** B. Server

**Explanation:** A file server stores files for all network users.

---

## Q51

- **PDF page:** 59
- **Type:** image_single

**Question:**

> What type of interface is the administrator installing in the router?  

**Exhibit (exact description of the image / diagram / command output):**

*Image file:* `exhibits/Q51_page59.png`

Photograph (to the right of the options) of the front of a network device in a rack. Several modular slots are visible with LC fiber patch cables (blue connectors on white/yellow cables) already plugged in, and green status LEDs. On the right, a person's hand holds a small rectangular pluggable transceiver module and is pushing it into an empty slot. A yellow fiber cable runs along the bottom of the photo. The key visual is the small removable transceiver (SFP) being inserted into its cage, which is clearly different from fixed RJ-45, USB, serial, or PoE ports.  

**Options:**

- A. USB (Universal Serial Bus)
- B. SFP (Small Form-factor Pluggable)
- C. Serial
- D. PoE (Power over Ethernet)

**Answer:** B. SFP (Small Form-factor Pluggable)

**Explanation:** A small hot-pluggable transceiver module being inserted into a module slot is an SFP.

---

## Q52

- **PDF page:** 60
- **Type:** image_single

**Question:**

> A Cisco PoE switch is shown in the following image. Which type of port will provide both data connectivity and power to an IP phone?  

**Exhibit (exact description of the image / diagram / command output):**

(Reconstruction, not in PDF.) Front panel of a Cisco PoE switch with numbered callouts: 2 → console port; 3 and 4 → other management/function ports; 6 → group of RJ-45 PoE Ethernet ports; 7 → SFP/fiber ports. The answer choices refer only to these numbers.  

**Options:**

- A. Port identified with number 2
- B. Ports identified with number 6
- C. Ports identified with number 7
- D. Ports identified with number 3 and 4.

**Answer:** B. Ports identified with number 6

**Explanation:** IP phones normally connect to RJ-45 Ethernet switch ports, and on a PoE switch those RJ-45 ports can deliver both network data and electrical power over the same cable. In the reconstructed exhibit, callout 6 marks the block of RJ-45 PoE access ports. The console port is for local management only, and SFP/fiber ports are uplinks rather than PoE access ports.

---

## Q53

- **PDF page:** 61
- **Type:** single

**Question:**

> Which standard contains the specifications for Wi-Fi networks?  

**Options:**

- A. GSM
- B. LTE
- C. IEEE 802.11
- D. IEEE 802.3
- E. EIA/TIA 568A

**Answer:** C. IEEE 802.11

**Explanation:** Wi-Fi is defined by IEEE 802.11. 802.3 is Ethernet; GSM/LTE are cellular; 568A is a cabling standard.

---

## Q54

- **PDF page:** 62
- **Type:** single

**Question:**

> Which device is an Internet of Things (IoT) device?  

**Options:**

- A. An internet-accessible thermostat
- B. A video streaming server
- C. A virtual private network concentrator
- D. A cloud-based file storage array

**Answer:** A. An internet-accessible thermostat

**Explanation:** IoT devices are everyday objects with embedded network connectivity; the others are infrastructure.

---

## Q55

- **PDF page:** 63
- **Type:** single

**Question:**

> Which network technology is not impacted by electromagnetic and radio wave interference?  

**Options:**

- A. Wireless
- B. Twisted Pair
- C. Fiber
- D. Copper

**Answer:** C. Fiber

**Explanation:** Fiber carries light, so it is immune to EMI/RFI; copper and wireless are susceptible.

---

## Q56

- **PDF page:** 64
- **Type:** single

**Question:**

> A Cisco switch is not accessible from the network. You need to view its running configuration. Which out-of-band method can you use to access it?  

**Options:**

- A. SSH
- B. SNMP
- C. Console
- D. Telnet

**Answer:** C. Console

**Explanation:** The console port is out-of-band: a direct local connection that works without network connectivity.

---

# Section 4 — Infrastructure

*PDF pages 67–68 (Q57–Q58)*


## Q57

- **PDF page:** 67
- **Type:** image_matching

**Question:**

> Examine the connections shown in the following image. Move the cable types on the right to the appropriate connection description on the left. You may use each cable type more than once or not at all.  

**Exhibit (exact description of the image / diagram / command output):**

*Image file:* `exhibits/Q57_page67.png`

Two server-rack diagrams side by side, with a black label bar "Underground Conduit" at the bottom between them.  
LEFT rack, titled "Distribution Rack 1 - Building 5", top to bottom: a patch panel (row of ports), "Power Distribution Device0", switch S2, switch S1, router R1, router R2.  
RIGHT rack, titled "Data Center Rack 2 - Building 1", top to bottom: a patch panel (row of ports), router R3, switch S3, then a large server chassis labeled "Server0".  
Cables drawn: (1) a short green cable from S1 down to R1 (switch to router R1 Gi0/0/1); (2) a short orange cable between R1 and R2 (R1 Gi0/0/0 to R2 Gi0/0/1); (3) a long blue line from R2 down out of the left rack, through the Underground Conduit, and up into the right rack to R3 (R2 Gi0/0/0 to R3 Gi0/0/0) — this blue line represents the fiber run; (4) green cables in the right rack from R3 to S3 and from S3 over to the network interface card of Server0. Copper links stay inside each rack; the fiber link is the only inter-building link.  

**Items (left):**

- Straight-through UTP Cable
- Fiber Optic Cable
- Crossover UTP Cable

**Targets (right):**

- Connects Switch to Router R1 Gi0/0/1 interface
- Connects Router R2 Gi0/0/0 to Router R3 Gi0/0/0 via underground conduit
- Connects Router R1 Gi0/0/0 to Router R2 Gi0/0/1
- Connects Switch S3 to Server0 network interface card

**Answer (pairs):**

| Item | Target |
|---|---|
| Straight-through UTP Cable | Connects Switch to Router R1 Gi0/0/1 interface |
| Fiber Optic Cable | Connects Router R2 Gi0/0/0 to Router R3 Gi0/0/0 via underground conduit |
| Crossover UTP Cable | Connects Router R1 Gi0/0/0 to Router R2 Gi0/0/1 |
| Straight-through UTP Cable | Connects Switch S3 to Server0 network interface card |

**Explanation:** Use cable type by link purpose and distance. A switch-to-router link and a switch-to-server link are unlike-device Ethernet connections, so they use straight-through UTP in the classic cabling model. A router-to-router copper Ethernet link is a like-device connection, so the expected legacy answer is crossover UTP. The long run between buildings through underground conduit should be fiber optic cable because fiber supports longer distances and avoids electrical/grounding issues between buildings.

---

## Q58

- **PDF page:** 68
- **Type:** multiple

**Question:**

> A local company requires two networks in two new buildings. The addresses used in these networks must be in the private network range. Which two address ranges should the company use? (Choose 2.)  

**Options:**

- A. 172.16.0.0 to 172.31.255.255
- B. 192.16.0.0 to 192.16.255.255
- C. 11.0.0.0 to 11.255.255.255
- D. 192.168.0.0 to 192.168.255.255

**Answer:** A and D

**Explanation:** RFC 1918 private ranges are 10.0.0.0/8, 172.16.0.0/12 (172.16.0.0–172.31.255.255), and 192.168.0.0/16. B (192.16.x.x) and C (11.x.x.x) are public.

---

# Section 5 — Diagnosing Problems

*PDF pages 71–98 (Q59–Q86)*


## Q59

- **PDF page:** 71
- **Type:** image_multiple

**Question:**

> Examine the following command output. Which two conclusions can you make from the output of the tracert command? (Choose 2.)  

**Exhibit (exact description of the image / diagram / command output):**

*Image file:* `exhibits/Q59_page71.png`

```text
Windows Command Prompt (black screen, white monospaced text):
C:\Admin>tracert www.cisco.com
5   (a stray "5" line appears in the image)
over a maximum of 30 hops:

  1   <1 ms   <1 ms   <1 ms  2603-6081-943f-72ec-a240-a0ff-fe67-3c14.res6.big.com [2603:6081:943f:72ec:a240:a0ff:fe67:3c14]
  2   13 ms   11 ms   16 ms  2603-90b3-0a00-01bb-0000-0000-0000-0001.wifi6.biginternet.com [2603:90b3:a00:1bb::1]
  3   17 ms   25 ms   18 ms  lag-61.zblnnc1001h.netops.exchange.com [2001:db8:a000:0:4::8:d4c]
  4   16 ms   13 ms   11 ms  lag-29.drhmncev02r.netops.exchange.com [2001:db8:a000:0:4::2:152]
  5    *        *        *    Request timed out.
  6    *        *        *    Request timed out.
  7   19 ms   18 ms   27 ms  lag-0.pr2.dca10.netops.provider.com [2001:db8:1998:0:4::517]
  8   21 ms   32 ms   23 ms  2001:db8:1998:0:8::639
  9   16 ms   15 ms   18 ms  vlan-103.r10.spine101.iad03.fab.netarch.provider.com [2600:1408:b400:40b::1]
 10   15 ms   17 ms   22 ms  vlan-110.r03.leaf101.iad03.fab.netarch.provider.com [2600:1408:b400:f03::1]
 11   17 ms   17 ms   23 ms  vlan-104.r08.tor101.iad03.fab.netarch.provider.com [2600:1408:b400:2908::1]
 12   25 ms   19 ms   19 ms  g2600-1408-c400-038d-0000-0000-0000-0b33.deploy.static.et.com [2600:1408:c400:38d::b33]

Trace complete.
```

**Options:**

- A. The trace successfully reached the www.cisco.com server.
- B. The trace failed after the fourth hop.
- C. The IPv6 address associated with the www.cisco.com server is 2600:1408:c400:38d::b33.
- D. The routers at hops 5 and 6 are offline.
- E. The device sending the trace has IPv6 address 2600:1408:c400:38d::b33.

**Answer:** A and C

**Explanation:** The trace ends with "Trace complete." and hop 12 is the www.cisco.com server at 2600:1408:c400:38d::b33. Hops 5 and 6 time out only because those routers do not answer (traffic still passed through them), so B and D are false; E confuses the destination address with the sender's.

---

## Q60

- **PDF page:** 72
- **Type:** multiple

**Question:**

> Which two pieces of information should you include when you initially create a support ticket? (Choose 2.)  

**Options:**

- A. A detailed description of the fault
- B. Details about the computers connected to the network
- C. A description of the conditions when the fault occurs
- D. The actions taken to resolve the fault
- E. The description of the top-down fault-finding procedure

**Answer:** A and C

**Explanation:** At creation you record what the fault is and the conditions under which it occurs. Actions taken to resolve it are added later.

---

## Q61

- **PDF page:** 73
- **Type:** multiple
- **Duplicate of:** Q25

**Question:**

> Which two statements are true about the IPv4 address of the default gateway configured on a host? (Choose 2.)  

**Options:**

- A. The IPv4 address of the default gateway must be the first host address in the subnet.
- B. The same default gateway IPv4 address is configured on each host on the local network.
- C. The default gateway is the Loopback0 interface IPv4 address of the router connected to the same local network as the host.
- D. The default gateway is the IPv4 address of the router interface connected to the same local network as the host.
- E. Hosts learn the default gateway IPv4 address through router advertisement.

**Answer:** B and D

**Explanation:** This is a near-duplicate of Q25. The idea is the same: hosts on the same local network use the same default gateway address, and that address is the router interface on their local subnet.

---

## Q62

- **PDF page:** 74
- **Type:** image_command

**Question:**

> An administrator is configuring the host PC-A on the network shown in the following graphic. PC-A must be able to communicate on the local network and on the internet. There is no DHCP server on the network. What information does the administrator need to input in the IPv4 protocol properties window?  

**Exhibit (exact description of the image / diagram / command output):**

*Image file:* `exhibits/Q62_page74.png`

Combined graphic. LEFT: Windows "Internet Protocol Version 4 (TCP/IPv4) Properties" dialog, General tab. Radio button "Use the following IP address" is selected, with empty fields IP address, Subnet mask, Default gateway. Radio button "Use the following DNS server addresses" is selected, with Preferred DNS server filled in (reads about 172.100.025.4) and an empty Alternate DNS server. A "Validate settings upon exit" checkbox, and Advanced..., OK, Cancel buttons.  
RIGHT: network topology. Top right: an Internet cloud connected to an "ISP" router (address label 10.10.100.254 next to the red link). The ISP router is linked by a red line to "Router1". Router1 interface G0/1 is labeled 10.10.100.78 (facing the ISP). Router1 interface G0/0 is labeled with a red-dashed box "172.100.0.1" (facing the LAN). A red line runs from Router1 down to "Switch1". Switch1 is connected to a server icon on the right (labeled 172.100.0.254) and to "PC-A" below. The LAN is drawn inside a large shaded oval, with a red-dashed box at the bottom reading "Network 172.100.0.0/16".  

**Answer:** IP address — any unused host address in 172.100.0.0/16 (for example 172.100.0.10, not .1 or .254); Subnet mask — 255.255.0.0; Default gateway — 172.100.0.1 (Router1 G0/0); DNS server — 172.100.0.254.

**Explanation:** Because there is no DHCP server, PC-A needs manual IPv4 settings. The host IP must be an unused address in the LAN `172.100.0.0/16`; it cannot reuse Router1's `172.100.0.1` or the server's `172.100.0.254`. The subnet mask for `/16` is `255.255.0.0`. The default gateway must be Router1's LAN-facing interface, `172.100.0.1`, because that is how PC-A reaches other networks and the internet. The DNS server should be the LAN server shown in the topology, `172.100.0.254`.

---

## Q63

- **PDF page:** 75
- **Type:** single

**Question:**

> A help desk technician receives the four trouble tickets listed below. Which ticket should receive the highest priority and be addressed first?  

**Options:**

- A. Ticket 1: A user requests relocation of a printer to a different network jack in the same office. The jack must be patched and made active.
- B. Ticket 2: An online webinar is taking place in the conference room. The video conferencing equipment lost internet access.
- C. Ticket 3: A user reports that response time for a cloud-based application is slower than usual.
- D. Ticket 4: Two users report that wireless access in the cafeteria has been down for the last hour.

**Answer:** B. Ticket 2: An online webinar is taking place in the conference room. The video conferencing equipment lost internet access.

**Explanation:** Priority = impact and urgency. Ticket 2 is a live event affected right now. Ticket 1 is a routine move/add/change, Ticket 3 is degraded (not down), and Ticket 4 affects two users in a lower-impact area.

---

## Q65

- **PDF page:** 77
- **Type:** single

**Question:**

> You are a senior network administrator tasked with diagnosing intermittent connectivity issues on the executive floor of a multinational corporation, which primarily uses iOS devices. After initial checks, you suspect that the problem may be related to SSID settings and network configuration specifics not aligning correctly with the corporate security protocols. Given the high-security requirements and the exclusive use of iOS devices on this floor, which approach should you take to verify and rectify the network settings directly on the affected devices?  

**Options:**

- A. Network Reset
- B. Manual Configuration
- C. Use Fing
- D. SSID Reconfiguration

**Answer:** B. Manual Configuration

**Explanation:** Manually inspect and configure the Wi-Fi profile (SSID, security mode, certificates) on each affected iOS device. A network reset wipes settings without verifying them; Fing is a third-party scanner; SSID reconfiguration changes the infrastructure instead of checking the devices.

---

## Q66

- **PDF page:** 78
- **Type:** image_multiple

**Question:**

> Which two statements are true about the impact to communication on the network while the router is temporarily offline? Evaluate the graphic.  

**Exhibit (exact description of the image / diagram / command output):**

*Image file:* `exhibits/Q66_page78.png`

Network topology. "Router1" at top center, linked by a red line to an "Internet" cloud on its right. Router1 has two red links going down: down-left to "Switch1" and down-right to "Switch2". Switch1 and Switch2 are also linked directly by a horizontal red line. Under Switch1: a beige box containing PC-A and PC-B, labeled "172.100.0.0/16" and "VLAN 100". Under Switch2: a light-blue box containing PC-C and PC-D, labeled "172.110.0.0/16" and "VLAN 110". To the right of Switch2, outside the boxes: a server icon "File-Srv" labeled "10.0.0.5/16" and "VLAN 10" (no separate cable is clearly drawn to it in the image; it is placed beside Switch2). Caption under the diagram: "While making a configuration change to Router1, a junior technician accidentally reboots the router."  

**Options:**

- A. None of the PCs can access the file server (File-Srv)
- B. The file server (File-Srv) can still access the internet
- C. PC-A and PC-B can still communicate with each other.
- D. PC-A, PC-B, PC-C and PC-D can still communicate with each other
- E. PC-C and PC-D can still communicate with the file server (File-Srv)

**Answer:** A and C

**Explanation:** With Router1 offline, inter-VLAN routing and internet access fail. The PCs cannot reach File-Srv if File-Srv is in a different VLAN/subnet that requires Router1 for routing, so A is true. PC-A and PC-B are in the same VLAN/subnet, so they can still communicate locally through the switch, making C true. Hosts in VLAN 100 and VLAN 110 cannot all communicate with each other without routing, so D is false.

---

## Q67

- **PDF page:** 79
- **Type:** image_single

**Question:**

> Which action does Switch1 take?  
> In the network shown in the following graphic, Switch1 is a Layer 2 switch.  
> PC-A sends a frame to PC-C.  
> Switch1 does not have a mapping entry for the MAC address of PC-C.  

**Exhibit (exact description of the image / diagram / command output):**

*Image file:* `exhibits/Q67_page79.png`

Topology. "Router1" at top center with interfaces G0/0 (left) and G0/1 (right). Red link from Router1 G0/0 to Switch1 port G0/24 (Switch1 at left). Red link from Router1 G0/1 to Switch2 port G0/24 (Switch2 at right). Red horizontal link between Switch1 G0/23 and Switch2 G0/23. Switch1: PC-A on G0/1, PC-B on G0/2. Switch2: PC-C on G0/1, PC-D on G0/2. Text under the picture: "PC-A sends a frame to PC-C." and "Switch1 does not have a mapping entry for the MAC address of PC-C." Header text above: "In the network shown in the following graphic, Switch1 is a Layer 2 switch."  

**Options:**

- A. Switch1 queries Switch2 for the MAC address of PC-C
- B. Switch1 drops the frame and sends an error message back to PC-A
- C. Switch1 sends an ARP request to obtain the MAC address of PC-C
- D. Switch1 floods the frame out all active ports except port Gi0/1

**Answer:** D. Switch1 floods the frame out all active ports except port Gi0/1

**Explanation:** A switch floods a frame with an unknown destination MAC out every active port except the one it arrived on (PC-A is on Gi0/1). Switches do not send ARP requests, query other switches, or return errors.

---

## Q68

- **PDF page:** 80
- **Type:** image_single

**Question:**

> Which port should you identify?  
> You have two switches that are connected as shown in the image.  
> The laptop is connected to port A on the first switch. The second switch is connected to port D on the first switch.  
> The laptop sends a broadcast frame to the first switch.  
> You need to identify the ports through which the broadcast frame is forwarded.  

**Exhibit (exact description of the image / diagram / command output):**

*Image file:* `exhibits/Q68_page80.png`

Two blue Ethernet switches side by side. First (left) switch has four adjacent ports labeled A, B, C, D (and a larger uplink-style symbol to the right). A laptop sits above the first switch with a thin blue line down to port A. Black curved cables leave ports B and C and go off the top of the picture (to other devices not shown), and a curved cable from port D arcs over to the first port of the second (right) switch. Port A is the ingress port; B, C, D are the other connected ports.  

**Options:**

- A. D only
- B. A, B and D only
- C. B and C only
- D. B, C and D only

**Answer:** D. B, C and D only

**Explanation:** A broadcast is flooded out every active port except the ingress port. It arrived on A, so it leaves on B, C, and D (D leads to the second switch).

---

## Q69

- **PDF page:** 81
- **Type:** single

**Question:**

> A support technician examines the front panel of a Cisco switch and sees 4 Ethernet cables connected in the first four ports. Ports 1, 2 and 3 have a green LED. Port 4 has a blinking green light. What is the state of Port 4?  

**Options:**

- A. Link is up and not stable
- B. Link is up and there is no activity
- C. Link is up with cable malfunctions
- D. Link is up and active

**Answer:** D. Link is up and active

**Explanation:** Solid green = link up, no activity; blinking green = link up and passing traffic.

---

## Q70

- **PDF page:** 82
- **Type:** single

**Question:**

> A user reports a problem connecting to network resources. Other users connected to the same switch are not experiencing the same problem. The user's computer is patched to switch port Gi0/15. The status indicator for this port is blinking alternately green then amber. What does the light pattern indicate about the status of port Gi0/15?  

**Options:**

- A. The port is administratively shut down
- B. The port is experiencing a high rate of errors.
- C. The port is blocked by a firewall rule.
- D. The port is not connected to a powered-on device.

**Answer:** B. The port is experiencing a high rate of errors.

**Explanation:** Alternating green/amber indicates the link is up but experiencing a fault or high error rate. An administratively down port shows no light; firewalls do not affect port LEDs.

---

## Q71

- **PDF page:** 83
- **Type:** image_single

**Question:**

> What can you tell from the command output? A user reports that a company website is not available. The help desk technician issues a tracert command to determine if the server hosting the website is reachable over the network. The output of the command is shown as follows:  

**Exhibit (exact description of the image / diagram / command output):**

*Image file:* `exhibits/Q71_page83.png`

```text
Windows Command Prompt (black, low resolution):
C:\>tracert 192.168.1.10
Tracing route to 192.168.1.10 over a maximum of 30 hops:
  1   0 ms   0 ms   1 ms   192.168.5.1
  2   1 ms   0 ms   0 ms   10.0.1.1
  3    *       *       *     Request timed out.
  4   1 ms   1 ms   0 ms   10.0.0.2
  5   1 ms   1 ms   0 ms   192.168.1.10
```

**Options:**

- A. The server with address 192.168.1.10 is reachable over the network
- B. The router at hop 3 is not forwarding packets to the IP address 192.168.1.10
- C. Requests to the web server at 192.168.1.10 are being delayed and time out.
- D. The server address 192.168.1.10 is being blocked by a firewall on the router at hop 3.

**Answer:** A. The server with address 192.168.1.10 is reachable over the network

**Explanation:** The trace reaches hop 5, the destination itself. The timeout at hop 3 only means that router does not reply to TTL-exceeded messages; hops 4 and 5 answered, so traffic passes through it.

---

## Q72

- **PDF page:** 84
- **Type:** image_single

**Question:**

> Which action can be run directly from the Cisco router's IOS mode shown?  

**Exhibit (exact description of the image / diagram / command output):**

*Image file:* `exhibits/Q72_page84.png`

A black terminal box containing only the prompt "router1#" with a text cursor right after the # (no "(config)" shown). The # prompt is the clue that the router is in privileged EXEC mode.  

**Options:**

- A. Enable a routing process
- B. Show running system information
- C. Enter interface IP configuration subcommands
- D. Select an interface to configure

**Answer:** B. Show running system information

**Explanation:** The prompt router1# is privileged EXEC mode, where show and debug commands run. A, C, and D require global configuration mode (router1(config)#).

---

## Q73

- **PDF page:** 85
- **Type:** image_single

**Question:**

> What can you determine about this switch from the command output? Examine the output of the show mac-address-table command on a Cisco 24-port Ethernet switch.  

**Exhibit (exact description of the image / diagram / command output):**

*Image file:* `exhibits/Q73_page85.png`

```text
Cisco terminal (black, low resolution):
Switch>show mac-address-table
Mac Address Table
Vlan   Mac Address        Type      Ports
1      0001.63a7.3614     DYNAMIC   Fa0/4
1      0030.a363.8719     DYNAMIC   Gig0/1
2      0001.4244.7dd5     DYNAMIC   Gig0/1
2      0030.a363.8719     DYNAMIC   Gig0/1
2      00d0.ff78.00d5     DYNAMIC   Gig0/1
2      00e0.b08e.2dcb     DYNAMIC   Gig0/1
3      0030.a363.8719     DYNAMIC   Gig0/1
3      0060.5c25.494d     DYNAMIC   Fa0/3
3      00e0.b08e.2dcb     DYNAMIC   Gig0/1
3      00e0.f740.c81a     DYNAMIC   Fa0/2
3      ec2e.9879.d11b     STATIC    Fa0/5
(MAC digits are read from a low-resolution image; the port/VLAN/type pattern is what matters.)
```

**Options:**

- A. There are eleven active ports on this switch
- B. Port Fa0/5 is set to administratively down.
- C. All entries were learned by examining incoming frames.
- D. Port Gi0/1 connects to another switch

**Answer:** D. Port Gi0/1 connects to another switch

**Explanation:** Many MAC addresses from several VLANs are learned on Gig0/1, which is typical of an uplink/trunk to another switch. C is wrong because one entry is STATIC (configured, not learned). A is wrong because the table shows only a few distinct ports.

---

## Q74

- **PDF page:** 86
- **Type:** image_true_false

**Question:**

> For each statement about output, select True or False.  
> You connect to a Cisco switch and run the following command: show ip interface brief  
> The command displays the following partial output.  

**Exhibit (exact description of the image / diagram / command output):**

*Image file:* `exhibits/Q74_page86.png`

```text
Cisco terminal table (black):
Interface            IP-Address     OK?   Method   Status                  Protocol
GigabitEthernet0/0   192.168.1.10   YES   manual   up                      up
GigabitEthernet0/1   unassigned     YES   manual   down                    down
GigabitEthernet0/2   unassigned     YES   unset    administratively down   down
```

**Statements:**

- 1. A device connected to GigabitEthernet0/1 can send out broadcast traffic.
- 2. A technician issued the shutdown command on interface GigabitEthernet0/2.
- 3. A technician set the IP address for GigabitEthernet0/0 by using the CLI.

**Answer:** 1 — False; 2 — True; 3 — True

**Explanation:** (1) Gi0/1 is down/down, so nothing can be sent. (2) "administratively down" appears only when shutdown is configured. (3) Method "manual" means the address was configured by hand (CLI), not by DHCP.

---

## Q75

- **PDF page:** 87
- **Type:** image_true_false

**Question:**

> You purchase a new Cisco switch, turn it on and connect to its console port. You then run the following command.  

**Exhibit (exact description of the image / diagram / command output):**

*Image file:* `exhibits/Q75_page87.png`

```text
Black Cisco CLI window:
#show running-config | section include interface
interface GigabitEthernet0/1
!
interface GigabitEthernet0/2
!
<output omitted>
(No shutdown commands and no IP address commands appear under either interface.)
```

**Statements:**

- 1. The two interfaces can communicate over Layer 2.
- 2. The two interfaces are administratively shut down.
- 3. The two interfaces have default IP address assigned.

**Answer:** 1 — True; 2 — False; 3 — False

**Explanation:** A default Layer 2 switch normally has access ports enabled and in VLAN 1, so two connected hosts can communicate at Layer 2 if their host IP settings are compatible. The shown interface configuration does not include `shutdown`, so statement 2 is false. Layer 2 switch access ports do not need IP addresses for basic switching, so statement 3 is false.

---

## Q76

- **PDF page:** 88
- **Type:** image_command

**Question:**

> A help desk technician is working on a computer that is unable to resolve URLs in the browser. The technician runs the ipconfig /all command and receives the following output.  
> You need to issue a command to view the network devices in the path from the computer to the server that resolves the host name. What command should you issue?  

**Exhibit (exact description of the image / diagram / command output):**

*Image file:* `exhibits/Q76_page88.png`

```text
Black console excerpt of ipconfig /all:
Connection-specific DNS Suffix  . : local.co
Physical Address. . . . . . . . . : 0004.9A64.227D
IPv4 Address. . . . . . . . . . . : 192.168.0.10
Subnet Mask . . . . . . . . . . . : 255.255.255.0
Default Gateway . . . . . . . . . : 192.168.0.1
DHCP Servers. . . . . . . . . . . : 192.168.10.1
DNS Servers . . . . . . . . . . . : 64.100.8.8
```

**Answer:** tracert 64.100.8.8

**Explanation:** The question asks for the path to the DNS server, and the exhibit identifies the DNS server as `64.100.8.8`. On Windows, `tracert 64.100.8.8` sends probes with increasing TTL values and reports each router hop on the way to that destination. `ping` would only test reachability; it would not list the path.

---

## Q77

- **PDF page:** 89
- **Type:** command

**Question:**

> An app on a user's computer is having problems downloading data. The app uses the following URL to download data: https://www.companypro.net:7100/api  
> You need to use Wireshark to capture packets sent to and received from that URL. What Wireshark filter options would you use to filter the results?  

**Answer:** tcp.port == 7100

**Explanation:** The URL includes a service running on TCP port `7100`, so a Wireshark display filter can isolate that traffic with `tcp.port == 7100`. This matches packets where either the source or destination TCP port is 7100, so it catches both directions of the conversation. `tcp.port eq 7100` is an equivalent Wireshark form. An IP-based filter could also work only after the hostname has been resolved to an address.

---

## Q78

- **PDF page:** 90
- **Type:** image_command

**Question:**

> Computers in a small office are unable to access companypro.net. You run the ipconfig command on one of the computers. The results are shown in the exhibit. You need to determine if you can reach the router. Which command should you use?  

**Exhibit (exact description of the image / diagram / command output):**

*Image file:* `exhibits/Q78_page90.png`

```text
Black console excerpt of ipconfig:
DHCP Enabled. . . . . . . . . . . : Yes
Autoconfiguration Enabled . . . . : Yes
IPv4 Address. . . . . . . . . . . : 192.168.0.14(Preferred)
Subnet Mask . . . . . . . . . . . : 255.255.255.0
Lease Obtained. . . . . . . . . . : Sunday, January 8, 2023 11:00:02 AM
Lease Expires . . . . . . . . . . : Sunday, January 8, 2023 12:00:12 PM
Default Gateway . . . . . . . . . : 192.168.0.1
DHCP Server . . . . . . . . . . . : 192.168.0.1
DNS Servers . . . . . . . . . . . : 8.8.8.8
                                    8.8.4.4
NetBIOS over Tcpip. . . . . . . . : Enabled
```

**Answer:** ping 192.168.0.1

**Explanation:** To test whether the host can reach its local router, ping the default gateway address shown in the exhibit: `192.168.0.1`. A successful ping proves the host IP settings, local cabling/Wi-Fi, switch path, and router LAN interface are working at a basic Layer 3 level. It does not prove internet access by itself; it only validates the first hop.

---

## Q79

- **PDF page:** 91
- **Type:** command

**Question:**

> You want to list the IPv4 addresses associated with the host name www.companypro.net. What is the command to execute in this scenario?  

**Answer:** nslookup www.companypro.net

**Explanation:** `nslookup www.companypro.net` asks DNS for records associated with that hostname. If the host has IPv4 A records, `nslookup` displays the IPv4 address or addresses returned by DNS. This is the right tool when the task is name-to-address lookup; `ping` or `tracert` may also resolve names, but they are primarily connectivity/path tools.

---

## Q80

- **PDF page:** 92
- **Type:** single
- **Duplicate of:** Q69

**Question:**

> A support technician examines the front panel of a Cisco switch and sees 4 Ethernet cables connected in the first four ports. Ports 1, 2, and 3 have a green LED. Port 4 has a blinking green light. (What is the state of Port 4?)  

**Options:**

- A. Link is up with cable malfunctions.
- B. Link is up and not stable.
- C. Link is up and active.
- D. Link is up and there is no activity.

**Answer:** C. Link is up and active.

**Explanation:** This repeats Q69's port-LED concept. A solid green switch-port LED means the physical link is up but there is no current traffic activity. A blinking green LED usually means the link is up and actively passing frames.

---

## Q82

- **PDF page:** 94
- **Type:** image_command

**Question:**

> What command will display the following output?  

**Exhibit (exact description of the image / diagram / command output):**

*Image file:* `exhibits/Q82_page94.png`

```text
Black console output (the first line is literally "Image is command output that states the following."):
Capability Codes: R - Router, T - Trans Bridge, B - Source Route Bridge, S - Switch, H - Host, I - IGMP,

Device ID       Local Intrfce   Holdtme   Capability   Platform    Port ID
esxi            Gig 0/5         177       S            VMware ES   vmnic0
esxi            Gig 0/7         177       S            VMware ES   vmnic1
esxi            Gig 0/6         177       S            VMware ES   vmnic2
981888fc23a7    Gig 0/47        160       R S          Meraki MR   Port 0
3456fecd1d08    Gig 0/1         178       S            MS120-8LP   Port 9"
```

**Answer:** show cdp neighbors

**Explanation:** The output columns `Device ID`, `Local Interface`, `Holdtime`, `Capability`, `Platform`, and `Port ID` match Cisco Discovery Protocol neighbor output. The command `show cdp neighbors` summarizes directly connected Cisco devices and the local/remote interfaces used to reach them. It is a discovery command, not a routing-table or interface-status command.

---

## Q83

- **PDF page:** 95
- **Type:** single

**Question:**

> A network administrator can successfully ping www.cisco.com, but cannot ping a corporate server located at a remote branch in another city. You need to identify the specific router where packets are being dropped in the path to the remote branch. Which utility should you use?  

**Options:**

- A. Traceroute
- B. Netstat
- C. Telnet
- D. ipconfig

**Answer:** A. Traceroute

**Explanation:** Traceroute (tracert on Windows) lists each hop; the last responding hop shows where packets stop.

---

## Q84

- **PDF page:** 96
- **Type:** multiple

**Question:**

> You need to determine whether a remote host is reachable through the network. Which two commands can you use? Each correct answer is a complete solution.  

**Options:**

- A. Netstat
- B. Ping
- C. Route print
- D. Ipconfig
- E. Traceroute or tracert

**Answer:** B and E

**Explanation:** Use `ping` first to test basic reachability to the destination. If ping fails or is inconsistent, use `traceroute`/`tracert` to see each hop and determine where packets stop or where delay appears. `netstat`, `route print`, and `ipconfig` are useful local diagnostics, but they do not directly test remote reachability and path progression.

---

## Q85

- **PDF page:** 97
- **Type:** single

**Question:**

> In a network with multiple VLANs, a user is unable to communicate with other users in the same VLAN but can communicate with users in different VLANs. Which of the following could be the cause of this issue?  

**Options:**

- A. User's switchport is not configured as an access port.
- B. User's switchport is not assigned to the correct VLAN.
- C. User's switchport is configured with the wrong duplex setting.
- D. User's switchport is experiencing a spanning tree loop.

**Answer:** B. User's switchport is not assigned to the correct VLAN.

**Explanation:** If the user's switchport is assigned to the wrong VLAN, the user may still reach routed resources in other VLANs through the default gateway, but local same-team devices in the intended VLAN will not be in the same broadcast domain. That symptom points to VLAN membership on the access port.

---
