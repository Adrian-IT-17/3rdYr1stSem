# CCST Networking Reviewer — Question Bank (86 questions)

> **Source:** `CCST_Networking_Reviewer.pdf` (99 slides, exported from PowerPoint). Questions are not numbered in the PDF, so they are numbered Q1–Q86 in PDF order. Duplicates are intentionally kept.
>
> **Fidelity rules used in this file**
> - Question and option wording follows the PDF word for word. Only grammar, spacing, capitalization, and punctuation were cleaned (for example "IPv6address" → "IPv6 address", "OS2LC" → "OS2 LC", stray spaces inside IPv6 addresses removed).
> - **`Answer` is always the reviewer's answer** as highlighted or written in the PDF, even when it is technically wrong. When a reviewer answer looks wrong, a **`⚠ Flag`** explains what is actually correct. Do not silently replace the reviewer's key; show the flag to the learner.
> - Where the PDF slide shows **no answer** at all (Q62, Q76–Q79, Q82), the answer is labeled **"NO ANSWER SHOWN IN THE PDF"** and a suggested answer is given.
> - Every question that has a picture, topology, or command output has an **`Exhibit`** section that transcribes it exactly. Where an extracted image file exists, it is named in `Image file` (found in the `exhibits/` folder alongside this file). Q52's picture is missing from the PDF itself (flagged).

## How to use this file (for Codex / app generation)

Each question uses this structure:

```
## Q<n>
- PDF page: <slide number>
- Type: single | multiple | matching | true_false | command | image_single | image_multiple | image_matching | image_true_false | image_command
Question / Exhibit / Options (or Pairs, or Statements) / Answer / Explanation / Flag
```

- `single` = one correct option; `multiple` = "Choose 2" style (select all correct).
- `matching` = drag items on the left to targets on the right; the **Pairs** table is the answer key. Left items may be reused (see the question note).
- `true_false` = each statement is graded True/False separately; the answer line gives all of them in order.
- `command` / `image_command` = free-text answer (accept case-insensitive, trimmed matches and obvious equivalents).
- Build visual exhibits (topologies, CLI output) from the `Exhibit` text, or display the provided image file when available.

## Flag summary (questions where the reviewer's answer or the source needs attention)

| Q | Issue |
|---|-------|
| Q1 | Reviewer marks /20; correct is /22 (mask 255.255.252.0). |
| Q14 | NIC grouped at Physical layer (usually Data Link). |
| Q22 | Reviewer marks TFTP for SLAAC; correct is ICMPv6. |
| Q31 | OSPF options garbled; reviewer marks "Llo (Link-Local Operations)"; real answer is IP protocol 89, not offered. |
| Q35 | SNMP keyed; SSH/Telnet is the real-world answer (not offered). |
| Q45 | Two pairings swapped (WPS vs SSID broadcasting). |
| Q52 | The image is missing from the PDF; exhibit reconstructed. |
| Q66 | Reviewer marks A and D; D is doubtful, C is clearly true. |
| Q62, Q76, Q77, Q78, Q79, Q82 | No answer shown in the PDF; suggested answers given. |
| Q75 | Only statement 1 is marked; 2 and 3 are unmarked (False). |
| Q15, Q18, Q19, Q20, Q43, Q44, Q57, Q80, Q84 | Typos or truncations in the PDF, noted in each question. |

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

**Answer:** D. 172.16.100.25/20

**Explanation:** This is what the reviewer highlighted in the PDF.

**⚠ Flag:** QUESTIONABLE ANSWER. The mask 255.255.252.0 has 22 consecutive 1-bits (255.255.11111100.0), so the correct CIDR prefix is /22, which is option A. The reviewer highlights D (/20), which contradicts Q4 (same mask, where the reviewer correctly highlights /22). Also, the question says 172.16.199.25 but every option says 172.16.100.25 (an inconsistency in the PDF itself). Keep D as the reviewer's key; show the flag so the learner knows /22 is correct.

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

**Explanation:** Only one "::" is allowed per address (eliminates A and B). Leading zeros may be dropped within a group, but 2000 must stay 2000 (eliminates C). In D: 0db8→db8, 0000→0, 0016→16, 0000→"::", 001b→1b, 2000, 0056→56.

