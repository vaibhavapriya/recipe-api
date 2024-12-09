# Recipes App

A full-featured CRUD application for managing recipes, built with Node.js, Express.js, and Mongoose. This app follows the MVC architecture and includes API documentation via Postman.

---
### **Link to Postman Documentation**
[Recipes API Documentation](https://elements.getpostman.com/redirect?entityId=40143357-bb9b3a84-9f0b-462a-9d68-7ec8bbf6a634&entityType=collection)


### **Link to Deployment**
[Recipes API ](https://recipe-api-61jq.onrender.com/api/recipes)

---

## **Features**
- **Create a Recipe**: Add a new recipe with ingredients and instructions.
- **Retrieve Recipes**: Fetch all recipes or a specific recipe by ID.
- **Update a Recipe**: Modify existing recipes.
- **Delete a Recipe**: Remove unwanted recipes.

---

## **Tech Stack**
- **Backend**: Node.js, Express.js
- **Database**: MongoDB (via Mongoose)
- **API Testing and Documentation**: Postman

---

## **Project Structure**
```plaintext
├── controllers
│   └── recipeController.js   # Handles recipe-related logic
├── models
│   └── recipe.js             # Mongoose schema for recipes
├── routes
│   └── recipeRoutes.js       # Routes for recipes
├── views                     # Placeholder for potential UI rendering
├── server.js                 # Main application file
├── .env                      # Environment variables (not included in repo)
├── README.md                 # Project documentation
└── package.json              # Project metadata and dependencies
```

---

## **Setup Instructions**

### **1. Prerequisites**
- Install Node.js (v16 or higher recommended).
- Have a MongoDB Atlas account or local MongoDB instance ready.

### **2. Clone the Repository**
```bash
git clone <repository-url>
cd recipe-api
```

### **3. Install Dependencies**
```bash
npm install
```

### **4. Configure Environment Variables**
Create a `.env` file in the root directory and add:
```
MONGO_URI=<your-mongodb-connection-string>
PORT=5000
```

### **5. Start the Server**
```bash
node server.js
```
The server will run at `http://localhost:5000`.

---

## **API Endpoints**
| Method | Endpoint         | Description                     |
|--------|------------------|---------------------------------|
| POST   | /api/recipes     | Create a new recipe            |
| GET    | /api/recipes     | Retrieve all recipes           |
| GET    | /api/recipes/:id | Retrieve a recipe by ID        |
| PUT    | /api/recipes/:id | Update a recipe by ID          |
| DELETE | /api/recipes/:id | Delete a recipe by ID          |

---

## **Postman Documentation**
### **How to Use the Postman Documentation**
1. Open the provided Postman documentation link.
2. Explore each endpoint in the collection.
3. Follow the examples to test the API.

## **Deployment**
The api is deployed in render.com

## **Sample Request and Response**

### **Create Recipe**
- **Method**: POST  
- **Endpoint**: `/api/recipes`  
- **Request Body**:
  ```json
  {
      "title": "Vanilla Cake",
      "ingredients": ["Flour", "Vanilla Extract", "Sugar", "Eggs", "Butter"],
      "instructions": "Preheat oven to 350°F. Mix ingredients. Bake for 25 minutes."
  }
  ```
- **Response**:
  ```json
  {
      "message": "Recipe created successfully",
      "recipe": {
          "_id": "64f21e857e583b002c6fca1e",
          "title": "Vanilla Cake",
          "ingredients": ["Flour", "Vanilla Extract", "Sugar", "Eggs", "Butter"],
          "instructions": "Preheat oven to 350°F. Mix ingredients. Bake for 25 minutes."
      }
  }
  ```


