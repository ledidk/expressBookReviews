Project Overview: Scenario and Review Criteria

Project Overview

You will have the chance to practice and put your skills, knowledge, and abilities to use Node.JS & Express.JS by developing Online Book review application in your final project.

FINAL PROJECT SCENARIO

In this project you will assume the role of a back-end developer working for an online retailer selling books. You have been tasked with developing a server-side application that stores, retrieves and manages book ratings and reviews.

Your server-side application is required to provide the following features and capabilities to allow users to:

Retrieve a list of all books available in the bookshop
Search for specific books and retrieve their details based on the book’s ISBN code, author names and titles
Retrieve reviews/comments for specified books
Register as a new user of the application
Login to the application
Add a new review for a book (logged in users only)
Modify a book review (logged in users can modify only their own reviews)
Delete a book review (logged in users can delete only their own reviews)
(Multiple users) Access the application at the same time to view and manage different book reviews simultaneously
As is the case with most software development projects, different people in the team work on different parts of the application. Another front-end developer in your team is working on the web-based client-side application that will communicate with your server-side application using REST. Therefore your job is to implement your server-side application as a RESTful web service. A software architect on your team has written the skeleton code for your server-side application using Node.js and Express.js.

To complete the project you will fork the skeleton code into your own repo, clone it locally into your development environment, and develop the code further to implement the CRUD capabilities listed above as HTTP methods in your Express server and test them using Postman. You will also implement Session and JWT authentication to allow only logged in users to perform certain operations. For your reference, this application comes preloaded with all of the book information.

Furthermore you will need to enhance your code using Promises, Callbacks or Async/Await functions to allow multiple users to interact with the application simultaneously and not have to wait for each other’s operations to complete.

Evaluation Criteria –30 marks total

Please take the particular screenshots for each particular task for your peer review as mentioned in the lab instructions. Your peers who are also completing the course during the same session will grade this project. This project carries 30 points toward your final grade and is weighted as follows:

General users:

Task 1: Get the book list available in the shop.- 2 Points

Task 2: Get the books based on ISBN.- 2 Points

Task 3: Get all books by Author. -2 Points

Task 4: Get all books based on Title - 2 Points

Task 5: Get book Review. - 2 Points

Task 6: Register New user – 3 Points

Task 7: Login as a Registered user - 3 Points

Registered Users:

Task 8: Add/Modify a book review. - 2 Points

Task 9: Delete book review added by that particular user - 2 Points

Node.JS program with 4 methods:

Use Async/Await or Promises with Axios in Node.js for all the four methods.
Task 10: Get all books – Using async callback function – 2 Points

Task 11: Search by ISBN – Using Promises – 2 Points

Task 12: Search by Author – 2 Points

Task 13: Search by Title - 2 Points

Task 14: Submission of Project GitHub Link - 2 Points


Project Breakdown

This final project for this course has several steps that you must complete. To give you an overview of the project, all the high-level steps are listed below. The project is then divided into several tasks that give the detailed instructions for each step. You must complete all the task to successfully complete the project.

Prerequisite: You need to complete the following two labs before starting the final project.

Hands-on Lab - CRUD operations with Node.js.
Practice Project - CRUD operations on Express server with JWT & Session Authentication.
Part A: Fork the Git repository to have the server side book review application code you need to start

Create your own copy of the git repository which has the code you need to start the project.
Clone the repository into the theia environment.
Part B: npm install the necessary packages and Postman Login

Change to the express JS server directory and install all the packages required in your local environment for the server to run.
Use your Google mail credentials to register or log in with Postman and test the API endpoints for your final project.
Part C: Implementing Authentication for using the Book Review application

You will create access restrictions to some endpoints using JWT and session level authentication.
Part D: Access the book review application as general purpose user and register user

General user can access all the books available in the shop and get all books based on ISBN,Author,Title,Review.
Once a user register with the app, they are able to add or modify and delete book reviews.
Part E: Use Async/Await or Promises with Axios in Node.js for each of the four CRUD Operations.

Using the async,callback function, retrieve all books. Using Promises, search for the book by ISBN and then search by author or title.
Now test the API endpoints using Postman.
  
# coding-project-template

Update and test the general user routes in general.js

Note:

Please remember to push your work to the GitHub repository after completing every task or if you're not completing the lab in one session. You can find the steps for pushing the repository to GitHub in Task 14. This will help you avoid losing your progress.

If you encounter difficulties using Postman, you can alternatively use curl commands to test the API endpoints, as demonstrated in Module 3: Hands-on Lab: CRUD Operations with Node.js and Express. Please provide screenshots showing the JSON output of your curl commands in your submission for peer review.

Task 1:

