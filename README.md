# Scalable Production Ready API

## 📌 Overview
This project was built as a hands-on exploration of how modern backend systems work in real-world applications.

Instead of just using frameworks, the focus was on understanding:

- How servers handle requests
- Middleware flow
- Logging and monitoring
- Authentication and security
- Database interaction
- Containerization using Docker
---

## 🎯 Objectives
- Understand backend architecture in a practical way
- Learn how to structure a scalable Node.js application
- Explore production-level tools (logging, validation, security)
- Deploy and run services using Docker

---

## 🛠️ Tech Stack
### Core Backend
- Node.js – runtime for server-side logic
- Express.js – API framework for routing & middleware
###  Logging & Monitoring
- Winston – structured logging system
= Morgan – HTTP request logger (connected to Winston)

👉 Why both?

- Morgan logs incoming HTTP requests
- Winston stores and formats logs for better debugging
### Middleware & Request Handling
- express.json() → parses JSON request bodies
- express.urlencoded() → handles form & nested data
- cookie-parser → parses cookies from client requests

### Security
- Helmet → secures HTTP headers
- CORS → allows cross-origin requests
- Arcjet → rate limiting & bot protection

### Authentication
- JWT (JSON Web Token) → stateless authentication
- bcrypt → password hashing

### Validation
Zod → schema validation

👉 Why Zod?

- Ensures request data is correct
- Gives clean error messages
- Prevents invalid data reaching the database

### Database
- Neon (PostgreSQL) – serverless database
- Drizzle ORM – type-safe database queries

👉 Note:
Drizzle was installed locally due to Windows path-related issues during setup.

### Dev Tools
- ESLint → code linting
- Prettier → code formatting
- Testing
- Jest → unit testing
- Supertest → API endpoint testing
- DevOps
- Docker → containerization

👉 Why Docker?

- Ensures consistent environment
- Makes deployment easier
- Avoids “works on my machine” issues
---
## 🚀 Features
- ✅ REST API with structured routing
- ✅ JWT-based authentication
- ✅ Role-based access control
- ✅ Request validation using Zod
- ✅ Structured logging (Winston + Morgan)
- ✅ PostgreSQL integration (Neon + Drizzle)
- ✅ Security middleware (Helmet, CORS, Arcjet)
- ✅ Dockerized environment
- ✅ Unit & integration testing (Jest + Supertest)

## Project Structure 

```c
src/
│
├── controllers/      # Request handling logic
├── routers/           # API route definitions
├── middleware/       # Custom middleware (auth, validation)
├── services/         # Business logic
├── db/               # Database config & schema (Drizzle)
├── utils/            # Logger, helpers
├── validations/      
├── config/           # Environment configs
└── app.js          # Main app entry

```
🐳 Running with Docker

```c
docker build -t backend-app .
docker run -p 3000:3000 backend-app
```
⚡ Local Setup
```c
git clone <your-repo>
cd <your-project>

npm install
npm run dev
```
Environment Variables
```c
PORT=3000
NODE_ENV=development
DATABASE_URL=
ARCJET_KEY=
JWT_SECRET=
```
Testing
```c
npm test
```

## What I Learned
- How backend systems actually process requests
- Importance of middleware architecture
- Difference between logging vs monitoring
- Secure authentication design
- Validation before database interaction
- Real-world DevOps using Docker


  
