# Megaplan API Automation (Postman)

## Description
This repository contains an automated Postman collection for testing the API of the "Megaplan" task management system. The collection simulates a complete end-to-end business flow involving two user roles: a Director and a Staff Member.

## Business Flow
The collection automates the following scenario:
1. **Director's Authorization:** Obtains a Bearer token and saves it to collection variables.
2. **Task Creation:** The Director creates a new task and assigns it to an employee. The `task_id` is parsed and saved for future requests.
3. **Task Modification:** The Director adds a description to the created task.
4. **Staff Member's Authorization:** The assigned employee logs in and obtains their own token.
5. **Accepting the Task:** The employee accepts the task (status change).
6. **Completing the Task:** The employee marks the task as 'done'.
7. **Commenting:** The employee adds a comment to the task.
8. **Director's Re-authorization:** The Director logs in again to review.
9. **Task Acceptance:** The Director accepts the completed work.
10. **Task Deletion:** The Director deletes the task (cleaning up test data).

## Key Skills Demonstrated
* **API Testing:** Interacting with RESTful APIs using POST and DELETE methods.
* **Chaining Requests:** Passing data (tokens, IDs) between requests using Postman variables.
* **JavaScript Testing:** Writing assertions in the `Tests` tab to validate response codes (200 OK) and response bodies (parsing JSON).
* **Role-Based Testing:** Simulating workflows using different authorization credentials.
* **Test Data Management:** Cleaning up created entities at the end of the test run.

## How to run
1. Clone this repository.
2. Open Postman.
3. Click `Import` and select the `megaplan.json` file.
4. Run the collection using the Postman Collection Runner. *(Note: Valid credentials are required in the request bodies to execute the flow successfully).*
