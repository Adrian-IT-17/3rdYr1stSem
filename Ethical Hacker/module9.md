# Module 9: Reporting and Communication

## Q1
**Question:** Which industry-standard method has created a catalog of known vulnerabilities that provides a score indicating the severity of a vulnerability?
**Type:** single
**Options:**
- CVSS
- CVE
- OWASP WSTG
- NIST SP 800-115
**Answer:** CVSS
**Explanation:** The Common Vulnerability Scoring System (CVSS) provides a score from 0 to 10 indicating a vulnerability's severity. CVE lists publicly known vulnerabilities with IDs, OWASP WSTG is a web application testing guide, and NIST SP 800-115 provides security testing planning guidelines.

## Q2
**Question:** Which vulnerability catalog creates a list of publicly known vulnerabilities, each assigned an ID number, description, and reference?
**Type:** single
**Options:**
- CVE
- CVSS
- OWASP WSTG
- NIST SP 800-115
**Answer:** CVE
**Explanation:** Common Vulnerabilities and Exposures (CVE) is a list of publicly known vulnerabilities, each with an ID number, description, and reference. CVSS provides a severity score instead.

## Q3
**Question:** Match the CVSS metric group with the respective information.
**Type:** matching
**Pairs:**
- Base metric group -> Includes exploitability metrics and impact metrics
- Temporal metric group -> Includes exploit code maturity, remediation level, and report confidence
- Environmental metric group -> Includes modified base metrics, confidentiality, integrity, and availability requirements
**Explanation:** CVSS scores are built from three metric groups covering the core exploitability/impact, time-sensitive factors, and organization-specific environmental context.

## Q4
**Question:** Which three items are included in the base metric group used by CVSS? (Choose three.)
**Type:** multi
**Options:**
- Attack complexity
- Integrity impact
- Modified base metrics
- User interaction
- Availability requirements
- Remediation level
**Answer:** Attack complexity; Integrity impact; User interaction
**Explanation:** The Base metric group includes exploitability metrics (attack vector, attack complexity, privileges required, user interaction) and impact metrics (confidentiality, integrity, and availability impact).

## Q5
**Question:** Which item is included in the environmental metric group used by CVSS?
**Type:** single
**Options:**
- Privileges required
- Confidentiality requirements
- Report confidence
- Availability impact
**Answer:** Confidentiality requirements
**Explanation:** The Environmental metric group includes modified base metrics and confidentiality, integrity, and availability requirements.

## Q6
**Question:** Which item is included in the temporal metric group used by CVSS?
**Type:** single
**Options:**
- Exploit code maturity
- Integrity impact
- Modified base metrics
- Attack vector
**Answer:** Exploit code maturity
**Explanation:** The Temporal metric group includes exploit code maturity, remediation level, and report confidence.

## Q7
**Question:** Which tool can ingest the results from many penetration testing tools a cybersecurity analyst uses and help this professional produce reports in formats such as CSV, HTML, and PDF?
**Type:** single
**Options:**
- Dradis
- Mimikatz
- Nessus
- PowerSploit
**Answer:** Dradis
**Explanation:** Dradis ingests results from many penetration testing tools and helps produce consolidated reports in formats like CSV, HTML, and PDF.

## Q8
**Question:** Match the description to the respective control category.
**Type:** matching
**Pairs:**
- Key rotation -> Technical control
- Input sanitization -> Technical control
- Secure software development life cycle -> Administrative control
- Role-based access control -> Administrative control
- Time-of-day restrictions -> Operational control
- Job rotation -> Operational control
- Video surveillance -> Physical control
- Biometric controls -> Physical control
**Explanation:** Remediation recommendations in a pen test report are grouped into technical, administrative, operational, and physical control categories, each addressing risk in a different way.

## Q9
**Question:** Which two items are examples of technical controls that can be recommended as mitigations and remediation of the vulnerabilities found during a pen test? (Choose two.)
**Type:** multi
**Options:**
- Multifactor authentication
- Certificate management
- RBAC
- Mandatory vacations
- Access control vestibule
**Answer:** Multifactor authentication; Certificate management
**Explanation:** Technical controls use technology to reduce vulnerabilities: system hardening, input sanitization/query parameterization, MFA, process-level remediation, patch management, key rotation, certificate management, secrets management, and network segmentation.

## Q10
**Question:** A recent pen-test results in a cybersecurity analyst report, including information on process-level remediation, patch management, and secrets management solutions. Which control category is represented by this example?
**Type:** single
**Options:**
- Technical
- Administrative
- Operational
- Physical
**Answer:** Technical
**Explanation:** Process-level remediation, patch management, and secrets management are all technical controls, which use technology to reduce vulnerabilities.

## Q11
**Question:** Which document provides several cheat sheets and detailed guidance on preventing vulnerabilities such as cross-site scripting, SQL injection, and command injection?
**Type:** single
**Options:**
- OWASP
- CVE
- GDPR
- CVSS
**Answer:** OWASP
**Explanation:** OWASP provides cheat sheets and detailed guidance on input validation best practices to mitigate vulnerabilities such as XSS, CSRF, SQL injection, command injection, and XML external entities.