**⚠ Flag:** NOTE: The PDF prints option D with stray spaces ("2001:db8: 0:16: :1b: 2000:56"). Spacing is normalized here.

---

## Q7

- **PDF page:** 11
- **Type:** single
- **Duplicate of:** Q5

**Question:**

> Which address is included in the 192.168.200.0/24 network?  

**Options:**

- A. 192.168.200.13
- B. 192.168.201.13
- C. 192.168.1.13
- D. 192.168.199.13

**Answer:** A. 192.168.200.13

**Explanation:** Duplicate of Q5 with the options in a different order.

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

Slide layout: the five OSI layers (Physical, Data Link, Network, Application, Transport) are listed in a left column as drag targets. The five items (SMTP, FTP / TCP, UDP / Cable, Hub, NIC / Switch / Router) are shown color-highlighted on the right, each with the reviewer's answer written beside it: Application, transport, Physical, data link, network.  

**Items (left):**

- SMTP, FTP
- TCP, UDP
- Cable, Hub, NIC
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
| Cable, Hub, NIC | Physical |
| Switch | Data Link |
| Router | Network |

**Explanation:** SMTP/FTP are Application layer; TCP/UDP are Transport; a switch is Data Link (Layer 2); a router is Network (Layer 3).

**⚠ Flag:** QUESTIONABLE ANSWER. The reviewer groups the NIC with Cable and Hub at the Physical layer. A NIC operates at Layer 1 and Layer 2 and is usually taught at the Data Link layer (it has the MAC address). Keep the reviewer's grouping as the key and show this flag.

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
- Network

**Answer (pairs):**

| Item | Target |
|---|---|
| TCP | Transport |
| IP | Internetwork |
| FTP | Application |
| Ethernet | Network |

**Explanation:** TCP = Transport, IP = Internetwork, FTP = Application, Ethernet = bottom layer.

**⚠ Flag:** NOTE: The TCP/IP model's bottom layer is normally called "Network Access" (or "Link"). The reviewer labels it "Network". Keep the reviewer's label.

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

**Explanation:** (1) Latency does not change bandwidth (bandwidth is a link capacity), so False. (2) Low bandwidth can cause queuing and delay, so True. (3) Lower latency can improve effective throughput, so True.

**⚠ Flag:** NOTE: Statement 3 is cut off in the PDF ("decreasing network ."). The missing word is almost certainly "latency". The reviewer's marks (F, T, T) are shown next to the statements on the slide.

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

**Explanation:** PaaS = platform to build apps; IaaS = virtualized infrastructure (VMs, virtual networks); SaaS = finished app over the internet for a subscription.

**⚠ Flag:** NOTE: The PDF prints the list as "LAAS SAAS PAAS" (typo for IAAS) and the answers as "PAAS / IAAS / SAAS".

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

**Explanation:** PaaS = platform for building/running apps; IaaS = pay-as-you-go compute and storage; SaaS = on-demand applications.

**⚠ Flag:** NOTE: The PDF prints the list as "LAAS SAAS PAAS" (typo for IAAS).

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

**Answer:** C. TFTP

**Explanation:** This is what the reviewer highlighted in the PDF.

**⚠ Flag:** QUESTIONABLE ANSWER. Stateless address autoconfiguration (SLAAC) uses ICMPv6 Router Solicitation / Router Advertisement messages, so the technically correct answer is B. ICMPv6. TFTP is a file-transfer protocol and has nothing to do with address configuration. Keep C as the reviewer's key and show this flag.

---

## Q23

- **PDF page:** 27
- **Type:** single
- **Duplicate of:** Q11

**Question:**

> During the data encapsulation process, which OSI layer adds a header that contains MAC addressing information and a trailer used for error checking?  

**Options:**

- A. Network
- B. Transport
- C. Data Link
- D. Session

**Answer:** C. Data Link

**Explanation:** Duplicate of Q11 with a different option order.

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

## Q26

- **PDF page:** 30
- **Type:** multiple
- **Duplicate of:** Q25

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

