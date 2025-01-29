# Recipes App

## Overview
The **Recipes App** is a CRUD application designed to manage recipes. It is built using Node.js, Express.js, and Mongoose, following the MVC (Model-View-Controller) architectural pattern. The app includes comprehensive API documentation created with Postman, enabling developers to easily understand and test the application endpoints.

##
GET METHOD
![GET method](https://github.com/user-attachments/assets/ccda1563-586d-4fbc-92e1-fba874018cd5)
![GET method mdb](https://github.com/user-attachments/assets/ac3a26d7-c64e-4488-b9c9-3464524a398a)

POST METHOD
![POST method](https://github.com/user-attachments/assets/5580e6f5-c581-44dd-8918-45bf0083617e)
![POST method mdb](https://github.com/user-attachments/assets/de53ecc6-ae4e-4516-9e40-1e8f7e842420)

PUT METHOD
![PUT method](https://github.com/user-attachments/assets/31b4697e-70c2-4776-bade-50891065066e)
![PUT method mdb](https://github.com/user-attachments/assets/55c06c51-efe7-4a04-952c-7d90111d30eb)

DELETE METHOD
![DELETE method](https://github.com/user-attachments/assets/df9d30d7-6af3-4352-915e-b7b748eb1ce4)
![DELETE method mdb](https://github.com/user-attachments/assets/0ad5e05f-a02c-4229-a98c-e39916b05e11)

GET BY ID METHOD
![GET by id](https://github.com/user-attachments/assets/273b332c-72a3-42f9-bcf9-95cb3696be4c)

## Features
The application provides the following functionalities:

- **Create a Recipe:** Add a new recipe to the database.
- **Retrieve All Recipes:** Fetch a list of all available recipes.
- **Retrieve a Recipe by ID:** Get detailed information about a specific recipe by its unique ID.
- **Update a Recipe:** Modify an existing recipe by its ID.
- **Delete a Recipe:** Remove a recipe from the database by its ID.

## Tech Stack
- **Backend:** Node.js
- **Framework:** Express.js
- **Database:** MongoDB (integrated with Mongoose)
- **API Documentation:** Postman

## Project Structure
The project follows the MVC pattern, with the following directory structure:
```
.
├── models
│   └── recipeModel.js      # Defines the Recipe schema and model
├── controllers
│   └── recipeController.js # Contains the logic for handling CRUD operations
├── routes
│   └── recipeRoutes.js     # Defines API routes
├── config
│   └── database.js         # MongoDB connection setup
├── app.js                  # Main entry point of the application
└── README.md               # Project documentation
```

## Installation
1. Clone the repository:
   ```bash
   git clone <repository-url>
   ```

2. Navigate to the project directory:
   ```bash
   cd recipes-app
   ```

3. Install dependencies:
   ```bash
   npm install
   ```

4. Set up environment variables:
   Create a `.env` file in the root directory and add the following:
   ```env
   MONGO_URI=your_mongodb_connection_string
   PORT=your_preferred_port
   ```

5. Start the application:
   ```bash
   npm start
   ```

6. Access the application at `http://localhost:<PORT>`.

## API Endpoints
### Base URL: `http://localhost:<PORT>/api/recipes`

1. **Create a Recipe**
   - **Method:** POST
   - **Endpoint:** `/`
   - **Request Body:**
     ```json
     {
       "title": "Recipe Title",
       "ingredients": ["ingredient1", "ingredient2"],
       "instructions": "Step-by-step instructions"
     }
     ```
   - **Response:**
     ```json
     {
       "message": "Recipe created successfully",
       "data": { /* Recipe object */ }
     }
     ```

2. **Retrieve All Recipes**
   - **Method:** GET
   - **Endpoint:** `/`
   - **Response:**
     ```json
     [
       { /* Recipe object 1 */ },
       { /* Recipe object 2 */ }
     ]
     ```

3. **Retrieve a Recipe by ID**
   - **Method:** GET
   - **Endpoint:** `/:id`
   - **Response:**
     ```json
     { /* Recipe object */ }
     ```

4. **Update a Recipe**
   - **Method:** PUT
   - **Endpoint:** `/:id`
   - **Request Body:**
     ```json
     {
       "title": "Updated Recipe Title",
       "ingredients": ["updated ingredient1"],
       "instructions": "Updated instructions"
     }
     ```
   - **Response:**
     ```json
     {
       "message": "Recipe updated successfully",
       "data": { /* Updated Recipe object */ }
     }
     ```

5. **Delete a Recipe**
   - **Method:** DELETE
   - **Endpoint:** `/:id`
   - **Response:**
     ```json
     {
       "message": "Recipe deleted successfully"
     }
     ```

## Error Handling
- Proper error messages are returned for invalid requests, such as:
  - Missing fields in the request body.
  - Invalid recipe ID.
  - Non-existent resources.

## Postman Documentation
- The API endpoints, along with sample requests and responses, are documented in a Postman collection.
- Import the collection from the following file: `postman-collection.json`.

## Contribution
Contributions are welcome! Follow these steps:
1. Fork the repository.
2. Create a new branch:
   ```bash
   git checkout -b feature-branch-name
   ```
3. Commit your changes:
   ```bash
   git commit -m "Add your message here"
   ```
4. Push to the branch:
   ```bash
   git push origin feature-branch-name
   ```
5. Create a pull request.

## License
This project is licensed under the MIT License.
