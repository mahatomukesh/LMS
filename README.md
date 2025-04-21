# Library Management System

A full-stack web application for managing a library's books, users, and borrowing system.

## Features

- **User Authentication**
  - User & Admin signup with email verification
  - Secure login with JWT authentication
  - Password recovery

- **Book Management**
  - Browse books with pagination
  - Filter books by category
  - View featured and recent books
  - Book recommendation system
  - Request books

- **Admin Dashboard**
  - Manage books (add, update, delete)
  - Track user borrowing history
  - Process book requests
  - Automated fine charging for late returns

## Tech Stack

### Frontend
- React.js
- Bootstrap
- Axios for API requests

### Backend
- Node.js
- Express.js
- MongoDB for database
- JWT for authentication

## Installation

### Prerequisites
- Node.js
- MongoDB

### Setup
1. Clone the repository
   ```
   git clone <repository-url>
   cd Library_Management_System-main
   ```

2. Install backend dependencies
   ```
   cd backend
   npm install
   ```

3. Install frontend dependencies
   ```
   cd ../frontend
   npm install
   ```

4. Create a `.env` file in the backend directory with the following variables:
   ```
   CONNECTION_URL=<your-mongodb-connection-string>
   CONNECTION_PORT=5000
   JWT_SECRET=<your-jwt-secret>
   ```

5. Build the frontend
   ```
   npm run build
   ```

6. Start the application
   ```
   cd ../backend
   node app.js
   ```

7. Access the application at `http://localhost:5000`

## Deployment to Render

1. Create a new Web Service on Render
2. Link your GitHub repository
3. Configure the following settings:
   - **Build Command:** `cd backend && npm install && cd ../frontend && npm install && npm run build`
   - **Start Command:** `cd backend && node app.js`
4. Add environment variables in the Render dashboard

## API Endpoints

- **Authentication**
  - `/api/v1/signup` - Register a new user
  - `/api/v1/login` - Login
  - `/api/v1/forgotpassword` - Password recovery

- **Books**
  - `/api/v1/books` - CRUD operations for books
  - `/api/v1/recentBooks` - Get recently added books
  - `/api/v1/featuredBooks` - Get featured books
  - `/api/v1/recommendedBooks` - Get book recommendations

- **Users**
  - `/api/v1/users` - User management

## Project Structure

- **backend/** - Server-side code
  - **controller/** - API route handlers
  - **middleware/** - Authentication and error handling
  - **routes/** - API route definitions
  - **database/** - Database connection
  - **uploads/** - Uploaded files

- **frontend/** - Client-side code
  - **src/** - React application source
    - **CLIENT/** - User-facing components
    - **ADMIN/** - Admin dashboard components

## License

[MIT License](LICENSE) 