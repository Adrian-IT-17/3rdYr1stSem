# Formative Assessment 5

## Q1
**Question:** Regular Expression is also known as
**Type:** single
**Options:**
- rex
- regp
- regex
- regx
**Answer:** regex
**Explanation:** Regex is the common abbreviation for Regular Expression, used for pattern matching and text processing.

## Q2
**Question:** An associative array of variables passed to the current script via the environment method
**Type:** single
**Options:**
- $_REQUEST
- $_COOKIE
- $_SESSION
- $_ENV
**Answer:** $_ENV
**Explanation:** $_ENV contains variables passed to the current script through the environment.

## Q3
**Question:** An associative array containing session variables available to the script
**Type:** single
**Options:**
- $_COOKIE
- $_SESSION
- $_ENV
- $_REQUEST
**Answer:** $_SESSION
**Explanation:** $_SESSION stores session variables that persist across multiple pages.

## Q4
**Question:** Which of the following will set a cookie that expires after 1 minute?
**Type:** single
**Options:**
- setcookie("name1","value1",time()+60);
- settingcookie("name1","value1",time()+60);
- cookiesetting("name1","value1",time()+60);
- cookieset("name1","value1",time()+60);
**Answer:** setcookie("name1","value1",time()+60);
**Explanation:** time()+60 sets the cookie to expire 60 seconds (1 minute) later.

## Q5
**Question:** Cookies are mechanism for storing data in the remote browser and thus tracking or identifying return users.
**Type:** single
**Options:**
- False
- True
**Answer:** True
**Explanation:** Cookies are stored in the user's browser and help identify returning users.

## Q6
**Question:** $_SESSION is an associative array of variables passed to the current script via the environment method.
**Type:** single
**Options:**
- False
- True
**Answer:** False
**Explanation:** $_SESSION stores session variables. Environment variables are stored in $_ENV.

## Q7
**Question:** Syntax for setting a cookie
**Type:** single
**Options:**
- cookieset()
- settingcookie()
- cookiesetting()
- setcookie()
**Answer:** setcookie()
**Explanation:** setcookie() is the PHP function used to create cookies.

## Q8
**Question:** Cookies are small amount of information containing
**Type:** single
**Options:**
- value=string
- string=value
- value=variable
- variable=value
**Answer:** variable=value
**Explanation:** A cookie stores data as a name/value pair — in PHP, the cookie's name acts as the variable and is paired with its corresponding value (e.g., setcookie("name1","value1")).

## Q9
**Question:** Regular Expression Meta characters: Symbol for not in range (every character except a, b, or c)
**Type:** single
**Options:**
- '^abc'
- (^abc)
- {^abc}
- [^abc]
**Answer:** [^abc]
**Explanation:** [^abc] matches any character except a, b, or c.

## Q10
**Question:** $_SERVER is an entries created by the
**Type:** single
**Options:**
- Application server
- Computer server
- Web server
- Matrix server
**Answer:** Web server
**Explanation:** $_SERVER contains information provided by the web server.

## Q11
**Question:** Regular Expression Meta characters: Symbol for group elements
**Type:** single
**Options:**
- ""
- []
- {}
- ()
**Answer:** ()
**Explanation:** Parentheses () group expressions and create capturing groups.

## Q12
**Question:** `<form action="<?php echo $_SERVER['PHP_SELF'] ?>" method="get"></form>` Check if the code is valid or invalid.
**Type:** single
**Options:**
- Valid
- Invalid
**Answer:** Valid
**Explanation:** The form correctly submits to the current page using the GET method.

## Q13
**Question:** `<form action="<?php echo $_SERVER['PHP_SELF'] ?>" method="post"></form>` Check if the code is valid or invalid.
**Type:** single
**Options:**
- Valid
- Invalid
**Answer:** Valid
**Explanation:** The form correctly submits to the current page using the POST method.

## Q14
**Question:** Regular Expression Meta characters: Symbol for any white-space character
**Type:** single
**Options:**
- \S
- \w
- \s
- \W
**Answer:** \s
**Explanation:** \s matches any whitespace character (space, tab, newline, etc.).

## Q15
**Question:** Sample session variable: `$_SESSION[myvalue];` Check if the code is valid or invalid.
**Type:** single
**Options:**
- Invalid
- Valid
**Answer:** Invalid
**Explanation:** The session key should be quoted: $_SESSION["myvalue"] or $_SESSION['myvalue'].

## Q16
**Question:** What does P in PCRE stand for?
**Type:** single
**Options:**
- Program
- Present
- Percl
- Popular
**Answer:** Percl
**Explanation:** PCRE stands for Perl Compatible Regular Expressions. The quiz's "Percl" is a typo for Perl.

## Q17
**Question:** Regular Expression Meta characters: Symbol for matches any single character
**Type:** single
**Options:**
- '
- .
- :
- "
**Answer:** .
**Explanation:** The dot (.) matches any single character except a newline by default.

## Q18
**Question:** $_REQUEST is an associative array that by default contains the contents except
**Type:** single
**Options:**
- $_POST
- $_COOKIE
- $_SESSION
- $_GET
**Answer:** $_SESSION
**Explanation:** $_REQUEST contains $_GET, $_POST, and $_COOKIE, but not $_SESSION.

## Q19
**Question:** Regular expression example that will match the word hello
**Type:** single
**Options:**
- [hello]
- +hello+
- {hello}
- '/hello/'
**Answer:** '/hello/'
**Explanation:** In PCRE, regex patterns are commonly enclosed in forward slashes.

## Q20
**Question:** Use to unset session variables
**Type:** single
**Options:**
- unsession()
- usession()
- uset()
- unset()
**Answer:** unset()
**Explanation:** unset() removes a variable, including a session variable such as unset($_SESSION['user']);.