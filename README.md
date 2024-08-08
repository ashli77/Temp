# Online Bookstore

This project is an online bookstore system that allows customers to browse books, make purchases, and leave reviews. The system also includes functionality for authors, publishers, and orders.

## Table of Contents

- [Features](#features)
- [Tech Stack](#tech-stack)
- [Setup](#setup)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Running the Application](#running-the-application)
- [API Endpoints](#api-endpoints)
- [Testing](#testing)
  - [Running Unit Tests](#running-unit-tests)
  - [Running Integration Tests](#running-integration-tests)
- [Project Structure](#project-structure)
- [License](#license)

## Features

- Manage authors, publishers, customers, books, reviews, and orders.
- CRUD operations for all entities.
- Containerized with Docker.
- Unit and integration tests using Jest and Supertest.

## Tech Stack

- **Backend**: Node.js, Express
- **Database**: PostgreSQL
- **ORM**: TypeORM
- **Language**: TypeScript
- **Testing**: Jest, Supertest
- **Containerization**: Docker, Docker Compose

## Setup

### Prerequisites

- [Node.js](https://nodejs.org/en/) (v14 or higher)
- [Docker](https://www.docker.com/get-started)
- [Docker Compose](https://docs.docker.com/compose/)

### Installation

1. **Navigate to the project directory**:
   ```sh
   cd /path/to/your/project
Install dependencies:

sh
Copy code
npm install
Create a ormconfig.json file in the root directory with the following content:

json
Copy code
{
  "type": "postgres",
  "host": "db",
  "port": 5432,
  "username": "postgres",
  "password": "postgres",
  "database": "online_bookstore",
  "synchronize": true,
  "logging": false,
  "entities": ["src/entity/**/*.ts"],
  "migrations": ["src/migration/**/*.ts"],
  "subscribers": ["src/subscriber/**/*.ts"],
  "cli": {
    "entitiesDir": "src/entity",
    "migrationsDir": "src/migration",
    "subscribersDir": "src/subscriber"
  }
}
Running the Application
Build and start the containers:

sh
Copy code
docker-compose up --build
Access the application: The server will be running at http://localhost:3000.

API Endpoints
Authors
POST /authors: Create a new author.
GET /authors/:id: Get an author by ID.
PUT /authors/:id: Update an author by ID.
DELETE /authors/:id: Delete an author by ID.
Publishers
POST /publishers: Create a new publisher.
GET /publishers/:id: Get a publisher by ID.
PUT /publishers/:id: Update a publisher by ID.
DELETE /publishers/:id: Delete a publisher by ID.
Customers
POST /customers: Create a new customer.
GET /customers/:id: Get a customer by ID.
PUT /customers/:id: Update a customer by ID.
DELETE /customers/:id: Delete a customer by ID.
Books
POST /books: Create a new book.
GET /books/:id: Get a book by ID.
PUT /books/:id: Update a book by ID.
DELETE /books/:id: Delete a book by ID.
Reviews
POST /reviews: Create a new review.
GET /reviews/:id: Get a review by ID.
PUT /reviews/:id: Update a review by ID.
DELETE /reviews/:id: Delete a review by ID.
Orders
POST /orders: Create a new order.
GET /orders/:id: Get an order by ID.
PUT /orders/:id: Update an order by ID.
DELETE /orders/:id: Delete an order by ID.
Testing
Running Unit Tests
Unit tests are located in the src/service/__tests__ directory. To run unit tests:

sh
Copy code
npm test
Running Integration Tests
Integration tests are also located in the src/service/__tests__ directory. To run integration tests:

sh
Copy code
npm test
