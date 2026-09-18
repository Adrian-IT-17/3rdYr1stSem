# CCST Networking Reviewer — Full Question Extraction

> **Notes on conventions used in this extraction:**
> - The source PDF does not number its questions, so questions are numbered sequentially (Q1–Q86) in the order they appear in the PDF.
> - All question text, options, spelling, capitalization, punctuation, and typos are preserved EXACTLY as written in the PDF, even where incorrect or garbled.
> - Where the PDF text is truncated/cut off, this is marked with `[cut off in PDF]`.
> - Where the reviewer's indicated answer differs from (or is questionable against) the logically correct answer, the Explanation explicitly flags it.
> - Duplicate questions are kept, as instructed.

---

## Q1

**Question:** How is given the IP Address 172.16.199.25and the subnet mask 255.255.252.0.What is the CIDR notation for this address?

**Type:** single

**Options:**

- A. 172.16.100.25/22
- B. 172.16.100.25/21
- C. 172.16.100.25/23
- D. 172.16.100.25/20

**Answer:** A. 172.16.100.25/22

**Explanation:** The subnet mask 255.255.252.0 has 22 consecutive 1-bits (255.255.11111100.0), so the CIDR notation is /22. ⚠️ Note: The question text says the IP address is 172.16.199.25, but ALL four options say 172.16.100.25 — this inconsistency exists in the PDF itself and was preserved. The correct prefix length is /22 regardless of which host address is used.

---

## Q2

**Question:** How is the following IP address written when using a CIDR notation? IP Address:192.168.0.16Subnet Mask: `[cut off in PDF]`

**Type:** single

**Options:**

- A. 192.168.0.16/30
- B. 192.168.0.16/15
- C. 192.168.0.16/28
- D. 192.168.0.16/24

**Answer:** C. 192.168.0.16/28

**Explanation:** ⚠️ The subnet mask value itself is cut off in the PDF. The original version of this exam question uses subnet mask 255.255.255.240, which equals /28, making C the answer. (/30, /15, and /24 do not correspond to any common mask that would make a different option uniquely correct.)

---

## Q3

**Question:** What is the CIDR prefix notation for a subnet mask of `[cut off in PDF]`

**Type:** single

**Options:**

- A. /24
- B. /8
- C. /16
- D. 32

**Answer:** C. /16

**Explanation:** ⚠️ The subnet mask is cut off in the PDF, so this answer is inferred from the original circulating version of this question, which uses the mask 255.255.0.0 — that mask has 16 network bits, so its CIDR prefix notation is /16. (Option D is also written without a "/" in the PDF — preserved as-is.)

---

## Q4

**Question:** A host is given the IP address 172.16.100.25and the subnet mask `[cut off in PDF]`

**Type:** single

**Options:**

- A. 172.16.100.25/23
- B. 172.16.100.25/20
- C. 172.16.100.25/21
- D. 172.16.100.25/22

**Answer:** D. 172.16.100.25/22

**Explanation:** ⚠️ The subnet mask is cut off in the PDF, but this is the same question as Q1 (see Q1, where the mask 255.255.252.0 is shown). The mask 255.255.252.0 equals /22, so the correct CIDR notation is 172.16.100.25/22.

---

## Q5

**Question:** Which address is included in the 192.168.200.0/24network?

**Type:** single

**Options:**

- A. 192.168.199.13
- B. 192.168.200.13
- C. 192.168.201.13
- D. 192.168.1.13

**Answer:** B. 192.168.200.13

**Explanation:** The network 192.168.200.0/24 covers host addresses from 192.168.200.1 to 192.168.200.254. Only 192.168.200.13 falls inside that range.

---

## Q6

**Question:** What is the most compressed valid format of the IPv6address 2001:0db8:0000:0016:0000:001b:2000:0056?

**Type:** single

**Options:**

- A. 2001:db8::16::1b:2:56
- B. 2001:db8::16::1b:2000:56
- C. 2001:db8:16::1b:2:56
- D. 2001:db8:0:16::1b:2000:56

**Answer:** D. 2001:db8:0:16::1b:2000:56

**Explanation:** IPv6 compression rules allow only ONE "::" per address (which eliminates options A and B immediately), and leading zeros may only be dropped within a group — 2000 must stay 2000 (it cannot become 2), and 0056 becomes 56. Option C wrongly rewrites 2000 as 2. Option D correctly drops leading zeros (0db8→db8, 0000→0, 0016→16, 001b→1b, 0056→56) and uses a single "::" for the remaining zero group.

---

## Q7

**Question:** Which address is included in the 192.168.200.0/24network?

**Type:** single

**Options:**

- A. 192.168.200.13
- B. 192.168.201.13 (the PDF prints this option label as "3." — preserved note)
- C. 192.168.1.13
- D. 192.168.199.13

**Answer:** A. 192.168.200.13

**Explanation:** Duplicate of Q5 with the options in a different order. The 192.168.200.0/24 network only contains addresses in the range 192.168.200.1 – 192.168.200.254, so 192.168.200.13 is the only valid choice. ⚠️ In the PDF the second option is mislabeled "3." instead of "B." — this typo was preserved.

---

## Q8

**Question:** Which address is a link-local IPV6address?

**Type:** single

**Options:**

- A. FDF8:F535:82EF::53
- B. FE80::261:2EFE:FE10:765
- C. 2001:0db8:85a3:0000:0000:8a2e:0370:7334
- D. 2401:db00:21:70e4:face:0:3:0

**Answer:** B. FE80::261:2EFE:FE10:765

**Explanation:** IPv6 link-local addresses always begin with FE80::/10. The other addresses are a ULA (FDF8...), a global unicast (2001:0db8...), and a global unicast (2401:db00...).

---

## Q9

**Question:** At which OSI layer is the data stream broken up into segments that include source and destination port numbers?

**Type:** single

**Options:**

- A. Network
- B. Session
- C. Transport
- D. Data Link

**Answer:** C. Transport

**Explanation:** The Transport layer (Layer 4) segments the data stream and adds a header containing source and destination port numbers (TCP or UDP).

---

## Q10

**Question:** Which information is included in the header of UDP segment?

**Type:** single

**Options:**

- A. Port Numbers
- B. IP Address
- C. Sequence Numbers
- D. Mac Address

**Answer:** A. Port Numbers

**Explanation:** A UDP segment header contains only source port, destination port, length, and checksum. IP addresses belong to the Layer 3 header, MAC addresses to the Layer 2 header, and UDP has no sequence numbers (that is a TCP feature).

---

## Q11

**Question:** During the data encapsulation process which OSI layer adds a header that contains MAC addressing information and a trailer used for error `[checking]`

**Type:** single

**Options:**

- A. Network
- B. Session
- C. Transport
- D. Data Link

**Answer:** D. Data Link

**Explanation:** The Data Link layer (Layer 2) builds frames: it adds a header with source and destination MAC addresses and a trailer containing a Frame Check Sequence (FCS) used for error detection.

---

## Q12

**Question:** Which protocol allows you to securely upload files to another computer on the internet?

**Type:** single

**Options:**

- A. SFTP
- B. HTTP
- C. NTP
- D. ICMP

**Answer:** A. SFTP

**Explanation:** SFTP (Secure File Transfer Protocol / SSH File Transfer Protocol) encrypts file transfers over an SSH connection on TCP port 22. HTTP is unencrypted, NTP is for time synchronization, and ICMP is for diagnostics.

---

## Q13

**Question:** Move each of the protocol on the left to its their characteristics on the right

**Type:** matching

**Options (protocols):**

- SFTP
- TFTP
- DNS
- DHCP
- ICMP

