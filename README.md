# Authentication API

This is a simple authentication API built with Node.js, Express, MongoDB, and JWT. It provides user signup, login, and user detail retrieval functionality with protected routes using JWT tokens.

## Features

- User signup
- User login
- Retrieve user details (protected route)
- JWT-based authentication
- Password hashing with bcrypt

## Prerequisites

- Node.js installed
- MongoDB installed and running
- Thunder Client (or any API testing tool like Postman)

## Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/rameshvellani/auth-api.git
cd auth-api


Install Dependencies
npm install


3. Set Up Environment Variables
Create a .env file in the root directory of the project with the following content:
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
PORT=5000

Replace your_mongodb_connection_string with your actual MongoDB connection string and your_jwt_secret with a secure secret key for JWT signing.

4. Start the Server
node server.js

This will start the server on the port specified in the .env file (default is 5000).

API Endpoints
Signup
URL: /api/auth/signup
Method: POST
Body: JSON
{
  "name": "ram",
  "email": "ram@example.com",
  "password": "password123"
}

Response
{
  "token": "your_jwt_token"
}


Login
URL: /api/auth/login
Method: POST
Body: JSON
{
  "email": "ram@example.com",
  "password": "password123"
}

response
{
  "token": "your_jwt_token"
}



Get User Details (Protected Route)
URL: /api/auth/user
Method: GET
Headers:
x-auth-token: your_jwt_token
{
  "_id": "user_id",
  "name": "ram",
  "email": "ram@example.com"
}



Testing with Thunder Client
Signup:

Set method to POST and URL to http://localhost:5000/api/auth/signup.
Set body to
{
  "name": "ram",
  "email": "ram@example.com",
  "password": "password123"
}

Send the request. You should receive a response with a JWT token.


Login:

Set method to POST and URL to http://localhost:5000/api/auth/login.
Set body to:
{
  "email": "ram@example.com",
  "password": "password123"
}

Send the request. You should receive a response with a JWT token.


Get User Details:
Set method to GET and URL to http://localhost:5000/api/auth/me.
Set header x-auth-token to the JWT token received from the login response.
Send the request. You should receive a response with the user details.


summary:

