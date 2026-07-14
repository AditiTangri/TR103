# MERN STACK
### DAY-17
## Date: 14 July 2026

# React Router

React Router is a library that enables **client-side routing** in React applications. It allows users to navigate between different pages without reloading the entire website.

### Example:

- `/` → Home page
- `/about` → About page
- `/contact` → Contact page


# 1. BrowserRouter


`BrowserRouter` is the top-level component that enables routing using the browser's History API. It wraps the entire application so React Router can manage URLs.

## Syntax

```jsx
import { BrowserRouter } from "react-router-dom";

function App() {
  return (
    <BrowserRouter>
      {/* All routes go here */}
    </BrowserRouter>
  );
}
```


# 2. Routes


`Routes` is a container that holds all the `Route` components. It renders the first route that matches the current URL.

## Syntax

```jsx
<Routes>
  <Route path="/" element={<Home />} />
  <Route path="/about" element={<About />} />
</Routes>
```


# 3. Route

A `Route` maps a URL path to a React component.

## Syntax

```jsx
<Route path="/about" element={<About />} />
```

## Attributes

| Prop | Description |
|------|-------------|
| path | URL path |
| element | Component to display |


# Link


`Link` is a component provided by React Router that is used to create navigation links between different pages in a React application.

It works like an HTML `<a>` (anchor) tag, but it does not reload the entire page. Instead, it updates the URL and allows React Router to display the required component using client-side routing.

## Syntax

```jsx
<Link to="/about">About</Link>
```


# useState


`useState` is a React Hook that allows functional components to store and manage state (data that can change over time).

Before Hooks, state was mainly used inside class components. With `useState`, functional components can also create and update state.

## Import Syntax

To use `useState`, import it from React:

```jsx
import { useState } from "react";
```


## Basic Syntax

```jsx
const [state, setState] = useState(initialValue);
```



| Part | Meaning |
|------|---------|
| state | Current value stored in state |
| setState | Function used to update the state |
| initialValue | Starting value of the state |





## How useState Works

```
Component Render
        |
        ↓
useState(initialValue)
        |
        ↓
Creates State Variable
        |
        ↓
User Action
        |
        ↓
setState() Updates Value
        |
        ↓
Component Re-renders
```

**NAME: ADITI TANGRI**

**URN: 2302460**

**CRN:2315004**