**Match To (characteristics):**

- Enables the use of SSH keys to prevent impostor from connecting to the server.
- Ensures data integrity and data security for the file transfers using port 22.
- Enables backup of network and router configuration files using UDP.
- Transfer small files within a LAN using port 69.
- Perform a query to translate companypro.net to an IP Address.
- Assign the reserved IP Address 10.10.10.200 to a web server at your company.
- Perform a ping to ensure that a server is responding to network connections.

**Answer:** SFTP → Enables the use of SSH keys to prevent impostor from connecting to the server; SFTP → Ensures data integrity and data security for the file transfers using port 22; TFTP → Enables backup of network and router configuration files using UDP; TFTP → Transfer small files within a LAN using port 69; DNS → Perform a query to translate companypro.net to an IP Address; DHCP → Assign the reserved IP Address 10.10.10.200 to a web server at your company; ICMP → Perform a ping to ensure that a server is responding to network connections.

**Explanation:** SFTP runs over SSH (port 22) and supports SSH-key authentication. TFTP uses UDP port 69 and is commonly used for transferring configuration files and small files within a LAN. DNS resolves names to IP addresses; DHCP assigns IP addresses (including reserved/reservation addresses); ICMP is the protocol used by ping.

---

## Q14

**Question:** Move each protocol or device type from the list on the left to the correct OSI layer on the right.

**Type:** matching

**Options (protocols and devices):**

- SMTP, FTP
- TCP, UDP
- Cable, Hub, NIC
- Switch
- Router

**Match To (OSI layers):**

- Physical
- Data Link
- Network
- Application
- Transport

**Answer:** SMTP, FTP → Application; TCP, UDP → Transport; Cable, Hub, NIC → Physical (as shown in the reviewer image); Switch → Data Link; Router → Network.

**Explanation:** Application-layer protocols include SMTP and FTP; TCP and UDP are Transport-layer protocols; a switch operates at Layer 2 (Data Link) and a router at Layer 3 (Network). ⚠️ Note: The reviewer places the NIC at the Physical layer together with cable and hub. This is questionable — a NIC is generally considered to operate at Layer 2 (Data Link) as well as Layer 1, and most CCNA/CCST curricula classify the NIC at the Data Link layer. The reviewer's grouping was preserved as shown.

---

## Q15

**Question:** Move each protocol from the list on the left to the correct TCP/IP model layer on the right.

**Type:** matching

**Options (protocols):**

- TCP
- IP
- FTP
- Ethernet

**Match To (TCP/IP model layers):**

- Internetwork
- Application
- Transport
- Network

**Answer:** TCP → Transport; IP → Internetwork; FTP → Application; Ethernet → Network (as labeled in the reviewer).

**Explanation:** In the TCP/IP model, TCP is the Transport layer protocol, IP is the Internetwork layer protocol, and FTP is an Application layer protocol. Ethernet maps to the bottom (network access/link) layer. ⚠️ Note: The TCP/IP model's bottom layer is properly called "Network Access" (or Link); the reviewer labels it "Network," which is preserved as shown.

---

## Q16

**Question:** Move each category on the left to its correct definition on the right

**Type:** matching

**Options (categories):**

- LAN
- PAN
- WAN

**Match To (definitions):**

- Connects devices such as computers, telephones, tables, and printers within a range of about 10 meters.
- Spans a small area such as a room, home, office building or small group of building.
- Spans a large geographical distance and connects smaller networks over leased lines and VPN's or tunnels.

**Answer:** PAN → Connects devices such as computers, telephones, tables, and printers within a range of about 10 meters; LAN → Spans a small area such as a room, home, office building or small group of building; WAN → Spans a large geographical distance and connects smaller networks over leased lines and VPN's or tunnels.

**Explanation:** A PAN (Personal Area Network, e.g., Bluetooth) covers roughly 10 meters; a LAN covers a small site such as a home or office building; a WAN spans large geographic distances, often over leased lines or VPN tunnels.

---

## Q17

**Question:** Which command will display all the current operational settings configured on a Cisco router?

**Type:** single

**Options:**

- A. show protocols
- B. show startup-config
- C. show version
- D. show running-config

**Answer:** D. show running-config

**Explanation:** The show running-config command displays the currently active (operational) configuration in RAM. show startup-config shows the saved configuration in NVRAM (which only matches the running config if it has been saved), and show version shows hardware/software information.

---

## Q18

**Question:** For each statement about bandwidth and throughput. Select True or False

**Type:** true_false

**Options:**

- High levels of network latency decreases network `[cut off in PDF — presumably "throughput"]`
- Low Bandwidth can increase network `[cut off in PDF]`
- You can increase throughput by decreasing network `[cut off in PDF — presumably "latency"]`

**Answer:** Statement 1 — True; Statement 2 — True (inferred); Statement 3 — True (inferred).

**Explanation:** ⚠️ All three statements are cut off at the end in the PDF, so the answers are inferred from the visible fragments and standard networking knowledge: (1) High latency reduces effective throughput — True; (2) Low bandwidth can increase network delay/congestion — True; (3) Decreasing latency improves throughput — True. Verify against a complete copy of the reviewer if available.

---

## Q19

**Question:** Move each cloud computing service model from the list on the left to the correct example on the `[right]`

**Type:** matching

**Options (service models):**

- IAAS
- SAAS
- PAAS

**Match To (examples):**

- A company develops application using cloud-based resources and `[cut off in PDF]`
- These virtual machines are connected by a virtual network in the cloud
- User access a web-based graphics design application in the cloud for a monthly fee

**Answer:** PAAS → A company develops application using cloud-based resources; IAAS → These virtual machines are connected by a virtual network in the cloud; SAAS → User access a web-based graphics design application in the cloud for a monthly fee.

**Explanation:** PaaS provides a platform for developing applications; IaaS provides virtualized infrastructure (VMs, virtual networks, storage); SaaS delivers finished applications over the internet on a subscription basis.

---

## Q20

**Question:** Move each cloud service model on the left to its correct description on the right.

**Type:** matching

**Options (service models):**

- IAAS
- SAAS
- PAAS

**Match To (descriptions):**

- Provides the hardware and software needed for developing, running, and managing applications.
- Provide pay-as-you-go access to resources provided on virtual machines and virtual storage.
- Provide on-demand access to applications delivered remotely over the internet.

**Answer:** PAAS → Provides the hardware and software needed for developing, running, and managing applications; IAAS → Provide pay-as-you-go access to resources provided on virtual machines and virtual storage; SAAS → Provide on-demand access to applications delivered remotely over the internet.

**Explanation:** PaaS = platform for building/running apps; IaaS = pay-as-you-go compute/storage infrastructure; SaaS = on-demand applications over the internet.

---

## Q21

**Question:** Which protocol does an IPv6host use to resolve the MAC address associated with a destination IPv6address?

**Type:** single

**Options:**

- A. Address Resolution Protocol (ARP)
- B. Cisco Discovery Protocol (CDP)
- C. Neighbor Discovery Protocol (NDP)
- D. Dynamic Host Configuration Protocol (DHCP)

**Answer:** C. Neighbor Discovery Protocol (NDP)

**Explanation:** IPv6 does not use ARP; it uses Neighbor Discovery Protocol (NDP), which operates with ICMPv6, to resolve IPv6 addresses to MAC addresses.

---

## Q22

**Question:** Which protocol is used by IPV6enabled host to perform automatic stateless address configuration?

**Type:** single

**Options:**

- A. DHCPV6
- B. ICMPV6
- C. TFTP
- D. DNS

**Answer:** B. ICMPV6

