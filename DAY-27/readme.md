## MERN STACK  
## DAY-27
### 25 July 2026  

# ParkEasy - Parking Management System



# LOGIN PAGE DEVELOPMENT

## Overview

The Login Page is developed as an authentication module for the ParkEasy parking management system.

It allows registered users to securely access the application by verifying their email and password. The page is developed using React.js with React Hooks for managing user input and navigation.

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

## Login Page Features

### Authentication

- The Login Page provides secure user authentication.
- Users can enter their registered email and password.
- The system verifies user credentials through the backend API.

### React Hooks Used

- `useState()`  
  - Used to manage input values.
  - Handles email and password states.

- `useNavigate()`  
  - Imported from `react-router-dom`.
  - Used to navigate users to different pages after successful login.

---

## Login Form

The Login Form allows existing users to enter:

- Email Address
- Password

The entered user credentials are sent to the backend using the Fetch API.

The login request is made using a POST method:
```
http://localhost:5000/login
```


The user data is sent in JSON format:

```json
{
  "email": "user email",
  "password": "user password"
}
```

After successful authentication, user details are stored in localStorage:

- User Role
- User Name
- User ID
# Working
1. The Login() functional component is created to handle user login functionality.
2. useState() is used to store email and password values entered by the user.
3. The user enters login credentials into the input fields.
4. When the Login button is clicked, the handleLogin() function is executed.
5. The handleLogin() function sends the entered email and password to the backend using a POST request.
6. The backend verifies the user credentials from the database.
7. If authentication is successful, user details are stored in localStorage.
8. The application checks the user role received from the server.
9. Based on the user role, the user is navigated to the respective dashboard.
10. If authentication fails, the system displays an appropriate error message.

---

**NAME : 2302460**

**URN : 2302460**

**CRN : 2315004**
