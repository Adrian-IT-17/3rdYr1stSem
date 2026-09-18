# FA1 - Networking Reviewer Reference

# Exhibit Rendering Instructions

Some questions originally contain Cisco networking diagrams or CLI screenshots.

For every question containing `**Has Exhibit:** Yes`:

1. Generate a visual exhibit above the question.
2. Follow the `Exhibit / Topology Description` as closely as possible.
3. Use a clean Cisco Packet Tracer / networking textbook style.
4. Show all IP addresses, VLAN IDs, interface names, device names, and CLI output specified in the description.
5. Do not reveal, highlight, color-code, or otherwise indicate the correct answer in the exhibit.
6. The exhibit must contain only information that would have been available to the student before answering.
7. Keep the topology readable on both desktop and mobile.
8. Prefer recreating the topology with HTML/CSS/SVG rather than relying on an external image.
9. Network links should clearly connect to the correct devices and interfaces.
10. If a question shares an exhibit with another question, reuse the same visual component rather than generating a different topology.

## Q1

**Question:** Match the **login** command with the device mode at which the command is entered.

**Type:** single

**Options:**

- R1#
- R1(config)#
- R1(config-if)#
- R1(config-line)#

**Answer:** R1(config-line)#

**Explanation:** The `login` command is configured in line configuration mode. This mode is used when configuring console or VTY lines for access to a Cisco device.

## Q2

**Question:** Match the **ip address 192.168.1.1 255.255.255.0** command with the device mode at which the command is entered.

**Type:** single

**Options:**

- R1(config-line)#
- R1#
- R1(config-if)#
- R1(config)#

**Answer:** R1(config-if)#

**Explanation:** The `ip address` command is entered in interface configuration mode because it assigns an IP address and subnet mask to a specific interface.

## Q3

**Question:** How is SSH different from Telnet?

**Type:** single

**Options:**

- SSH requires the use of the PuTTY terminal emulation program. Tera Term must be used to connect to devices through the use of Telnet.
- SSH makes connections over the network, whereas Telnet is for out-of-band access.
- SSH provides security to remote sessions by encrypting messages and using user authentication. Telnet is considered insecure and sends messages in plaintext
- SSH must be configured over an active network connection, whereas Telnet is used to connect to a device from a console connection.

**Answer:** SSH provides security to remote sessions by encrypting messages and using user authentication. Telnet is considered insecure and sends messages in plaintext

**Explanation:** SSH provides encrypted remote access and supports secure user authentication. Telnet transmits information in plaintext, making it less secure.

## Q4

**Question:** To support SSH in a Cisco Switch. The IOS version should have a filename that has?

**Type:** single

**Options:**

- K7
- K6
- K8
- K9

**Answer:** K9

**Explanation:** The K9 designation in a Cisco IOS image filename indicates that the image includes strong cryptographic features required to support technologies such as SSH.

## Q5

**Question:** HQ(config)# interface gi0/1

HQ(config-if)# description Connects to the Branch LAN

HQ(config-if)# ip address 172.19.99.99 255.255.255.0

HQ(config-if)# no shutdown

HQ(config-if)# interface gi0/0

HQ(config-if)# description Connects to the Store LAN

HQ(config-if)# ip address 172.19.98.230 255.255.255.0

HQ(config-if)# no shutdown

HQ(config-if)# interface s0/0/0

HQ(config-if)# description Connects to the ISP

HQ(config-if)# ip address 10.98.99.254 255.255.255.0

HQ(config-if)# no shutdown

HQ(config-if)# interface s0/0/1

HQ(config-if)# description Connects to the Head Office WAN

HQ(config-if)# ip address 209.165.200.120 255.255.255.0

HQ(config-if)# no shutdown

HQ(config-if)# end

Refer to the exhibit. A network administrator is connecting a new host to the Store LAN. The host needs to communicate with remote networks. What IP address would be configured as the default gateway on the new host?

**Type:** single

**Options:**

- 209.165.200.120
- 10.98.99.254
- 172.19.98.230
- 172.19.98.1

**Answer:** 172.19.98.230

**Explanation:** A host's default gateway should be the IP address of the router interface connected to its local network. The Store LAN is connected through Gi0/0, which has the IP address 172.19.98.230.

