
# MERN STACK
## DAY-19
## Date: 16 July 2026

---

# React

## useContext

`useContext` is a built-in React Hook that allows a component to access and use data from a Context directly. It provides a way to share data between multiple components without passing props through every intermediate component.

It is mainly used for managing global or shared state that is required by multiple components.

---

## Why useContext is Needed

In React, data normally flows from a parent component to a child component using props. When the same data is required by deeply nested components, props need to be passed through every component level.

This process is called **Prop Drilling**.

`useContext` solves this problem by allowing components to access shared data directly from Context without passing props manually.

---

# Context

Context is a React feature that provides a way to create and share data globally between components.

A Context contains three main parts:

## 1. Context Object

Created using `createContext()`.

```javascript
import { createContext } from "react";

const MyContext = createContext();
````

---

## 2. Provider

Provider supplies the shared value to the child components.

```jsx
<MyContext.Provider value={value}>
    <Child />
</MyContext.Provider>
```

---

## 3. Consumer (useContext)

Consumer reads the shared data from Context.

```javascript
const value = useContext(ContextName);
```

---

# TASK - 1

## Local Storage

Local Storage is a browser storage mechanism used to store data permanently as key-value pairs.

The data remains available even after closing the browser and is removed only when it is manually deleted.

### Set Data

```javascript
localStorage.setItem("key", "value");
```

### Get Data

```javascript
localStorage.getItem("key");
```

---

## Session Storage

Session Storage is a browser storage mechanism used to store data temporarily for a single browser session.

The stored data is automatically removed when the browser tab or window is closed.

### Set Data

```javascript
sessionStorage.setItem("key", "value");
```

### Get Data

```javascript
sessionStorage.getItem("key");
```

---

# TASK - 2

* Implemented Local Storage functionality.
* Implemented Session Storage functionality.
* Stored and retrieved data using browser storage methods.
* Displayed stored values dynamically using React state.

---

# TASK - 3

# Login Signup Page

## Features

* Created Signup page using React.
* Stored user details using Local Storage.
* Created Login page for user authentication.
* Compared entered credentials with stored data.
* Displayed success and failure messages.
* Implemented navigation between Signup and Login pages.

---

**NAME: ADITI TANGRI**

**URN: 2302460**

**CRN: 2315004**