**Explanation:** Exact duplicate of Q25.

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

## Q28

- **PDF page:** 32
- **Type:** single
- **Duplicate of:** Q10

**Question:**

> Which information is included in the header of a UDP segment?  

**Options:**

- A. IP addresses
- B. Sequence numbers
- C. Port numbers
- D. MAC addresses

**Answer:** C. Port numbers

**Explanation:** Duplicate of Q10 with a different option order.

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

**Answer:** D. Llo (Link-Local Operations)

**Explanation:** This is what the reviewer highlighted in the PDF.

**⚠ Flag:** QUESTIONABLE ANSWER / GARBLED OPTIONS. OSPF forms neighbors with Hello packets carried directly over IP (IP protocol 89), not TCP or UDP. None of the printed options is technically accurate (option text looks like truncated "TCP", "IP", "MP"...). B ("P") may be a truncated "IP". The reviewer's key is D; keep D as the key and show this flag.

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

**Explanation:** The mask marks which bits are the network portion.

**⚠ Flag:** NOTE: B is also arguably true (the mask also defines the host portion). The reviewer keys A.

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

**Answer:** D. SNMP (Simple Network Management Protocol)

**Explanation:** Among the choices, SNMP is the network-management protocol.

**⚠ Flag:** NOTE: In practice, viewing a switch configuration from the command line is done with SSH or Telnet, which is not offered. The reviewer keys SNMP.

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

**Explanation:** Authentication verifies identity. Authorization defines permissions; accounting records activity.

**⚠ Flag:** NOTE: The PDF's first printing of this question reads "identify verification" (typo); the same question reappears as Q46 spelled "identity verification".

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
> Factors: Possession, Inference, Knowledge  

**Items (left):**

- Possession
- Inference
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
| Inference | Holding your phone to your face to be recognized. |

**Explanation:** Something you know = password; something you have = device receiving the code; something you are = biometrics.

**⚠ Flag:** NOTE: The PDF's factor list says "Inference", but the reviewer's answer on the slide says "Inherence". The correct MFA term is Inherence (biometrics). In an app, label that factor "Inherence" (optionally show "Inference" as printed in the PDF).

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

**Explanation:** WEP is the legacy standard using 40-bit (or 104-bit) keys; WPA-Enterprise authenticates against a RADIUS server (802.1X); WPA2-Personal uses AES with a pre-shared key.

**⚠ Flag:** NOTE: The PDF prints "RADIU Server" (typo for RADIUS); corrected here.

---

## Q45

- **PDF page:** 51
- **Type:** matching

**Question:**

> You need to configure wireless settings for a home router. Move the actions from the list on the left to the correct scenarios on the right.  

**Exhibit (exact description of the image / diagram / command output):**

Slide layout: the three scenarios are listed on the left, and the reviewer wrote a small answer label after each one ("Disable SSID broadcasting", "Set the security mode to WPA2-PSK", "Disable WPS"). The three action options are shown color-highlighted on the right.  

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
| Disable SSID broadcasting | You want to prevent users from using the push-button method for accessing the network. |
| Set the security mode to WPA2-PSK | You want devices to use a pre-shared key when connecting to the network. |
| Disable WPS | You want to prevent devices from discovering the name of the WiFi network. |

**Explanation:** This is exactly how the reviewer paired them on the slide.

**⚠ Flag:** QUESTIONABLE ANSWER (two pairings are swapped). The reviewer pairs the push-button scenario with "Disable SSID broadcasting" and the hide-the-network-name scenario with "Disable WPS". Logically: push-button method → Disable WPS; discovering the network name → Disable SSID broadcasting; pre-shared key → Set security mode to WPA2-PSK (that one is correct). Keep the reviewer's pairing as the key and show this flag.

---

## Q46

- **PDF page:** 52
- **Type:** single
- **Duplicate of:** Q40

**Question:**

> Which component of the AAA service security model provides identity verification?  

**Options:**

- A. Authorization
- B. Auditing
- C. Authentication
- D. Accounting

**Answer:** C. Authentication

**Explanation:** Duplicate of Q40 with a different option order.

