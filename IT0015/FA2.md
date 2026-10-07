# Networking Quiz Review — 40 Questions

> **Purpose for Codex:** Rebuild these questions as a quiz/study
> interface. Preserve the question wording, options, answer, and
> explanation. When `Visual Type` is present, recreate that visual
> rather than showing only a text placeholder.
>
> **Review flags:** Questions tagged `CODEX_VERIFY` have wording/options
> that appear ambiguous, altered from common Cisco/NetAcad versions, or
> otherwise deserve independent verification. Do not silently change
> them; verify the expected answer against the exact source/version if
> available.

------------------------------------------------------------------------

## Q1

**Question:** A network administrator is configuring an EtherChannel
link between switches SW1 and SW2 by using the command
`SW1(config-if-range)# channel-group 1 mode auto`. Which command must be
used on SW2 to enable this EtherChannel?

**Type:** single

**Options:**

- `SW2(config-if-range)# channel-group 1 mode passive`
- `SW2(config-if-range)# channel-group 1 mode active`
- `SW2(config-if-range)# channel-group 1 mode on`
- `SW2(config-if-range)# channel-group 1 mode desirable`

**Answer:** `SW2(config-if-range)# channel-group 1 mode desirable`

**Explanation:** `auto` and `desirable` are PAgP modes. `auto` waits
passively, while `desirable` actively negotiates the EtherChannel.

------------------------------------------------------------------------

## Q2

**Question:** Which one is a component of a bridge ID?

**Type:** single

**Options:**

- IP address
- MAC address
- port ID
- extended system ID

**Answer:** extended system ID

**Explanation:** The STP Bridge ID includes the bridge priority,
extended system ID, and MAC address.

------------------------------------------------------------------------

## Q3

**Question:** Which one is a network design feature that requires
Spanning Tree Protocol (STP) to ensure correct network operation?

**Type:** single

**Options:**

- removing single points of failure with multiple Layer 2 switches
- implementing VLANs to contain broadcasts
- static default routes
- link-state dynamic routing that provides redundant routes

**Answer:** removing single points of failure with multiple Layer 2
switches

**Explanation:** Redundant Layer 2 paths can create switching loops. STP
prevents those loops while preserving redundancy.

------------------------------------------------------------------------

## Q4

**Question:** When the `show spanning-tree vlan 33` command is issued on
a switch, three ports are shown in the forwarding state. In which port
role could these interfaces function while in the forwarding state?

**Type:** single

**Options:**

- blocked
- alternate
- root
- disabled

**Answer:** root

**Explanation:** A root port can operate in the forwarding state.
Alternate/blocked ports do not forward user traffic.

------------------------------------------------------------------------

## Q5

**Question:** What is the value used to determine which port on a
non-root bridge will become a root port in a STP network?

**Type:** single

**Options:**

- the path cost
- the lowest MAC address of all the ports in the switch
- the VTP revision number
- the highest MAC address of all the ports in the switch

**Answer:** the path cost

**Explanation:** A non-root switch selects the path with the lowest
total STP path cost toward the root bridge.

------------------------------------------------------------------------

## Q6

**Question:** A switch is configured to run STP. What term describes the
reference point for all path calculations?

**Type:** single

**Options:**

- alternate port
- root bridge
- designated port
- root port

**Answer:** root bridge

**Explanation:** The root bridge is the reference point from which STP
path costs are calculated.

------------------------------------------------------------------------

## Q7

**Question:** Which protocol is a link aggregation protocol?

**Type:** single

**Options:**

- STP
- PAgP
- RSTP
- EtherChannel

**Answer:** PAgP

**Explanation:** PAgP is Cisco's Port Aggregation Protocol used to
negotiate EtherChannel formation. EtherChannel is the link aggregation
technology itself.

------------------------------------------------------------------------

## Q8

**Question:** A switch is configured to run STP. What term describes the
switch port closest, in terms of overall cost, to the root bridge?

**Type:** single

**Options:**

- alternate port
- designated port
- root bridge
- root port

**Answer:** root port

**Explanation:** The root port is the non-root switch port with the
best, lowest-cost path to the root bridge.

------------------------------------------------------------------------

## Q9 — CODEX_VERIFY

**Question:** What will happen if one port in an EtherChannel is
configured in VLAN22 & all other ports are configured in VLAN11?

**Type:** single

**Options as provided:**

