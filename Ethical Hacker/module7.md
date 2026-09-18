# Module 7: Cloud, Mobile, and IoT Security

## Q1
**Question:** Which term is an essential characteristic of cloud computing as defined in NIST SP 800-145?
**Type:** single
**Options:**
- Centralized storage
- Resource pooling
- Reduced bandwidth requirements
- Slow elasticity
**Answer:** Resource pooling
**Explanation:** NIST SP 800-145 defines five essential characteristics of cloud computing: on-demand self-service, broad network access, resource pooling, rapid elasticity, and measured service.

## Q2
**Question:** Which cloud technology attack method involves breaching the infrastructure to gather and steal information such as valid usernames, passwords, tokens, and PINs?
**Type:** single
**Options:**
- Account takeover
- Credential harvesting
- Privilege escalation
- Side-channel attacks
**Answer:** Credential harvesting
**Explanation:** Credential harvesting is the act of gathering and stealing valid usernames, passwords, tokens, PINs, and other credentials through infrastructure breaches.

## Q3
**Question:** Which cloud technology attack method could exploit a bug in a software application to gain access to resources that normally would not be accessible to a user?
**Type:** single
**Options:**
- Account takeover
- Credential harvesting
- Privilege escalation
- Side-channel attacks
**Answer:** Privilege escalation
**Explanation:** Privilege escalation exploits a bug or design flaw in a software or firmware application to access resources normally protected from that application or user.

## Q4
**Question:** Which term describes when a lower-privileged user accesses functions reserved for higher-privileged users?
**Type:** single
**Options:**
- Vertical privilege escalation
- Horizontal privilege escalation
- Credential harvesting
- Metadata service attacks
**Answer:** Vertical privilege escalation
**Explanation:** Vertical privilege escalation occurs when a lower-privileged user accesses functions reserved for higher-privileged users, such as a standard user accessing administrator functions.

## Q5
**Question:** Which cloud technology attack method could a threat actor use to access a user or application account that allows access to more accounts and information?
**Type:** single
**Options:**
- Account takeover
- Metadata service attacks
- Resource exhaustion and DoS attacks
- Side-channel attacks
**Answer:** Account takeover
**Explanation:** In an account takeover attack, the threat actor gains access to a user or application account and uses it to access further accounts and information.

## Q6
**Question:** Which tool could be used to find vulnerabilities that could lead to metadata service attacks?
**Type:** single
**Options:**
- Nimbostratus
- Clair
- Falco
- Dagda
**Answer:** Nimbostratus
**Explanation:** Nimbostratus is a tool that can be used to find vulnerabilities that could lead to metadata service attacks.

## Q7
**Question:** Which cloud technology attack method could generate crafted packets to cause a cloud application to crash?
**Type:** single
**Options:**
- Resource exhaustion attack
- Account takeover
- Metadata service attack
- Side-channel attack
**Answer:** Resource exhaustion attack
**Explanation:** Threat actors can launch DoS attacks against cloud-hosted applications, including leveraging single-packet DoS vulnerabilities or crafted-packet tools, causing resource exhaustion and application crashes.

## Q8
**Question:** Which cloud technology attack method would require the threat actor to create a malicious application and install it into a SaaS, PaaS, or IaaS environment?
**Type:** single
**Options:**
- Resource exhaustion attack
- Account takeover
- Metadata service attack
- Cloud malware injection attack
**Answer:** Cloud malware injection attack
**Explanation:** In a cloud malware injection attack, the attacker injects a malicious application into a SaaS, PaaS, or IaaS environment, where it runs as a valid instance and can be used to launch further attacks such as backdoors, eavesdropping, and data theft.

## Q9
**Question:** What is a common cause of data breaches in attacks against misconfigured cloud assets?
**Type:** single
**Options:**
- Using insecure permission configurations for cloud object storage services
- Using hard-coded credentials to access different services
- Implementing metadata service to get a set of temporary access credentials
- Adding sensitive information in user startup scripts
**Answer:** Using insecure permission configurations for cloud object storage services
**Explanation:** Insecure permission configurations for cloud object storage services, such as Amazon S3 buckets, are a frequent cause of cloud data breaches.

