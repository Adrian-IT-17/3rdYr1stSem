# IT0049 Formative Assessment 3

<!-- Converted from 39 Canvas attempt-export blocks. Removed 11 repeated question(s) from the second attempt. -->

## Q1
**Question:** Why should a Delete action normally be submitted using POST rather than a normal GET link?
**Type:** single

**Options:**
- GET cannot open pages.
- Destructive actions should not be triggered by simple page visits or crawlers.
- GET routes cannot use controllers.
- POST is required for all routes.
**Answer:** Destructive actions should not be triggered by simple page visits or crawlers.
**Explanation:** The correct answer is Destructive actions should not be triggered by simple page visits or crawlers.. Use that as the key CodeIgniter 4 fact for this question.

## Q2
**Question:** Validation should normally run after saving the submitted data.
**Type:** single

**Options:**
- True
- False
**Answer:** False
**Explanation:** The statement is False. Read the wording carefully and connect it to the CodeIgniter 4 behavior being tested.

## Q3
**Question:** Which line moves an uploaded file object named $file into the public uploads folder using a generated name?
**Type:** single

**Options:**
- $file->render('uploads');
- $file->move(FCPATH . 'uploads', $newName);
- $file->saveAsRoute($newName);
- $file->copyToDatabase($newName);
**Answer:** $file->move(FCPATH . 'uploads', $newName);
**Explanation:** The correct answer is $file->move(FCPATH . 'uploads', $newName);. Use that as the key CodeIgniter 4 fact for this question.

## Q4
**Question:** Which form attribute is required when a CodeIgniter page must upload a file?
**Type:** single

**Options:**
- method="GET"
- autocomplete="off"
- target="_blank"
- enctype="multipart/form-data"
**Answer:** enctype="multipart/form-data"
**Explanation:** The correct answer is enctype="multipart/form-data". Use that as the key CodeIgniter 4 fact for this question.

## Q5
**Question:** A controller receives a submitted title field. Which line safely reads the posted value through CodeIgniter's request object?
**Type:** single

**Options:**
- $this->request->getPost('title');
- $_TITLE['title'];
- $routes->post('title');
- $this->view->title();
**Answer:** $this->request->getPost('title');
**Explanation:** The correct answer is $this->request->getPost('title');. Use that as the key CodeIgniter 4 fact for this question.

## Q6
**Question:** Which CodeIgniter helper function is commonly placed inside a form to include CSRF protection?
**Type:** single

**Options:**
- csrf_field()
- csrf_input_only()
- csrf_token()
- protect_form()
**Answer:** csrf_field()
**Explanation:** The correct answer is csrf_field(). Use that as the key CodeIgniter 4 fact for this question.

## Q7
**Question:** Which description matches "getFile()"?
**Type:** single

**Options:**
- Describes what submitted input must satisfy before saving
- Transfers an accepted uploaded file to a target folder
- Restores previously submitted input on a redisplayed form
- Reads an uploaded file object from the request
**Answer:** Reads an uploaded file object from the request
**Explanation:** getFile() matches this description: Reads an uploaded file object from the request.

## Q8
**Question:** Which statement best describes CRUD?
**Type:** single

**Options:**
- A routing shortcut for GET requests only.
- A CodeIgniter file-upload library.
- The four record actions: create, read, update, and delete.
- A database credential format.
**Answer:** The four record actions: create, read, update, and delete.
**Explanation:** The correct answer is The four record actions: create, read, update, and delete.. Use that as the key CodeIgniter 4 fact for this question.

## Q9
**Question:** What helper can print the validation error message for one field in a view?
**Type:** command
**Answer:** validation_show_error()
**Explanation:** Type validation_show_error() exactly; this is the CodeIgniter 4 term, path, or function the question is asking for.

## Q10
**Question:** A form field is named email, but the controller validates user_email. What is the most likely result?
**Type:** single

**Options:**
- CodeIgniter will combine both names.
- The route will change automatically.
- Validation will not check the submitted email field correctly.
- The database will rename the column.
**Answer:** Validation will not check the submitted email field correctly.
**Explanation:** The correct answer is Validation will not check the submitted email field correctly.. Use that as the key CodeIgniter 4 fact for this question.

## Q11
**Question:** A view should normally decide by itself which database record to delete.
**Type:** single

**Options:**
- True
- False
**Answer:** False
**Explanation:** The statement is False. Read the wording carefully and connect it to the CodeIgniter 4 behavior being tested.

## Q12
**Question:** File type and file size restrictions help reduce unsafe upload behavior.
**Type:** single

**Options:**
- True
- False
**Answer:** True
**Explanation:** The statement is True. Read the wording carefully and connect it to the CodeIgniter 4 behavior being tested.

## Q13
**Question:** Which description matches "old()"?
**Type:** single

**Options:**
- Restores previously submitted input on a redisplayed form
- Transfers an accepted uploaded file to a target folder
- Reads an uploaded file object from the request
- Describes what submitted input must satisfy before saving
**Answer:** Restores previously submitted input on a redisplayed form
**Explanation:** old() matches this description: Restores previously submitted input on a redisplayed form.

## Q14
**Question:** Which description matches "Validation rule"?
**Type:** single

**Options:**
- Transfers an accepted uploaded file to a target folder
- Reads an uploaded file object from the request
- Restores previously submitted input on a redisplayed form
- Describes what submitted input must satisfy before saving
**Answer:** Describes what submitted input must satisfy before saving
**Explanation:** Validation rule matches this description: Describes what submitted input must satisfy before saving.

