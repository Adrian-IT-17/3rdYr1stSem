# IT0049 Formative Assessment 2

<!-- Converted from 39 Canvas attempt-export blocks. Removed 11 repeated question(s) from the second attempt. -->

## Q1
**Question:** The public folder should contain the application's business logic, including Models.
**Type:** single

**Options:**
- True
- False
**Answer:** False
**Explanation:** The statement is False. Read the wording carefully and connect it to the CodeIgniter 4 behavior being tested.

## Q2
**Question:** Which Query Builder method retrieves every record from a Model's table?
**Type:** single

**Options:**
- selectAll()
- getAll()
- find()
- findAll()
**Answer:** findAll()
**Explanation:** The correct answer is findAll(). Use that as the key CodeIgniter 4 fact for this question.

## Q3
**Question:** A new priority column is added directly in the database, but $allowedFields is never updated to include it. What happens when a controller tries to save a priority value through this Model?
**Type:** single

**Options:**
- CodeIgniter automatically detects and adds new columns
- It saves normally since the column physically exists
- The Model throws a fatal, uncatchable error
- It is silently dropped because $allowedFields still does not list it
**Answer:** It is silently dropped because $allowedFields still does not list it
**Explanation:** The correct answer is It is silently dropped because $allowedFields still does not list it. Use that as the key CodeIgniter 4 fact for this question.

## Q4
**Question:** What does a Model's $allowedFields property control?
**Type:** single

**Options:**
- The order fields appear in a view
- Which fields are required to connect to the database
- Which columns can be viewed in a browser
- Which fields may be mass-assigned during insert() or update()
**Answer:** Which fields may be mass-assigned during insert() or update()
**Explanation:** The correct answer is Which fields may be mass-assigned during insert() or update(). Use that as the key CodeIgniter 4 fact for this question.

## Q5
**Question:** Comparing SELECT * FROM tasks WHERE status = '$status' (built by directly inserting a variable into a SQL string) against $builder->where('status', $status)->get();, which is safer and why?
**Type:** single

**Options:**
- The raw SQL version, because it is more explicit about what it does
- Both are equally safe since PHP always validates strings
- Neither is safe unless wrapped in a Model
- The Query Builder version, because it automatically escapes the value and reduces SQL injection risk
**Answer:** The Query Builder version, because it automatically escapes the value and reduces SQL injection risk
**Explanation:** The correct answer is The Query Builder version, because it automatically escapes the value and reduces SQL injection risk. Use that as the key CodeIgniter 4 fact for this question.

## Q6
**Question:** The .env file is used to store view templates.
**Type:** single

**Options:**
- True
- False
**Answer:** False
**Explanation:** The statement is False. Read the wording carefully and connect it to the CodeIgniter 4 behavior being tested.

## Q7
**Question:** Chaining where() and orderBy() lets you filter and sort a query in a single statement.
**Type:** single

**Options:**
- True
- False
**Answer:** True
**Explanation:** The statement is True. Read the wording carefully and connect it to the CodeIgniter 4 behavior being tested.

## Q8
**Question:** A view shows "Undefined variable $tasks" even though the Model successfully retrieves records in the controller. What is the most likely cause?
**Type:** single

**Options:**
- The database connection failed
- The Model's $table property is misspelled
- The controller did not include tasks in the data array passed to view()
- Query Builder does not support foreach loops
**Answer:** The controller did not include tasks in the data array passed to view()
**Explanation:** The correct answer is The controller did not include tasks in the data array passed to view(). Use that as the key CodeIgniter 4 fact for this question.

## Q9
**Question:** Which description matches "$allowedFields"?
**Type:** single

**Options:**
- Tells a Model which database table it represents
- Retrieves every record from a Model's table
- Restricts which fields may be mass-assigned during insert or update
- Filters query results based on a condition
**Answer:** Restricts which fields may be mass-assigned during insert or update
**Explanation:** $allowedFields matches this description: Restricts which fields may be mass-assigned during insert or update.

## Q10
**Question:** Which description matches "findAll()"?
**Type:** single

**Options:**
- Tells a Model which database table it represents
- Filters query results based on a condition
- Retrieves every record from a Model's table
- Restricts which fields may be mass-assigned during insert or update
**Answer:** Retrieves every record from a Model's table
**Explanation:** findAll() matches this description: Retrieves every record from a Model's table.

## Q11
**Question:** Why is CodeIgniter's Query Builder generally considered safer than concatenating raw SQL strings with user input?
**Type:** single

**Options:**
- Query Builder does not require a database connection
- Raw SQL cannot retrieve more than one row
- Query Builder is faster to type
- Query Builder automatically escapes values, reducing the risk of SQL injection
**Answer:** Query Builder automatically escapes values, reducing the risk of SQL injection
**Explanation:** The correct answer is Query Builder automatically escapes values, reducing the risk of SQL injection. Use that as the key CodeIgniter 4 fact for this question.

## Q12
**Question:** CodeIgniter automatically creates database tables the first time a Model is used.
**Type:** single

**Options:**
- True
- False
**Answer:** False
**Explanation:** The statement is False. Read the wording carefully and connect it to the CodeIgniter 4 behavior being tested.

## Q13
**Question:** What term describes an unauthorized attempt to manipulate a database through injected SQL, which Query Builder helps prevent?
**Type:** command
**Answer:** SQL injection
**Explanation:** Type SQL injection exactly; this is the CodeIgniter 4 term, path, or function the question is asking for.