## Q6

**Question:** What is a characteristic of an IPv4 loopback interface on a Cisco IOS router?​

**Type:** single

**Options:**

- The no shutdown command is required to place this interface in an UP state.
- It is a logical interface internal to the router.
- Only one loopback interface can be enabled on a router.
- It is assigned to a physical port and can be connected to other devices.

**Answer:** It is a logical interface internal to the router.

**Explanation:** A loopback interface is a virtual or logical interface created internally on a router. It is not associated with a physical port and normally remains available as long as the router is operating.

## Q7

**Question:** Which command configures a name on the router?

**Type:** single

**Options:**

- Router(config)# enable password Cisco
- Router(config)# password Cisco
- Router(config)# hostname CL1
- Router(config)# banner motd #

**Answer:** Router(config)# hostname CL1

**Explanation:** The `hostname` command changes the device name. In this example, the router's hostname is changed to CL1.

## Q8

**Question:** SSH Operation uses TCP port?

**Type:** single

**Options:**

- 22
- 23
- 20
- 21

**Answer:** 22

**Explanation:** SSH uses TCP port 22 by default for secure remote access to network devices and systems.

## Q9

**Question:** What is the minimum Ethernet frame size that will not be discarded by the receiver as a runt frame?

**Type:** single

**Options:**

- 1024 bytes
- 512 bytes
- 1500 bytes
- 64 bytes

**Answer:** 64 bytes

**Explanation:** The minimum valid Ethernet frame size is 64 bytes. Ethernet frames smaller than 64 bytes are normally considered runt frames and are discarded.

## Q10

**Question:** Which command is used if you want to enter the console interface?

**Type:** single

**Options:**

- Line console 0
- Enable password
- Line vty 0 15
- Interface vlan 1

**Answer:** Line console 0

**Explanation:** The `line console 0` command enters line configuration mode for the physical console connection of a Cisco device.

## Q11

**Question:** Which one is the third phase during the boot up process of a Cisco Router?

**Type:** single

**Options:**

- enter setup mode
- locate and load the startup configuration file
- perform the POST and load the bootstrap program
- locate and load the Cisco IOS software

**Answer:** locate and load the startup configuration file

**Explanation:** After performing POST and loading the bootstrap program, the router locates and loads the IOS. The third major phase is locating and loading the startup configuration file from NVRAM.

## Q12

**Question:** using the shutdown command will turn on the deactivated port of a router.

**Type:** single

**Options:**

- True
- False

**Answer:** False

**Explanation:** The `shutdown` command administratively disables an interface. The `no shutdown` command is used to enable or activate it.

## Q13

**Question:** If one end of an Ethernet connection is configured for full duplex and the other end of the connection is configured for half duplex, where would late collisions be observed?

**Type:** single

**Options:**

- on both ends of the connection
- on the half-duplex end of the connection
- on the full-duplex end of the connection
- only on serial interfaces

**Answer:** on the half-duplex end of the connection

**Explanation:** A duplex mismatch can cause collisions because the half-duplex side uses collision detection while the full-duplex side does not. Late collisions are therefore observed on the half-duplex side.

## Q14

**Question:** It is a DTP mode that actively attempts to convert the link to a trunk.

**Type:** single

**Options:**

- Nonegotiate
- Dynamic auto
- Dynamic desirable
- Trunk

**Answer:** Dynamic desirable

**Explanation:** Dynamic desirable actively sends DTP messages in an attempt to negotiate a trunk connection with the neighboring switch.

## Q15

**Question:** Store-and-Forward switching have error checking and buffering characteristics.

**Type:** single

**Options:**

- True
- False

**Answer:** True

**Explanation:** Store-and-forward switching receives and buffers the entire Ethernet frame before forwarding it. This allows the switch to perform error checking using the frame's FCS/CRC information.

## Q16

**Question:** What type of VLAN is configured specifically for network traffic such as SSH, Telnet, HTTPS, HHTP, and SNMP?

**Type:** single

**Options:**

- management VLAN
- voice VLAN
- trunk VLAN
- security VLAN

**Answer:** management VLAN

**Explanation:** A management VLAN is used for network management traffic and provides access to network devices through protocols and services such as SSH, Telnet, HTTP/HTTPS, and SNMP.

