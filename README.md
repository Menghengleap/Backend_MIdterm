Quotes API
The Quotes API is a RESTful web service that allows you to manage a collection of quotes, authors, and categories. It supports operations for creating, retrieving, updating, and deleting quotes, as well as managing their associated authors and categories.

Getting Started
These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

Prerequisites
PHP 7.4 or higher
MySQL 5.7 or higher
Apache server (XAMPP/WAMP/MAMP/LAMP stack recommended for development)

Installing
Clone the repository to your local machine or download the ZIP file and extract it in your web server's root directory (e.g., htdocs for XAMPP).

Navigate to the project directory and import the quotesdb.sql file into your MySQL database. This file includes the necessary schema for the database.

Configure your database connection settings by editing the api/Database.php file with your database credentials.

Start your Apache and MySQL servers using your server stack's control panel.

Access the API through http://localhost/api/.

API Endpoints
Quotes
GET /api/quotes/ - Retrieve all quotes
GET /api/quotes/?id=4 - Retrieve a specific quote by ID
GET /api/quotes/?author_id=10 - Retrieve all quotes from a specific author by author ID
GET /api/quotes/?category_id=8 - Retrieve all quotes in a specific category by category ID
POST /api/quotes/ - Create a new quote (requires quote, author_id, and category_id in the request body)
PUT /api/quotes/ - Update an existing quote (requires id, quote, author_id, and category_id in the request body)
DELETE /api/quotes/ - Delete a quote (requires id in the request body)
Authors
GET /api/authors/ - Retrieve all authors
GET /api/authors/?id=5 - Retrieve a specific author by ID
POST /api/authors/ - Create a new author (requires author in the request body)
PUT /api/authors/ - Update an existing author (requires id and author in the request body)
DELETE /api/authors/ - Delete an author (requires id in the request body)
Categories
GET /api/categories/ - Retrieve all categories
GET /api/categories/?id=7 - Retrieve a specific category by ID
POST /api/categories/ - Create a new category (requires category in the request body)
PUT /api/categories/ - Update an existing category (requires id and category in the request body)
DELETE /api/categories/ - Delete a category (requires id in the request body)
Running the Tests
Explain how to run the automated tests for this system (if applicable).

Testing
Step 1: Start Your Local Server
Open your server control panel (e.g., XAMPP, WAMP, MAMP, or LAMP).
Start the Apache and MySQL services. Ensure MySQL is running if your API interacts with a database.
Check that the server is running by navigating to http://localhost in your web browser. You should see the default server page.
Step 2: Import or Set Up Your Database
Open phpMyAdmin or your preferred MySQL management tool.
Create a new database and import any .sql file provided with your API, if applicable.
Step 3: Ensure Your API Is Placed Correctly
Make sure your API's project folder (api in this case) is placed in the correct directory of your local server (e.g., htdocs for XAMPP).
Step 4: Open Postman
If you haven't installed Postman yet, download it from the official Postman website and install it.
Open Postman after installation.
Step 5: Create a New Request in Postman
Click the "New" button in the upper-left corner, then select "Request".
Give your request a name, choose or create a collection, and then click "Save to".
Step 6: Configure Your Request
Select the HTTP method you want to test (GET, POST, PUT, DELETE) from the dropdown next to the URL field.
Enter the URL of your API endpoint you wish to test. For a local server, it will usually start with http://localhost/. For example, to fetch all quotes, the URL might be http://localhost/api/quotes/.
Step 7: Add Headers (If Required)
Some requests, especially POST or PUT, might require you to set headers. Common headers include Content-Type: application/json for JSON payloads.
Go to the "Headers" tab and add any required headers.
Step 8: Add Request Body (For POST and PUT Requests)
Go to the "Body" tab.
Select "raw" and then choose "JSON" from the dropdown.
Enter your JSON data in the text field.
Step 9: Send the Request and Analyze the Response
Click the "Send" button. Postman will execute the request to your API and display the response.
Review the Status, Time, and the Body of the response. Check if the response data and status codes are as expected based on your API's functionality.
Step 10: Iterating Over Different Endpoints
Repeat the steps for different endpoints (e.g., creating a new quote, updating a quote, deleting a quote) by changing the HTTP method, updating the URL, modifying the headers if necessary, and adjusting the request body for each specific action.

Built With
PHP - The server-side scripting language used
MySQL - The relational database management system used"# Backend_MIdterm" 
