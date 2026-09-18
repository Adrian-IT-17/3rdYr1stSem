# Module 8: Performing Post-Exploitation Techniques

## Q1
**Question:** Which resource is a Windows utility that combines the old CMD functionality with a new scripting/cmdlet instruction set with built-in system administration functionality?
**Type:** single
**Options:**
- Socat
- Wsc2
- PowerShell
- Twittor
**Answer:** PowerShell
**Explanation:** Windows PowerShell combines the old command prompt (CMD) with a scripting/cmdlet instruction set and built-in system administration functionality, letting users automate complex tasks with reusable scripts. Socat, wsc2, and Twittor are C2 utilities.

## Q2
**Question:** An attacker opens a port or a listener on the compromised system and waits for a connection. The goal is to connect to the victim from any system, execute commands, and further manipulate the victim. What type of malicious activity is being performed?
**Type:** single
**Options:**
- Reverse shell
- Horizontal privilege escalation
- Bind shell
- Vertical privilege escalation
**Answer:** Bind shell
**Explanation:** With a bind shell, the attacker opens a port or listener on the compromised system and waits for an incoming connection, then uses it to execute commands and manipulate the victim system.

## Q3
**Question:** Which resource is a lightweight and portable tool that allows the creation of bind and reverse shells from a compromised host?
**Type:** single
**Options:**
- WMImplant
- WSC2
- BloodHound
- Netcat
**Answer:** Netcat
**Explanation:** Netcat is a lightweight, portable, and versatile tool for creating bind and reverse shells. WMImplant leverages WMI for C2, wsc2 uses WebSockets for C2, and BloodHound reveals hidden relationships in Active Directory environments.

## Q4
**Question:** A cybersecurity student is learning about Netcat commands that could be used in a penetration testing engagement. Which Netcat command is used to connect to a TCP port?
**Type:** single
**Options:**
- nc -nv <IP address> <Port>
- nc -lvp <port>
- nc -z <IP address> <port range>
- nc -nv <IP address> <input.txt>
**Answer:** nc -nv <IP address> <Port>
**Explanation:** `nc -nv <IP> <Port>` connects to a TCP port. `nc -lvp <port>` listens on a port, the file-transfer pair uses `-lvp` with output redirection and `-nv` with an input file, and `nc -z <IP> <port range>` is used for port scanning.

## Q5
**Question:** Which Meterpreter command is used to execute Meterpreter commands that are listed inside a text file and also to help accelerate the actions taken on the victim system?
**Type:** single
**Options:**
- search
- execute
- resource
- shell
**Answer:** resource
**Explanation:** The `resource` command executes Meterpreter commands listed inside a text file, accelerating actions on the victim system. `search` locates files, `shell` drops into a standard shell, and `execute` runs commands on the victim system.

## Q6
**Question:** Which two resources are C2 utilities? (Choose two.)
**Type:** multi
**Options:**
- Socat
- Empire
- BloodHound
- Netcat
- Twittor
**Answer:** Socat; Twittor
**Explanation:** Socat can create multiple reverse shells for C2, and Twittor uses Twitter direct messages for command and control. Netcat is a general-purpose network utility, and BloodHound reveals Active Directory relationships rather than functioning as a C2 channel.

## Q7
**Question:** What kind of channel is created by a C2 with a system that has been compromised?
**Type:** single
**Options:**
- Wireless channel
- Encrypted channel
- Covert channel
- Command channel
**Answer:** Covert channel
**Explanation:** A C2 creates a covert channel — an adversarial technique letting an attacker transfer information between processes or systems that a security policy would normally disallow from communicating.

## Q8
**Question:** Which living-off-the-land post-exploitation technique can get directory listings, copy and move files, get a list of running processes, and perform administrative tasks?
**Type:** single
**Options:**
- PowerShell
- Sysinternals
- WMI
- BloodHound
**Answer:** PowerShell
**Explanation:** PowerShell can list directories, copy/move files, list running processes, and perform administrative tasks. Sysinternals lets admins control Windows machines remotely, BloodHound maps AD relationships, and WMI manages Windows data and operations.