## Q17

**Question:** VLAN 1006-4095 are used by service providers.

**Type:** single

**Options:**

- True
- False

**Answer:** True

**Explanation:** VLAN IDs 1006 through 4094 are part of the extended VLAN range and are commonly associated with environments that require large numbers of VLANs, including service-provider networks.

## Q18

**Question:** What type of VLAN is designed to have a delay of less than 150 ms across the network?

**Type:** single

**Options:**

- desirable VLAN
- trunk VLAN
- security VLAN
- voice VLAN

**Answer:** voice VLAN

**Explanation:** A voice VLAN is designed to carry voice traffic. Voice traffic is sensitive to latency and requires low delay to maintain acceptable call quality.

## Q19

**Question:** Which command displays the encapsulation type, the voice VLAN ID, and the access mode VLAN for the Fa0/1 interface?

**Type:** single

**Options:**

- show interfaces Fa0/1 switchport
- show vlan brief
- show mac address-table interface Fa0/1
- show interfaces trunk

**Answer:** show interfaces Fa0/1 switchport

**Explanation:** The `show interfaces Fa0/1 switchport` command displays detailed Layer 2 switchport information, including administrative and operational mode, access VLAN, voice VLAN, and trunking information.

## Q20

**Question:** Which switching method uses the CRC value in a frame?

**Type:** single

**Options:**

- fragment-free
- cut-through
- fast-forward
- store-and-forward

**Answer:** store-and-forward

**Explanation:** Store-and-forward switching receives the complete frame before forwarding it, allowing the switch to check the frame for errors using the FCS/CRC value.

## Q21

**Question:** DTP is On by default on Catalyst 2960 and 2950 switches.

**Type:** single

**Options:**

- True
- False

**Answer:** True

**Explanation:** DTP can operate by default on these Catalyst switch platforms to negotiate whether a link should operate as a trunk, depending on the switchport configuration and IOS behavior.

## Q22

**Question:** Under which occasion should an administrator disable DTP while managing a local area network?

**Type:** single

**Options:**

- on links that should not be trunking
- when a neighbor switch uses a DTP mode of dynamic desirable
- when a neighbor switch uses a DTP mode of dynamic desirable
- on links that should dynamically attempt trunking

**Answer:** on links that should not be trunking

**Explanation:** DTP should be disabled on links that are not intended to become trunks. This prevents unnecessary trunk negotiation and helps ensure that the port remains in its intended mode.

## Q23

**Question:** Refer to the exhibit. A network administrator is reviewing port and VLAN assignments on switch S2 and notices that interfaces Gi0/1 and Gi0/2 are not included in the output. Why would the interfaces be missing from the output?

**Type:** single

**Options:**

- They are administratively shut down.
- There is no media connected to the interfaces.
- There is a native VLAN mismatch between the switches.
- They are configured as trunk interfaces.

**Answer:** They are configured as trunk interfaces.

**Explanation:** The `show vlan brief` output lists access ports assigned to VLANs but does not list trunk ports in the same way. Gi0/1 and Gi0/2 connect S2 to other switches and are configured as trunk interfaces.

## Q24

**Question:** A switch build a MAC address table, also known as ___________.

**Type:** fill-in-the-blank

**Options:**

- N/A

**Answer:** CAM table

**Explanation:** A switch stores learned MAC addresses in a Content Addressable Memory (CAM) table. The table maps MAC addresses to switch ports so frames can be forwarded to the correct destination.

## Q25

**Question:** What type of VLAN is configured specifically for network traffic such as SSH, Telnet, HTTPS, HHTP, and SNMP?

**Type:** single

**Options:**

- native VLAN
- management VLAN
- security VLAN
- voice VLAN

**Answer:** management VLAN

**Explanation:** A management VLAN is dedicated to traffic used to configure, monitor, and manage network devices using services such as SSH, Telnet, HTTP/HTTPS, and SNMP.

## Q26

**Question:** Broadcast domains may be broken up by a layer 3 device, like a router.

**Type:** single

**Options:**

- True
- False

**Answer:** True

**Explanation:** Routers and other Layer 3 devices separate broadcast domains because they normally do not forward Layer 2 broadcast traffic between different networks.

## Q27

