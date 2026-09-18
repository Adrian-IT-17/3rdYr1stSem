# Formative Assessment 4

## Q1
**Question:** Most of the developers use include functions for their header and footer.
**Type:** single
**Options:**
- False
- True
**Answer:** True
**Explanation:** PHP developers commonly use include or require for reusable files like headers and footers to avoid code duplication.

## Q2
**Question:** Syntax for require_once
**Type:** single
**Options:**
- require_once(filename.php);
- require_once(filename.inc);
- filename("require_once");
- require_once("filename.inc");
**Answer:** require_once("filename.inc");
**Explanation:** require_once() includes a file only once and uses the syntax require_once("filename");.

## Q3
**Question:** Syntax to get a part of a given string
**Type:** single
**Options:**
- string partstr(string $string, int $start [, int $length])
- string strpart(string $string, int $start [, int $length])
- string substr(string $string, int $start [, int $length])
- string strsub(string $string, int $start [, int $length])
**Answer:** string substr(string $string, int $start [, int $length])
**Explanation:** substr() returns a portion of a string.

## Q4
**Question:** `$x = ceil(10.01); echo $x;` What is the output?
**Type:** single
**Options:**
- 11
- Blank
- 10
- Error
**Answer:** 11
**Explanation:** ceil() rounds a number upward to the nearest integer.

## Q5
**Question:** Syntax used to format a local time and date
**Type:** single
**Options:**
- string time(string $format [, int $timestamp = time()])
- string time_date(string $format [, int $timestamp = time()])
- string date_time(string $format [, int $timestamp = time()])
- string date(string $format [, int $timestamp = time()])
**Answer:** string date(string $format [, int $timestamp = time()])
**Explanation:** date() formats a local date and time.

## Q6
**Question:** Returns the next highest integer by rounding the value upwards
**Type:** single
**Options:**
- high()
- up()
- top()
- ceil()
**Answer:** ceil()
**Explanation:** ceil() always rounds a number upward.

## Q7
**Question:** `$x = ceil(5.2); echo $x;` What is the output?
**Type:** single
**Options:**
- 5
- Blank
- Error
- 6
**Answer:** 6
**Explanation:** ceil(5.2) returns 6.

## Q8
**Question:** You can separate your PHP file and embed it into your HTML using PHP include functions.
**Type:** single
**Options:**
- True
- False
**Answer:** True
**Explanation:** include, include_once, require, and require_once allow reusable code across files.

## Q9
**Question:** Make a string's first character uppercase
**Type:** single
**Options:**
- firstcu()
- fsupper()
- upperfs()
- ucfirst()
**Answer:** ucfirst()
**Explanation:** ucfirst() capitalizes the first character of a string.

## Q10
**Question:** Used to generate random integers
**Type:** single
**Options:**
- random()
- ran()
- rndm()
- rand()
**Answer:** rand()
**Explanation:** rand() generates a random integer.

## Q11
**Question:** Format character for numeric representation of a month, without leading zeros
**Type:** single
**Options:**
- n
- z
- r
- m
**Answer:** n
**Explanation:** n displays the month as 1–12 without leading zeros.

## Q12
**Question:** Used to declare constants
**Type:** single
**Options:**
- derive
- function
- define
- set
**Answer:** define
**Explanation:** define() declares constants in PHP.

## Q13
**Question:** Syntax for require
**Type:** single
**Options:**
- require(filename.php);
- require(filename.inc);
- filename("require");
- require("filename.inc");
**Answer:** require("filename.inc");
**Explanation:** require() includes a file and stops execution if the file is missing.

## Q14
**Question:** Syntax for random
**Type:** single
**Options:**
- int random(void)
- int ran(void)
- int rand(void)
- int rndm(void)
**Answer:** int rand(void)
**Explanation:** rand() returns a random integer.

## Q15
**Question:** Syntax to transform a string to uppercase
**Type:** single
**Options:**
- string strupper(string $str)
- string stringtoupper(string $str)
- string upperstr(string $str)
- string strtoupper(string $str)
**Answer:** string strtoupper(string $str)
**Explanation:** strtoupper() converts all letters in a string to uppercase.

## Q16
**Question:** Format character for English ordinal suffix for the day of the month, 2 characters
**Type:** single
**Options:**
- S
- C
- D
- E
**Answer:** S
**Explanation:** S returns ordinal suffixes such as st, nd, rd, and th.

## Q17
**Question:** `$x = rand(5,10); echo $x;` What is the minimum value of the output?
**Type:** single
**Options:**
- Error
- 10
- 5
- 0
**Answer:** 5
**Explanation:** rand(5,10) generates integers from 5 to 10, inclusive.

## Q18
**Question:** Syntax for length of a string
**Type:** single
**Options:**
- int strlen(string $string)
- int stringlen(string $string)
- int lengthstring(string $string)
- int lenstr(string $string)
**Answer:** int strlen(string $string)
**Explanation:** strlen() returns the number of characters in a string.

## Q19
**Question:** Performs the same way as the include function. Generates a fatal error if the file is not found, stopping the script.
**Type:** single
**Options:**
- include
- include_once
- require
- require_once
**Answer:** require
**Explanation:** require behaves like include, but execution stops with a fatal error if the file cannot be found.

## Q20
**Question:** `$x = min(7, 4.7, 4.25, 5); echo $x;` What is the output?
**Type:** single
**Options:**
- 7
- 5
- 4.7
- 4.25
**Answer:** 4.25
**Explanation:** min() returns the smallest value among its arguments.