**Explanation:** Stateless address autoconfiguration (SLAAC) is performed using ICMPv6 Router Solicitation and Router Advertisement messages. DHCPv6 is used for stateful address assignment, which is a different mechanism.

---

## Q23

**Question:** During the data encapsulation process, which OSI layer adds a header that contains MAC addressing information and a trailer used for error checking?

**Type:** single

**Options:**

- A. Network
- B. Transport
- C. Data Link
- D. Session

**Answer:** C. Data Link

**Explanation:** Duplicate of Q11 with different option order. The Data Link layer adds the MAC-address header and the FCS error-checking trailer to form a frame.

---

## Q24

**Question:** A user initiates a trouble ticket stating that an external web page is not loading. You determine that other resources both internal and external are still reachable. Which command can you use to help locate where the issue is in the network path to the external web page?

**Type:** single

**Options:**

- A. ping -t
- B. tracert
- C. ipconfig/all
- D. nslookup

**Answer:** B. tracert

**Explanation:** tracert traces the path packet-by-packet (hop by hop) to the destination, letting you see exactly where along the path the traffic stops — ideal for "one specific site unreachable" scenarios. Since internal and other external resources work, DNS (nslookup) and basic connectivity (ping) are less targeted.

---

## Q25

**Question:** Which two statements are true about the IPv4address of the default gateway configured on a host? (Choose 2.) Note: You will receive partial credit for each correct

**Type:** multiple

**Options:**

- A. The IPv4address of the default gateway must be the first host address in the subnet.
- B. The same default gateway IPv4address is configured on each host on the local network.
- C. The default gateway is the Loopback0interface IPv4address of the router connected to the same local network as the host.
- D. The default gateway is the IPv4address of the router interface connected to the same local network as the host.
- E. Hosts learn the default gateway IPv4address through router advertisement

**Answer:** B and D

**Explanation:** All hosts on the local network must use the same default gateway address — the address of the router interface on that local network (Layer 3 gateway). It does not have to be the first usable address (A is false), it is not a loopback address (C is false), and IPv4 hosts do not learn the gateway via router advertisements — that is an IPv6 mechanism (E is false).

---

## Q26

**Question:** Which two statements are true about the IPv4address of the default gateway configured on a host? (Choose 2.) Note: You will receive partial credit for each correct

**Type:** multiple

**Options:**

- A. The IPv4address of the default gateway must be the first host address in the subnet.
- B. The same default gateway IPv4address is configured on each host on the local network.
- C. The default gateway is the Loopback0interface IPv4address of the router connected to the same local network as the host.
- D. The default gateway is the IPv4address of the router interface connected to the same local network as the host.
- E. Hosts learn the default gateway IPv4address through router advertisement

**Answer:** B and D

**Explanation:** Exact duplicate of Q25. The default gateway is the router interface address on the local network, and every host on that network uses the same gateway address.

---

## Q27

**Question:** An engineer configured a new VLAN named VLAN2for the Data Center team. When the team tries to ping addresses outside VLAN2from a computer in VLAN2, they are unable to reach them. What should the engineer configure?

**Type:** single

**Options:**

- A. Additional VLAN
- B. Default route
- C. Default gateway
- D. Static route

**Answer:** C. Default gateway

**Explanation:** A computer needs a default gateway to reach destinations outside its own local VLAN/subnet. Without a gateway, only local VLAN traffic works — matching the symptom described.

---

## Q28

**Question:** Which information is included in the header of a UDP segment?

**Type:** single

**Options:**

- A. IP addresses
- B. Sequence numbers
- C. Port numbers
- D. MAC addresses

**Answer:** C. Port numbers

**Explanation:** Duplicate of Q10 with different option order. The UDP header contains source and destination port numbers (plus length and checksum). IP addresses are in the Layer 3 header, MAC addresses in the Layer 2 header, and sequence numbers are a TCP feature.

---

## Q29

**Question:** What is the purpose of assigning an IPaddress to the management VLAN interface on a Layer 2switch?

**Type:** single

**Options:**

- A. To enable access to the CLI on the switch through Telnet or SSH
- B. To enable the switch to provide DHCP services to other switches in the network
- C. To enable the switch to act as a default gateway for the attached devices
- D. To enable the switch to resolve URLs for the attached the devices

**Answer:** A. To enable access to the CLI on the switch through Telnet or SSH

**Explanation:** A Layer 2 switch needs an IP address on its management (SVI) interface so it can be managed remotely via Telnet or SSH. A pure Layer 2 switch does not route (so it cannot be a default gateway), does not resolve URLs, and does not provide DHCP services by default.

---

## Q30

**Question:** Which of the following is a characteristic of the Spanning Tree Protocol (STP)?

**Type:** single

**Options:**

- A. prevents loops in a network by blocking redundant links.
- B. provides load balancing across multiple paths in a network.
- C. prioritizes network traffic based on Quality of Service (QoS)settings.
- D. allows for rapid convergence by eliminating the need for spanning tree

**Answer:** A. prevents loops in a network by blocking redundant links.

**Explanation:** STP's sole purpose is to prevent Layer 2 loops in networks with redundant links by placing redundant ports into a blocking state, creating a loop-free logical topology.

---

## Q31

**Question:** What protocol is used by OSPF to form neighbor relationships and exchange routing information?

**Type:** single

**Options:**

- A. CP (Control Protocol)
- B. P (Protocol)
- C. MP (Multiprotocol)
- D. Llo (Link-Local Operations)

**Answer:** B. P (Protocol)

**Explanation:** ⚠️ The PDF options are clearly truncated (only fragments remain: "CP", "P", "MP", "Llo"), so the exact option wording and the reviewer's intended answer cannot be fully verified. Technically, OSPF does not use TCP or UDP — its messages (including Hello packets used to form neighbor relationships) are encapsulated directly in IP (IP protocol number 89), so the intended answer is the IP option, corresponding to option B as printed.

---

## Q32

**Question:** What information is contained in the MAC address table of a switch?

**Type:** single

**Options:**

- A. Dynamically learned Layer2and Layer3addresses of devices communicating on active ports on the switch
- B. The MAC addresses of devices communicating on active ports and static MAC addresses configured by the administrator
- C. All active ports on the switch and the host Layer3addresses that were dynamically learned on each port.
- D. MAC addresses to IP Address mappings learned through ARP requests or manually configured by the administrator

**Answer:** B. The MAC addresses of devices communicating on active ports and static MAC addresses configured by the administrator

**Explanation:** A switch MAC address table maps MAC addresses to ports. It contains dynamically learned entries plus any static MAC addresses configured by the administrator. Layer 3 (IP) information is not stored in the MAC table — option D describes an ARP table, not a MAC address table.

---

## Q33

**Question:** What is the purpose of a subnet mask?

**Type:** single

**Options:**

- A. determine the network portion of an IP address
- B. determine the host portion of an IP address
- C. determine the default gateway for a network
- D. determine the DNS server for a network

**Answer:** A. determine the network portion of an IP address

**Explanation:** The subnet mask's primary purpose is to identify which part of an IP address is the network portion (the bits where the mask is 1). ⚠️ Note: By extension it also reveals the host portion (option B), since the mask divides the address into the two parts, but the reviewer treats A as the best answer — a subnet mask has nothing to do with gateways or DNS servers.

---

## Q34

**Question:** A user at you company cannot connect to website on the internet. However, they can connect to network resources on the company LAN. You want to use the divide and conquer approach to troubleshoot the issue. What should you do first?

**Type:** single

**Options:**

- A. Run the Telnet command from the user's computer
- B. Ping the default gateway from the user's computer
- C. Check the computer's cable connections
- D. Check the computer's network adapter

