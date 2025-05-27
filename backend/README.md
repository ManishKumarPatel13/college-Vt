# User Authentication Backend

This is a Node.js Express backend for user authentication using PostgreSQL.

## Features
- Register and login endpoints
- Passwords are hashed using bcryptjs
- JWT-based authentication
- Uses environment variables for secrets and database URL

## Setup
1. Install dependencies:
   ```powershell
   npm install
   ```
2. Create a `.env` file (already provided) and set your database URL and JWT secret.
3. Ensure your PostgreSQL database has a `users` table:
   ```sql
   CREATE TABLE users (
     id SERIAL PRIMARY KEY,
     username VARCHAR(255) UNIQUE NOT NULL,
     password VARCHAR(255) NOT NULL
   );
   ```
4. Start the server:
   ```powershell
   node index.js
   ```

The server will run on port 5000 by default.
