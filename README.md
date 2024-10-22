This repository contains the Postman collection for the Student Management System focusing on managing student data. The APIs allow users to create, read, update, and delete (CRUD) student records.

. Table of Contents
. Introduction
. Prerequisites
. Postman Collection
. Environment Setup
. Student API Endpoints
  .  GET /students
  .  GET /students/{id}
  .  POST /students
  . PUT /students/{id}
  .  DELETE /students/{id}
. How to Run Tests
. Common Error Codes

** Introduction:-
The Student Management System (SMS) API allows for the management of student data in an educational institution. This API focuses on performing CRUD operations for student records such as adding new students, retrieving student details, updating student information, and deleting student records.

** Prerequisites:- 
To use the Postman collection, ensure you have the following installed:

** Postman Collection:- 
This collection contains requests related to student management. You can download and import the collection into Postman.

Steps to Import:
Download the collection JSON file.
Open Postman and click Import.
Select the collection JSON file.
The collection will now appear in your Postman workspace.

** Environment Setup:- 
Before making requests, set up an environment in Postman to store common variables such as the base_url.

Steps to Set Up Environment:
Open Postman and navigate to Environments.
Student API Endpoints
1. GET All Students
Description: Retrieve a list of all students.
Method: GET
URL: {{base_url}}/students
Response Codes:
200: Success
500: Server Error
Sample Response:
json
[
  {
    "id": 1,
    "name": "John Doe",
    "email": "john@example.com",
    "dob": "2000-01-01"
  },
  {
    "id": 2,
    "name": "Jane Smith",
    "email": "jane@example.com",
    "dob": "1999-05-12"
  }
]
2. GET Student by ID
Description: Retrieve the details of a student by their ID.
Method: GET
URL: {{base_url}}/students/{id}
Response Codes:
200: Success
404: Student Not Found
500: Server Error
Sample Response:
json
{
  "id": 1,
  "name": "John Doe",
  "email": "john@example.com",
  "dob": "2000-01-01"
}
3. Create New Student
Description: Add a new student to the system.
Method: POST
URL: {{base_url}}/students
Body (example):
json
{
  "name": "John Doe",
  "email": "john@example.com",
  "dob": "2000-01-01"
}
Response Codes:
201: Created
400: Bad Request (e.g., missing required fields)
500: Server Error
Sample Response:
json
{
  "id": 3,
  "name": "John Doe",
  "email": "john@example.com",
  "dob": "2000-01-01"
}
4. Update Student by ID
Description: Update the details of an existing student.
Method: PUT
URL: {{base_url}}/students/{id}
Body (example):
json
{
  "name": "John Updated",
  "email": "john.updated@example.com",
  "dob": "2000-01-01"
}
Response Codes:
200: Success
404: Student Not Found
400: Bad Request
500: Server Error
Sample Response:
json
{
  "id": 3,
  "name": "John Updated",
  "email": "john.updated@example.com",
  "dob": "2000-01-01"
}
5. Delete Student by ID
Description: Delete a student from the system by their ID.
Method: DELETE
URL: {{base_url}}/students/{id}
Response Codes:
200: Success
404: Student Not Found
500: Server Error
Sample Response:
json
{
  "message": "Student successfully deleted"
}
How to Run Tests
Open Postman and navigate to the imported collection.
Select the request (e.g., GET /students).
Ensure that the environment (SMS API) is selected.
Click Send to execute the request.
View the response in the Body section and check the Status.
Running the Entire Collection:
To run all the requests in the collection:

Open Runner in Postman.
Select the Student Management System collection.
Choose the environment (SMS API).
Click Run.
Common Error Codes
400 Bad Request: The server cannot process the request due to client error (e.g., missing required fields).
404 Not Found: The specified resource does not exist (e.g., student ID not found).
500 Internal Server Error: The server encountered an unexpected condition.
Contributing
Contributions are welcome! Please follow these steps to contribute:

This README provides a detailed guide for using the Student Management System API related to student data, with instructions on testing using Postman.
