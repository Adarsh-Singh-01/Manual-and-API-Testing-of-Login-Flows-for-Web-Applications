Project Title: Manual and API Testing of Login Flows for Web Applications
Website Tested: Practice Test Automation Login Page 
Dummy API: https://reqres.in/api/login 
Tools Used: Google Chrome, Postman, Google Sheets, Browser Developer Tools


1. Objective
The aim of this project is to validate the login functionality of a web application using manual testing and API testing. The project ensures that:
•	Users can log in successfully with valid credentials.
•	Proper error messages are displayed for invalid or empty inputs.
•	The backend APIs respond correctly for authentication.
•	Usability features like password masking and button behavior are working correctly.
________________________________________
2. Tools & Technologies
•	Google Chrome / Edge: For frontend manual testing
•	Postman: For API testing and validating backend login responses
•	Google Sheets / Excel: For recording test cases, results, and bug reports
•	Browser Developer Tools: Inspecting fields and debugging UI
________________________________________
3. Test Cases
3.1 Manual UI Test Cases
Test Case ID	Scenario	Steps	Expected Result	Actual Result	Status
TC01	Login with valid credentials	Enter username: student, password: Password123, click Submit	Login successful, success message or dashboard shown	Login successful, redirected to success page	Pass
TC02	Invalid password	Enter username: student, password: wrongpass, click Submit	Error message “Your password is invalid!”	Error message displayed	Pass
TC03	Invalid username	Enter username: wronguser, password: Password123, click Submit	Error message “Your username is invalid!”	Error message displayed	Pass
TC04	Empty username	Leave username blank, password: Password123, click Submit	Message “Username required”	Message displayed	Pass
TC05	Empty password	Enter username: student, leave password blank, click Submit	Message “Password required”	Message displayed	Pass
TC06	Both fields empty	Leave username & password blank, click Submit	Validation message displayed	Message displayed	Pass
TC07	Password masking	Type password in the field	Password hidden as dots or asterisks	Masking works correctly	Pass
TC08	Login button disabled before input	Click login without filling fields	Login button inactive	Button disabled until input entered	Pass
________________________________________



3.2 API Test Cases (Postman)
Test Case ID	Scenario	Input Data	Expected Result	Actual Result	Status
TC09	API valid login	{"email":"eve.holt@reqres.in","password":"cityslicka"}	Status 200 OK, returns token	Received 200 OK, token returned	Pass
TC10	API invalid login	{"email":"peter@klaven"}	Status 400 Bad Request, error: “Missing password”	Received 400 Bad Request, error message shown	Pass
________________________________________
4. Bug Reporting / Observations
Bug ID	Description	Steps to Reproduce	Severity	Status
B01	Error message for empty username displayed as generic instead of “Username required”	Leave username blank, enter password, click Submit	Medium	Resolved (Expected behavior documented)
B02	Invalid password message not very prominent on UI	Enter wrong password, click Submit	Low	Resolved (Observed and recorded)
B03	API returns 400 instead of 401 for invalid login	POST invalid credentials to API	Low	Accepted as expected for API
Observation: All test cases passed successfully; backend APIs correctly handle both positive and negative scenarios. UI validations like password masking and button behavior work as expected.
________________________________________
5. Execution Summary
•	Designed and executed 10 test cases covering manual UI testing and API testing.
•	Verified that login functionality works as expected with valid credentials.
•	Ensured proper error handling for invalid or empty input scenarios.
•	Documented all results and observed bugs in Google Sheets.
•	Used Postman to validate backend login API responses, covering both positive and negative test cases.
•	Gained practical exposure to manual testing, API validation, bug reporting, and QA workflow.
________________________________________
6. Learning Outcomes
•	Hands-on experience with manual web testing and test case design.
•	Knowledge of API testing using Postman and interpreting HTTP response codes.
•	Understanding of frontend validations, usability features, and error handling.
•	Ability to document results, create bug reports, and track test execution in a structured manner.
•	Exposure to real-world QA processes relevant for Test Engineer / QA Automation roles.
________________________________________
7. Tools / Skills Highlighted
•	Manual Testing: Functional, boundary, and negative test cases
•	API Testing: Postman, JSON, HTTP methods (POST/GET)
•	Test Documentation: Google Sheets / Excel
•	UI Validation: Password masking, button behavior, error message checks