**Answer:** B. Ping the default gateway from the user's computer

**Explanation:** With the divide-and-conquer method you start at the middle of the OSI stack (Layer 3) rather than at the bottom. Since LAN access works, Layers 1–2 are likely fine; pinging the default gateway tests Layer 3 and immediately tells you which half of the stack to investigate.

---

## Q35

**Question:** Your company has 20Cisco switches throughout its building. You need to view the configuration of each switch from the command line. Which protocol should you use?

**Type:** single

**Options:**

- A. FTP (File Transfer Protocol)
- B. RDP (Remote Desktop Protocol)
- C. SMTP (Simple Mail Transfer Protocol)
- D. SNMP (Simple Network Management Protocol)

**Answer:** D. SNMP (Simple Network Management Protocol)

**Explanation:** Among the listed options, SNMP is the network management protocol used to access and collect data from network devices. ⚠️ Note: In real practice, viewing a switch's configuration from the command line is done via SSH (or Telnet), which is not offered as an option here; given the choices, the reviewer intends SNMP as the management protocol answer.

---

## Q36

**Question:** Which device protects the network by permitting or denying traffic based on IP address, port number, or application?

**Type:** single

**Options:**

- A. Firewall
- B. Access point
- C. VPN gateway
- D. Intrusion detection system

**Answer:** A. Firewall

**Explanation:** A firewall filters traffic based on rules that examine source/destination IP addresses, port numbers, protocols, and applications, permitting or denying traffic accordingly.

---

## Q37

**Question:** How does a firewall determine which traffic to block?

**Type:** single

**Options:**

- A. The firewall matches traffic based on the IP address in the ARP table
- B. The firewall performs a one-to-many network address translation
- C. The firewall matches the traffic based on source and destination IP address
- D. The firewall performs a one-to-one network address `[translation]`

**Answer:** C. The firewall matches the traffic based on source and destination IP address

**Explanation:** Firewalls examine traffic against configured rules — matching attributes such as source and destination IP addresses (as well as ports and protocols) — to decide whether to permit or deny. NAT functions (options B and D) are address translation, not traffic filtering logic, and the ARP table (option A) is unrelated to firewall rule decisions.

---

## Q38

**Question:** You plan to use a network firewall to protect computers at a small `[office / business]`

**Type:** true_false

**Options:**

- A firewall can block traffic to specific ports on internal computers.
- A firewall can direct all web traffic to a specific IP address.
- A firewall can prevent specific apps from running on a computer.

**Answer:** Statement 1 — True; Statement 2 — True; Statement 3 — False.

**Explanation:** As indicated in the reviewer: A firewall can filter traffic by port (True), and it can redirect/direct traffic such as web traffic to a specific address (True) — but preventing applications from running on a computer is endpoint/application-control software functionality, not a network firewall function (False).

---

## Q39

**Question:** Which best describes confidentiality with regards to network security?

**Type:** single

**Options:**

- A. Ensures data is available for access by providing redundant systems.
- B. Ensures data is not changed during transit between system.
- C. Ensures data is kept secret using safeguards to prevent unauthorized access.
- D. Ensures data is trusted and has not been tampered with or changed

**Answer:** C. Ensures data is kept secret using safeguards to prevent unauthorized access.

**Explanation:** Confidentiality means keeping data secret from unauthorized parties. Option A describes availability, while options B and D describe integrity.

---

## Q40

**Question:** Which component of the AAA service security model provides identify verification?

**Type:** single

**Options:**

- A. Authentication
- B. Accounting
- C. Auditing
- D. Authorization

**Answer:** A. Authentication

**Explanation:** Authentication is the "who are you?" step of AAA — it verifies identity (e.g., username/password, certificates). Authorization defines what a user may do, and accounting records what the user did.

---

## Q41

**Question:** When setting up a wireless network which security benefit is provided by enabling WPA3?

**Type:** single

**Options:**

- A. Limits network access to only specified devices
- B. Sends traffic through an encrypted tunnel
- C. Secures authentication between client and access point
- D. Makes it more difficult to discover wireless network

**Answer:** C. Secures authentication between client and access point

**Explanation:** WPA3's headline improvement is Simultaneous Authentication of Equals (SAE), which replaces the WPA2 PSK 4-way handshake and secures the client-to-access-point authentication exchange (resistant to offline dictionary attacks). Encryption of traffic already existed in WPA2; "encrypted tunnel" (option B) describes a VPN, not WPA3.

---

## Q42

**Question:** Move the CIA security principles from the list on the left to its example on the right.

**Type:** matching

**Options (CIA principles):**

- Confidentiality
- Integrity
- Availability

**Match To (examples):**

- You generate a digital signature and attach it to a message
- You encrypt a sensitive email message
- You configure three redundant web servers at your company

**Answer:** Integrity → You generate a digital signature and attach it to a message; Confidentiality → You encrypt a sensitive email message; Availability → You configure three redundant web servers at your company.

**Explanation:** Digital signatures prove a message was not altered (integrity). Encryption keeps content secret (confidentiality). Redundant servers keep services up (availability).

---

## Q43

**Question:** Move the MFA factors from the list on the left to their correct examples on he right Factors: Possession, Inference, Knowledge

**Type:** matching

**Options (factors):**

- Possession
- Inference
- Knowledge

**Match To (examples):**

- Specifying your name and password to log on to a service
- Entering a one-time security code send to your device after logging in
- Holding your phone to your face to be recognized

**Answer:** Knowledge → Specifying your name and password to log on to a service; Possession → Entering a one-time security code send to your device after logging in; Inherence → Holding your phone to your face to be recognized.

**Explanation:** Something you know = password; something you have = the device receiving the one-time code; something you are = biometric face recognition. ⚠️ Note: The PDF's factor list says "Inference" but the shown answer uses "Inherence" — the correct MFA term is Inherence (biometrics). Both spellings are preserved as they appear.

---

## Q44

**Question:** Move the security options from the list on the left to its characteristics on the right. You may use each security option once, more than once, or not at `[all]`

**Type:** matching

**Options (security options):**

- WEP
- WPA2-Personal
- WPA-Enterprise

**Match To (characteristics):**

- Uses a minimum of 40bits for encryption
- Use a RADIU Server for authentication
- Use AES and a pre-shared key for authentication

**Answer:** WEP → Uses a minimum of 40bits for encryption; WPA-Enterprise → Use a RADIU Server for authentication; WPA2-Personal → Use AES and a pre-shared key for authentication.

**Explanation:** WEP is the legacy, weak standard using 40-bit (or 104-bit) keys. WPA/WPA2-Enterprise authenticate users against a RADIUS server (802.1X). WPA2-Personal uses AES-CCMP with a pre-shared key (PSK). ⚠️ Note: "RADIU" is a typo in the PDF for "RADIUS" — preserved as written.

---

## Q45

**Question:** You need to configure wireless settings for a home router. Move the actions from the list on the left to the correct scenarios on the `[right]`

**Type:** matching

**Options (actions):**

- Disable SSID broadcasting
- Set the security mode to WPA2-PSK
- Disable WPS

**Match To (scenarios):**

- You want to prevent users from using the pushbutton method for accessing the `[network]`
- You want devices to use a pre-shared key when connecting to the network.
- You want to prevent devices from discovering the name of the WIFI network

**Answer:** Disable WPS → You want to prevent users from using the pushbutton method for accessing the network; Set the security mode to WPA2-PSK → You want devices to use a pre-shared key when connecting to the network; Disable SSID broadcasting → You want to prevent devices from discovering the name of the WIFI network.

