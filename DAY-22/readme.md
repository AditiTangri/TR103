
# MERN STACK
# DAY -22
## Date: 20 July 2026

# MongoDB - POST Method

## Introduction

The **POST method** is an HTTP request method used to send data from the client to the server. It is mainly used for creating new records in a database.

In a MERN stack application, the POST method is commonly used to insert new documents into MongoDB through an Express.js API.


# Parameters

| Parameter | Description |
|-----------|-------------|
| path | URL route where the request is sent |
| callback_function | Function executed when the route receives a POST request |

---

# Request Object (req)

## Definition

The **request object (`req`)** contains information sent by the client to the server.

It is used to access data submitted from frontend applications.

---

# Response Object (res)

## Definition

The **response object (`res`)** is used by the server to send data back to the client.

It sends messages, data, or operation status to the client.

---

# Async and Await

## Definition

`async` and `await` are JavaScript features used to handle asynchronous operations.

`await` pauses execution until database operations are completed.

---

# Mongoose Model

## Definition

A Mongoose Model is an object that provides an interface to communicate with MongoDB collections.

It is created using a schema and is used for database operations.

---

# findOne() Function

## Definition

`findOne()` is a Mongoose method used to search for a single document in MongoDB.

It returns the first matching document from the collection.

---

# save() Function

## Definition

The `save()` method is used to insert a new document into MongoDB.

It permanently stores the document in the database.

---

# Status Code Response

The API sends custom responses to identify the result of an operation.

### Success

```json
{
 "statuscode":1,
 "msg":"Success"
}
```
---
# POST API WORKING FLOW
Client
  |
POST Request
  |
Express Route
  |
Check Existing Data
  |
Create Document
  |
Save Data in MongoDB
  |
Send Response


---
**NAME : ADITI TANGRI**

**URN: 2302460**

**CRN: 2315004**
