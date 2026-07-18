# MERN Stack
## DAY-21
**Date:** 18 July 2026

# MongoDB

**MongoDB** is a NoSQL, document-oriented database used to store large amounts of data in a flexible format. Unlike traditional relational databases, MongoDB stores data as **BSON (Binary JSON)** documents instead of rows and columns.

## Features of MongoDB

- Document-oriented: Stores data in JSON-like documents.
- Schema-less: Documents in the same collection can have different fields.
- High Performance: Fast read and write operations.
- Scalable: Supports horizontal scaling through sharding.
- High Availability: Replica sets provide automatic failover.
- Indexing: Improves query performance.
- Aggregation Framework: Performs complex data processing and analytics.

---

# MongoDB Installation (Windows)

1. Download **MongoDB Community Server** from the official MongoDB website.
2. Run the installer.
3. Select **Complete Installation**.
4. Choose **Install MongoDB as a Service**.
5. Complete the installation.
6. Install **MongoDB Compass** (optional GUI).
7. Verify installation using:

```bash
mongod --version
```

or

```bash
mongosh
```

---

# MongoDB Backend Setup

A backend application built with **Node.js**, **Express.js**, and **MongoDB** allows you to create APIs that communicate with a database.

---

## Step 1: Create Backend Folder

```bash
mkdir backend
cd backend
```

---

## Step 2: Initialize Node Project

```bash
npm init -y
```

### About npm

- **npm** = Node Package Manager.
- Used to install and manage packages.
- Creates a **package.json** file.

---

## Step 3: Install Required Packages

```bash
npm install express mongoose cors
```

### Package Description

- **Express** – Creates web servers and REST APIs.
- **Mongoose** – Connects Node.js with MongoDB using schemas and models.
- **CORS** – Allows communication between frontend and backend running on different origins.

---

## Step 4: Create `server.js`

```javascript
const mongoose = require("mongoose");
const express = require("express");
const cors = require("cors");

const app = express();

app.use(cors());
app.use(express.json());

app.listen(9000, () => {
    console.log("connected");
});

mongoose.connect("mongodb://127.0.0.1:27017/newcrud")
.then(() => {
    console.log("DB CONNECTED");
})
.catch((err) => {
    console.log(err);
});
```

---

# Code Explanation

### `const mongoose = require("mongoose");`

- Imports the **Mongoose** library.
- Used to connect Node.js with MongoDB and perform database operations.

---

### `const express = require("express");`

- Imports the **Express** framework.
- Used to create the server and REST APIs.

---

### `const cors = require("cors");`

- Imports the **CORS** middleware.
- Allows communication between frontend and backend running on different origins.

---

### `const app = express();`

- Creates an Express application.

---

### `app.use(cors());`

- Enables Cross-Origin Resource Sharing (CORS).

---

### `app.use(express.json());`

- Parses incoming JSON data.
- Makes request data available in `req.body`.

---

### `app.listen(9000, () => { ... });`

- Starts the server on **port 9000**.

---

### `mongoose.connect("mongodb://127.0.0.1:27017/newcrud")`

- Connects the application to the **newcrud** MongoDB database.
- `127.0.0.1` → Localhost.
- `27017` → Default MongoDB port.

---

### `.then(() => { console.log("DB CONNECTED"); })`

- Executes if the database connection is successful.

---

### `.catch((err) => { console.log(err); })`

- Handles database connection errors.

---

# Output

```text
connected
DB CONNECTED
```

---

# Project Structure

```text
backend/
│── node_modules/
│── package.json
│── package-lock.json
└── server.js
```

---

**Name:** ADITI TANGRI

**URN:** 2302460

**CRN:** 2315004
