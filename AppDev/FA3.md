# Formative Assessment 3

## Q1
**Question:** Is used to aggregate a series of similar items together, arranging and dereferencing them in some specific way.
**Type:** single
**Options:**
- Variable
- Index
- Function
- Array
**Answer:** Array
**Explanation:** An array stores multiple related values under one variable and allows access through indexes or keys.

## Q2
**Question:** asort(), ksort(), arsort(), and krsort() maintain their reference for each value.
**Type:** single
**Options:**
- True
- False
**Answer:** True
**Explanation:** These sorting functions preserve the association between array keys and their corresponding values.

## Q3
**Question:** A function that is declared inside a function is said to be hidden.
**Type:** single
**Options:**
- False
- True
**Answer:** False
**Explanation:** A function declared inside another function is called a nested function, not a hidden function.

## Q4
**Question:** `$fruit = array("orange","apple","grape","banana");` What is the value of index 0?
**Type:** single
**Options:**
- apple
- banana
- orange
- grape
**Answer:** orange
**Explanation:** PHP arrays are zero-indexed by default, so index 0 contains "orange".

## Q5
**Question:** `$mo = array("jan","feb","mar"); echo "<pre>"; var_dump($mo); echo "</pre>";` Check the code if valid or invalid.
**Type:** single
**Options:**
- Valid
- Invalid
**Answer:** Valid
**Explanation:** var_dump() is a valid PHP function for displaying an array's structure and data types.

## Q6
**Question:** Specify an array expression within a set of parentheses following the foreach keyword.
**Type:** single
**Options:**
- False
- True
**Answer:** True
**Explanation:** The foreach syntax requires an array expression inside parentheses.

## Q7
**Question:** Is a statement used to iterate or loop through the elements in an array.
**Type:** single
**Options:**
- seteach()
- everyone()
- everyeach()
- foreach()
**Answer:** foreach()
**Explanation:** foreach() is the PHP statement designed for traversing arrays.

## Q8
**Question:** `$g = 200; function a(){echo "5";} function b(){echo "4";} ab();` What is the output?
**Type:** single
**Options:**
- error
- 54
- 200
- 45
**Answer:** error
**Explanation:** ab() is not defined, resulting in a fatal error.

## Q9
**Question:** `function count($val){ $c=0; $c+=$val; echo $c; } count(10); count(5);` What is the output?
**Type:** single
**Options:**
- Error
- 105
- 5
- 15
**Answer:** Error
**Explanation:** count() is already a built-in PHP function and cannot be redeclared.

## Q10
**Question:** You can insert CSS code inside of a function.
**Type:** single
**Options:**
- True
- False
**Answer:** True
**Explanation:** A PHP function can output CSS or HTML using echo or by closing PHP tags.

## Q11
**Question:** Functions can only have 1 parameter.
**Type:** single
**Options:**
- False
- True
**Answer:** False
**Explanation:** PHP functions can have zero, one, or multiple parameters.

## Q12
**Question:** Array index in PHP can also be called array storage.
**Type:** single
**Options:**
- True
- False
**Answer:** False
**Explanation:** An array index is the key or position used to access an element; it is not called array storage.

## Q13
**Question:** You can pass values to a function and ask functions to return a value.
**Type:** single
**Options:**
- True
- False
**Answer:** True
**Explanation:** Functions can receive arguments and return values using the return statement.

## Q14
**Question:** `function a($a,$b){ return $a+$b; } echo a(5,4);` What is the output?
**Type:** single
**Options:**
- 4
- Error
- 9
- 5
**Answer:** 9
**Explanation:** The function returns 5 + 4 = 9.

## Q15
**Question:** You can create a function inside of a function.
**Type:** single
**Options:**
- False
- True
**Answer:** True
**Explanation:** PHP supports nested function declarations.

## Q16
**Question:** Function is used to print the array structure.
**Type:** single
**Options:**
- print_s
- print_r
- print_f
- print_a
**Answer:** print_r
**Explanation:** print_r() displays arrays and objects in a readable format.

## Q17
**Question:** `foreach($arr as ______)`
**Type:** single
**Options:**
- value$
- val
- $value
- val$
**Answer:** $value
**Explanation:** $value receives each array element during every iteration.

## Q18
**Question:** `function a($a,$b){ return $a+$b; } echo a(6,5);` What is the value of $a?
**Type:** single
**Options:**
- Error
- 5
- 6
- 11
**Answer:** 6
**Explanation:** $a receives the first argument passed to the function, which is 6.

## Q19
**Question:** `$mo = array("jan","feb","mar"); echo "<pre>"; print_r($mo); echo "</pre>";` Check the code if valid or invalid.
**Type:** single
**Options:**
- Invalid
- Valid
**Answer:** Valid
**Explanation:** print_r() correctly prints the array structure, and the code is valid PHP.

## Q20
**Question:** `function count($val){ static $c=0; $c+=$val; echo $c; } count(4); count(3);` What is the output?
**Type:** single
**Options:**
- 7
- 43
- error
- 47
**Answer:** error
**Explanation:** The function is named count(), which conflicts with PHP's built-in count() function, causing a fatal error. (If renamed, the output would have been 47 because static $c retains its value.)