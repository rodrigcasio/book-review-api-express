# Book Review API (Node.js & Express)

This is a REST API project I built as my final project for the IBM Node.js & Express course on Coursera. It's a book review API that lets users browse books and leave reviews. This was my first time learning Node.js and Express, and I put a lot of time and effort into understanding how to build server-side applications and RESTful APIs.

## What does it do?

- **User Registration & Authentication**: Users can register accounts and log in securely using JWT (JSON Web Tokens).
- **Browse Books**: Public endpoints to view all books, search by ISBN, author, or title.
- **Book Reviews**: Authenticated users can add and delete their own book reviews.
- **Session Management**: Uses Express sessions to keep users logged in securely.
- **Async/Await**: Demonstrates modern JavaScript with Promises, async/await, and Axios for API calls.

## Features

- **Public Endpoints**: Anyone can browse the book catalog and read reviews
  - Get all books
  - Search by ISBN
  - Search by author name
  - Search by book title
  - Get reviews for a specific book

- **Authenticated Endpoints**: Only logged-in users can:
  - Register new accounts
  - Login with username and password
  - Add book reviews
  - Delete their own reviews

- **Book Catalog**: Features 24 books I've read or want to read, including programming books, physics books, and fiction.

## Why did I make this?

I built this as my final project for the IBM Node.js & Express course to demonstrate what I learned about building REST APIs. This project helped me understand:
- How to create RESTful APIs with Express.js
- User authentication with JWT and sessions
- Handling HTTP requests (GET, POST, PUT, DELETE)
- Working with async/await and Promises
- Building server-side applications in JavaScript

## Technologies Used

- **Node.js**: JavaScript runtime for building server applications
- **Express.js**: Web framework for creating APIs
- **JWT (jsonwebtoken)**: For secure user authentication
- **express-session**: For managing user sessions
- **Axios**: For making HTTP requests within the API
- **JavaScript**: Core programming language

## How to Run

1. Make sure you have Node.js installed on your computer.
2. Navigate to the `book-review-api` directory:
   ```
   cd book-review-api
   ```
3. Install dependencies:
   ```
   npm install
   ```
4. Start the server:
   ```
   npm start
   ```
5. The server will run on `http://localhost:5000`

## API Endpoints

### Public Endpoints (No authentication required)

- `GET /` - Get all books
- `GET /isbn/:isbn` - Get book by ISBN number
- `GET /author/:author` - Get book by author name
- `GET /title/:title` - Get book by book title
- `GET /review/:isbn` - Get reviews for a specific book
- `POST /register` - Register a new user

### Authenticated Endpoints (Login required)

- `POST /customer/login` - Login with username and password
- `PUT /customer/auth/review/:isbn` - Add a book review (requires login)
- `DELETE /customer/auth/review/:isbn` - Delete your book review (requires login)

## Example Usage

### Register a new user:
```bash
POST http://localhost:5000/register
Body: { "username": "rodrigo", "password": "password123" }
```

### Login:
```bash
POST http://localhost:5000/customer/login
Body: { "username": "rodrigo", "password": "password123" }
```

### Get all books:
```bash
GET http://localhost:5000/
```

### Add a review:
```bash
PUT http://localhost:5000/customer/auth/review/1?review=Great book!
```

## What I Learned

- How to build RESTful APIs with Express.js
- User authentication and authorization with JWT tokens
- Session management for keeping users logged in
- Handling different HTTP methods (GET, POST, PUT, DELETE)
- Working with async/await and Promises in Node.js
- Making HTTP requests with Axios
- Organizing code with routes and middleware
- Error handling and status codes in APIs

## Author

Rodrigo Casio  
[My GitHub Profile](https://github.com/rodrigcasio)

