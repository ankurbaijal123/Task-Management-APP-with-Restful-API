# Task Management Web Application

## Overview

This Task Management Web Application is a full-stack solution for managing tasks efficiently. It features a React frontend with a responsive design using Tailwind CSS, and a backend API built with Node.js and Express. The application allows users to create, read, update, and delete tasks, as well as manage user authentication.

## Features

- User Authentication (Register, Login, Logout)
- Create, Read, Update, and Delete Tasks
- Responsive Design
- RESTful API
- Persistent Data Storage with MongoDB

## Tech Stack

- Frontend: React, Tailwind CSS
- Backend: Node.js, Express
- Database: MongoDB
- Authentication: JSON Web Tokens (JWT)

## Prerequisites

Before you begin, ensure you have the following installed:
- Node.js (v14 or later)
- npm (v6 or later)
- MongoDB

## Setup and Installation

1. Clone the repository:
   ```
   git clone https://github.com/yourusername/task-management-app.git
   cd task-management-app
   ```

2. Install dependencies:
   ```
   npm install
   cd client
   npm install
   cd ..
   ```

3. Set up environment variables:
   Create a `.env` file in the root directory and add the following:
   ```
   PORT=5000
   MONGODB_URI=your_mongodb_connection_string
   JWT_SECRET=your_jwt_secret
   ```

4. Start the development server:
   ```
   npm run dev
   ```

   This will start both the backend server and the React frontend.

## API Documentation

### Authentication Endpoints

#### Register a new user
- **POST** `/api/auth/register`
- Body: `{ "username": "string", "password": "string" }`

#### Login
- **POST** `/api/auth/login`
- Body: `{ "username": "string", "password": "string" }`

#### Logout
- **POST** `/api/auth/logout`
- Requires Authentication

### Task Endpoints

#### Get all tasks
- **GET** `/api/tasks`
- Requires Authentication

#### Get a single task
- **GET** `/api/tasks/:id`
- Requires Authentication

#### Create a new task
- **POST** `/api/tasks`
- Requires Authentication
- Body: `{ "title": "string", "description": "string", "dueDate": "date" }`

#### Update a task
- **PUT** `/api/tasks/:id`
- Requires Authentication
- Body: `{ "title": "string", "description": "string", "dueDate": "date", "completed": boolean }`

#### Delete a task
- **DELETE** `/api/tasks/:id`
- Requires Authentication

