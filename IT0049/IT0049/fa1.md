# IT0049 Formative Assessment 1

<!-- Converted from 39 Canvas attempt-export blocks. Removed 11 repeated question(s) from the second attempt. -->

## Q1
**Question:** In a default CodeIgniter 4 installation, which folder should be set as the web server's document root for production hosting?
**Type:** single

**Options:**
- system
- public
- writable
- app
**Answer:** public
**Explanation:** The correct answer is public. Use that as the key CodeIgniter 4 fact for this question.

## Q2
**Question:** Which description matches "Model"?
**Type:** single

**Options:**
- Displays information to the user, usually as HTML
- Manages data and communicates with the database
- Decides what should happen when a specific URL is requested
- Maps an incoming URL to a specific controller and method
**Answer:** Manages data and communicates with the database
**Explanation:** Model matches this description: Manages data and communicates with the database.

## Q3
**Question:** A CodeIgniter View file can only contain plain HTML and is not allowed to include any PHP code.
**Type:** single

**Options:**
- True
- False
**Answer:** False
**Explanation:** The statement is False. Read the wording carefully and connect it to the CodeIgniter 4 behavior being tested.

## Q4
**Question:** Installing CodeIgniter 4 with Composer is the only way to create a new CodeIgniter project.
**Type:** single

**Options:**
- True
- False
**Answer:** False
**Explanation:** The statement is False. Read the wording carefully and connect it to the CodeIgniter 4 behavior being tested.

## Q5
**Question:** What is the name of the function used inside a CodeIgniter controller to load a View file and optionally pass data to it?
**Type:** command
**Answer:** view()
**Explanation:** Type view() exactly; this is the CodeIgniter 4 term, path, or function the question is asking for.

## Q6
**Question:** A controller currently has public function about() { return view('about'); }. A developer wants the About page to also display the current year automatically. What is the correct way to do this?
**Type:** single

**Options:**
- Pass the year from the controller to the view using an array, e.g. return view('about', ['year' => date('Y')]);
- Create a completely separate route just for the year
- Store the year inside Routes.php
- Hardcode the year directly into the view file
**Answer:** Pass the year from the controller to the view using an array, e.g. return view('about', ['year' => date('Y')]);
**Explanation:** The correct answer is Pass the year from the controller to the view using an array, e.g. return view('about', ['year' => date('Y')]);. Use that as the key CodeIgniter 4 fact for this question.

## Q7
**Question:** Which description matches "Route"?
**Type:** single

**Options:**
- Displays information to the user, usually as HTML
- Decides what should happen when a specific URL is requested
- Manages data and communicates with the database
- Maps an incoming URL to a specific controller and method
**Answer:** Maps an incoming URL to a specific controller and method
**Explanation:** Route matches this description: Maps an incoming URL to a specific controller and method.

## Q8
**Question:** Route definitions in CodeIgniter are typically written in the file app/Config/Routes.php.
**Type:** single

**Options:**
- True
- False
**Answer:** True
**Explanation:** The statement is True. Read the wording carefully and connect it to the CodeIgniter 4 behavior being tested.

## Q9
**Question:** Which description matches "View"?
**Type:** single

**Options:**
- Decides what should happen when a specific URL is requested
- Manages data and communicates with the database
- Displays information to the user, usually as HTML
- Maps an incoming URL to a specific controller and method
**Answer:** Displays information to the user, usually as HTML
**Explanation:** View matches this description: Displays information to the user, usually as HTML.

## Q10
**Question:** What does MVC stand for in the context of web application architecture?
**Type:** single

**Options:**
- Multiple-Variable-Class
- Method-Value-Component
- Model-View-Controller
- Model-Variable-Controller
**Answer:** Model-View-Controller
**Explanation:** The correct answer is Model-View-Controller. Use that as the key CodeIgniter 4 fact for this question.

