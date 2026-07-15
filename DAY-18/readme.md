# MERN STACK
### DAY-18
## Date: 15 July 2026

# React 

---

# TASK - 1

## React Introduction

React is a JavaScript library used for building fast and interactive user interfaces. It allows developers to create reusable components and manage application data efficiently.

---

# TASK - 2 TODO LIST

## Description

A Todo List is a task management application used to add and display tasks that need to be completed. In React, a Todo List is created using components, state management, and event handling.

## Concepts Used

### 1. React Component

- A reusable piece of UI that contains logic and structure.
- The Todo List is created as a functional component.

Example:

```jsx
export const Todo = () => {
    return (
        <>
        </>
    );
};
```

# useEffect Hook

## Introduction

`useEffect` is a React Hook that allows functional components to perform **side effects** after rendering.

A side effect is any operation that happens outside the normal component rendering process.

Examples of side effects:

- Showing an alert
- Fetching data from an API
- Changing the document title
- Setting timers (`setTimeout`, `setInterval`)
- Adding or removing event listeners
- Updating local storage

`useEffect` runs after the component renders.

---

## Syntax

```jsx
useEffect(() => {
    // side effect code
}, [dependency]);
```
# Dependency Array Behavior in useEffect

The dependency array controls **when the useEffect hook runs**. It is written as the second argument of the `useEffect()` function.

| Code | When it runs | Example |
|------|--------------|---------|
| `useEffect(() => {})` | Runs after every render of the component | Executes every time the component renders or state/props change |
| `useEffect(() => {}, [])` | Runs only once when the component loads (mounts) | Used for initial API calls, loading data, or setup operations |
| `useEffect(() => {}, [state])` | Runs whenever the specified state changes | Executes when the value of the given state variable is updated |

---

# TASK - 3 COUNTER

## Introduction

A Counter is a React application used to increase and decrease a numerical value. It is created using React state management and event handling.

## Concepts Used

### 1. useState Hook

- Used to store and update the counter value.
- It manages changing data inside a React component.

### 2. Event Handling

- Used to handle user actions like button clicks.
- Increment increases the counter value.
- Decrement decreases the counter value.

**NAME : ADITI TANGRI**

**URN : 2302460**

**CRN : 2315004**