## Q10
**Question:** A threat actor has compromised a VM in a cloud environment that shares the same physical hardware as non-compromised VMs. Which cloud technology attack method could now be used to exfiltrate credentials, cryptographic keys, and other sensitive information?
**Type:** single
**Options:**
- Side-channel attack
- Cloud malware injection attack
- Resource exhaustion attack
- Account takeover
**Answer:** Side-channel attack
**Explanation:** Side-channel attacks exploit information gained from the physical implementation of a system (like shared hardware) rather than a specific software weakness.

## Q11
**Question:** Which tool helps software developers and cloud consumers deploy applications in the cloud and use the resources that the cloud provider offers?
**Type:** single
**Options:**
- Software development kits (SDKs)
- Cloud development kits (CDKs)
- Identity and access management (IAM)
- Nimbostratus
**Answer:** Cloud development kits (CDKs)
**Explanation:** CDKs help developers and cloud consumers deploy applications and consume the resources a cloud provider offers.

## Q12
**Question:** Which mobile device vulnerability is targeted when a threat actor reverse engineers a mobile app to see how it creates and stores keys in the iOS Keychain?
**Type:** single
**Options:**
- Insecure storage
- Passcode vulnerabilities and biometric integrations
- Certificate pinning
- Using known vulnerable components
**Answer:** Insecure storage
**Explanation:** An attacker may use static analysis or reverse engineering to examine how an app creates and stores keys in the iOS Keychain, targeting insecure storage practices.

## Q13
**Question:** Which tool is an open-source framework used to test the security of iOS applications?
**Type:** single
**Options:**
- Needle
- Drozer
- APK Studio
- ApkX
**Answer:** Needle
**Explanation:** Needle is an open-source framework for testing iOS application security. Drozer, APK Studio, and ApkX are Android-focused testing tools.

## Q14
**Question:** Match the Bluetooth Low Energy (BLE) phase to the description.
**Type:** matching
**Pairs:**
- Phase 1 -> Transport-specific key distribution
- Phase 2 -> Short-term key generation
- Phase 3 -> Pairing feature exchange
**Explanation:** BLE pairing proceeds through these three phases, as listed in the source material.

## Q15
**Question:** Which option is a security vulnerability that affects IoT implementations?
**Type:** single
**Options:**
- Plaintext communication and data leakage
- VM escape vulnerabilities
- Certificate pinning
- Hyperjacking
**Answer:** Plaintext communication and data leakage
**Explanation:** Common IoT vulnerabilities include insecure defaults, plaintext communication and data leakage, hard-coded configurations, and outdated firmware/hardware or insecure components.

## Q16
**Question:** Which two IoT systems should never be exposed to the Internet? (Choose two.)
**Type:** multi
**Options:**
- Turbines in a power plant
- Robots in a factory
- Refrigerators in a restaurant
- Thermostat in a home
- Carbon monoxide detectors in a home
**Answer:** Turbines in a power plant; Robots in a factory
**Explanation:** Many IoT, ICS, and SCADA systems — such as PLCs controlling power plant turbines, stadium lighting, or factory robots — should never be exposed directly to the Internet.

## Q17
**Question:** Which option is a collection of compute interface specifications designed to offer management and monitoring capabilities independently of the CPU, firmware, and operating system of the host?
**Type:** single
**Options:**
- Intelligent Platform Management Interface (IPMI)
- Shodan
- Supervisory control and data acquisition (SCADA)
- Mobile Security Framework (MobSF)
**Answer:** Intelligent Platform Management Interface (IPMI)
**Explanation:** IPMI is a collection of compute interface specifications, often used in IoT systems, providing management and monitoring capabilities independent of the host's CPU, firmware, and OS.

