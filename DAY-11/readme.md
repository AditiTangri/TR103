# MERN Stack 
## Day 11


**Date:** 7 July 2026

## JavaScript: Document Object Model (DOM)

# Document Object Model (DOM)

The **Document Object Model (DOM)** is a programming interface that represents an HTML document as a **tree-like structure**. Every HTML element, attribute, and piece of text is represented as an **object (node)**. JavaScript uses the DOM to access, modify, add, delete, and style HTML elements dynamically without reloading the web page.

When a browser loads an HTML page, it automatically creates the DOM. JavaScript communicates with the web page through this DOM to make websites interactive and dynamic.

---

## DOM Tree Structure

```
Document
│
└── html
    │
    ├── head
    │    └── title
    │
    └── body
         │
         ├── h1
         ├── p
         ├── div
         └── button
```

Every element shown above is called a **DOM Node**.

---

# Accessing Elements in DOM

JavaScript uses the **document** object to access HTML elements.

### General Syntax

```javascript
document.methodName("selector");
```

---

## 1. getElementById()

Selects a single element using its unique **id**.

### Syntax

```javascript
document.getElementById("idName");
```

### Example

```javascript
document.getElementById("heading").innerHTML = "Welcome";
```

---

## 2. getElementsByClassName()

Returns all elements having the specified class name.

### Syntax

```javascript
document.getElementsByClassName("className");
```

### Example

```javascript
let items = document.getElementsByClassName("demo");
```

---

## 3. getElementsByTagName()

Returns all elements with the specified HTML tag.

### Syntax

```javascript
document.getElementsByTagName("tagName");
```

### Example

```javascript
let paragraphs = document.getElementsByTagName("p");
```

---

## 4. querySelector()

Returns the **first** element that matches the specified CSS selector.

### Syntax

```javascript
document.querySelector("CSS Selector");
```

### Examples

```javascript
document.querySelector("#heading");
document.querySelector(".demo");
document.querySelector("p");
```

---

## 5. querySelectorAll()

Returns **all** elements that match the specified CSS selector.

### Syntax

```javascript
document.querySelectorAll("CSS Selector");
```

### Example

```javascript
let paragraphs = document.querySelectorAll(".demo");
```

---




**Name:** Aditi Tangri  
**URN:** 2302460  
**CRN:** 2315004
