# MERN STACK
**DAY-7**
---
**Date : 2 July 2026**

# CSS Display & Flexbox

CSS **Display** and **Flexbox** properties are used to control how elements appear and how they are arranged on a web page.

---

## CSS display Property

The **display** property specifies how an HTML element is displayed on the webpage.

It can have the following values:

- **inline** – Element appears on the same line and takes only the required width.
- **block** – Element starts on a new line and occupies the full available width.
- **inline-block** – Element stays on the same line while allowing width and height to be set.
- **flex** – Creates a flexible layout container for arranging child elements.

---

## display: inline

An inline element is displayed on the same line as other inline elements.

### Characteristics
- Does not start on a new line.
- Takes only the width required by its content.
- Width and height cannot be applied.
- Mostly used for text elements.

**Examples:** `<span>`, `<a>`, `<strong>`

---

## display: block

A block element starts on a new line and occupies the full width available.

### Characteristics
- Starts on a new line.
- Takes full available width.
- Width and height can be changed.
- Used for creating page sections.

**Examples:** `<div>`, `<p>`, `<h1>`

---

## display: inline-block

An inline-block element combines the properties of both inline and block elements.

### Characteristics
- Appears on the same line.
- Width and height can be applied.
- Useful for buttons, menus, images, and cards.

---

## display: flex

The **flex** value makes an element a **Flex Container**.

All direct child elements become **Flex Items**, making alignment and spacing much easier.

### Advantages
- Easy horizontal and vertical alignment.
- Responsive layouts.
- Better control over spacing between items.

---

## CSS flex-direction

The **flex-direction** property specifies the direction in which flex items are placed.

### Values

- **row** – Items are placed from left to right (Default).
- **row-reverse** – Items are placed from right to left.
- **column** – Items are placed from top to bottom.
- **column-reverse** – Items are placed from bottom to top.

---

## CSS flex-wrap

The **flex-wrap** property controls whether flex items stay on one line or move to the next line.

### Values

- **nowrap** – Items remain on a single line (Default).
- **wrap** – Items move to the next line when required.
- **wrap-reverse** – Items wrap onto new lines in reverse order.

---

## CSS gap

The **gap** property creates space between flex or grid items without using margins.

### Advantages

- Creates equal spacing between items.
- Makes layouts cleaner.
- Reduces the need for margins.

---

## CSS align-self

The **align-self** property aligns an individual flex item differently from other items in the same flex container.

### Common Values

- **flex-start**
- **center**
- **flex-end**
- **stretch**
- **baseline**

It overrides the alignment specified by the container's **align-items** property.

---

## CSS order

The **order** property changes the visual order of flex items without changing the HTML structure.

### Characteristics

- Default value is **0**.
- Lower order values appear first.
- Higher order values appear later.

It is useful for rearranging items in responsive layouts.

---

## Summary Table

| Property | Purpose |
|----------|---------|
| **display: inline** | Displays elements on the same line. |
| **display: block** | Displays elements on a new line with full width. |
| **display: inline-block** | Displays elements inline while allowing width and height. |
| **display: flex** | Creates a flexible layout container. |
| **flex-direction** | Sets the direction of flex items. |
| **flex-wrap** | Controls whether items wrap to the next line. |
| **gap** | Creates spacing between flex or grid items. |
| **align-self** | Aligns one specific flex item individually. |
| **order** | Changes the display order of flex items. |

---

**Name : Aditi Tangri**  
**URN : 2302460**  
**CRN : 2315004**
