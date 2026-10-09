# IT0049 Formative Assessment 4

<!-- Converted from 20 Canvas attempt-export blocks. Removed 0 repeated question(s). Correct-answer markers were used over selected wrong answers. -->

## Q1
**Question:** Why should passwords be verified using a password-checking function rather than comparing plain text?
**Type:** single

**Options:**
- It removes the need for login forms.
- Plain text comparison is slower in every case.
- Secure verification works with hashed passwords instead of exposing raw passwords.
- It turns sessions into database tables.
**Answer:** Secure verification works with hashed passwords instead of exposing raw passwords.
**Explanation:** Passwords should be stored as hashes and checked with a verification function, not compared as readable text.

## Q2
**Question:** Which line is a reasonable way to remove all authentication session data on logout?
**Type:** single

**Options:**
- view('logout')->erase();
- $routes->deleteAll();
- $model->dropSessionTable();
- session()->destroy();
**Answer:** session()->destroy();
**Explanation:** The correct answer is session()->destroy();. Logout should clear the authenticated session state so the browser is no longer treated as signed in.

## Q3
**Question:** What is a common reason to redirect after processing login?
**Type:** single

**Options:**
- It prevents the same form submission from being repeated by browser refresh.
- It disables validation.
- It changes the PHP version.
- It deletes the controller.
**Answer:** It prevents the same form submission from being repeated by browser refresh.
**Explanation:** Redirecting after login helps prevent the same form submission from being repeated by browser refresh.

## Q4
**Question:** What is the safest general description of authentication?
**Type:** single

**Options:**
- Changing all routes to POST.
- Rendering a database table.
- Styling a login button.
- Confirming a user's identity before allowing access.
**Answer:** Confirming a user's identity before allowing access.
**Explanation:** Authentication means confirming a user's identity before allowing access.

## Q5
**Question:** A controller checks if session()->get('isLoggedIn') is true before returning the dashboard view. What security goal does this support?
**Type:** single

**Options:**
- Session-based access control
- Route caching only
- Image resizing
- Database migration
**Answer:** Session-based access control
**Explanation:** The correct answer is Session-based access control. Protected content must be checked before it is displayed, even if the navigation link is hidden.

## Q6
**Question:** Hiding a menu link is enough to secure a protected page even if the route remains accessible.
**Type:** single

**Options:**
- True
- False
**Answer:** False
**Explanation:** The statement is False. Authentication and session checks must be enforced in the controller or route flow, not only in what the user can see on the page.

## Q7
**Question:** Password verification should work against hashed passwords rather than exposing raw passwords.
**Type:** single

**Options:**
- True
- False
**Answer:** True
**Explanation:** The statement is True. Authentication and session checks must be enforced in the controller or route flow, not only in what the user can see on the page.

## Q8
**Question:** What should a controller check before showing a protected page?
**Type:** command
**Answer:** Session/authentication state
**Explanation:** Type Session/authentication state exactly. For protected pages, the controller should verify the user's current session or authentication state before rendering restricted content.

## Q9
**Question:** A login page shows 'Invalid credentials' only after a failed attempt and then the message disappears. What feature most likely supports this?
**Type:** single

**Options:**
- Flash data
- Seeder classes
- File upload rules
- Route placeholders
**Answer:** Flash data
**Explanation:** The correct answer is Flash data. Flash data is meant for short-lived messages that survive only to the next request.

## Q10
**Question:** Why should access-control checks happen before displaying protected content?
**Type:** single

**Options:**
- To prevent unauthorized users from seeing restricted pages.
- To avoid using routes.
- To make CSS files load faster.
- To remove the need for HTML.
**Answer:** To prevent unauthorized users from seeing restricted pages.
**Explanation:** Protected content must be checked before it is displayed, even if the navigation link is hidden.

## Q11
**Question:** A developer stores the full password hash and user role in session after login. What should be evaluated?
**Type:** single

**Options:**
- Whether only necessary, non-sensitive session data is stored.
- Whether views can run without controllers.
- Whether sessions can replace all database queries.
- Whether the public folder should store controllers.
**Answer:** Whether only necessary, non-sensitive session data is stored.
**Explanation:** Sessions should store only the identity data needed for the app, not sensitive values like password hashes.

## Q12
**Question:** Which session value would be reasonable to store after login?
**Type:** single

**Options:**
- The Composer executable file.
- The complete database dump.
- The logged-in user's id or username.
- The user's plaintext password.
**Answer:** The logged-in user's id or username.
**Explanation:** A user id or username is reasonable session data because it identifies the logged-in user without storing the password.

## Q13
**Question:** What should happen after a successful login?
**Type:** single

**Options:**
- Disable the session library.
- Display the password in the browser.
- Store appropriate user identity data in the session and redirect to a protected page.
- Delete all routes.
**Answer:** Store appropriate user identity data in the session and redirect to a protected page.
**Explanation:** After login, the app should remember appropriate identity data in the session and move the user to an allowed page.

## Q14
**Question:** Which description matches "Session"?
**Type:** single

**Options:**
- Verifies that a user is who they claim to be
- Removes the authenticated session state
- Stores a short message for the next request
- Stores small user-related data across requests
**Answer:** Stores small user-related data across requests
**Explanation:** Session matches this description: Stores small user-related data across requests.

## Q15
**Question:** A login workflow usually redirects after successful authentication.
**Type:** single

**Options:**
- True
- False
**Answer:** True
**Explanation:** The statement is True. Authentication and session checks must be enforced in the controller or route flow, not only in what the user can see on the page.

## Q16
**Question:** Which description matches "Logout"?
**Type:** single

**Options:**
- Stores small user-related data across requests
- Removes the authenticated session state
- Verifies that a user is who they claim to be
- Stores a short message for the next request
**Answer:** Removes the authenticated session state
**Explanation:** Logout matches this description: Removes the authenticated session state.

## Q17
**Question:** Which description matches "Flash data"?
**Type:** single

**Options:**
- Removes the authenticated session state
- Stores a short message for the next request
- Stores small user-related data across requests
- Verifies that a user is who they claim to be
**Answer:** Stores a short message for the next request
**Explanation:** Flash data matches this description: Stores a short message for the next request.

## Q18
**Question:** What is the main purpose of logout?
**Type:** single

**Options:**
- To create a new user record.
- To remove the user's authenticated session state.
- To change the public folder.
- To insert a database row.
**Answer:** To remove the user's authenticated session state.
**Explanation:** Logout should clear the authenticated session state so the browser is no longer treated as signed in.

## Q19
**Question:** Which description matches "Authentication"?
**Type:** single

**Options:**
- Stores small user-related data across requests
- Stores a short message for the next request
- Verifies that a user is who they claim to be
- Removes the authenticated session state
**Answer:** Verifies that a user is who they claim to be
**Explanation:** Authentication matches this description: Verifies that a user is who they claim to be.

## Q20
**Question:** What is the primary purpose of a session in a web application?
**Type:** single

**Options:**
- To write CSS rules into views.
- To permanently replace the database.
- To store small user-related data across multiple requests.
- To create routes automatically.
**Answer:** To store small user-related data across multiple requests.
**Explanation:** A session stores small user-related data across requests, such as whether the user is signed in.