## Q14
**Question:** A table has columns id, title, status, created_at. Which line correctly inserts a new row with only a title?
**Type:** single

**Options:**
- $model->create('title', 'Buy groceries');
- $model->new(['title' => 'Buy groceries']);
- $model->add(['Buy groceries']);
- $model->insert(['title' => 'Buy groceries']);
**Answer:** $model->insert(['title' => 'Buy groceries']);
**Explanation:** The correct answer is $model->insert(['title' => 'Buy groceries']);. Use that as the key CodeIgniter 4 fact for this question.

## Q15
**Question:** In the typical CodeIgniter data flow, which component calls the Model to retrieve data before passing it to a View?
**Type:** single

**Options:**
- The route
- The .env file
- The Controller
- The View itself
**Answer:** The Controller
**Explanation:** The correct answer is The Controller. Use that as the key CodeIgniter 4 fact for this question.

## Q16
**Question:** Which property in a Model tells CodeIgniter which database table the Model represents?
**Type:** single

**Options:**
- $dataset
- $table
- $from
- $source
**Answer:** $table
**Explanation:** The correct answer is $table. Use that as the key CodeIgniter 4 fact for this question.

## Q17
**Question:** Which Query Builder method retrieves a single record by its primary key?
**Type:** single

**Options:**
- find($id)
- getById($id)
- first($id)
- findOne($id)
**Answer:** find($id)
**Explanation:** The correct answer is find($id). Use that as the key CodeIgniter 4 fact for this question.

## Q18
**Question:** Which description matches "where()"?
**Type:** single

**Options:**
- Retrieves every record from a Model's table
- Tells a Model which database table it represents
- Filters query results based on a condition
- Restricts which fields may be mass-assigned during insert or update
**Answer:** Filters query results based on a condition
**Explanation:** where() matches this description: Filters query results based on a condition.

## Q19
**Question:** Which description matches "$table"?
**Type:** single

**Options:**
- Restricts which fields may be mass-assigned during insert or update
- Filters query results based on a condition
- Tells a Model which database table it represents
- Retrieves every record from a Model's table
**Answer:** Tells a Model which database table it represents
**Explanation:** $table matches this description: Tells a Model which database table it represents.

## Q20
**Question:** Using Query Builder instead of raw SQL strings reduces the risk of SQL injection.
**Type:** single

**Options:**
- True
- False
**Answer:** True
**Explanation:** The statement is True. Read the wording carefully and connect it to the CodeIgniter 4 behavior being tested.

## Q21
**Question:** Which CodeIgniter file typically stores database connection settings such as hostname, username, and database name?
**Type:** single

**Options:**
- Database.php only
- .env
- Routes.php
- Autoload.php
**Answer:** .env
**Explanation:** The correct answer is .env. Use that as the key CodeIgniter 4 fact for this question.

## Q22
**Question:** What is the primary purpose of a CodeIgniter Model?
**Type:** single

**Options:**
- To manage data and communicate with the database
- To store session data
- To render HTML output
- To define routes for the application
**Answer:** To manage data and communicate with the database
**Explanation:** The correct answer is To manage data and communicate with the database. Use that as the key CodeIgniter 4 fact for this question.

## Q23
**Question:** What does the $primaryKey property in a Model define?
**Type:** single

**Options:**
- The column CodeIgniter treats as the unique identifier for each row
- The database name
- The default sort column for all queries
- The first column shown in a view
**Answer:** The column CodeIgniter treats as the unique identifier for each row
**Explanation:** The correct answer is The column CodeIgniter treats as the unique identifier for each row. Use that as the key CodeIgniter 4 fact for this question.

## Q24
**Question:** A model defines protected $allowedFields = ['title', 'status']; but a controller tries to insert a record that also includes a description value. What happens?
**Type:** single

**Options:**
- The description value is silently ignored because it is not in $allowedFields
- The insert succeeds, including description
- An exception always halts the application
- CodeIgniter automatically adds description to $allowedFields
**Answer:** The description value is silently ignored because it is not in $allowedFields
**Explanation:** The correct answer is The description value is silently ignored because it is not in $allowedFields. Use that as the key CodeIgniter 4 fact for this question.

## Q25
**Question:** Every CodeIgniter application must have at least one Model, even if it does not use a database.
**Type:** single

**Options:**
- True
- False
**Answer:** False
**Explanation:** The statement is False. Read the wording carefully and connect it to the CodeIgniter 4 behavior being tested.

## Q26
**Question:** What term describes the special class that represents and manages a specific database table?
**Type:** command
**Answer:** Model
**Explanation:** Type Model exactly; this is the CodeIgniter 4 term, path, or function the question is asking for.

## Q27
**Question:** What Query Builder method sorts retrieved records by a specific column, ascending or descending?
**Type:** command
**Answer:** orderBy()
**Explanation:** Type orderBy() exactly; this is the CodeIgniter 4 term, path, or function the question is asking for.

## Q28
**Question:** A Model's $allowedFields property lists the columns permitted for mass assignment.
**Type:** single

**Options:**
- True
- False
**Answer:** True
**Explanation:** The statement is True. Read the wording carefully and connect it to the CodeIgniter 4 behavior being tested.