**Explanation:** WPS (Wi-Fi Protected Setup) is the pushbutton/PIN easy-join method — disabling it blocks that method. WPA2-PSK mode uses a pre-shared key. Disabling SSID broadcast hides the network name from casual discovery.

---

## Q46

**Question:** Which component of the AAA service security model provides identity verification?

**Type:** single

**Options:**

- A. Authorization
- B. Auditing
- C. Authentication
- D. Accounting

**Answer:** C. Authentication

**Explanation:** Duplicate of Q40 with different option order. Authentication is the AAA component that verifies identity.

---

## Q47

**Question:** Which wireless security option uses a pre-shared key to authenticate clients?

**Type:** single

**Options:**

- A. WPA2-Personal
- B. 802.1x
- C. 802.1q
- D. WPA2-Enterprise

**Answer:** A. WPA2-Personal

**Explanation:** WPA2-Personal (WPA2-PSK) authenticates clients using a pre-shared key known by everyone on the network. WPA2-Enterprise uses 802.1X/RADIUS per-user authentication; 802.1Q is VLAN tagging, a security non-sequitur.

---

## Q48

**Question:** You need to connect a computer's network adapter to a switch using a 1000BASE-T cable. Which connector should you use?

**Type:** single

**Options:**

- A. Coax
- B. RJ-11
- C. OS2LC
- D. RJ-45

**Answer:** D. RJ-45

**Explanation:** 1000BASE-T is Gigabit Ethernet over twisted-pair copper cable, terminated with RJ-45 connectors. RJ-11 is for telephone lines, and OS2LC is a fiber connector.

---

## Q49

**Question:** Which type of connector should you use to terminate unshielded twisted pair (UTP)cable?

**Type:** single

**Options:**

- A. ST (Straight Tip)
- B. SC (Subscriber Connector)
- C. RJ-45(Registered Jack 45)
- D. OS2LC

**Answer:** C. RJ-45(Registered Jack 45)

**Explanation:** UTP (twisted-pair copper Ethernet cable) is terminated with RJ-45 connectors. ST, SC, and LC are all fiber-optic connector types.

---

## Q50

**Question:** You want to store files that will be accessible by every user on your network. Which endpoint device do you need?

**Type:** single

**Options:**

- A. Access point
- B. Server
- C. Hub
- D. Switch

**Answer:** B. Server

**Explanation:** A file server stores files and makes them accessible to all users on the network. Access points, hubs, and switches are connectivity devices, not storage endpoints.

---

## Q51

**Question:** What type of interface is the administrator installing in the router? `[image shows a small pluggable transceiver being inserted into a router/switch module slot]`

**Type:** image_single

**Options:**

- A. USB (Universal Serial Bus)
- B. SFP (Small Form-factor Pluggable)
- C. Serial
- D. PoE (Power over Ethernet)

**Answer:** B. SFP (Small Form-factor Pluggable)

**Explanation:** The image shows a small hot-pluggable transceiver module being inserted into a module slot — that is an SFP interface, used to add fiber or copper uplink ports to a router or switch.

---

## Q52

**Question:** A Cisco PoE switch is shown in the following image.Which type of port will provide both data connectivity and power to an IP phone?

**Type:** image_single

**Options:**

- A. Port identified with number 2
- B. Ports identified with number 6
- C. Ports identified with number 7
- D. Ports identified with number 3and `[cut off in PDF — presumably "number 4"]`

**Answer:** B. Ports identified with number 6

**Explanation:** In the switch image, the ports labeled 6 are the RJ-45 Ethernet ports that support Power over Ethernet, delivering both data and power to devices such as IP phones. (Port 2 is the console port, 3/4 are management/function ports, and 7 marks the SFP fiber ports.) ⚠️ Option D is cut off in the PDF ("number 3and ..."), and the option order in this reviewer differs from other circulating versions of this question — the keyed answer is "ports identified with number 6," which is option B in this PDF's ordering.

---

## Q53

**Question:** Which standard contains the specifications for Wi-Fi networks?

**Type:** single

**Options:**

- A. GSM
- B. LTE
- C. IEEE 802.11
- D. IEEE 802.3
- E. EIA/TIA 568A

**Answer:** C. IEEE 802.11

**Explanation:** Wi-Fi is defined by the IEEE 802.11 family of standards. IEEE 802.3 is Ethernet (wired LAN), GSM/LTE are cellular standards, and EIA/TIA 568A is a cabling/wiring standard.

---

## Q54

**Question:** Which device is an Internet of Things (IoT)device?

**Type:** single

**Options:**

- A. An internet-accessible thermostat
- B. A video streaming server
- C. A virtual private network concentrator
- D. A Cloud-based file storage array

**Answer:** A. An internet-accessible thermostat

**Explanation:** An IoT device is an everyday physical object with embedded network connectivity — a smart thermostat is the classic example. Servers, VPN concentrators, and storage arrays are infrastructure devices, not IoT endpoints.

---

## Q55

**Question:** Which network technology is not impacted by electromagnetic and radio wave interference?

**Type:** single

**Options:**

- A. Wireless
- B. Twisted Pair
- C. Fiber
- D. Copper

**Answer:** C. Fiber

**Explanation:** Fiber-optic cable transmits data as light through glass/plastic, so it is completely immune to electromagnetic interference (EMI) and radio-frequency interference (RFI). All copper media (twisted pair included) and wireless are susceptible.

---

## Q56

**Question:** A cisco switch is not accessible from the network. You need to view its running configuration. Which out of band method can you use to access it?

**Type:** single

**Options:**

- A. SSH
- B. SNMP
- C. Console
- D. Telnet

**Answer:** C. Console

**Explanation:** The console port provides out-of-band management — a direct local connection that works even when the switch has no network (IP) connectivity. SSH, SNMP, and Telnet are all in-band methods requiring network access.

---

## Q57

**Question:** Examine the connections shown in the following image. Move the cable types on the right to the appropriate connection description on the left. You may use each cable type more than once or not at `[all]`

**Type:** image_matching

**Options (cable types):**

- Straight-through UTP Cable
- Fiber Optic Cable
- Crossover UTP Cable

**Match To (connections):**

- Connects Switch to Router R1Gi0/0/1interface
- Connects Router R2Gi0/0/0to Router R3Gi0/0/0via underground conduit
- Connects Router R1Gi0/0/0to Router R2Gi0/0/1
- Connects Switch S3to Server0network interface card

**Answer:** Straight-through UTP Cable → Connects Switch S1 to Router R1 Gi0/0/1 interface; Fiber Optic Cable → Connects Router R2 Gi0/0/0 to Router R3 Gi0/0/0 via underground conduit; Crossover UTP Cable → Connects Router R1 Gi0/0/0 to Router R2 Gi0/0/1; Straight-through UTP Cable → Connects Switch S3 to Server0 network interface card.

**Explanation:** Unlike devices (switch-to-router, switch-to-server/PC) use straight-through UTP; like devices (router-to-router) use crossover UTP; the long underground run between buildings uses fiber optic cable.

---

## Q58