Complete the code for getting the list of books available in the shop under public_users.get('/',function (req, res) {.
Hint: Use the JSON.stringify method for displaying the output neatly.

Run npm install for installing the required modules & start the server.

Test the output on Postman.

Please take a screenshot of the same and save it with the name 1-getallbooks.png for submitting under Task 1 for the Peer Review Assignment.

Task 2:

Complete the code for getting the book details based on ISBN under public_users.get('/isbn/:isbn',function (req, res) {.
Hint: Retrieve the ISBN from the request parameters

Test the output on Postman.

Please take a screenshot of the same and save it with the name 2-gedetailsISBN.png for submitting under Task 2 for the Peer Review Assignment.

Task 3:

Complete the code for getting the book details based on the author under public_users.get('/author/:author',function (req, res) {.
Hints:
1. Obtain all the keys for the ‘books’ object.
2. Iterate through the ‘books’ array & check the author matches the one provided in the request parameters.

Test the output on Postman.

Please take a screenshot of the same and save it with the name 3-getbooksbyauthor.png for submitting under Task 3 for the Peer Review Assignment.

Task 4:

Complete the code for getting the book details based on the title under public_users.get('/title/:title',function (req, res) {.
Hint: This will be similar to Exercise 3

Test the output on Postman.

Please take a screenshot of the same and save it with the name 4-getbooksbytitle.png for submitting under Task 4 for the Peer Review Assignment.

Task 5:

Complete the code for getting book reviews under public_users.get('/review/:isbn',function (req, res) {.
Hint: Get the book reviews based on ISBN provided in the request parameters.

Please take a screenshot of the same and save it with the name 5-getbookreview.png for submitting under Task 5 for the Peer Review Assignment.
Task 6:

Complete the code for registering a new user
Hint: The code should take the ‘username’ and ‘password’ provided in the body of the request for registration. If the username already exists, it must mention the same & must also show other errors like eg. when username &/ password are not provided.

Test the output on Postman.

Please take a screenshot of the same and save it with the name 6-register.png for submitting under Task 6 for the Peer Review Assignment.


Update and test the authenticated user routes in auth_users.js.

Task 7:

Complete the code for logging in as a registered user.
Hint: The code must validate and sign in a customer based on the username and password created in Exercise 6. It must also save the user credentials for the session as a JWT.
As you are required to login as a customer, while testing the output on Postman, use the endpoint as "customer/login"

Test the output on Postman.

Please take a screenshot of the same and save it with the name 7-login.png for submitting under Task 7 for the Peer Review Assignment.

Task 8:

Complete the code for adding or modifying a book review.
Hint: You have to give a review as a request query & it must get posted with the username (stored in the session) posted. If the same user posts a different review on the same ISBN, it should modify the existing review. If another user logs in and posts a review on the same ISBN, it will get added as a different review under the same ISBN.

Test the output on Postman.

Please take a screenshot of the same and save it with the name 8-reviewadded.png for submitting under Task 8 for the Peer Review Assignment.

Task 9:

Complete the code for deleting a book review under regd_users.delete("/auth/review/:isbn", (req, res) => {

Hint: Filter & delete the reviews based on the session username, so that a user can delete only his/her reviews and not other users’.

Test the output on Postman.

Please take a screenshot of the same and save it with the name 9-deletereview.png for submitting under Task 9 for the Peer Review Assignment.

With this you have implemented and tested the codes for the general and authenticated user routes.

Improving the scope of Tasks 1-4 using Promises or Async-Await

You will now use Promise callbacks or Async-Await functions for doing the same functionality which we covered synchronously in Tasks 1-4.

Note: Please take a screenshot of your code implementation using either async/await or Promises for Tasks 10-13. This screenshot will be used for peer review submission.
Task 10:

Add the code for getting the list of books available in the shop (done in Task 1) using Promise callbacks or async-await with Axios.
Hint: Refer to this lab on Promises and Callbacks.

Please ensure that the general.js file has the code for getting the list of books available in the shop using Promise callbacks or async-await with Axios is covered.

Please take a screenshot of the same and save it with the name task10.png for submitting under Task 10 for the Peer Review Assignment.

Task 11:

Add the code for getting the book details based on ISBN (done in Task 2) using Promise callbacks or async-await with Axios.
Hint: Refer to this lab on Promises and Callbacks.

Please ensure that the general.js file has the code for getting the book details based on ISBN using Promise callbacks or async-await with Axios is covered.

Please take a screenshot of the same and save it with the name task11.png for submitting under Task 11 for the Peer Review Assignment.

Task 12:

Add the code for getting the book details based on Author (done in Task 3) using Promise callbacks or async-await with Axios.
Hint: Refer to this lab on Promises and Callbacks.

Please ensure that the general.js file has the code for or getting the book details based on Author using Promise callbacks or async-await with Axios is covered.

Please take a screenshot of the same and save it with the name task12.png for submitting under Task 12 for the Peer Review Assignment.

Task 13:

Add the code for getting the book details based on Title (done in Task 4) using Promise callbacks or async-await with Axios.
Hint: Refer to this lab on Promises and Callbacks.

Please ensure that the general.js file has the code for or getting the book details based on Title using Promise callbacks or async-await with Axios is covered.

Please take a screenshot of the same and save it with the name task13.png for submitting under Task 13 for the Peer Review Assignment.

