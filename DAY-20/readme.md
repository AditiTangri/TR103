# MERN STACK
### DAY-20
## Date: 17 July 2026

# React

## Fetch API

The Fetch API is a built-in JavaScript method used to request data from a server or API. It is commonly used to perform **GET, POST, PUT, and DELETE** operations.

## Features

- Built into JavaScript (no extra library needed).
- Returns a Promise.
- Supports asynchronous programming with `.then()` or `async/await`.
- Used to communicate with REST APIs.

---

# Fetch API using async/await

`async` and `await` are JavaScript keywords used to handle asynchronous operations (such as fetching data from an API). They make asynchronous code easier to read and write.

### async
- Declares a function as asynchronous.
- An async function always returns a Promise.

### await
- Waits for a Promise to resolve before continuing to the next line of code.
- It can only be used inside an async function.

## Syntax

```javascript
async function functionName() {
  try {
    const response = await fetch("API_URL");
    const data = await response.json();

    console.log(data);
  } catch (error) {
    console.log(error);
  }
}

functionName();
```

---

# TASK-1

## Fetch API Implementation

- Created a React component.
- Used Fetch API to get data from an API.
- Displayed fetched data using React state and mapping.

---

# TASK-2

## Bill Generator

Created a GST Bill Generator using React.

### Features:
- Takes customer name input.
- Takes laptop and accessories price.
- Calculates discount based on total amount.
- Calculates GST (18%).
- Displays final bill amount.

### Calculation Flow

```
Laptop Price + Accessories Price
              ↓
          Apply Discount
              ↓
        Calculate GST (18%)
              ↓
        Display Final Amount
```
**NAME: ADITI TANGRI**

**URN: 2302460**

**CRN: 2315004**

















