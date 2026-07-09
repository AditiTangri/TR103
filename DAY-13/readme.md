# MERN STACK
## DAY-13
**Date : 9 July 2026**

# JAVASCRIPT

## addEventListener()

`addEventListener()` is a JavaScript method used to attach an event to an HTML element. It allows the programmer to specify what action should be performed when a particular event occurs.

It can handle different types of events such as:

- click
- submit
- change
- keydown
- mouseover

### Syntax:

```javascript
element.addEventListener(event, function);
```

or

```javascript
element.addEventListener(event, function(eventObject) {
    // statements
});
```

### Parameters:

- **element** → The HTML element on which the event is applied.
- **event** → The name of the event to listen for.
- **function** → The function that executes when the event occurs.
- **eventObject** → An object containing information about the event.

---

## event.preventDefault()

`preventDefault()` is a JavaScript method used to stop the default behavior of an event.

Browsers automatically perform certain actions for some events. This method prevents those automatic actions from happening while allowing the event handling code to run.

### Syntax:

```javascript
event.preventDefault();
```

### Parameter:

- **event** → The event object passed to the event handler.

---

## textContent

`textContent` is a JavaScript property used to read or modify the text content of an HTML element.

It accesses only the text inside an element and does not interpret HTML tags. It treats the assigned value as plain text.

### Syntax:

**To set text:**

```javascript
element.textContent = "text";
```

**To get text:**

```javascript
let variable = element.textContent;
```

### Difference between textContent and innerHTML:

- `textContent` handles only plain text.
- `innerHTML` can read or insert HTML content.

---

**NAME** : ADITI TANGRI
**URN** : 2302460
**CRN** : 2315004
