"#api"

# API Name
MyFirst API
This is a simple API built using the Slim framework for managing names in a database. It provides endpoints to insert, retrieve, update, and delete names.

 


## API
The MyFirst API serves as a straightforward web service for managing a collection of names within a database. Its primary purpose is to facilitate basic CRUD (Create, Read, Update, Delete) operations on the names dataset. The API is implemented using the Slim framework and employs JSON for data exchange.

The API is designed to be a practical tool for applications or systems that need to interact with a backend database to handle information related to personal names. Whether it's for user profiles, contacts, or any other scenario requiring the management of names, MyDemo API provides a lightweight and accessible solution.

 


## API
Endpoints


1. Create (POST/postName) http://localhost/api/public/postName
Allows the addition of new names to the database.
Users can submit a JSON payload containing the first name (fname) and last name (lname).
Parameters:
fname (string): First name.
lname (string): Last name.

2. Read (GET /getName) http://localhost/api/public/getName
Retrieves all names from the database.
Provides a simple way to fetch the entire dataset of names.

3. Update (POST/updateName)
Enables the modification of an existing name in the database.
Requires the user to provide the ID of the name to be updated, along with the new first name (fname) and last name (lname).
Parameters:
id (int): ID of the name to be updated.
fname (string): New first name.
lname (string): New last name.

4. Delete (POST/deleteName)
Allows the removal of a name from the database.
Users must specify the ID of the name to be deleted.
Parameters:
id (int): ID of the name to be deleted.




## Request
Payload

Request Payload Structure
1. POST /postName
To insert a new name into the database, the API expects a JSON payload with the following structure:
{
  "lname": "hortizuela",
  "fname": "manny"
}
Required Fields:
lname (string): The last name of the individual.
fname (string): The first name of the individual.
Optional Fields:
None

2. POST /updateName
To update an existing name in the database, the API requires a JSON payload with the following structure:
{
  "id": 1,
  "lname": "wick",
  "fname": "john"
}
Required Fields:
id (int): The ID of the name to be updated.
lname (string): The new last name.
fname (string): The new first name.
Optional Fields:
None

3. POST /deleteName
To delete a name from the database, the API expects a JSON payload with the following structure:
{
  "id": 1
}
Required Fields:
id (int): The ID of the name to be deleted.
Optional Fields:
None

 


## Response


API Response Structure
1. Success Response:
For successful operations, the API responds with a JSON object containing a "status" field set to "success" and optional "data" field. Here's an example:
{
  "status": "success",
  "data": null
}
Status Codes:
200 OK: The request was successful.
201 Created: The resource was successfully created (applicable for POST requests).
204 No Content: The request was successful, and there is no additional content to send (applicable for DELETE requests).

2. Error Response:
In case of errors, the API responds with a JSON object containing a "status" field set to "error" and a "message" field providing details about the error. Here's an example:
{
  "status": "error",
  "message": "Database connection error."
}
Status Codes:
400 Bad Request: The request was malformed or invalid.
401 Unauthorized: Authentication is required, and credentials are missing or incorrect.
403 Forbidden: Authentication succeeded, but the authenticated user does not have the necessary permissions.
404 Not Found: The requested resource could not be found.
500 Internal Server Error: The server encountered an unexpected condition that prevented it from fulfilling the request.


Example Responses:
a. POST /postName - Success:
{
  "status": "success",
  "data": null
}

b. POST /updateName - Success:
{
  "status": "success",
  "data": null
}

c. POST /deleteName - Success:
{
  "status": "success",
  "data": null
}

d. Error:
{
  "status": "error",
  "message": "Invalid input. Please provide a valid ID."
}



 


## Usage


Using Postman to Work with the API:

Get Postman Ready: Make sure you have Postman installed and set up on your system.

Add Data to the Database:

Opt for the "POST" HTTP method. Type in the URL: http://localhost/api/public/postName. In the request body, include the "lname" and "fname" parameters with the values you want to insert. Click "Send" to execute the request. Update Existing Data:

Select the "GET" HTTP method. Specify the URL: http://localhost/api/public/getName. Keep the request body empty, as no additional parameters are needed. Click "Send" to fetch the data. Delete Data from the Database:

Choose the "POST" HTTP method. Enter the URL: http://localhost/api/public/updateName. Add the "id," "fname," and "lname" parameters to the request body with the updated values. Click "Send" to submit the request. Retrieve Data from the Database:

Set the HTTP method to "POST." Input the URL: http://localhost/api/public/deleteName. In the request body, include the "id" parameter with the ID of the data you want to delete. Click "Send" to start the deletion process.


 


## License


No License.

 


## Contributors


Dr. Manny Hortizuela:

some codes, 
structure of the database, 
payloads, 
others

 


## Contact
Name: Florante F. Rosiete Jr.
Email: florante.rosiete@student.dmmmsu.edu.ph 
Number: 09918487421
Fb Account: https://www.facebook.com/profile.php?id=100007440554245&mibextid=ZbWKwL
Telegram: @BadGalFLORI3