## Q12
**Question:** A cybersecurity analyst report should contain minimum password requirements and policies and procedures. These are examples that are included in which control category?
**Type:** single
**Options:**
- Technical
- Administrative
- Operational
- Physical
**Answer:** Administrative
**Explanation:** Administrative controls are policies, rules, or training designed to reduce risk, including RBAC, secure SDLC, minimum password requirements, and organizational policies and procedures.

## Q13
**Question:** Which control category includes information on mandatory vacations and user training in the cybersecurity analyst report?
**Type:** single
**Options:**
- Technical
- Administrative
- Operational
- Physical
**Answer:** Operational
**Explanation:** Operational controls focus on day-to-day operations and strategies, including job rotation, time-of-day restrictions, mandatory vacations, and user training.

## Q14
**Question:** When creating a cybersecurity analyst report, which control category includes information concerning the access control vestibule?
**Type:** single
**Options:**
- Technical
- Administrative
- Operational
- Physical
**Answer:** Physical
**Explanation:** Physical controls use security measures to prevent or deter unauthorized access to sensitive locations or materials, including access control vestibules, biometric controls, and video surveillance.

## Q15
**Question:** Match the term to the respective description.
**Type:** matching
**Pairs:**
- False positive -> A security device triggers an alarm, but there is no malicious activity or actual attack taking place
- True positive -> A successful identification of a security attack or a malicious event
- False negative -> Malicious activities that are not detected by a network security device
- True negative -> An intrusion detection device identifies an activity as acceptable behavior and the activity is acceptable
**Explanation:** These four detection outcomes describe whether an alert was raised or missed, and whether that outcome matched reality.

## Q16
**Question:** Which kind of event is also called a "benign trigger"?
**Type:** single
**Options:**
- False positive
- False negative
- True positive
- True negative
**Answer:** False positive
**Explanation:** False positives are "false alarms" or "benign triggers" — problematic because unjustified alerts diminish the value and urgency of real alerts.

## Q17
**Question:** What kind of events diminishes the value and urgency of real alerts?
**Type:** single
**Options:**
- False positives
- False negatives
- True negatives
- True positives
**Answer:** False positives
**Explanation:** False positives occur when a security device triggers an alarm with no actual malicious activity, and their frequency diminishes the perceived urgency of real alerts.

## Q18
**Question:** Which kinds of events are malicious activities not detected by a network security device?
**Type:** single
**Options:**
- False positives
- False negatives
- True negatives
- True positives
**Answer:** False negatives
**Explanation:** False negatives are malicious activities that go undetected by a network security device.

## Q19
**Question:** Which kind of event occurs when an intrusion detection device identifies an activity as acceptable behavior and the activity is acceptable?
**Type:** single
**Options:**
- False positives
- False negatives
- True negatives
- True positives
**Answer:** True negatives
**Explanation:** True negatives occur when an IDS correctly identifies acceptable activity as acceptable.

## Q20
**Question:** Which kind of event is a successful identification of a security attack?
**Type:** single
**Options:**
- False negative
- False positive
- True positive
- True negative
**Answer:** True positive
**Explanation:** A true positive is the successful identification of a genuine security attack or malicious event.

## Q21
**Question:** Which example of technical control is recommended to mitigate and prevent vulnerabilities such as cross-site scripting, cross-site request forgery, SQL injection, and command injection?
**Type:** single
**Options:**
- User input sanitization
- Process-level remediation
- Secrets management solution
- Certificate management
**Answer:** User input sanitization
**Explanation:** Input validation (user input sanitization) best practices mitigate vulnerabilities such as XSS, CSRF, SQL injection, command injection, and XML external entities.

## Q22
**Question:** Which example of administrative controls enables administrators to control what users can do at both broad and granular levels?
**Type:** single
**Options:**
- RBAC
- Secure software development life cycle
- Policies and procedures
- Minimum password requirements
**Answer:** RBAC
**Explanation:** Role-based access control (RBAC) bases access permissions on roles assigned to users, letting administrators control what users can do at both broad and granular levels.

## Q23
**Question:** A document entitled "Building an Information Technology Security Awareness and Training Program" succinctly defines why security education and training are so important for users. The document defines ways to improve the security operations of an organization. Which document is being described?
**Type:** single
**Options:**
- NIST SP 800-50
- NIST SP 800-115
- OWASP WSTG
- CVSS
**Answer:** NIST SP 800-50
**Explanation:** NIST Special Publication 800-50, "Building an Information Technology Security Awareness and Training Program," explains why security education and training matter and how they improve an organization's security operations.

## Q24
**Question:** How is the score that CVSS provides interpreted?
**Type:** single
**Options:**
- Scores are rated from 0 to 100, with 100 being the most severe
- Scores are rated from 0 to 100, with 0 being the most severe
- Scores are rated from 0 to 10, with 10 being the most severe
- Scores are rated from 0 to 10, with 0 being the most severe
**Answer:** Scores are rated from 0 to 10, with 10 being the most severe
**Explanation:** CVSS, developed and maintained by FIRST.org, rates vulnerability severity on a 0-to-10 scale, with 10 representing the most severe.

## Q25
**Question:** What control category does system hardening belong to?
**Type:** single
**Options:**
- Technical
- Administrative
- Operational
- Physical
**Answer:** Technical
**Explanation:** System hardening is a technical control — applying security best practices, patches, and configuration changes to remediate or mitigate vulnerabilities in systems and applications.