## Q9
**Question:** Which resource is an open-source framework that allows rapid deployment of post-exploitation modules, including keyloggers, bind and reverse shells, and adaptable communication to evade detection?
**Type:** single
**Options:**
- BloodHound
- Sysinternals
- WMI
- Empire
**Answer:** Empire
**Explanation:** Empire includes a PowerShell Windows agent and Python Linux agent, enabling rapid deployment of post-exploitation modules such as keyloggers, bind/reverse shells, Mimikatz, and detection-evading communication.

## Q10
**Question:** Which resource is a single-page JavaScript web application that can be used to find complex attack paths in Microsoft Azure?
**Type:** single
**Options:**
- Empire
- Netcat
- BloodHound
- Sysinternals
**Answer:** BloodHound
**Explanation:** BloodHound uses graph theory to reveal hidden relationships in Windows Active Directory and can also be used to find complex attack paths in Microsoft Azure, useful for both attackers and incident responders.

## Q11
**Question:** Which utility can be used to write scripts or applications to automate administrative tasks on remote computers and can also be used by malware to perform different activities in a compromised system?
**Type:** single
**Options:**
- WMI
- PowerShell
- Empire
- BloodHound
**Answer:** WMI
**Explanation:** Windows Management Instrumentation (WMI) manages data and operations on Windows systems and can be scripted for remote administrative tasks — malware (e.g., NotPetya) has used WMI to perform administrative actions on compromised systems.

## Q12
**Question:** Which Sysinternals tool is used by penetration testers to modify Windows registry values and connect a compromised system to another system?
**Type:** single
**Options:**
- PsInfo
- PsLoggedOn
- PsGetSid
- PsExec
**Answer:** PsExec
**Explanation:** PsExec is one of the most powerful Sysinternals tools — it can remotely execute anything runnable from a Windows command prompt, modify registry values, execute scripts, and connect a compromised system to another.

## Q13
**Question:** Which three tools are living-off-the-land post-exploitation techniques? (Choose three.)
**Type:** multi
**Options:**
- Twittor
- PowerSploit
- Socat
- WMImplant
- WinRM
- Empire
**Answer:** PowerSploit; WinRM; Empire
**Explanation:** Living-off-the-land post-exploitation techniques include Empire, WMI, BloodHound, PowerShell, Sysinternals, WinRM, and PowerSploit. WMImplant, Twittor, and socat are C2 utilities, not living-off-the-land tools.

## Q14
**Question:** An attacker wants to allow further connections to a compromised system and maintain persistent access. The attacker uses the Windows system command `Enable-PSRemoting -SkipNetworkProfileCheck -Force`. What tool is being enabled using this command?
**Type:** single
**Options:**
- WinRM
- BloodHound
- PsExec
- WMImplant
**Answer:** WinRM
**Explanation:** This command enables WinRM, configuring the service to start automatically and setting up a firewall rule to allow inbound connections to the compromised system for further post-exploitation access.

## Q15
**Question:** What kind of malicious activity is performed by a lower-privileged user who accesses functions reserved for higher-privileged users?
**Type:** single
**Options:**
- Horizontal privilege escalation
- Steganography
- Bind shell
- Vertical privilege escalation
**Answer:** Vertical privilege escalation
**Explanation:** Vertical privilege escalation occurs when a lower-privileged user gains access to functions reserved for higher-privileged users, such as root or administrator access.

## Q16
**Question:** What task can be accomplished with the steghide tool?
**Type:** single
**Options:**
- To modify Windows registry values and to connect a compromised system to another system
- To find complex attack paths in Microsoft Azure
- To obfuscate, to evade and to cover the attacker tracks
- To allow administrators to control a Windows-based computer from a remote terminal
**Answer:** To obfuscate, to evade and to cover the attacker tracks
**Explanation:** Steganography hides a message or content inside an image or video file, and tools like steghide let attackers use this technique to obfuscate, evade detection, and cover their tracks.

## Q17
**Question:** After compromising a system during a penetration testing engagement, all penetration work should be cleaned up, including extra files, system changes, and modified logs. The media sanitation methodology should be discussed with the client and the owner of the affected systems. What document guides media sanitation?
**Type:** single
**Options:**
- NIST SP 800-88
- OWASP ZAP
- OSSTMM
- PCI DSS
**Answer:** NIST SP 800-88
**Explanation:** NIST Special Publication 800-88, Revision 1, "Guidelines for Media Sanitization," guides how systems should be cleaned up after a penetration testing engagement, including secure deletion methods.

