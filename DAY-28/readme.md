## MERN STACK  
# DAY-28
### 27 July 2026  
# ParkEasy - Parking Management System



# SIGNUP PAGE DEVELOPMENT

## Overview

The Signup Page is developed as a user registration module for the ParkEasy parking management system.

It allows new users to create an account and register themselves into the application. The Signup functionality is developed using React.js with React Hooks for managing user input data.

---

## Technologies Used

### Frontend
- React.js
- React Router DOM
- JavaScript
- CSS3

### Backend
- Node.js
- Express.js

### Database
- MongoDB

---

## Signup Page Features

### User Registration

- The Signup Page allows new users to create an account.
- User registration details are collected through a registration form.
- The user information is sent to the backend for storing in the database.

### React Hook Used

`useState()`

- Used to manage user input values.
- Stores registration details such as:
  - Name
  - Email
  - Password
  - Role

---

## Signup Form

The Signup Page collects the following user information:

1. Full Name
2. Email Address
3. Password
4. User Role

The role selection allows users to register as:

1. User
2. Admin

When the user clicks the Sign Up button, the `handleSignup()` function is executed.

The entered user details are sent to the backend server using the Fetch API.

The signup request is made using a POST method:
```
http://localhost:5000/signup
```



The registration data is sent in JSON format:

```json
{
  "name": "user name",
  "email": "user email",
  "password": "user password",
  "role": "user role"
}
```

**NAME: ADITI TANGRI**
**URN : 2302460**
**CRN: 2315004**