**Question:** With VLANs, unicast, multicast, and broadcast traffic is confined to a VLAN. Without a Layer 3 device to connect the VLANs, devices in different VLANs cannot communicate.

**Type:** single

**Options:**

- True
- False

**Answer:** True

**Explanation:** Each VLAN forms a separate logical network and broadcast domain. Communication between different VLANs requires Layer 3 routing, such as a router or multilayer switch.

## Q28

**Question:** Which of the following is used to configure VLAN 1 on an switch with an IP address of 208.211.78.200/28?

**Type:** single

**Options:**

- Switch(config)#set int vlan1
- Switch(config)#ip address 208.211.78.200 255.255.255.240
- Switch#conf t
- Switch(config)#vlan1 ip address 208.21.78.200 255.255.255.240
- Switch(config)#set vlan1 ip address 208.21.78.200 255.255.255.240
- Switch(config)#int vlan 1
  Switch(config-if)#ip address 208.211.78.200 255.255.255.240

**Answer:** Switch(config)#int vlan 1
Switch(config-if)#ip address 208.211.78.200 255.255.255.240

**Explanation:** VLAN 1 is configured through its switched virtual interface (SVI). The administrator first enters interface VLAN 1 configuration mode and then assigns the IP address and /28 subnet mask of 255.255.255.240.

## Q29

**Question:** Which solution would help a college alleviate network congestion due to collisions?

**Type:** single

**Options:**

- a router with two Ethernet ports
- a router with three Ethernet ports
- a firewall that connects to two Internet providers
- a high port density switch

**Answer:** a high port density switch

**Explanation:** A switch creates a separate collision domain for each switch port. A high port density switch provides many dedicated switched connections, helping reduce congestion caused by collisions.

## Q30

**Question:** Which solution would help a college alleviate network congestion due to collisions?

**Type:** single

**Options:**

- a router with two Ethernet ports
- a router with three Ethernet ports
- a firewall that connects to two Internet providers
- a high port density switch

**Answer:** a high port density switch

**Explanation:** Each switch port forms its own collision domain. Using a high port density switch gives devices dedicated switched connections and reduces the possibility of Ethernet collisions.

## Q31

**Question:** Management VLAN is used for dedicated to user-generated traffic.

**Type:** single

**Options:**

- True
- False

**Answer:** False

**Explanation:** A management VLAN is intended for traffic used to manage network devices. A data VLAN is the VLAN type dedicated to user-generated traffic.

## Q32

**Question:** Match the IEEE 802.1Q standard VLAN tag field with the description. A VLAN number.

**Type:** single

**Options:**

- Type
- Canonical Format Identifier
- User Priority
- VLAN ID

**Answer:** VLAN ID

**Explanation:** The VLAN ID field in an IEEE 802.1Q tag identifies the VLAN to which the Ethernet frame belongs.

## Q33

**Question:** Native VLAN is used for trunk links only.

**Type:** single

**Options:**

- True
- False

**Answer:** True

**Explanation:** The native VLAN is associated with IEEE 802.1Q trunk links and is used to handle untagged traffic received on the trunk.

## Q34

**Question:** Refer to the exhibit. A network administrator is reviewing port and VLAN assignments on switch S2 and notices that interfaces Gi0/1 and Gi0/2 are not included in the output. Why would the interfaces be missing from the output?

**Type:** single

**Options:**

- They are administratively shut down.
- There is no media connected to the interfaces.
- There is a native VLAN mismatch between the switches.
- They are configured as trunk interfaces.

**Answer:** They are configured as trunk interfaces.

**Explanation:** The displayed `show vlan brief` command primarily shows access-port VLAN assignments. The GigabitEthernet links connecting the switches are trunk ports, which is why Gi0/1 and Gi0/2 are not listed as access ports.

## Q35

**Question:** Which is statement is correct with respect to SVI inter-VLAN routing?

**Type:** single

**Options:**

- SVIs can be bundled into EtherChannels.
- Virtual interfaces support subinterfaces.
- Switching packets is faster with SVI.
- SVIs eliminate the need for a default gateway in the hosts.

**Answer:** Switching packets is faster with SVI.

**Explanation:** A multilayer switch can perform inter-VLAN routing using SVIs in hardware, providing high-speed packet forwarding without requiring an external router for traffic between VLANs.

## Q36

**Question:** Which statement IS true about interVLAN routing in the topology that is shown in the exhibit?

**Type:** single

**Options:**

- Host E and host F use the same IP gateway address.
- The FastEthernet 0/0 interface on Router1 and Switch2 trunk ports must be configured using the same encapsulation type
- Routed and Switch2 should be connected via a crossover cable.
- Router1 will not play a role in communications between host A and host D.

**Answer:** The FastEthernet 0/0 interface on Router1 and Switch2 trunk ports must be configured using the same encapsulation type

**Explanation:** In router-on-a-stick inter-VLAN routing, the router and switch trunk link must use compatible VLAN trunk encapsulation. This allows tagged VLAN traffic to be correctly exchanged across the trunk.

## Q37

**Question:** It is a DTP mode that is passively waits for the neighbor to initiate trunking.

**Type:** single

**Options:**

- Nonegotiate
- Dynamic desirable
- Dynamic auto
- Trunk

**Answer:** Dynamic auto

**Explanation:** Dynamic auto is a passive DTP mode. It does not actively attempt to form a trunk but can become a trunk when the neighboring port actively negotiates trunking.

## Q38

**Question:** The network shown in the diagram is experiencing connectivity problems. Which of the following will correct the problems?

**Type:** single

**Options:**

- Configure the masks on both hosts to be 255.255.255.224.
- Configure the gateway on Host A as 10.1.1.1.
- Configure the IP address of Host A as 10.1.2.2.
- Configure the gateway on Host B as 10.1.2.254.

**Answer:** Configure the gateway on Host B as 10.1.2.254.

**Explanation:** Host B belongs to VLAN 2 and the 10.1.2.0/24 network. Its correct default gateway is the router subinterface Fa0/0.2 at 10.1.2.254/24, rather than the VLAN 1 gateway.

## Q39

**Question:** How many VLANs can you create with subinterfaces on a FastEthernet interface?

**Type:** single

**Options:**

- 2
- 1000
- 4.2 billion
- 20000

**Answer:** 1000

**Explanation:** From the provided choices, 1000 is the intended answer. Router-on-a-stick allows many VLANs to share one physical FastEthernet interface by creating separate logical subinterfaces for the VLANs.

## Q40

**Question:** To verify DTP mode. Use the ___________ command.

**Type:** fill-in-the-blank

**Options:**

- N/A

**Answer:** show dtp interface

**Explanation:** The `show dtp interface` command displays Dynamic Trunking Protocol information for switch interfaces and can be used to verify DTP operation and mode.

## Q41

**Question:** What is an advantage of using multilayer switches?

**Type:** single

**Options:**

- The route processor also performs the switching of Layer 2 packets between switch ports.
- The router is highly integrated within the switch and allows high speed routing.
- It is not as efficient as router-on-a-stick
- The route switch processor is faster since all switching is performed in software

**Answer:** The router is highly integrated within the switch and allows high speed routing.

**Explanation:** A multilayer switch combines Layer 2 switching and Layer 3 routing capabilities in the same device. This integration allows inter-VLAN and other routing operations to be performed at high speeds using switching hardware.


-----------------
## Q23

**Question:** Refer to the exhibit. A network administrator is reviewing port and VLAN assignments on switch S2 and notices that interfaces Gi0/1 and Gi0/2 are not included in the output. Why would the interfaces be missing from the output?

**Type:** single

**Has Exhibit:** Yes

**Exhibit Type:** Network topology + Cisco CLI output

**Exhibit / Topology Description:**

Recreate the exhibit as a simple Cisco-style network topology.

Topology:
- Three switches are arranged in a triangle.
- S1 is at the top.
- S2 is at the bottom-left.
- S3 is at the bottom-right.
- S1 connects directly to S2.
- S1 connects directly to S3.
- S2 connects directly to S3.
- The links between the switches represent inter-switch links.
- On S2, interfaces Gi0/1 and Gi0/2 are used as links to the other switches.

Below the topology, display Cisco CLI output from switch S2 for the command:

`S2# show vlan brief`

The output should show VLANs and their access ports, but Gi0/1 and Gi0/2 should NOT appear in the VLAN access-port assignments.

