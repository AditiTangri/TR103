# MERN Stack
## DAY-25
### Date: 23 July 2026


# Login API

## Description

The Login API authenticates users by verifying their email and password. If the credentials are valid, the API returns a success response along with the user's ID and user type. Otherwise, it returns an appropriate error message.

## Endpoint

```
POST /api/login
```

## Request Body

```json
{
  "mail": "user@example.com",
  "pass": "password123"
}
```

## Working

1. Receives the user's email and password from the client.
2. Searches the database for a user with the given email.
3. If the user exists, compares the entered password with the stored password.
4. If the password matches:
   - Returns `statuscode: 1`
   - Returns a success message
   - Returns the user's `_id`
   - Returns the user's `usertype`
5. If the password is incorrect, returns an "Invalid credentials" message.
6. If the email is not found, returns a "User not found" message.



**NAME: ADITI TANGRI**

**URN: 2302460**

**CRN: 2315004**
