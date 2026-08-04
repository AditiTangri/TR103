
# MERN STACK
# DAY-29
## Date: 28 July 2026

# Project: PARKEASY - Parking Management System

## User Schema Development

The **User Schema** is created using **Mongoose** to define the structure of user data stored in the MongoDB database.

## Purpose

- The User Schema is used to store user information required for authentication and parking management operations.
- It provides a structured format for storing user-related data in MongoDB.
- The schema defines the fields and data types required for user documents.

---

# User Schema Fields

The User Schema contains the following fields:

## 1. Name
- Stores the user's full name.

## 2. Email
- Stores the user's email address.
- The email field is unique to prevent duplicate user accounts.

## 3. Password
- Stores the user's password for authentication.

## 4. Role
- Stores the type of user.
- Available roles:
  - User
  - Admin

## 5. Vehicle Details

Stores vehicle information associated with the user.

### Vehicle Information Includes:

- Vehicle Number
- Vehicle Type

## 6. Bookings Array

Stores parking booking details of the user.

### Booking Information Includes:

- Slot Number
- Vehicle
- Booking Date
- Start Time
- End Time
- Booking Status
- Entry Time
- Exit Time
- Parking Status
- Parking Duration

Default values are provided for fields such as:

- Booking Status
- Entry Time
- Exit Time
- Parking Status

---

# Working

1. The `mongoose.Schema()` function is used to create the structure of user documents.

2. User details such as:
   - Name
   - Email
   - Password
   - Role
   
   are defined inside the schema.

3. Vehicle information is stored as an embedded object within the user document.

4. Parking booking details are stored as an array of objects inside each user document.

5. The schema structure is used to create and manage user data in MongoDB.

6. User data is used by authentication and parking management APIs for:
   - User registration
   - User login
   - Vehicle management
   - Parking booking operations

---
**NAME : ADITI TANGRI**

**URN: 2302460**
**CRN: 2315004**
