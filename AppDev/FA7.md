# Formative Assessment 7

## Q1
**Question:** Used to close a file
**Type:** single
**Options:**
- fileclose()
- fclose()
- closef()
- closefile()
**Answer:** fclose()
**Explanation:** fclose() closes an open file after it has been opened with fopen().

## Q2
**Question:** Complete the syntax: `move_uploaded_file(____, new location);`
**Type:** single
**Options:**
- Size
- location
- File
- Type
**Answer:** File
**Explanation:** The first parameter is the uploaded file (temporary filename).

## Q3
**Question:** The name or offset of the field being retrieved.
**Type:** single
**Options:**
- $result_query
- Table
- Field
- Row
**Answer:** Field
**Explanation:** A field is a column in a database table.

## Q4
**Question:** Using the global PHP $_FILES array you can upload files from a client computer to the remote server.
**Type:** single
**Options:**
- True
- False
**Answer:** True
**Explanation:** $_FILES stores information about uploaded files.

## Q5
**Question:** To save permanently the uploaded file, use the move_uploaded_file() function. This function returns TRUE on success or FALSE on failure.
**Type:** single
**Options:**
- False
- True
**Answer:** True
**Explanation:** move_uploaded_file() moves an uploaded file to a permanent location and returns a Boolean value.

## Q6
**Question:** Checking if it is a file
**Type:** single
**Options:**
- check_file()
- file_valid()
- file_check()
- is_file()
**Answer:** is_file()
**Explanation:** is_file() checks whether the given path is a regular file.

## Q7
**Question:** Syntax for removing an existing file
**Type:** single
**Options:**
- drop("myfile.txt")
- delete("myfile.txt")
- remove("myfile.txt")
- unlink("myfile.txt")
**Answer:** unlink("myfile.txt")
**Explanation:** unlink() deletes a file from the filesystem.

## Q8
**Question:** `$query = mysql_query("SELECT MIN(tuition) FROM tblinfo"); $fetch = mysql_fetch_array($query); echo $fetch[0];` Check the code if valid or invalid.
**Type:** single
**Options:**
- Valid
- Invalid
**Answer:** Valid
**Explanation:** The result can be accessed using the numeric index 0.

## Q9
**Question:** `$query = mysql_query("SELECT MAX(tuition) FROM tblinfo"); $fetch = mysql_fetch_array($query); echo $fetch["MAX(tuition)"];` Check the code if valid or invalid.
**Type:** single
**Options:**
- Invalid
- Valid
**Answer:** Valid
**Explanation:** mysql_fetch_array() allows associative access using the column name.

## Q10
**Question:** Function to save permanently the uploaded file
**Type:** single
**Options:**
- move_uploaded_file()
- upload_file()
- save_uploaded_file()
- save_file()
**Answer:** move_uploaded_file()
**Explanation:** move_uploaded_file() moves an uploaded file to a permanent destination.

## Q11
**Question:** The row number from the result that's being retrieved. Row numbers start at 0.
**Type:** single
**Options:**
- $result_query
- Table
- Row
- Field
**Answer:** Row
**Explanation:** Rows in result sets are zero-indexed.

## Q12
**Question:** Syntax that attempts to create an empty file
**Type:** single
**Options:**
- touch("$file")
- attempt("$file")
- empty("$file")
- create("$file")
**Answer:** touch("$file")
**Explanation:** touch() creates an empty file if it does not already exist.

## Q13
**Question:** `$query = mysql_query("SELECT MAX(tuition) FROM tblinfo"); $fetch = mysql_fetch_array($query); echo $fetch[0];` Check the code if valid or invalid.
**Type:** single
**Options:**
- Invalid
- Valid
**Answer:** Valid
**Explanation:** The aggregate result can be accessed using index 0.

## Q14
**Question:** `$query = mysql_query("SELECT MAX(tuition) FROM tblinfo"); $fetch = mysql_result($query,0); echo $fetch;` Check the code if valid or invalid.
**Type:** single
**Options:**
- Valid
- Invalid
**Answer:** Valid
**Explanation:** mysql_result() retrieves the value from the specified row and field.

## Q15
**Question:** Checking for file existence
**Type:** single
**Options:**
- check_file()
- file_check()
- exists_file()
- file_exists()
**Answer:** file_exists()
**Explanation:** file_exists() checks whether a file or directory exists.

## Q16
**Question:** Syntax to tell the last line (end) of a file
**Type:** single
**Options:**
- feof("$file")
- lastfile("$file")
- endoffile("$file")
- lastline("$file")
**Answer:** feof("$file")
**Explanation:** feof() checks whether the end of a file has been reached.

## Q17
**Question:** Complete the syntax: `move_uploaded_file(file, ________);`
**Type:** single
**Options:**
- new location
- name
- type
- size
**Answer:** new location
**Explanation:** The second parameter specifies where the uploaded file will be saved.

## Q18
**Question:** Use to tell the last line (end) of a file
**Type:** single
**Options:**
- feof()
- endoffile()
- lastfile()
- lastline()
**Answer:** feof()
**Explanation:** feof() detects the end-of-file condition.

## Q19
**Question:** Complete the syntax: `mysql_result(_____, row, field)`
**Type:** single
**Options:**
- $result
- $query_result
- $query
- $result_query
**Answer:** $result
**Explanation:** mysql_result() expects the result resource returned by mysql_query().

## Q20
**Question:** SQL command that will get the sum of a specified field
**Type:** single
**Options:**
- PLUS
- SUM
- SUMMATION
- ADD
**Answer:** SUM
**Explanation:** SUM() is the SQL aggregate function used to calculate the total of a numeric column.