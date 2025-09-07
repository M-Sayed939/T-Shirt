# T-Shirt Store API

This repository hosts the official backend service for the T-Shirt Store Web application. The primary function of this API is to manage users, products, and orders, providing a complete set of RESTful endpoints for the client-side application.

This codebase is a refactored and organized version of an earlier project, focusing on improved structure, maintainability, and performance.

**Original Repository:** 
The original source code and its contribution history can be found at the following repository:[Back Source](https://github.com/M-Sayed939/back-source.git)

-----

## Table of Contents

1.  [Core Features](https://www.google.com/search?q=%23core-features)
2.  [Technology Stack](https://www.google.com/search?q=%23technology-stack)
3.  [Project Setup](https://www.google.com/search?q=%23project-setup)
4.  [API Endpoints](https://www.google.com/search?q=%23api-endpoints)
5.  [Contributors](https://www.google.com/search?q=%23contributors)

-----

## Core Features

  - **User Authentication**: Secure user registration and login using JSON Web Tokens (JWT).
  - **Product Management**: CRUD (Create, Read, Update, Delete) operations for t-shirt products.
  - **Order Processing**: API endpoints for creating and managing customer orders.
  - **Secure & Robust**: Implements security best practices using Helmet.js and password hashing with bcrypt.

## Technology Stack

  - **Runtime Environment**: Node.js
  - **Framework**: Express.js
  - **Database**: MongoDB with Mongoose ODM
  - **Authentication**: Passport.js (passport-jwt strategy)
  - **Middleware**: CORS, Helmet, Morgan (for logging)

-----

## Project Setup

To get a local instance of the server running, please follow the steps below.

### Prerequisites

  - [Node.js](https://nodejs.org/) (v14 or newer recommended)
  - npm (Node Package Manager)
  - A running MongoDB instance (local or cloud-based)

### Installation Steps

1.  **Clone the repository:**
    ```sh
    git clone https://github.com/M-Sayed939/T-Shirt.git
    ```
2.  **Navigate into the project directory:**
    ```sh
    cd server
    ```
3.  **Install project dependencies:**
    ```sh
    npm install
    ```
4.  **Configure Environment Variables:**
    Create a `.env` file in the project's root directory and add the following variables:
    ```
    # The connection URI for your MongoDB database
    MONGO_URI=your_mongodb_connection_string

    # A secret key for signing JSON Web Tokens
    JWT_SECRET=your_strong_jwt_secret
    ```

### Running the Server

To start the server in development mode with automatic reloading via `nodemon`, run:

```sh
npm run dev
```

The API will be available at the configured port (e.g., `http://localhost:5000`).

-----

## API Endpoints

The following are the primary endpoints exposed by the API.

### Authentication

| Method | Endpoint              | Description                    |
| :----- | :-------------------- | :----------------------------- |
| `POST` | `/api/users/register` | Registers a new user.          |
| `POST` | `/api/users/login`    | Logs in a user, returns a JWT. |

### Products

| Method | Endpoint              | Description                           | Access  |
| :----- | :-------------------- | :------------------------------------ | :------ |
| `GET`  | `/api/products`       | Retrieves a list of all products.     | Public  |
| `GET`  | `/api/products/:id`   | Retrieves a single product by its ID. | Public  |
| `POST` | `/api/products`       | Creates a new product.                | Private |
| `PUT`  | `/api/products/:id`   | Updates an existing product.          | Private |
| `DELETE`| `/api/products/:id`  | Deletes a product.                    | Private |

### Orders

| Method | Endpoint         | Description                         | Access  |
| :----- | :--------------- | :---------------------------------- | :------ |
| `POST` | `/api/orders`    | Creates a new order for the user.   | Private |
| `GET`  | `/api/orders/my` | Retrieves all orders for the user.  | Private |
| `GET`  | `/api/orders/:id`| Retrieves a specific order by ID.   | Private |

-----

## Contributors

This project was developed by the following team. Individual contributions can be viewed in the original repository.

  * Mohamed Sayed Fahim
  * Alaa Khaled Kamal El-Din
  * Mohamed Sayed Mohamed