## Q11
**Question:** Which line of code correctly defines a route that maps the URL /about to the about() method of the Pages controller?
**Type:** single

**Options:**
- $routes->view('about', 'Pages');
- $routes->about('Pages::index');
- $routes->controller('Pages@about');
- $routes->get('/about', 'Pages::about');
**Answer:** $routes->get('/about', 'Pages::about');
**Explanation:** The correct answer is $routes->get('/about', 'Pages::about');. Use that as the key CodeIgniter 4 fact for this question.

## Q12
**Question:** A controller method needs to send the value $name = 'Maria' to a view so it can be displayed. Which line correctly accomplishes this?
**Type:** single

**Options:**
- echo view('profile', $name);
- return view('profile', $name);
- return view('profile', ['name' => $name]);
- return $name->view('profile');
**Answer:** return view('profile', ['name' => $name]);
**Explanation:** The correct answer is return view('profile', ['name' => $name]);. Use that as the key CodeIgniter 4 fact for this question.

## Q13
**Question:** What is the name of the PHP dependency manager commonly used to install CodeIgniter 4?
**Type:** command
**Answer:** Composer
**Explanation:** Type Composer exactly; this is the CodeIgniter 4 term, path, or function the question is asking for.

## Q14
**Question:** Why might a developer choose to use a web framework like CodeIgniter instead of writing an application in plain PHP?
**Type:** single

**Options:**
- Frameworks automatically generate a complete user interface
- Frameworks eliminate the need to learn PHP
- Frameworks do not require a web server
- Frameworks provide reusable structure and tools, reducing repetitive setup work
**Answer:** Frameworks provide reusable structure and tools, reducing repetitive setup work
**Explanation:** The correct answer is Frameworks provide reusable structure and tools, reducing repetitive setup work. Use that as the key CodeIgniter 4 fact for this question.

## Q15
**Question:** A developer argues that since a static PHP array "basically behaves like a small database," there is no real reason to ever migrate a working application to a real database. What is the strongest counterargument?
**Type:** single

**Options:**
- A static array's data disappears when the server restarts and cannot be reliably shared, searched, or updated by multiple users the way a database can
- PHP arrays cannot technically store text data
- Static arrays are not permitted inside CodeIgniter controllers
- A real database is always slower than a static array
**Answer:** A static array's data disappears when the server restarts and cannot be reliably shared, searched, or updated by multiple users the way a database can
**Explanation:** The correct answer is A static array's data disappears when the server restarts and cannot be reliably shared, searched, or updated by multiple users the way a database can. Use that as the key CodeIgniter 4 fact for this question.

## Q16
**Question:** What architectural pattern separates an application into three interconnected components responsible for data, presentation, and control logic?
**Type:** command
**Answer:** MVC (Model-View-Controller)
**Explanation:** Type MVC (Model-View-Controller) exactly; this is the CodeIgniter 4 term, path, or function the question is asking for.

## Q17
**Question:** A view file contains the line <h1><?= $title ?></h1>, but the page displays an "Undefined variable $title" error. What most likely caused this?
**Type:** single

**Options:**
- The route was defined incorrectly
- The .htaccess file is missing
- The View file has the wrong file extension
- The controller did not pass title in the data array to view()
**Answer:** The controller did not pass title in the data array to view()
**Explanation:** The correct answer is The controller did not pass title in the data array to view(). Use that as the key CodeIgniter 4 fact for this question.

## Q18
**Question:** Which description matches "Controller"?
**Type:** single

**Options:**
- Maps an incoming URL to a specific controller and method
- Displays information to the user, usually as HTML
- Decides what should happen when a specific URL is requested
- Manages data and communicates with the database
**Answer:** Decides what should happen when a specific URL is requested
**Explanation:** Controller matches this description: Decides what should happen when a specific URL is requested.

## Q19
**Question:** In MVC, the Model is responsible for rendering HTML and displaying content to the user.
**Type:** single