- The EtherChannel bundle will stay up only if PAgP is used
- The EtherChannel bundle will stay up if either PAgP or LACP is used
- The EtherChannel bundle will stay up if the ports were configured with
  no negotiation between the switches to form the EtherChannel
- The EtherChannel bundle will stay up only if LACP is used

**Reviewed Answer:** None of the supplied choices cleanly states the
expected Cisco behavior.

**Expected Cisco Concept:** EtherChannel member ports must have
compatible Layer 2 settings, including the same access VLAN. A
mismatched VLAN causes an EtherChannel consistency problem; the
mismatched link/bundle will not operate normally.

**CODEX_VERIFY Note:** This question appears malformed or altered. A
common Cisco/NetAcad version includes an answer equivalent to **"The
EtherChannel will fail."** Verify against the exact quiz source before
assigning one of the four supplied choices.

------------------------------------------------------------------------

## Q10 — CODEX_VERIFY

**Question:** Which channel group mode would place an interface in a
negotiating state using PAgP?

**Type:** single

**Options:**

- active
- desirable
- on
- passive

**Answer:** desirable

**Explanation:** `desirable` is a PAgP mode that actively negotiates
EtherChannel formation.

**CODEX_VERIFY Note:** Some Cisco versions ask which **two** PAgP modes
place an interface in a negotiating state, in which case the answers are
`auto` and `desirable`. In this exact option set, `auto` is absent, so
`desirable` is the clear answer.

------------------------------------------------------------------------

## Q11

**Question:** Which switching technology would allow each access layer
switch link to be aggregated to provide more bandwidth between each
Layer 2 switch and the Layer 3 switch?

**Type:** single

**Options:**

- PortFast
- trunking
- HSRP
- EtherChannel

**Answer:** EtherChannel

**Explanation:** EtherChannel combines multiple physical Ethernet links
into one logical link, increasing available bandwidth and providing
redundancy.

------------------------------------------------------------------------

## Q12

**Question:** What is the function of STP in a scalable network?

**Type:** single

**Options:**

- It protects the edge of the enterprise network from malicious
  activity.
- It decreases the size of the failure domain to contain the impact of
  failures.
- It combines multiple switch trunk links to act as one logical link for
  increased bandwidth.
- It disables redundant paths to eliminate Layer 2 loops.

**Answer:** It disables redundant paths to eliminate Layer 2 loops.

**Explanation:** STP prevents Layer 2 switching loops by placing
selected redundant paths into a non-forwarding state.

------------------------------------------------------------------------

## Q13

**Question:** A switch is configured to run STP. What term describes a
field used to specify a VLAN ID?

**Type:** single

**Options:**

- bridge priority
- extended system ID
- MAC Address
- port ID

**Answer:** extended system ID

**Explanation:** In PVST/RPVST bridge IDs, the extended system ID
identifies the VLAN.

------------------------------------------------------------------------

## Q14

**Question:** You have two switches connected together with two
crossover cables for redundancy, and STP is disabled. Which of the
following will happen between the switches?

**Type:** single

**Options:**

- The routing tables on the switches will not update.
- The switches will automatically load-balance between the two links.
- Broadcast storms will occur on the switched network.
- The MAC forward/filter table will not update on the switch.

**Answer:** Broadcast storms will occur on the switched network.

**Explanation:** Without STP, redundant Layer 2 links can create a
switching loop, allowing broadcast frames to circulate continuously.

------------------------------------------------------------------------

## Q15

**Question:** If no bridge priority is configured in PVST, which
criteria is considered when electing the root bridge?

**Type:** single

**Options:**

- lowest IP address
- highest MAC address
- lowest MAC address
- highest IP address

**Answer:** lowest MAC address

**Explanation:** When bridge priorities are equal, the switch with the
lowest MAC address has the lowest Bridge ID and becomes the root bridge.

------------------------------------------------------------------------

## Q16

**Question:** A small company network has six interconnected Layer 2
switches. Currently all switches are using the default bridge priority
value. Which value can be used to configure the bridge priority of one
of the switches to ensure that it becomes the root bridge in this
design?

**Type:** single

**Options:**

- 34816
- 1
- 28672
- 32768

**Answer:** 28672

**Explanation:** The default priority is 32768. STP bridge priority
values use increments of 4096, and 28672 is a valid value lower than the
default.

------------------------------------------------------------------------

## Q17

**Question:** What does a switch do when a frame is received on an
interface and the destination hardware address is unknown or not in the
filter table?

**Type:** single

**Options:**

- Sends back a message to the originating station asking for a name
  resolution
