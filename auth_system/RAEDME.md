# User Authentication and Authorization System

This project is a Django-based user authentication and authorization system that uses JWT for authentication.

## Table of Contents
- [Features](#features)
- [Setup Instructions](#setup-instructions)
- [Usage](#usage)
- [Endpoints](#endpoints)
- [Testing](#testing)

## Features
- User registration
- User login with JWT authentication
- Token refresh
- User detail retrieval

## Setup Instructions

1. **Create and activate a virtual environment:**
    
    python -m venv venv
    venv\Scripts\activate  
    # On macOS/Linux
    source venv/bin/activate
    

2. **Install dependencies:**
    pip install -r requirements.txt

3. **Create a `.env` file and add the following variables:**
    SECRET_KEY=your-secret-key
    DEBUG=True
    ALLOWED_HOSTS=localhost,127.0.0.1

4. **Run migrations:**
    python manage.py migrate

5. **Create a superuser:**
    python manage.py createsuperuser

6. **Run the server:**
    python manage.py runserver
    

## Usage

### Register a new user
Send a POST request to `/api/register/` with the following data:
```json
{
  "email": "user@example.com",
  "username": "username",
  "password": "password"
}