**Options:**
- True
- False
**Answer:** False
**Explanation:** The statement is False. Read the wording carefully and connect it to the CodeIgniter 4 behavior being tested.

## Q20
**Question:** In the MVC pattern, the Controller is responsible for deciding which View is displayed in response to a request.
**Type:** single

**Options:**
- True
- False
**Answer:** True
**Explanation:** The statement is True. The controller handles the request and chooses the response, which often means returning the correct View.

## Q21
**Question:** Every folder inside a CodeIgniter 4 project is meant to be publicly accessible from the web server.
**Type:** single

**Options:**
- True
- False
**Answer:** False
**Explanation:** The statement is False. Read the wording carefully and connect it to the CodeIgniter 4 behavior being tested.

## Q22
**Question:** What is the term for a segment of a route pattern (such as (:num)) that captures part of the URL and passes it to a controller method as a parameter?
**Type:** command
**Answer:** Route placeholder (wildcard)
**Explanation:** Type Route placeholder (wildcard) exactly; this is the CodeIgniter 4 term, path, or function the question is asking for.

## Q23
**Question:** What is the purpose of the .htaccess file in the public folder of a CodeIgniter project?
**Type:** single

**Options:**
- It removes index.php from the URL through URL rewriting
- It defines routes for the application
- It configures the Composer autoloader
- It stores database credentials
**Answer:** It removes index.php from the URL through URL rewriting
**Explanation:** The correct answer is It removes index.php from the URL through URL rewriting. Use that as the key CodeIgniter 4 fact for this question.

## Q24
**Question:** A view file is saved as app/Views/tasks/index.php, but a controller calls return view('Tasks/Index'); using different capitalization. This works on a Windows machine but fails once deployed to a Linux server. What does this reveal?
**Type:** single

**Options:**
- Linux servers do not support the .php extension
- Views only work correctly on Windows servers
- View lookups can be case-sensitive depending on the operating system, so the path passed to view() should match the actual file's case
- The route file must be renamed to match the operating system
**Answer:** View lookups can be case-sensitive depending on the operating system, so the path passed to view() should match the actual file's case
**Explanation:** The correct answer is View lookups can be case-sensitive depending on the operating system, so the path passed to view() should match the actual file's case. Use that as the key CodeIgniter 4 fact for this question.

## Q25
**Question:** Passing data to a View requires converting the data into a special CodeIgniter-only data type before calling view().
**Type:** single

**Options:**
- True
- False
**Answer:** False
**Explanation:** The statement is False. Read the wording carefully and connect it to the CodeIgniter 4 behavior being tested.

## Q26
**Question:** Which function is used inside a CodeIgniter controller method to load and return a View?
**Type:** single

**Options:**
- render()
- display()
- view()
- show()
**Answer:** view()
**Explanation:** The correct answer is view(). Use that as the key CodeIgniter 4 fact for this question.

## Q27
**Question:** Which of the following best describes the role of a View in MVC?
**Type:** single

**Options:**
- It focuses only on presentation and displaying data
- It defines the URL structure of the application
- It manages database connections
- It handles all business logic and decision-making
**Answer:** It focuses only on presentation and displaying data
**Explanation:** The correct answer is It focuses only on presentation and displaying data. Use that as the key CodeIgniter 4 fact for this question.

## Q28
**Question:** A developer writes all of an application's HTML directly inside controller methods using echo statements, without using any View files. Why is this generally considered poor practice under the MVC pattern?
**Type:** single

**Options:**
- It causes routes to stop working entirely
- It prevents the use of static PHP arrays
- CodeIgniter does not allow echo inside controllers
- It mixes presentation code with request-handling logic, making the application harder to maintain
**Answer:** It mixes presentation code with request-handling logic, making the application harder to maintain
**Explanation:** The correct answer is It mixes presentation code with request-handling logic, making the application harder to maintain. Use that as the key CodeIgniter 4 fact for this question.