## Q18
**Question:** A threat actor uploaded a VM with malicious software to the VMware Marketplace. When an organization deploys the VM, the threat actor can manipulate the systems, applications, and user data. What type of VM vulnerability has been enabled?
**Type:** single
**Options:**
- VM repository vulnerability
- Hypervisor vulnerability
- Hyperjacking
- VM escape vulnerability
**Answer:** VM repository vulnerability
**Explanation:** A VM repository vulnerability occurs when a threat actor uploads fake or impersonated VMs containing malware or backdoors, which organizations then unknowingly deploy.

## Q19
**Question:** Which tool is a set of open-source analysis tools that uses the ClamAV antivirus engine to help detect vulnerabilities, Trojans, backdoors, and malware in Docker images and containers?
**Type:** single
**Options:**
- Anchore's Grype
- Clair
- Dagda
- Falco
**Answer:** Dagda
**Explanation:** Dagda is a set of open-source static analysis tools that uses the ClamAV antivirus engine to detect vulnerabilities, Trojans, backdoors, and malware in Docker images and containers.

## Q20
**Question:** Which credential harvesting tool could be used to send a spear phishing email with a link to a malicious site to a target victim?
**Type:** single
**Options:**
- Social-Engineer Toolkit (SET)
- Searchsploit
- Drozer
- Dagda
**Answer:** Social-Engineer Toolkit (SET)
**Explanation:** SET can perform social engineering attacks, including instantiating a fake website to run a credential harvesting attack via spear phishing emails.

## Q21
**Question:** Why do cloud architectures help minimize the impact of DoS or DDoS attacks compared to hosting services on-premise?
**Type:** single
**Options:**
- Cloud providers use a distributed architecture
- Cloud providers provide sandbox analysis
- Cloud providers limit network exposure to the internet
- Cloud providers use Intelligent Platform Management Interfaces (IPMI)
**Answer:** Cloud providers use a distributed architecture
**Explanation:** Leading cloud providers offer distributed, resilient architectures that help absorb and minimize the impact of DoS/DDoS attacks compared to on-premises hosting.

## Q22
**Question:** Which option is a characteristic of a VM hypervisor?
**Type:** single
**Options:**
- Type 1 hypervisors are also known as native or bare-metal hypervisors.
- Type 1 hypervisors run on top of other operating systems.
- Type 2 hypervisors include VMware ESXi and Microsoft Hyper-V.
- Type 2 hypervisors run directly on the physical (bare-metal) system.
**Answer:** Type 1 hypervisors are also known as native or bare-metal hypervisors.
**Explanation:** Type 1 (native/bare-metal) hypervisors run directly on physical hardware (e.g., VMware ESXi, Proxmox, Xen, Hyper-V). Type 2 (hosted) hypervisors run on top of an OS (e.g., VirtualBox, VMware Workstation/Player).

## Q23
**Question:** A threat actor has compromised a VM in a data center and discovered a vulnerability that provides access to data in another VM. What type of VM vulnerability has been discovered?
**Type:** single
**Options:**
- VM escape vulnerability
- VM repository vulnerability
- Hypervisor vulnerability
- Hyperjacking
**Answer:** VM escape vulnerability
**Explanation:** VM escape vulnerabilities let a threat actor "escape" a VM to access other virtual machines on the system, or the hypervisor itself.

## Q24
**Question:** Which tool can be used to perform on-path attacks in BLE implementations?
**Type:** single
**Options:**
- GATTacker
- Social-Engineer Toolkit (SET)
- Nimbostratus
- Dagda
**Answer:** GATTacker
**Explanation:** GATTacker is a tool that can be used to perform on-path attacks in Bluetooth Low Energy (BLE) implementations.

## Q25
**Question:** Which tool is an open-source container vulnerability scanner that can be used to find vulnerabilities in a Docker image?
**Type:** single
**Options:**
- Anchore's Grype
- GATTacker
- Social-Engineer Toolkit (SET)
- Nimbostratus
**Answer:** Anchore's Grype
**Explanation:** Anchore's Grype is an open-source container vulnerability scanner used to find vulnerabilities in Docker images.