---

# Section 3 — Endpoints & Media Types

*PDF pages 55–64 (Q47–Q56)*


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

**Explanation:** Ports marked 6 are the RJ-45 Ethernet ports with Power over Ethernet, which deliver both data and power to IP phones.

**⚠ Flag:** IMAGE MISSING IN THE PDF. The slide says "A Cisco PoE switch is shown in the following image" but no picture is present on this PDF page. The exhibit description below is NOT taken from the PDF; it is reconstructed from the answer choices and the well-known version of this question (2 = console port, 3 and 4 = other management/function ports, 6 = PoE RJ-45 Ethernet ports, 7 = SFP/fiber uplink ports). If an image is needed, draw a generic Cisco PoE switch front panel with prominent numbered callouts.

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

**Explanation:** Unlike devices (switch to router, switch to server) use straight-through UTP; like devices (router to router) use crossover UTP; the long inter-building run through the underground conduit uses fiber optic cable.

**⚠ Flag:** NOTE: In the PDF the bullet list of cable types prints four bullets ("Straight-through UTP Cable, Fiber Optic, Crossover UTP Cable, Straight-through UTP"); the fourth is a truncated repeat of the first. The three distinct cable types are used here. The first connection reads "Switch to Router R1" and means switch S1 (see diagram).

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

**Explanation:** Exact duplicate of Q25 and Q26 (third occurrence).

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

**Answer:** NO ANSWER SHOWN IN THE PDF. Suggested answer (derived from the diagram): IP address — any unused host address in 172.100.0.0/16 (for example 172.100.0.10, not .1 or .254); Subnet mask — 255.255.0.0; Default gateway — 172.100.0.1 (Router1 G0/0); DNS server — the DNS server value shown in the dialog.

**Explanation:** With no DHCP, every IPv4 setting is static. From the topology: the LAN is 172.100.0.0/16 (mask 255.255.0.0), the gateway is Router1's LAN interface 172.100.0.1, and the server on the LAN is 172.100.0.254.

**⚠ Flag:** NOTE: The slide shows only the question and the graphic; the answer is not written on it. In the dialog graphic, the Preferred DNS server field is already filled and reads approximately "172 . 100 . 025 . 4" (low resolution; likely meant to be 172.100.0.254, the server shown on the LAN). Treat the suggested answer above as unverified.

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

## Q64

- **PDF page:** 76
- **Type:** single
- **Duplicate of:** Q27

**Question:**

> An engineer configured a new VLAN named VLAN2 for the Data Center team. When the team tries to ping addresses outside VLAN2 from a computer in VLAN2, they are unable to reach them. What should the engineer configure?  

**Options:**

- A. Additional VLAN
- B. Default route
- C. Default gateway
- D. Static route

**Answer:** C. Default gateway

**Explanation:** Exact duplicate of Q27.

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

**Answer:** A and D

**Explanation:** This is what the reviewer highlighted in the PDF.

**⚠ Flag:** QUESTIONABLE ANSWER. A is correct (every PC is in a different VLAN/subnet from File-Srv, and inter-VLAN routing needs Router1). However D is doubtful: PC-A/PC-B (VLAN 100) and PC-C/PC-D (VLAN 110) are in different VLANs, so they cannot talk to each other without the router. C (PC-A and PC-B, same VLAN on the same switch) is the statement that is clearly still true, so the logically expected answer is A and C. Keep A and D as the reviewer's key and show this flag.

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

**Answer:** 1 — True; 2 — False (not marked in PDF); 3 — False (not marked in PDF)

**Explanation:** A new switch has all ports enabled at Layer 2 with no shutdown, so the interfaces can communicate at Layer 2. No shutdown command appears under either interface, and Layer 2 switch ports have no IP addresses by default.

**⚠ Flag:** NOTE: On the slide only statement 1 is highlighted as correct (True). Statements 2 and 3 carry no mark; they are False by the logic above.

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

**Answer:** NO ANSWER SHOWN IN THE PDF. Suggested answer: tracert 64.100.8.8