Important visual clue:
- Gi0/1 and Gi0/2 connect S2 to other switches.
- They are trunk links.
- The purpose of the exhibit is for the student to determine why these interfaces do not appear in `show vlan brief`.

**Options:**

- They are administratively shut down.
- There is no media connected to the interfaces.
- There is a native VLAN mismatch between the switches.
- They are configured as trunk interfaces.

**Answer:** They are configured as trunk interfaces.

**Explanation:** The `show vlan brief` output lists access ports assigned to VLANs but does not list trunk ports in the same way. Gi0/1 and Gi0/2 connect S2 to other switches and are configured as trunk interfaces.


## Q34

**Question:** Refer to the exhibit. A network administrator is reviewing port and VLAN assignments on switch S2 and notices that interfaces Gi0/1 and Gi0/2 are not included in the output. Why would the interfaces be missing from the output?

**Type:** single

**Has Exhibit:** Yes

**Exhibit Type:** Network topology + Cisco CLI output

**Exhibit / Topology Description:**

This question uses the SAME exhibit as Q23.

Recreate the exhibit as a simple Cisco-style network topology.

Topology:
- Three switches are arranged in a triangle.
- S1 is at the top.
- S2 is at the bottom-left.
- S3 is at the bottom-right.
- S1 connects directly to S2.
- S1 connects directly to S3.
- S2 connects directly to S3.
- On S2, Gi0/1 and Gi0/2 are inter-switch links.

Below the topology, show:

`S2# show vlan brief`

The output lists access ports assigned to VLANs but does not show S2 interfaces Gi0/1 and Gi0/2 among the VLAN access-port assignments.

Important visual clue:
- Gi0/1 and Gi0/2 are connections between switches.
- These interfaces are operating as trunk interfaces.

**Options:**

- They are administratively shut down.
- There is no media connected to the interfaces.
- There is a native VLAN mismatch between the switches.
- They are configured as trunk interfaces.

**Answer:** They are configured as trunk interfaces.

**Explanation:** The displayed `show vlan brief` command primarily shows access-port VLAN assignments. The GigabitEthernet links connecting the switches are trunk ports, which is why Gi0/1 and Gi0/2 are not listed as access ports.


## Q36

**Question:** Which statement IS true about interVLAN routing in the topology that is shown in the exhibit?

**Type:** single

**Has Exhibit:** Yes

**Exhibit Type:** Router-on-a-stick inter-VLAN topology

**Exhibit / Topology Description:**

Recreate the exhibit as a Cisco-style router-on-a-stick topology.

Overall layout:
- Router1 is positioned at the top.
- Switch2 is positioned directly below Router1.
- Router1 and Switch2 are connected using Router1 FastEthernet 0/0 and a switch trunk port.
- Multiple VLANs exist on Switch2.
- End devices are connected to access ports belonging to different VLANs.
- Hosts are labeled with letters, including Host A, Host D, Host E, and Host F.

Logical operation:
- Router1 performs inter-VLAN routing.
- The physical connection between Router1 and Switch2 carries traffic for multiple VLANs.
- Router1 uses its FastEthernet 0/0 connection for the VLAN trunk.
- The switch port connected to Router1 must also operate as a trunk.
- The trunk on Router1 and the trunk on Switch2 must use compatible IEEE 802.1Q encapsulation.

Important visual clue:
- A single physical Ethernet connection between Router1 and Switch2 carries multiple VLANs.
- This represents a router-on-a-stick configuration.
- Hosts in different VLANs rely on Router1 to communicate with one another.

Codex rendering guidance:
- Draw Router1 using a router icon.
- Draw Switch2 using a switch icon.
- Place several PC/host icons below or around Switch2.
- Label the hosts A, D, E, and F where appropriate.
- Clearly label the Router1-to-Switch2 connection as a trunk.
- Label the router side `Fa0/0`.
- Visually indicate that multiple VLANs traverse the trunk.

**Options:**

- Host E and host F use the same IP gateway address.
- The FastEthernet 0/0 interface on Router1 and Switch2 trunk ports must be configured using the same encapsulation type
- Routed and Switch2 should be connected via a crossover cable.
- Router1 will not play a role in communications between host A and host D.