**Question:** A local company requires two networks in two new buildings. The addresses used in these networks must be in the private network range. Which two address ranges should the company use? (Choose `[two]`)`

**Type:** multiple

**Options:**

- A. 172.16.0.0to 172.31.255.255
- B. 192.16.0.0to 192.16.255.255
- C. 11.0.0.0to 11.255.255.255
- D. 192.168.0.0to `[cut off in PDF — presumably 192.168.255.255]`

**Answer:** A and D

**Explanation:** The RFC 1918 private address ranges are 10.0.0.0–10.255.255.255, 172.16.0.0–172.31.255.255, and 192.168.0.0–192.168.255.255. Options B (192.16.x.x) and C (11.x.x.x) are public ranges. ⚠️ Option D's ending is cut off in the PDF but is clearly the 192.168.0.0 – 192.168.255.255 private range.

---

## Q59

**Question:** Which two conclusions can you make from the output of the tracert command? (Choose `[two]`) `[image shows a tracert to www.cisco.com over IPv6 with two intermediate "Request timed out" hops]`

**Type:** image_multiple

**Options:**

- A. The trace successfully reached the www.cisco.comserver.
- B. The trace failed after the fourth hop.
- C. The IPv6address associated with the www.cisco.com server is 2600:1408:c400:38d::b33.
- D. The routers at hops 5and 6are offline.
- E. The device sending the trace has IPv6address 2600:1408:c400:38d:: `[cut off in PDF]`

**Answer:** A and C

**Explanation:** ⚠️ The tracert output image is largely illegible in the PDF (OCR garbage). Based on the standard version of this question: although two intermediate hops return "Request timed out" (those routers simply do not respond to ICMP time-exceeded messages), the trace continues and completes, so the destination was successfully reached (A), and the final hop reveals the destination's IPv6 address (C). The timed-out hops are not offline — traffic still passed through them (D is false) — and the trace clearly did not fail after hop 4 (B is false). Option E is cut off and describes a source-address claim not supported by tracert output.

---

## Q60

**Question:** Which two pieces of information should you include when you initially create a support ticket? (Choose `[two]`)`

**Type:** multiple

**Options:**

- A. A detailed description of the fault
- B. Details about the computers connected to the network
- C. A description of the conditions when the fault occurs
- D. The actions taken to resolve the fault
- E. The description of the top-down fault-finding procedure

**Answer:** A and C

**Explanation:** At ticket creation you document what the fault is (a detailed description) and the conditions under which it occurs. Actions taken to resolve (D) are documented later as the ticket progresses, and network inventory details (B) or the troubleshooting procedure used (E) are not part of the initial ticket.

---

## Q61