- Floods the network with the frame looking for the device
- Drops the frame
- Forwards the switch to the first available link

**Answer:** Floods the network with the frame looking for the device

**Explanation:** An unknown unicast frame is flooded out the other ports
in the same VLAN, except the port on which it was received.

------------------------------------------------------------------------

## Q18 — CODEX_VERIFY

**Question:** Which channel group mode would place an interface in a
negotiating state using PAgP?

**Type:** single

**Options:**

- active
- passive
- auto
- desirable

**Reviewed Answer:** desirable

**Explanation:** `desirable` actively initiates PAgP negotiation, while
`auto` passively listens and can also participate in PAgP negotiation.

**CODEX_VERIFY Note:** This wording is ambiguous. A common Cisco/NetAcad
source question says **"Which two channel group modes..."**, for which
both `auto` and `desirable` are correct. If the LMS requires only one
answer, verify which adaptation it expects.

------------------------------------------------------------------------

## Q19

**Question:** Which mode configuration setting would allow formation of
an EtherChannel link between switches SW1 and SW2 without sending
negotiation traffic?

**Type:** single

**Options:**

- SW1: auto / SW2: auto / trunking enabled on both switches
- SW1: on / SW2: on
- SW1: desirable / SW2: desirable
- SW1: auto / SW2: auto / PortFast enabled on both switches

**Answer:** SW1: on / SW2: on

**Explanation:** `on` statically forces EtherChannel formation without
PAgP or LACP negotiation.

------------------------------------------------------------------------

## Q20

**Question:** Which one is a component of a bridge ID?

**Type:** single

**Options:**

- IP address
- cost
- extended system ID
- port ID

**Answer:** extended system ID

**Explanation:** The extended system ID is part of the STP Bridge ID.

------------------------------------------------------------------------

## Q21

**Question:** A network administrator configures a router to send RA
messages with M flag as 0 and O flag as 1. Which statement describes the
effect of this configuration when a PC tries to configure its IPv6
address?

**Type:** single

**Options:**

- It should use the information that is contained in the RA message
  exclusively.
- It should contact a DHCPv6 server for all the information that it
  needs.
- It should use the information that is contained in the RA message and
  contact a DHCPv6 server for additional information.
- It should contact a DHCPv6 server for the prefix, the prefix-length
  information, and an interface ID that is both random and unique.

**Answer:** It should use the information that is contained in the RA
message and contact a DHCPv6 server for additional information.

**Explanation:** M=0 means the host does not use stateful DHCPv6 for its
address. O=1 tells it to use DHCPv6 for other configuration information.
This is stateless DHCPv6.

------------------------------------------------------------------------

## Q22

**Question:** Which is a DHCPv4 address allocation method that assigns
IPv4 addresses for a limited lease period?

**Type:** single

**Options:**

- manual allocation
- automatic allocation
- pre-allocation
- dynamic allocation

**Answer:** dynamic allocation

**Explanation:** Dynamic allocation leases an address to a client for a
specified period.

------------------------------------------------------------------------

## Q23

**Question:** To enable SLAAC, it should have the following: Link-local
IPv6 address, Global Unicast address / subnet and IPv6 all-nodes group.

**Type:** true_false

**Options:**

- True
- False

**Answer:** True

**Explanation:** SLAAC operation uses IPv6 link-local addressing and
Router Advertisements to learn global-prefix information; IPv6 hosts
also participate in required multicast groups.

------------------------------------------------------------------------

## Q24 — CODEX_VERIFY

**Question:** A company uses DHCP to manage IP address deployment for
employee workstations. The IT department deploys multiple DHCP servers
in the data center and uses DHCP relay agents to facilitate the DHCP
requests from workstations. Which one UDP port is used to forward DHCP
traffic?

**Type:** single

**Options:**

- 67
- 68
- 23
- 53

**Reviewed Answer:** 67

**Explanation:** DHCP servers listen on UDP port 67, while DHCP clients
use UDP port 68.

**CODEX_VERIFY Note:** Common Cisco versions ask for **two UDP ports
used by DHCP**, with answers `67` and `68`. This adaptation asks for
only one. For relay-to-server traffic, `67` is the expected choice from
the supplied options, but verify the LMS/source wording.

------------------------------------------------------------------------

## Q25

**Question:** The O Flag signifies to use SLAAC to create an IPv6 Global
Unicast Address.

**Type:** true_false

**Options:**

- True
- False

**Answer:** False