**Answer:** The FastEthernet 0/0 interface on Router1 and Switch2 trunk ports must be configured using the same encapsulation type

**Explanation:** In router-on-a-stick inter-VLAN routing, the router and switch trunk link must use compatible VLAN trunk encapsulation. This allows tagged VLAN traffic to be correctly exchanged across the trunk.


## Q38

**Question:** The network shown in the diagram is experiencing connectivity problems. Which of the following will correct the problems?

**Type:** single

**Has Exhibit:** Yes

**Exhibit Type:** Router-on-a-stick VLAN troubleshooting topology

**Exhibit / Topology Description:**

Recreate the exhibit as a Cisco-style router-on-a-stick network.

Overall layout:
- One router is positioned at the top.
- One switch is positioned below the router.
- Two hosts are connected to the switch.
- Host A belongs to VLAN 1.
- Host B belongs to VLAN 2.
- The switch-to-router connection is a trunk.
- The router uses subinterfaces to provide Layer 3 gateways for the two VLANs.

Router configuration shown in the topology:
- Physical interface: FastEthernet 0/0
- Subinterface: FastEthernet 0/0.1
  - Associated with VLAN 1
  - IP address: `10.1.1.254/24`
- Subinterface: FastEthernet 0/0.2
  - Associated with VLAN 2
  - IP address: `10.1.2.254/24`

Host A:
- Connected to an access port in VLAN 1.
- Host A belongs to network `10.1.1.0/24`.
- Its correct gateway should therefore be `10.1.1.254`.

Host B:
- Connected to an access port in VLAN 2.
- Host B belongs to network `10.1.2.0/24`.
- Its correct gateway should therefore be `10.1.2.254`.
- The exhibit contains an incorrect gateway configuration for Host B, creating the connectivity problem.

Important visual clue:
- Router subinterface Fa0/0.1 is the gateway for VLAN 1.
- Router subinterface Fa0/0.2 is the gateway for VLAN 2.
- Host B must use `10.1.2.254` as its default gateway.

Codex rendering guidance:
- Place the router at the top center.
- Place the switch below it.
- Draw one trunk link between the router and switch.
- Place Host A on the left side of the switch.
- Place Host B on the right side of the switch.
- Label Host A as VLAN 1.
- Label Host B as VLAN 2.
- Show the router subinterface addresses next to the router.
- Show each host's IP configuration near its PC icon.
- Make the incorrect Host B gateway visible so the student has to diagnose it.
- Do NOT visually highlight or reveal the correct answer.

**Options:**

- Configure the masks on both hosts to be 255.255.255.224.
- Configure the gateway on Host A as 10.1.1.1.
- Configure the IP address of Host A as 10.1.2.2.
- Configure the gateway on Host B as 10.1.2.254.

**Answer:** Configure the gateway on Host B as 10.1.2.254.

**Explanation:** Host B belongs to VLAN 2 and the 10.1.2.0/24 network. Its correct default gateway is the router subinterface Fa0/0.2 at 10.1.2.254/24, rather than the VLAN 1 gateway.




Read thi part as a correction so you can double check the questions because the pasted questions and answers here got 38/40, correct it with your networking knowledge
Looking back through the answers we used, two stand out as likely responsible for the 38/40:

“VLAN 1006-4095 are used by service providers.”
We answered True. This is likely False. The extended VLAN range is generally 1006–4094; 4095 is reserved and cannot be used as a normal VLAN ID. So the statement as written is technically false.
“DTP is On by default on Catalyst 2960 and 2950 switches.”
We answered True. This one is suspicious and may be the other incorrect answer depending on the course material/version. The default switchport/DTP behavior differs across Catalyst models and IOS versions, so a blanket statement covering both 2950 and 2960 may be marked False in your reviewer.

There is also one answer I would investigate before locking #2 in: “How many VLANs can you create with subinterfaces on a FastEthernet interface?” → 1000. Of the provided choices, 1000 is clearly the intended classroom answer, but the wording is technically awkward because the number of router subinterfaces is not simply defined as “1000 VLANs.”

So my strongest candidate is Q17 (1006–4095) = False, while the second is most likely Q21 (DTP default) = False.

For the Codex reviewer, I would not keep Q17 as True.