**Question:** Which two statements are true about the IPv4address of the default gateway configured on a host? (Choose `[two]`)`

**Type:** multiple

**Options:**

- A. The IPv4address of the default gateway must be the first host address in the subnet.
- B. The same default gateway IPv4address is configured on each host on the local network.
- C. The default gateway is the Loopback0interface IPv4address of the router connected to the same local network as the host.
- D. The default gateway is the IPv4address of the router interface connected to the same local network as the host.
- E. Hosts learn the default gateway IPv4address through router advertisement

**Answer:** B and D

**Explanation:** Exact duplicate of Q25/Q26 (third occurrence). The default gateway is the address of the router interface on the local network, shared by all hosts on that network.

---

## Q62

**Question:** An administrator is configuring the host PC-A on the network shown in the following graphic. PC-A must be able to communicate on the local network and on the internet. There is no DHCP server on the network. What information does the administrator need to input in the IPV4protocol properties window?

**Type:** image_command

**Answer:** IP address: a valid unused host address in the 172.100.0.0/16 network (e.g., 172.100.0.10); Subnet mask: 255.255.0.0; Default gateway: 172.100.0.1 (the Router1 G0/0 interface); Preferred DNS server: 172.100.0.254.

**Explanation:** With no DHCP server, all IPv4 settings must be static. From the topology: the network is 172.100.0.0/16 (mask 255.255.0.0), the router interface G0/0 (the default gateway for this LAN) is 172.100.0.1, and the local DNS server shown is 172.100.0.254 — the ISP DNS is not reachable for name resolution without the gateway configured.

---

## Q63

**Question:** A help desk technician receives the four trouble tickets listed below. Which ticket should receive the highest priority and be addressed first?

**Type:** single

**Options:**

- A. Ticket 1: A user requests relocation of a printer to a different network jack in the same office. The jack must be patched and made active.
- B. Ticket 2: An online webinar is taking place in the conference room. The video conferencing equipment lost internet access.
- C. Ticket 3: A user reports that response time for a cloud-based application is slower than usual.
- D. Ticket 4: Two users report that wireless access in the cafeteria has been down for the last `[cut off in PDF]`

**Answer:** B. Ticket 2: An online webinar is taking place in the conference room. The video conferencing equipment lost internet access.

**Explanation:** Ticket priority is based on impact and urgency. Ticket 2 affects a live event with multiple participants right now (high urgency, high business impact). Ticket 1 is a routine move/add/change; Ticket 3 is degraded (not down) performance; Ticket 4 is an outage but in a cafeteria (lower business impact than a live webinar). ⚠️ Option D is cut off in the PDF ("...down for the last" — presumably "few days/hours").

---

## Q64

**Question:** An engineer configured a new VLAN named VLAN2for the Data Center team. When the team tries to ping addresses outside VLAN2from a computer in VLAN2, they are unable to reach them. What should the engineer configure?

**Type:** single

**Options:**

- A. Additional VLAN
- B. Default route
- C. Default gateway
- D. Static route

**Answer:** C. Default gateway

**Explanation:** Exact duplicate of Q27. Hosts in VLAN2 need a default gateway to send traffic to destinations outside their local subnet/VLAN.

---

## Q65

**Question:** You are a senior network administrator tasked with diagnosing intermittent connectivity issues on the executive floor of a multinational corporation, which primarily uses iOS devices. After initial checks, you suspect that the problem may be related to SSID settings and network configuration specifics not aligning correctly with the corporate security protocols. Given the high-security requirements and the exclusive use of iOS devices on this floor, which approach should you take to verify and rectify the network settings directly on the affected devices?

**Type:** single

**Options:**

- A. Network Reset
- B. Manual Configuration
- C. Use Fing
- D. SSID Reconfiguration

**Answer:** B. Manual Configuration

**Explanation:** To verify and correct SSID/security settings (e.g., exact SSID, WPA2/WPA3-Enterprise mode, certificates) on iOS devices in a high-security environment, you manually inspect and configure the Wi-Fi profile on each affected device. A network reset (A) wipes all settings without verifying them and is too blunt for a targeted security check; Fing (C) is a third-party network scanner, unsuitable for verifying corporate security alignment; SSID reconfiguration (D) implies changing the network infrastructure rather than checking the device. ⚠️ The PDF shows no marked answer for this item; B is the logically intended answer.

---

## Q66

**Question:** Which two statements are true about the impact to communication on the network while the router is temporarily offline. Evaluate the `[following]`

**Type:** image_multiple

**Options:**

- A. None of the PC's can access the file server (File-Srv)
- B. The file server (File-Srv) can still access the internet
- C. PC-A and PC-B can still communicate with each other.
- D. PC-A, PC-B, PC-C and PC-D can still communicate with each other
- E. PC-C and PC-D can still communicate with the file server (File-Srv)

**Answer:** A and C

**Explanation:** In the topology, Switch1 and Switch2 are directly connected at Layer 2, so same-VLAN local traffic keeps flowing: PC-A and PC-B (VLAN 100) can still communicate (C is true). However, every PC is in a different VLAN than the File-Srv (VLAN 10): PC-A/PC-B are in VLAN 100, PC-C/PC-D in VLAN 110. All inter-VLAN traffic must route through Router1, which is offline — so no PC can reach the file server (A is true, E is false), the server cannot reach the internet (B is false), and PCs in different VLANs cannot communicate with each other (D is false).

---

## Q67

**Question:** Which action does Switch1take? PC-AsendsaframetoPC-C Switch1doesnothaveamappingentryfortheMACaddressofPC-C

**Type:** image_single

**Options:**

- A. Switch1queries Switch2for the MAC address of PC-C
- B. Switch1drops the frame and sends an error message back to PC-A
- C. Switch1sends an ARP request to obtain the MAC address of PC-C
- D. Switch1floods the frame out all active ports except port Gi0/1

**Answer:** D. Switch1floods the frame out all active ports except port Gi0/1

**Explanation:** When a switch receives a unicast frame with an unknown destination MAC, it floods the frame out all active ports except the one it arrived on (PC-A is on Gi0/1, so the frame is flooded everywhere else, including the link toward Switch2 where PC-C resides). Switches never send ARP requests on behalf of hosts (the host does that), never "query" other switches, and do not drop unknown unicast or return error messages.

---

## Q68

**Question:** The laptop is connected to port A on the firslswitch. The second switch is connecled to port D on the first switch. The laptop sends a broadcast frame to the first switch. Which ports forward the frame?

**Type:** image_single

**Options:**

- A. D only
- B. A, B and D only
- C. B and C only
- D. B, C and D only

**Answer:** D. B, C and D only

**Explanation:** A broadcast frame is flooded out every active port except the port it was received on. The frame arrived on port A (where the laptop is attached), so it is forwarded out ports B, C, and D — including port D, which carries it to the second switch.

---

## Q69

**Question:** A support technician examines the front panel of a Cisco switch and sees 4Ethernet cables connected in the first four ports. Port 1,2and 3have a green LED. Port 4has a blinking green light. What is the state of the Port 4?

**Type:** single

**Options:**

- A. Link is up and not stable
- B. Link is up and there is no activity
- C. Link is up with cable malfunctions
- D. Link is up and active

**Answer:** D. Link is up and active

**Explanation:** On Cisco switch port LEDs, solid green means link is up with no current activity, while a blinking green LED means the link is up and actively transmitting/receiving traffic.

---

## Q70

**Question:** A user reports a problem connecting to network resources. Other users connected to the same switch are not experiencing the same problem. The user's computer is patched to a switch port Gi0/15. The status indicator for this port is blinking alternately green then amber. What does the light pattern indicate about the status of port Gi0/15?

**Type:** single

**Options:**

- A. The port is administratively shutdown
- B. The port is experiencing a high rate of errors.
- C. The port is blocked by a firewall rule.
- D. The port is not connected to a powered -on `[device]`

**Answer:** B. The port is experiencing a high rate of errors.

**Explanation:** An alternating green/amber blinking pattern on a Cisco switch port indicates the link is up but experiencing errors (typically a high error/collision rate or a link fault condition). An administratively down port shows no light, and an unconnected port shows amber (no link). Firewalls do not influence port LEDs. ⚠️ Option D is cut off in the PDF ("powered -on" ...).

---

## Q71

**Question:** What can you tell from the command output? A user report that a company website is not available. The help desk technician issues a tracert command to determine if the server hosting the website is reachable over the network. The output of the command is shown as follows: `[tracert to 192.168.1.10 — hop 3 shows "Request timed out" but hops 4 and 5 (the destination) reply successfully]`

**Type:** image_single

**Options:**

- A. The server with address 192.168.1.10is reachable over the network
- B. The router at hop 3is not forwarding packets to the IP address 192.168.1.10
- C. Requests to the web server at 192.168.1.10are being delayed and time out.
- D. The server address 192.168.1.10is being blocked by a firewall on the router at `[cut off in PDF]`

**Answer:** A. The server with address 192.168.1.10 is reachable over the network

**Explanation:** The trace completes all the way to hop 5, which is the destination 192.168.1.10 itself responding. The "Request timed out" at hop 3 only means that router does not reply to ICMP TTL-exceeded messages (common due to rate-limiting or policy) — traffic clearly passed through it, since hops 4 and 5 responded. If hop 3 were truly not forwarding (B) or filtering (D), the later hops could never have replied.

---

## Q72

**Question:** Which action can be run directly from the Cisco router's IOS mode shown? `[prompt shown: router1#]`

**Type:** image_single

**Options:**

- A. Enable a routing process
- B. Show running system information
- C. Enter interface IP configuration subcommands
- D. Select an interface to configure

**Answer:** B. Show running system information

**Explanation:** The prompt router1# is privileged EXEC mode. Privileged EXEC can run show/debug commands (e.g., show running-config, show version). Enabling a routing process, selecting an interface, and entering interface subcommands all require global configuration mode (router1(config)#), which is reached with the configure terminal command.

---

## Q73

**Question:** What can you determine about this switch from the command output? Examine the output of the show mac-address-table command on a Cisco 24ports Ethernet switch `[output shows multiple MAC addresses learned on port Gi0/1 across VLANs 1, 2, and 3, plus one STATIC entry on Fa0/5]`

**Type:** image_single

**Options:**

- A. There are eleven active ports on this switch
- B. Port Fa0/5is set to administratively down.
- C. All entries were learned by examining incoming frames.
- D. Port Gi0/1connects to another switch

**Answer:** D. Port Gi0/1connects to another switch

**Explanation:** Multiple MAC addresses from multiple VLANs are all learned on Gi0/1 — the signature of an uplink to another switch (or trunk carrying several VLANs). Option C is contradicted by the STATIC entry (static entries are configured, not learned from frames), and only a few distinct ports appear in the table, not eleven.

---

## Q74

**Question:** For each statement about output, select True or False. You connect to a Cisco switch and run the following command. show ip interface brief. The command displays the following partial `[output: Gi0/0 = 192.168.1.10, up/up; Gi0/1 = unassigned, down/down; Gi0/2 = unassigned, administratively down/down]`

**Type:** true_false

**Options:**

- A device connected to GigabitEthernet0/1can send out broadcast traffic.
- A technician issued the shutdown command on interface GigabitEthernet0/2.
- A technician set the IP address for GigabitEthernet0/0by using the CLI.

**Answer:** Statement 1 — False; Statement 2 — True; Statement 3 — True.

**Explanation:** As marked in the reviewer: (1) False — Gi0/1 is down/down, so no device can send any traffic, broadcast included; (2) True — Gi0/2 shows "administratively down," which only occurs when the shutdown command is configured; (3) True — Gi0/0's Method column shows "manual," meaning the IP address was configured manually via the CLI (not DHCP).

---

## Q75

**Question:** You purchase a new Cisco switch, turn it on and connect to its console port. You then run the following command: show running-config | section include interface — output: interface GigabitEthernet0/1, interface GigabitEthernet0/2 `[output omitted]`

**Type:** true_false

**Options:**

- The two interfaces can communicate over Layer 2.
- The two interfaces are administratively shut down.
- The two interfaces have default IP address `[cut off in PDF — likely "addresses configured"]`

**Answer:** Statement 1 — True; Statement 2 — False; Statement 3 — False.

**Explanation:** A brand-new (default) switch has all ports enabled at Layer 2 with no shutdown command, so interfaces on the same switch can communicate at Layer 2 (statement 1 True, statement 2 False). Layer 2 switch ports have no IP addresses at all by default, so the claim that they have (default) IP addresses is False. ⚠️ The third statement is cut off in the PDF, so its exact wording cannot be fully verified.

---

## Q76

**Question:** A help desk technician is working on a computer that is unable to resolve URLs in the browser. The technician runs the ipconfig/all command and receives the following `[output: IPv4 192.168.0.10, gateway 192.168.0.1, DHCP 192.168.10.1, DNS Servers 64.100.8.8]`. You need to issue a command to view the network devices in the path from the computer to the server that resolves the host name. What command should you issue?

**Type:** command

**Answer:** `tracert 64.100.8.8`

**Explanation:** The server that resolves host names is the DNS server, listed in the ipconfig/all output as 64.100.8.8. To view the network devices (hops) in the path to it, run tracert 64.100.8.8. (Note: the DNS server is on a different subnet than the PC — 64.100.x.x vs 192.168.0.x — which is itself suspicious for a DNS configuration, but per the question the requested command is tracert to the DNS address.)

---

## Q77

**Question:** An app on a user's computer is having problems downloading data. The app uses the following URL to download data https://www.companypro.net:7100/api. You need to use Wireshark to capture packets sent to and received from that `[server]`. What Wireshark filter options would you use to filter the results?

**Type:** command

**Answer:** `tcp.port == 7100`

**Explanation:** The only fixed, filterable value in the URL is the destination port 7100 (the hostname would resolve to a dynamic IP, and the path is not visible in an IP filter). Filtering on tcp.port == 7100 captures all packets sent to and from that port, i.e., both directions of the app's traffic. (tcp.port eq 7100 is an equivalent accepted syntax.)

---

## Q78

**Question:** Computers in a small office are unable to access companypro.net. You run the ipconfig command on one of the computers. The results are shown in the exhibit. `[ipconfig output: IPv4 192.168.0.14, mask 255.255.255.0, Default Gateway 192.168.0.1, DHCP 192.168.0.1, DNS 8.8.8.8 / 8.8.4.4]`. You need to determine if you can reach the router. Which command should you use?

**Type:** image_command

**Answer:** `ping 192.168.0.1`

**Explanation:** The router (default gateway) address from the exhibit is 192.168.0.1. Testing reachability to the router is done by pinging that address. (A successful ping confirms local Layer 1–3 connectivity to the gateway; failure isolates the problem to the local link or gateway.)

---

## Q79

**Question:** You want to list the IPV4addresses associated with the host name `[companypro.net]`. What is the command to execute in this scenario?

**Type:** command

**Answer:** `nslookup`

**Explanation:** nslookup (or nslookup followed by the host name) queries DNS and lists the address records — including the IPv4 (A) addresses — associated with a host name.

---

## Q80

**Question:** A support technician examines the front panel o fa Cisco switch and sees 4Ethernet cables connected in the first four ports. Ports 1,2,and 3have a green LED. Port 4has a blinking green light. `[What is the state of port 4?]`

**Type:** single

**Options:**

- A. Link is up with cable malfunctions.
- B. Link is up and not stable.
- C. Link is up and active.
- D. Link is up and there is no activity.

**Answer:** C. Link is up and active.

**Explanation:** Duplicate of Q69 with different option order. A blinking green LED on a Cisco switch port indicates the link is up and passing traffic (active). Solid green would mean link with no current activity.

---

## Q81

**Question:** What is the purpose of assigning an IP address to the management VLAN interface on a Layer 2switch?

**Type:** single

**Options:**

- A. To enable the switch to act as a default gateway for the attached devices
- B. To enable the switch to resolve URLs for the attached the devices
- C. To enable the switch to provide DHCP services to other switches in the network
- D. To enable access to the CLI on the switch through Telnet or SSH

**Answer:** D. To enable access to the CLI on the switch through Telnet or SSH

**Explanation:** Duplicate of Q29 with different option order. The management SVI IP on a Layer 2 switch exists for remote management access (SSH/Telnet).

---

## Q82

**Question:** What command will display the following output? `[output table: Device ID | Local Intrfce | Holdtme | Capability | Platform | Port ID — with entries for esxi on Gig0/5, Gig0/7, Gig0/6; 981888fc23a7 on Gig0/47 (Meraki MR); 3456fecd1d08 on Gig0/1 (MS120-8LP)]`

**Type:** command

**Answer:** `show cdp neighbors`

**Explanation:** The output columns (Device ID, Local Interface, Holdtime, Capability, Platform, Port ID) are the signature of the Cisco Discovery Protocol neighbor table, displayed with show cdp neighbors (detail).

---

## Q83

**Question:** A network administrator can successfully ping the URL www.cisco.com, but cannot ping a corporate server located at a remote branch in another city. You need to identify the specific router where packets are being dropped in the path to the remote branch. Which utility should you use?

**Type:** single

**Options:**

- A. Traceroute
- B. Netstat
- C. telnet
- D. ipconfig

**Answer:** A. Traceroute

**Explanation:** Traceroute (tracert on Windows) reports each hop in the path; the last responding hop before the failures pinpoints where packets are being dropped.

---

## Q84

**Question:** You need to determine whether a remote host is reachable through the network. Which two commands can you see? Each correct command is a complete `[solution]`

**Type:** multiple

**Options:**

- A. Netstat
- B. Ping
- C. Route print
- D. Ipconfig
- E. Traceroute or tracert

**Answer:** B and E

**Explanation:** Ping tests reachability to the remote host directly, and traceroute/tracert reveals the path and shows how far toward the host traffic gets — both determine whether a remote host is reachable through the network. Netstat shows local connections, and route print/ipconfig show local configuration only.

---

## Q85

**Question:** In a network with multiple VLANs, a user is unable to communicate with other users in the same VLAN but can communicate with users in different VLANs. Which of the following could be the cause of this issue?

**Type:** single

**Options:**

- A. user's switchport is not configured as an access port.
- B. user's switchport is not assigned to the correct VLAN.
- C. user's switchport is configured with the wrong duplex setting.
- D. user's switchport is experiencing a spanning tree `[issue/block]`

**Answer:** B. user's switchport is not assigned to the correct VLAN.

**Explanation:** If the user's port is assigned to the wrong VLAN, the user ends up in a different broadcast domain than the teammates they should reach (same-VLAN direct communication fails), while traffic to other VLANs still works because inter-VLAN routing through the router is functioning. ⚠️ Note: This question is ambiguous as written — option A (port configured as a trunk rather than an access port) produces a similar symptom in some topologies, since the host's traffic would land on the native VLAN instead of its intended VLAN. Based on the intended pedagogy (a Layer 2 VLAN-assignment fault with routing still working), B is the best answer. Option C (duplex mismatch) would cause errors/slowness, not selective VLAN failure, and option D is truncated in the PDF.

---

## Q86

**Question:** A user initiates a trouble ticket stating that an external web page is not loading. You determine that other resources both internal and external are still reachable. Which command can you use to help locate where the issue is in the network path to the external web page?

**Type:** single

**Options:**

- A. ping -t
- B. tracert
- C. ipconfig/all
- D. Nslookup

**Answer:** B. tracert

**Explanation:** Duplicate of Q24 (second occurrence). tracert traces the route hop-by-hop to the unreachable page so you can identify exactly where in the path the problem lies.

---

*End of extraction — 86 questions total, in original PDF order, duplicates preserved.*
Key flags to be aware of when studying from this reviewer (all detailed in the explanations above):
Q1 – question says 172.16.199.25, all options say 172.16.100.25 (PDF's own inconsistency, answer still /22).
Q2, Q3, Q4 – subnet masks cut off in the PDF; answers inferred from the original exam questions (/28, /16, /22 respectively).
Q14 – reviewer puts the NIC at the Physical layer (typically taught as Data Link).
Q18, Q75 – statements truncated in the PDF; answers inferred.
Q31 (OSPF) – options severely truncated ("CP", "P", "MP", "Llo"); OSPF runs directly over IP (protocol 89), so the IP option (B as printed) is the intent.
Q35 – SNMP is the keyed answer, though SSH would be the real-world choice (not listed).
Q52 (PoE) – option D cut off; keyed answer = ports labeled 6 (= option B in this PDF's ordering).
Q59 – tracert image mostly illegible; answers A and C per the standard version of this question.
Q65, Q85 – no marked answer in the PDF / ambiguous item; best-logical answers given (B and B) with the ambiguity explained.