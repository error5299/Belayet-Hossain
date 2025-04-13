# User Management API

This is a simple User Management API built with ASP.NET Core. It provides CRUD (Create, Read, Update, Delete) operations to manage users. The API allows you to create, update, retrieve, and delete users.

## Features

- _GET_ /api/users: Retrieve a list of all users.
- _GET_ /api/users/{id}: Retrieve a specific user by ID.
- _POST_ /api/users: Create a new user.
- _PUT_ /api/users/{id}: Update an existing user's details.
- _DELETE_ /api/users/{id}: Delete a user and return the remaining list of users.

## Technologies Used

- _ASP.NET Core 9_: For building the API.
- _C#_: For the implementation of business logic.
- _In-memory storage_: User data is stored in a static list for simplicity.

## Prerequisites

Before running the project, make sure you have the following installed:

- [.NET SDK](https://dotnet.microsoft.com/download/dotnet) (5.0 or higher)
- [Visual Studio Code](https://code.visualstudio.com/) (or any other IDE for C# development)
- [Postman](https://www.postman.com/) (or any API testing tool)

## Setup Instructions

1. Clone this repository:

   ```bash
   git clone https://github.com/rutvii126/user-management-api.git

   ```

2. Navigate to the project directory:

bash cd user-management-api

3. Restore the project dependencies:

bash dotnet restore

4. Build the project:

bash dotnet build

5. Run the project:

bash dotnet run

6. The API should now be running locally at http://localhost:5043

API Endpoints

1. Get all users
   URL: /api/users

   Method: GET

   Response:
   [
      {
      "id": 1,
      "name": "John Doe",
      "email": "john@example.com",
      "password": "password123"
      },
      {
      "id": 2,
      "name": "Jane Smith",
      "email": "jane@example.com",
      "password": "password321"
      }
   ] 
2. Get user by ID
   URL: /api/users/{id}

   Method: GET

   Response:
      {
      "id": 1,
      "name": "John Doe",
      "email": "john@example.com",
      "password": "password123"
      }

3. Create a new user
   URL: /api/users

   Method: POST

   Request Body:

   {
   "name": "Alice Cooper",
   "email": "alice@example.com",
   "password": "password789"
   }

   Response:

   {
   "id": 3,
   "name": "Alice Cooper",
   "email": "alice@example.com",
   "password": "password789"
   } 

4. Update a user
   URL: /api/users/{id}

   Method: PUT

   Request Body:

   {
   "name": "Updated Name",
   "email": "updated.email@example.com",
   "password": "newpassword123"
   }


   Response: 
   {
   "id": 1,
   "name": "Updated Name",
   "email": "updated.email@example.com",
   "password": "newpassword123"
   }


5. Delete a user
   URL: /api/users/{id}

   Method: DELETE

   Response: Updated list of users after deletion.
   [
   {
   "id": 2,
   "name": "Jane Smith",
   "email": "jane@example.com",
   "password": "password321"
   },
   {
   "id": 3,
   "name": "Alice Cooper",
   "email": "alice@example.com",
   "password": "password789"
   }
   ]