**Explanation:** The O flag means other configuration information should
be obtained through DHCPv6. SLAAC address generation is associated with
Router Advertisement prefix information and the Autonomous (A) flag.

------------------------------------------------------------------------

## Q26

**Question:** Refer to the exhibit. A network administrator is
configuring a router for DHCPv6 operation. Which conclusion can be drawn
based on the commands?

**Type:** single

**Visual Type:** CLI_TERMINAL

**CLI Content:**

``` text
R1# configure terminal
Enter configuration commands, one per line.  End with CNTL/Z.
R1(config)# ipv6 unicast-routing
R1(config)# ipv6 dhcp pool ACAD_CLASS
R1(config-dhcp)# dns-server 2001:db8:acad:a1::10
R1(config-dhcp)# domain-name netacad.net
R1(config-dhcp)# exit
R1(config)# interface gigabitEthernet 0/0
R1(config-if)# ipv6 address 2001:db8:acad:1::1/64
R1(config-if)# ipv6 dhcp server ACAD_CLASS
R1(config-if)# ipv6 nd other-config-flag
R1(config-if)# end
R1#
```

**Visual Recreation Instructions:** Render the CLI content inside a
bordered Cisco IOS-style terminal/exhibit box. Use monospaced text.
Preserve prompts, command order, capitalization, IPv6 addresses, and
configuration modes. The question and answer choices should appear below
the terminal.

**Options:**

- The router is configured for stateless DHCPv6 operation.
- The DHCPv6 server name is ACAD_CLASS.
- Clients would configure the interface IDs above 0010.
- The router is configured for stateful DHCPv6 operation, but the DHCP
  pool configuration is incomplete.

**Answer:** The router is configured for stateless DHCPv6 operation.

**Explanation:** `ipv6 nd other-config-flag` sets the O flag. Hosts use
SLAAC for their IPv6 address and DHCPv6 for additional information such
as DNS and domain name.

------------------------------------------------------------------------

## Q27

**Question:** Identify which message type to the order of the stateful
DHCPv6 process when a client first connects to an IPv6 network. DHCPv6
REPLY

**Type:** single

**Options:**

- Step 1
- Step 3
- Step 2
- Step 4

**Answer:** Step 4

**Explanation:** Stateful DHCPv6 initial exchange: SOLICIT → ADVERTISE →
REQUEST → REPLY.

------------------------------------------------------------------------

## Q28

**Question:** Refer to the exhibit. What should be done to allow PC-A to
receive an IPv6 address from the DHCPv6 server?

**Type:** single

**Visual Type:** NETWORK_TOPOLOGY_WITH_CLI

**Topology Recreation:**

- Place router **RTR1** near the upper center.
- Place switch **SW1** below-left of RTR1.
- Place **PC-A** below SW1.
- Place switch **SW2** below-right of RTR1.
- Place **DHCPv6 Server** below SW2.
- Connect `RTR1 Fa0/0` to SW1.
- Connect SW1 to PC-A.
- Connect `RTR1 Fa0/1` to SW2.
- Connect SW2 to the DHCPv6 Server.
- Left LAN prefix: `2001:DB8:1234:5678::/64`.
- RTR1 Fa0/0 address shown as `::1` on that prefix.
- Right LAN prefix: `2001:DB8:1234:ABCD::/64`.
- RTR1 Fa0/1 address shown as `::1` on that prefix.
- DHCPv6 Server address: `2001:DB8:1234:ABCD::10/64`.
- Use standard Cisco-style icons: router at top, two switches beneath
  it, PC under SW1, server under SW2.
- The original exhibit shows red link lines.

**CLI Content shown to the left of the topology:**

``` text
RTR1# show running-config
hostname RTR1
!
<output omitted>
interface FastEthernet0/0
 ip address dhcp
 duplex auto
 speed auto
 ipv6 address 2001:DB8:1234:5678::1/64
 ipv6 nd managed-config-flag
!
interface FastEthernet0/1
 no ip address
 duplex auto
 speed auto
 ipv6 address 2001:DB8:1234:ABCD::1/64
!
<output omitted>
```

**Visual Recreation Instructions:** Display the CLI panel and topology
side-by-side inside one exhibit. The CLI should be monospaced in a
bordered white box. Keep all IPv6 prefixes and interface labels visible.

**Options:**

- Add the IPv6 address `2001:DB8:1234:5678::10/64` to the interface
  configuration of the DHCPv6 server.
- Change the `ipv6 nd managed-config-flag` command to
  `ipv6 nd other-config-flag`.
- Configure the `ipv6 nd managed-config-flag` command on interface
  Fa0/1.
- Add the `ipv6 dhcp relay` command to interface Fa0/0.

**Answer:** Add the `ipv6 dhcp relay` command to interface Fa0/0.

**Explanation:** PC-A and the DHCPv6 server are on different IPv6
networks. Fa0/0 already advertises the managed flag for stateful DHCPv6,
but the router must relay DHCPv6 traffic between the client LAN and the
remote server.

------------------------------------------------------------------------

## Q29

**Question:** As a DHCPv4 client lease is about to expire, what is the
message that the client sends the DHCP server?

**Type:** single

**Options:**

- DHCPACK
- DHCPREQUEST
- DHCPDISCOVER
- DHCPOFFER

**Answer:** DHCPREQUEST

**Explanation:** A DHCP client sends DHCPREQUEST when attempting to
renew its existing lease.

------------------------------------------------------------------------

## Q30

**Question:** Refer to the exhibit. PC1 is configured to obtain a
dynamic IP address from the DHCP server. PC1 has been shut down for two
weeks. When PC1 boots and tries to request an available IP address,
which destination IP address will PC1 place in the IP header?

**Type:** single

**Visual Type:** NETWORK_TOPOLOGY

**Topology Recreation:**

- Draw one rectangular LAN/exhibit area.
- Place a **DHCP Server** near the upper-left/center.
- Place a Layer 2 switch below the DHCP Server.
- Place **PC1** below the switch.
- Place router **R1** to the right of the switch.
- Connect DHCP Server → switch.
- Connect PC1 → switch.
- Connect switch → R1.
- Label DHCP Server: `192.168.1.8/24`.
- Label PC1: `192.168.1.130/24` as its previous/illustrated address.
- Label R1 interface toward the LAN: `Fa 0/1` and `192.168.1.1/24`.
- Use standard Cisco-style server, switch, PC, and router icons.
- The original exhibit uses red connection lines.

**Options:**

- 192.168.1.255
- 255.255.255.255
- 192.168.1.1
- 192.168.1.8

**Answer:** 255.255.255.255

**Explanation:** When the client starts without a currently valid lease
and needs DHCP configuration, it sends an initial broadcast using the
limited broadcast IPv4 destination `255.255.255.255`.

------------------------------------------------------------------------

## Q31

**Question:** The address pool of a DHCP server is configured with
`10.7.30.0/24`. The network administrator reserves 5 IP addresses for
printers. How many IP addresses are left in the pool to be assigned to
other hosts?

**Type:** single

**Options:**

- 247
- 253
- 249
- 239

**Answer:** 249

**Explanation:** A /24 has 254 usable host addresses. After reserving 5,
`254 - 5 = 249`.

------------------------------------------------------------------------

## Q32

**Question:** What is the result of a network technician issuing the
command `ip dhcp excluded-address 10.0.15.1 10.0.15.15` on a Cisco
router?

**Type:** single

**Options:**

- The Cisco router will automatically create a DHCP pool using a /28
  mask.
- The Cisco router will allow only the specified IP addresses to be
  leased to clients.
- The Cisco router will exclude 15 IP addresses from being leased to
  DHCP clients.
- The Cisco router will exclude only the 10.0.15.1 and 10.0.15.15 IP
  addresses from being leased to DHCP clients.

**Answer:** The Cisco router will exclude 15 IP addresses from being
leased to DHCP clients.

**Explanation:** The command excludes the inclusive range `10.0.15.1`
through `10.0.15.15`.

------------------------------------------------------------------------

## Q33

**Question:** What is a method that can be used to generate an interface
ID by an IPv6 host that is using SLAAC?

**Type:** single

**Options:**

- Stateful DHCpv6
- ARP
- DAD
- random generation

**Answer:** random generation

**Explanation:** SLAAC hosts can generate an interface identifier
through random/privacy-based generation. DAD checks uniqueness but does
not generate the interface ID.

------------------------------------------------------------------------

## Q34

**Question:** Identify which message type to the order of the stateful
DHCPv6 process when a client first connects to an IPv6 network. DHCPv6
ADVERTISE

**Type:** single

**Options:**

- Step 1
- Step 3
- Step 4
- Step 2

**Answer:** Step 2

**Explanation:** Stateful DHCPv6 initial exchange: Step 1 SOLICIT → Step
2 ADVERTISE → Step 3 REQUEST → Step 4 REPLY.