## Q15
**Question:** What CodeIgniter constant points to the public front-controller path, often used when saving files under public/uploads?
**Type:** command
**Answer:** FCPATH
**Explanation:** Type FCPATH exactly; this is the CodeIgniter 4 term, path, or function the question is asking for.

## Q16
**Question:** What does validation_show_error('title') display in a CodeIgniter view?
**Type:** single

**Options:**
- The validation message for the title field.
- The current route name.
- The uploaded file size.
- The controller class name.
**Answer:** The validation message for the title field.
**Explanation:** The correct answer is The validation message for the title field.. Use that as the key CodeIgniter 4 fact for this question.

## Q17
**Question:** What should be saved in the database after a successful public image upload?
**Type:** single

**Options:**
- The user's original computer folder path.
- Only the generated filename or path needed to display the file.
- The entire binary file inside a text column.
- The contents of $_FILES without checking it.
**Answer:** Only the generated filename or path needed to display the file.
**Explanation:** The correct answer is Only the generated filename or path needed to display the file.. Use that as the key CodeIgniter 4 fact for this question.

## Q18
**Question:** Which description matches "move()"?
**Type:** single

**Options:**
- Restores previously submitted input on a redisplayed form
- Describes what submitted input must satisfy before saving
- Transfers an accepted uploaded file to a target folder
- Reads an uploaded file object from the request
**Answer:** Transfers an accepted uploaded file to a target folder
**Explanation:** move() matches this description: Transfers an accepted uploaded file to a target folder.

## Q19
**Question:** What file input form encoding is required for file uploads?
**Type:** command
**Answer:** multipart/form-data
**Explanation:** Type multipart/form-data exactly; this is the CodeIgniter 4 term, path, or function the question is asking for.

## Q20
**Question:** old() helps preserve submitted values when a form is redisplayed after validation failure.
**Type:** single

**Options:**
- True
- False
**Answer:** True
**Explanation:** The statement is True. old() is commonly used to repopulate form fields after validation fails so the user does not have to retype everything.

## Q21
**Question:** Which validation rule set best restricts an uploaded avatar to JPG or PNG images no larger than 2 MB?
**Type:** single

**Options:**
- is_unique[avatar]
- valid_email|permit_empty
- required|min_length[2]
- uploaded[avatar]|max_size[avatar,2048]|mime_in[avatar,image/jpg,image/jpeg,image/png]
**Answer:** uploaded[avatar]|max_size[avatar,2048]|mime_in[avatar,image/jpg,image/jpeg,image/png]
**Explanation:** The correct answer is uploaded[avatar]|max_size[avatar,2048]|mime_in[avatar,image/jpg,image/jpeg,image/png]. Use that as the key CodeIgniter 4 fact for this question.

## Q22
**Question:** A student saves uploaded avatars before checking file type and size. What is the main risk?
**Type:** single

**Options:**
- Unsafe or unexpected files may already be stored before rejection.
- The controller will always skip routing.
- The database cannot store filenames.
- The browser will not display HTML.
**Answer:** Unsafe or unexpected files may already be stored before rejection.
**Explanation:** The correct answer is Unsafe or unexpected files may already be stored before rejection.. Use that as the key CodeIgniter 4 fact for this question.

## Q23
**Question:** Deleting records through a normal GET link is a safe default for production systems.
**Type:** single

**Options:**
- True
- False
**Answer:** False
**Explanation:** The statement is False. Read the wording carefully and connect it to the CodeIgniter 4 behavior being tested.

## Q24
**Question:** Which CodeIgniter UploadedFile method generates a safer unique filename before moving the file?
**Type:** single

**Options:**
- makeSafe()
- newFilename()
- getRandomName()
- escapeName()
**Answer:** getRandomName()
**Explanation:** The correct answer is getRandomName(). Use that as the key CodeIgniter 4 fact for this question.

## Q25
**Question:** Why is a random server filename safer than using the uploaded file's original name?
**Type:** single

**Options:**
- It removes the need for file validation.
- It makes images larger.
- It automatically compresses the file.
- It reduces name collisions and avoids trusting user-supplied filenames.
**Answer:** It reduces name collisions and avoids trusting user-supplied filenames.
**Explanation:** The correct answer is It reduces name collisions and avoids trusting user-supplied filenames.. Use that as the key CodeIgniter 4 fact for this question.

## Q26
**Question:** Why should validation run before insert() or update() in a CodeIgniter controller?
**Type:** single

**Options:**
- It makes the view load before the controller.
- It automatically creates the database table.
- It removes the need for routes.
- It prevents invalid or unsafe input from being saved.
**Answer:** It prevents invalid or unsafe input from being saved.
**Explanation:** The correct answer is It prevents invalid or unsafe input from being saved.. Use that as the key CodeIgniter 4 fact for this question.

## Q27
**Question:** A page successfully saves a customer but displays a blank list afterward. The controller calls return view('customers/index') without passing records. What should be checked first?
**Type:** single

**Options:**
- Whether customer data is retrieved and passed to the view.
- Whether the public folder was renamed to app.
- Whether the CSS file has a body tag.
- Whether the image upload folder exists.
**Answer:** Whether customer data is retrieved and passed to the view.
**Explanation:** The correct answer is Whether customer data is retrieved and passed to the view.. Use that as the key CodeIgniter 4 fact for this question.

## Q28
**Question:** A CodeIgniter form that uploads files must use multipart/form-data.
**Type:** single

**Options:**
- True
- False
**Answer:** True
**Explanation:** The statement is True. Read the wording carefully and connect it to the CodeIgniter 4 behavior being tested.