**Explanation:** The server that resolves host names is the DNS server, 64.100.8.8. tracert to that address lists the devices (hops) in the path to it.

**⚠ Flag:** NOTE: Answer is not written on the slide; suggested answer is derived from the exhibit.

---

## Q77

- **PDF page:** 89
- **Type:** command

**Question:**

> An app on a user's computer is having problems downloading data. The app uses the following URL to download data: https://www.companypro.net:7100/api  
> You need to use Wireshark to capture packets sent to and received from that URL. What Wireshark filter options would you use to filter the results?  

**Answer:** NO ANSWER SHOWN IN THE PDF. Suggested answer: tcp.port == 7100

**Explanation:** The fixed, filterable value in the URL is the port, 7100. tcp.port == 7100 matches packets in both directions. (Another valid form is tcp.port eq 7100; filtering by the server's resolved IP with ip.addr == <address> also works.)

**⚠ Flag:** NOTE: The slide has the question only (no exhibit, no answer). Suggested answer is derived from the URL.

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

**Answer:** NO ANSWER SHOWN IN THE PDF. Suggested answer: ping 192.168.0.1

**Explanation:** The router is the default gateway, 192.168.0.1. Pinging it tests local connectivity to the router.

**⚠ Flag:** NOTE: Answer is not written on the slide; suggested answer is derived from the exhibit.

---

## Q79

- **PDF page:** 91
- **Type:** command

**Question:**

> You want to list the IPv4 addresses associated with the host name www.companypro.net. What is the command to execute in this scenario?  

**Answer:** NO ANSWER SHOWN IN THE PDF. Suggested answer: nslookup www.companypro.net

**Explanation:** nslookup queries DNS and lists the address records (including IPv4 A records) for a host name.

**⚠ Flag:** NOTE: The slide has the question only (no exhibit, no answer). Suggested answer is derived from the question.

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

**Explanation:** Duplicate of Q69 with a different option order.

**⚠ Flag:** NOTE: The PDF omits the final sentence of the question ("What is the state of Port 4?"); it is implied by Q69 and added here in parentheses.

---

## Q81

- **PDF page:** 93
- **Type:** single
- **Duplicate of:** Q29

**Question:**

> What is the purpose of assigning an IP address to the management VLAN interface on a Layer 2 switch?  

**Options:**

- A. To enable the switch to act as a default gateway for the attached devices
- B. To enable the switch to resolve URLs for the attached devices
- C. To enable the switch to provide DHCP services to other switches in the network
- D. To enable access to the CLI on the switch through Telnet or SSH

**Answer:** D. To enable access to the CLI on the switch through Telnet or SSH

**Explanation:** Duplicate of Q29 with a different option order.

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

**Answer:** NO ANSWER SHOWN IN THE PDF. Suggested answer: show cdp neighbors

**Explanation:** The columns (Device ID, Local Interface, Holdtime, Capability, Platform, Port ID) are the Cisco Discovery Protocol neighbor table.

**⚠ Flag:** NOTE: Answer is not written on the slide; suggested answer is derived from the exhibit.

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

**Explanation:** Ping tests reachability directly; traceroute/tracert shows the path and how far traffic gets. Netstat, route print, and ipconfig show local information only.

**⚠ Flag:** NOTE: The PDF prints "Which two commands can you see?" (typo for "use").

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

**Explanation:** If the port is in the wrong VLAN, the user is in a different broadcast domain from the intended teammates, while routing to other VLANs still works.

**⚠ Flag:** NOTE: The question is somewhat ambiguous (A could produce a similar symptom), but B is highlighted by the reviewer.

---

## Q86

- **PDF page:** 98
- **Type:** single
- **Duplicate of:** Q24

**Question:**

> A user initiates a trouble ticket stating that an external web page is not loading. You determine that other resources, both internal and external, are still reachable. Which command can you use to help locate where the issue is in the network path to the external web page?  

**Options:**

- A. ping -t
- B. tracert
- C. ipconfig /all
- D. nslookup

**Answer:** B. tracert

**Explanation:** Duplicate of Q24 (second occurrence).

---

*End of file — 86 questions, in original PDF order, duplicates preserved.*
