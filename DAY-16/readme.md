# MERN Stack
## DAY-16
**Date:** 13 July 2026

# React

## React

React is a JavaScript library for building user interfaces (UI). It helps create fast, reusable, and interactive web applications using components.

### Features

- Component-based architecture
- Virtual DOM for better performance
- Reusable UI components
- One-way data flow
- JSX syntax

### Basic React Component

```jsx
function App() {
  return (
    <h1>Hello, React!</h1>
  );
}

export default App;
```

---

# React App Setup

## 1. Install Node.js

Download and install **Node.js** from the official website.

Check the installation:

```bash
node -v
npm -v
```

## 2. Create a React App

`npx create-react-app` is a command used to create a new React project with all the required files and dependencies automatically.

### Syntax

```bash
npx create-react-app my-app
```

### Explanation

- **npx** → Runs a package without installing it globally.
- **create-react-app** → Tool that sets up a React application.
- **my-app** → Name of the project folder (can be replaced with any project name).

---

# React Project Structure

A React project structure is the organized arrangement of folders and files in a React application. It provides a clear and systematic way to organize the application's source code, components, assets, styles, and dependencies.

A standard React project contains the following folders and files:

```text
my-app/
│
├── node_modules/
├── public/
│   └── index.html
│
├── src/
│   ├── components/
│   ├── assets/
│   ├── App.js
│   ├── index.js
│   └── App.css
│
├── package.json
└── README.md
```

### Folder Description

- **src/** – Contains the application's source code.
- **public/** – Contains static files like `index.html`.
- **node_modules/** – Contains installed packages and dependencies.
- **package.json** – Stores project information and dependencies.
- **README.md** – Contains project documentation.

A well-organized project structure improves readability, maintenance, and scalability.

---

# Components

A React component is a reusable, independent, and self-contained piece of the user interface that represents a specific part of a web application. Components divide large applications into smaller and manageable parts such as headers, navigation bars, content sections, footers, and buttons.

React mainly uses **Functional Components**, which are JavaScript functions that return JSX and can use Hooks.

### Example

```jsx
function Header() {
  return <h1>Welcome</h1>;
}

export default Header;
```

### Advantages

- Reusable
- Easy to maintain
- Improves code organization
- Reduces code duplication
- Makes development faster

---

# Import

Import is used to bring components, functions, variables, or modules from one file into another.



- Import brings reusable code into another file.
- Written at the top of a JavaScript file.
- Helps organize React applications.
- Improves readability and maintainability.

### Example

```jsx
import Header from "./Header";
```

---

# Export

Export is used to make components, functions, variables, or modules available for use in other files.

### Types of Export

#### Default Export

- Only one default export is allowed per file.

```jsx
function Header() {
  return <h1>Header</h1>;
}

export default Header;
```

Importing:

```jsx
import Header from "./Header";
```

---

#### Named Export

- Multiple named exports are allowed in the same file.

```jsx
export function Header() {
  return <h1>Header</h1>;
}

export function Footer() {
  return <h1>Footer</h1>;
}
```

Importing:

```jsx
import { Header, Footer } from "./Header";
```
---
**NAME: ADITI TANGRI**

**URN: 2302460**

**CRN: 2315004**

-----

