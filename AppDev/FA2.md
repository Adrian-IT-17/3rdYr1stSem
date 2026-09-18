# Formative Assessment 2

> Review note: I checked all 20 answers against PHP's official documentation and corrected two that were wrong (Q7 and Q18 — see explanations below for the reasoning). Q1 and Q2 have some internal ambiguity in how the code/question is worded; I kept the original answers there since they're the most defensible reading, but flagged them in case your actual instructor key treats them differently.

## Q1
**Question:** `$u=30; do{ echo $y++; }while($u<31);` What is the output if `$y=33`?
**Type:** single
**Options:**
- 33
- 32
- 30
- 31
**Answer:** 33
**Explanation:** A do...while loop always executes its body at least once before checking the condition. `echo $y++;` prints the current value of $y (33) first, then increments it. (Note: since $u never changes inside the loop and $u=30 is always less than 31, this loop technically never terminates — likely a flaw in how this question was written. If your instructor's key differs here, it may be due to a different intended loop condition.)

## Q2
**Question:** `$m=3; switch($m){ case 1: echo "May"; break; case 2: echo "June"; break; case 3: echo "July"; break; default: echo "invalid"; }` What is the output if `$n` is 1?
**Type:** single
**Options:**
- June
- July
- May
- Invalid
**Answer:** July
**Explanation:** The switch statement evaluates $m, not $n — and $n isn't used anywhere in this code. Since $m is explicitly set to 3, case 3 executes and prints "July" regardless of $n's value. (If your instructor intended $n to be a typo for $m, meant to override the coded value, the intended answer could instead be "May" — worth double-checking the original wording if you're unsure.)

## Q3
**Question:** Statement is used to jump to other section of the program to support labels.
**Type:** single
**Options:**
- If
- Continue
- Goto
- Break
**Answer:** Goto
**Explanation:** goto transfers program execution to a labeled section of the code.

## Q4
**Question:** Associativity for Bitwise AND, Bitwise XOR, Bitwise OR
**Type:** single
**Options:**
- Right
- Left
- Middle
- NA
**Answer:** Left
**Explanation:** The bitwise operators &, ^, and | are all left-associative per PHP's official operator precedence table.

## Q5
**Question:** Associativity for Division, Multiplication, Modulus
**Type:** single
**Options:**
- Middle
- NA
- Left
- Right
**Answer:** Left
**Explanation:** The arithmetic operators *, /, and % are evaluated left to right.

## Q6
**Question:** Symbol for addition
**Type:** single
**Options:**
- =+
- +
- –
- ++
**Answer:** +
**Explanation:** The addition operator in PHP is +.

## Q7
**Question:** `$m=3; switch($m){ case 1: echo "May"; break; case 2: echo "June"; break; case 3: echo "July"; break; default: echo "invalid"; }` What is the output if `$m` is 1?
**Type:** single
**Options:**
- May
- June
- July
- Invalid
**Answer:** July
**Explanation:** **Corrected from the original answer (May).** The code explicitly assigns `$m = 3;` immediately before the switch statement. PHP executes the code as written — the question's phrasing doesn't retroactively change an assignment already present in the snippet. Since $m is 3, case 3 fires, printing "July." (If the instructor's intent was actually for you to substitute $m=1 into the code, overriding the shown assignment, the answer would be "May" instead — this ties into the same ambiguity as Q2.)

## Q8
**Question:** Associativity for Boolean AND, Boolean OR
**Type:** single
**Options:**
- Right
- NA
- Left
- Middle
**Answer:** Left
**Explanation:** Boolean operators (&&, ||) are both left-associative.

## Q9
**Question:** Syntax for Switch
**Type:** single
**Options:**
- switch($category)
- swt($cat)
- $switch($category)
- $Cat($switch)
**Answer:** switch($category)
**Explanation:** The correct PHP syntax begins with switch(expression).

## Q10
**Question:** Symbol that specifies a particular action in an expression.
**Type:** single
**Options:**
- Operator
- Precedence
- Associativity
- Purpose
**Answer:** Operator
**Explanation:** An operator is a symbol that performs a specific operation on one or more operands.

## Q11
**Question:** Operator for Ternary operator
**Type:** single
**Options:**
- <>
- //
- ?:
- ,,
**Answer:** ?:
**Explanation:** The ternary operator uses the symbols ? and : as a shorthand for if...else.

## Q12
**Question:** Syntax for for statement
**Type:** single
**Options:**
- for{expr1,expr2}(statement)
- for(expr1;expr2;expr3){statement}
- for(expr1){statement}expr2
- for(statement){expr}
**Answer:** for(expr1;expr2;expr3){statement}
**Explanation:** expr1 initializes the loop, expr2 is the condition, and expr3 updates the loop variable.

## Q13
**Question:** `$a=10; $b=20; if($a<$b){echo $a+$b;} else{echo $a-$b;}` What is the output?
**Type:** single
**Options:**
- -10
- 20
- 30
- 40
**Answer:** 30
**Explanation:** Since 10 < 20 is true, the if block executes and prints 10 + 20 = 30.

## Q14
**Question:** Associativity for object instantiation
**Type:** single
**Options:**
- Left
- Right
- Middle
- NA
**Answer:** NA
**Explanation:** Confirmed against PHP's official operator precedence documentation: the `clone`/`new` row is explicitly listed as "(n/a)" — not left, right, or middle. Associativity only meaningfully applies to binary/ternary operators; clone and new don't have that property.

## Q15
**Question:** Operator for assignment operators
**Type:** single
**Options:**
- +
- –
- >
- =
**Answer:** =
**Explanation:** The assignment operator = assigns a value to a variable.

## Q16
**Question:** Operator for Bitwise AND, Bitwise XOR, Bitwise OR
**Type:** single
**Options:**
- ,,
- &&||
- ?:
- & ^ |
**Answer:** & ^ |
**Explanation:** & = Bitwise AND, ^ = Bitwise XOR, | = Bitwise OR.

## Q17
**Question:** Symbol for subtraction
**Type:** single
**Options:**
- -=
- +
- -
- --
**Answer:** -
**Explanation:** The subtraction operator in PHP is -.

## Q18
**Question:** Characteristic of operators that determines the order in which they evaluate the operands surrounding them.
**Type:** single
**Options:**
- Operator Purpose
- Operator Character
- Operator Associativity
- Operator Precedence
**Answer:** Operator Associativity
**Explanation:** **Corrected from the original answer (Operator Precedence).** Precedence determines which *different* operators are evaluated first (e.g., * before +). Associativity specifically determines the *direction* (left-to-right or right-to-left) in which operators of equal precedence group their surrounding operands — which is exactly what this question describes.

## Q19
**Question:** Statement causes execution of the current loop iteration to end and commence at the beginning of the next iteration.
**Type:** single
**Options:**
- If
- Continue
- Goto
- Break
**Answer:** Continue
**Explanation:** continue skips the remainder of the current iteration and proceeds with the next iteration of the loop.

## Q20
**Question:** `$x=0; for($i=1;$i<5;$i++){$x+=$i;} echo $x;` What is the output?
**Type:** single
**Options:**
- 15
- 9
- 10
- 12
**Answer:** 10
**Explanation:** The loop adds 1 + 2 + 3 + 4 (stopping when i reaches 5), resulting in 10.