------------------------------------------------------------------------

## Q35

**Question:** A company uses DHCP servers to dynamically assign IPv4
addresses to employee workstations. The address lease duration is set as
5 days. An employee returns to the office after an absence of one week.
When the employee boots the workstation, it sends a message to obtain an
IP address. Which Layer 2 and Layer 3 destination addresses will the
message contain?

**Type:** single

**Options:**

- both MAC and IPv4 addresses of the DHCP server
- FF-FF-FF-FF-FF-FF and 255.255.255.255
- FF-FF-FF-FF-FF-FF and IPv4 address of the DHCP server
- MAC address of the DHCP server and 255.255.255.255

**Answer:** FF-FF-FF-FF-FF-FF and 255.255.255.255

**Explanation:** The old 5-day lease has expired after a week. The
client begins DHCP using a Layer 2 broadcast destination and the IPv4
limited broadcast address.

------------------------------------------------------------------------

## Q36

**Question:** A router that provides DHCPv6 forwarding services is a
DHCP Server.

**Type:** true_false

**Options:**

- True
- False

**Answer:** False

**Explanation:** A router that forwards DHCPv6 messages between clients
and a DHCPv6 server is acting as a DHCPv6 relay agent.

------------------------------------------------------------------------

## Q37

**Question:** What is an advantage of configuring a Cisco router as a
relay agent?

**Type:** single

**Options:**

- It reduces the response time from a DHCP server.
- It can provide relay services for multiple UDP services.
- It can forward both broadcast and multicast messages on behalf of
  clients.
- It will allow DHCPDISCOVER messages to pass without alteration.

**Answer:** It can provide relay services for multiple UDP services.

**Explanation:** Cisco `ip helper-address` can relay several supported
UDP broadcast services, including DHCP/BOOTP.

------------------------------------------------------------------------

## Q38

**Question:** What is the reason that an ISP commonly assigns a DHCP
address to a wireless router in a SOHO environment?

**Type:** single

**Options:**

- better connectivity
- better network performance
- easy configuration on ISP firewall
- easy IP address management

**Answer:** easy IP address management

**Explanation:** DHCP allows the ISP to centrally and automatically
allocate addresses without manually configuring each customer's router.

------------------------------------------------------------------------

## Q39

**Question:** A company uses the SLAAC method to configure IPv6
addresses for the employee workstations. Which address will a client use
as its default gateway?

**Type:** single

**Options:**

- the unique local address of the router interface that is attached to
  the network
- the global unicast address of the router interface that is attached to
  the network
- the link-local address of the router interface that is attached to the
  network
- the all-routers multicast address

**Answer:** the link-local address of the router interface that is
attached to the network

**Explanation:** IPv6 hosts learn the default router through Router
Advertisements and use the router interface's link-local address as the
next-hop/default gateway.

------------------------------------------------------------------------

## Q40

**Question:** To verify a Stateless DHCPv6 Client Router receiver other
necessary DHPCv6 information, using The **show ipv6 dhcp**
*interface-type interface-number* command in global configuration mode
of the Client Router.

**Type:** true_false

**Options:**

- True
- False

**Answer:** False

**Explanation:** `show ipv6 dhcp interface-type interface-number` is a
privileged EXEC (`Router#`) verification command, not a global
configuration (`Router(config)#`) command.

------------------------------------------------------------------------

# Codex Verification Summary

The following questions require extra checking against the exact
quiz/source before treating the answer key as final:

- **Q9 — HIGH PRIORITY:** The supplied choices appear to omit the normal
  Cisco answer that an EtherChannel with inconsistent VLAN configuration
  fails/has a consistency problem.
- **Q10 — LOW/MEDIUM PRIORITY:** `desirable` is correct from the
  supplied choices, but the source concept commonly treats both `auto`
  and `desirable` as PAgP negotiating modes.
- **Q18 — HIGH PRIORITY:** Both `auto` and `desirable` are PAgP
  negotiating modes in the underlying Cisco concept, yet the question is
  formatted as single-choice.
- **Q24 — MEDIUM PRIORITY:** DHCP uses UDP 67 and 68. The question asks
  for one port; `67` is the expected server/relay destination answer,
  but common source versions ask for both ports.

**Instruction to Codex:** For tagged questions, do not assume the
reviewed answer is the LMS's expected answer. Compare the exact
wording/options with authoritative Cisco/NetAcad material or the
original quiz source. Keep the rest of the question bank unchanged
unless verification finds a concrete discrepancy.
