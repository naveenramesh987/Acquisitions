# Acquisitions

A robust backend API for managing corporate or asset acquisitions, featuring high-end security, automated workflows, and database management.

## 📖 Overview

This project is a scalable Node.js backend service built with **Express 5** and **Drizzle ORM**. It is designed to handle user authentication and data management with a focus on security and developer experience. The system integrates Arcjet for security shielding and uses Neon/PostgreSQL for reliable data storage.

The architecture follows a clean separation of concerns with dedicated layers for routes, controllers, services, and models, ensuring the codebase remains maintainable as the project grows.

## ✨ Key Features

* **Secure Authentication**: Implements JWT-based authentication with secure cookie handling.
* **Database Management**: Uses Drizzle ORM for type-safe database queries and automated migrations.
* **Security Shield**: Integrated with Arcjet and Helmet to protect against common web vulnerabilities and rate-limiting.
* **Docker Ready**: Includes dedicated configurations for both development and production environments using Docker Compose.
* **Modern Tooling**: Leverages ESLint for code quality, Prettier for formatting, and Jest for comprehensive testing.

## 🛠️ Tech Stack

* **Runtime**: Node.js (ES Modules).
* **Framework**: Express.js 5.
* **Database**: PostgreSQL (via Neon) & Drizzle ORM.
* **Security**: Arcjet, Helmet, Bcrypt, and JSON Web Tokens (JWT).
* **Validation**: Zod for schema-based validation.
* **Logging**: Winston & Morgan for structured application logging.

## 🚀 Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/naveenramesh987/Acquisitions.git
   cd Acquisitions
   ```

2. **Install the required dependencies:**

   ```bash
   npm install
   ```

3. **Environment Setup:**

   Create a `.env` file in the root directory and add your database URL, JWT secret, and Arcjet key:

   ```env
   DATABASE_URL=your_postgresql_url
   ARCJET_KEY=your_arcjet_key
   JWT_SECRET=your_secret_key
   ```

## 📊 Database Management

The project uses Drizzle Kit to manage schema changes:

1. **Generate Migrations:**

   ```bash
   npm run db:generate
   ```

2. **Push Migrations to Database:**

   ```bash
   npm run db:migrate
   ```

3. **Explore Data (Studio):**

   ```bash
   npm run db:studio
   ```

## 🖥️ Usage

### Local Development

To run the server with hot-reloading:

```bash
npm run dev
```

### Docker Execution

To run the entire stack (App + DB) using Docker:

```bash
# Development mode
npm run dev:docker

# Production mode
npm run prod:docker
```

## 🧪 Testing

To run the test suite:

```bash
npm test
```

## 🛣️ API Endpoints

* `GET /health`: Check system status and uptime.
* `POST /api/auth/register`: User registration.
* `POST /api/auth/login`: User login.
* `GET /api/users/profile`: Retrieve authenticated user profile.