## Q18
**Question:** What procedure should be deployed to protect the network against lateral movement?
**Type:** single
**Options:**
- Database backups
- VPNs
- Strong passwords for user accounts
- VLANs
**Answer:** VLANs
**Explanation:** Lateral movement is possible when a network isn't properly segmented. Deploying VLANs (along with firewalls or access control policies) for segmentation helps limit an attacker's ability to move laterally.

## Q19
**Question:** What is the main advantage of Remote Desktop over Sysinternals?
**Type:** single
**Options:**
- It can upload, execute, and interact with executables on compromised hosts.
- It can run commands revealing information about running processes, and services can be killed and stopped.
- It can use PsExec to remotely execute anything that can run on a Windows command prompt.
- It gives a full, interactive GUI of the remote compromised computer.
**Answer:** It gives a full, interactive GUI of the remote compromised computer.
**Explanation:** Remote Desktop's main advantage over tools like Sysinternals is providing a full, interactive graphical user interface of the remote compromised machine; the other options describe Sysinternals capabilities.

## Q20
**Question:** An attacking system has a listener (port open), and the victim initiates a connection back to the attacking system. What type of vulnerability does this situation describe?
**Type:** single
**Options:**
- Reverse shell
- Horizontal privilege escalation
- Bind shell
- Vertical privilege escalation
**Answer:** Reverse shell
**Explanation:** In a reverse shell, the attacker's system has a listener open, and the victim initiates the connection back to the attacker — the opposite of a bind shell, where the attacker connects to a listener on the victim.

## Q21
**Question:** A cybersecurity student is learning about Netcat commands that could be used in a penetration testing engagement. The student wants to use Netcat as a port scanner. What command should be used?
**Type:** single
**Options:**
- nc -nv <IP address> <Port>
- nc -lvp <port>
- nc -z <IP address> <port range>
- nc -nv <IP address> <input.txt>
**Answer:** nc -z <IP address> <port range>
**Explanation:** `nc -z <IP> <port range>` is used as a port scanner. The other commands connect to a TCP port, listen on a port, or transfer files.

## Q22
**Question:** Which C2 utility is a PowerShell-based tool that leverages WMI to create a C2 channel?
**Type:** single
**Options:**
- Socat
- WMImplant
- WSC2
- TrevorC2
**Answer:** WMImplant
**Explanation:** WMImplant is a PowerShell-based tool that leverages WMI to create a C2 channel. Socat creates reverse shells, wsc2 uses WebSockets, and TrevorC2 is a Python-based C2 utility.

## Q23
**Question:** Which two C2 utilities are Python-based? (Choose two.)
**Type:** multi
**Options:**
- TrevorC2
- Socat
- DNSCat2
- Wsc2
- Twittor
**Answer:** TrevorC2; Wsc2
**Explanation:** Among common C2 utilities (Twittor, wsc2, DNSCat2, socat, TrevorC2), wsc2 and TrevorC2 are Python-based.

## Q24
**Question:** After the exploitation phase, it is necessary to maintain a foothold in a compromised system to perform additional tasks. Which way could maintain persistence?
**Type:** single
**Options:**
- Performing ARP scans and ping sweeps
- Performing additional enumeration of users, groups, forests, sensitive data, and unencrypted files
- Creating a bind or reverse shell
- Using local system tools
**Answer:** Creating a bind or reverse shell
**Explanation:** Persistence can be maintained by creating a bind or reverse shell, creating/manipulating scheduled jobs and tasks, creating custom daemons and processes, or creating new users.

## Q25
**Question:** Which two commands are the same in Meterpreter and Linux or Unix-based systems? (Choose two.)
**Type:** multi
**Options:**
- pwd
- hashdump
- clearev
- resource
- cat
**Answer:** pwd; cat
**Explanation:** Meterpreter commands shared with Linux/Unix-based systems include cat, cd, pwd, and ls. hashdump, clearev, and resource are Meterpreter-specific commands.