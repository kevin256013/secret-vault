# **Secret Vault**
<br/>

## Overview

Secret Vault is a web application that allows users to submit and view secrets anonymously. It uses user authentication and authorization with both local and Google OAuth login. Users can register, log in, and submit their personal secrets, which are stored in a PostgreSQL database.

## Features

User Registration and Login: Users can create an account or log in using Google OAuth or local authentication.

Secrets Submission: After logging in, users can submit their secrets, which are then stored in a PostgreSQL database.

Secret Viewing: Authenticated users can view their secrets.

## Tech Stack

Frontend: HTML, CSS, and EJS (Embedded JavaScript Templates)

Node.js - JavaScript runtime for building scalable applications.

Express - Web framework for Node.js to handle routing and HTTP requests.

PostgreSQL - Relational database for storing users and their secrets.

bcrypt - Library for hashing and comparing passwords.

passport.js - Authentication middleware for Node.js, used for local and Google OAuth login.

Google OAuth2 - Authentication strategy for Google login.

express-session - Middleware for session management.

## Installation & Usage

#### Clone the repository:

git clone https://github.com/kevin256013/secret-vault.git

cd secret-vault

#### Install Dependencies

npm install

#### Set up the PostgreSQL database:

Create a database named secrets or modify the database connection string in index.js to match your environment.

Create a sql table for users with (id, email, password, secret).

#### Create a .env file in the root directory with the following content:

PG_USER=your-postgres-username

PG_HOST=localhost

PG_DATABASE=secret_share

PG_PASSWORD=your-postgres-password

PG_PORT=5432

SESSION_SECRET=your-session-secret

GOOGLE_CLIENT_ID=your-google-client-id

GOOGLE_CLIENT_SECRET=your-google-client-secret

#### Run the Application:

node index.js

#### Visit the Application: 

The application will be available at http://localhost:3000.
