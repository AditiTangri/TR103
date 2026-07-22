# MERN STACK  
## DAY - 24
**Date:** 22 July 2026

# PUT Method

The **PUT** method is an HTTP request method used to **update an existing resource (data)** on the server. It sends the updated information from the client (**React**) to the server (**Node.js/Express**), and the server updates the corresponding record in the database.

## Example

### Before Update

| Id | Name  | Age | Email |
|----|-------|-----|------------------|
| 101 | Rahul | 20 | rahul@gmail.com |

### After Sending a PUT Request

| Id | Name  | Age | Email |
|----|-------|-----|------------------|
| 101 | Rahul | 22 | rahul@gmail.com |

> Only the existing record is updated.

---

## Frontend Syntax (React)

```javascript
fetch(url, {
    method: "PUT",
    headers: {
        "Content-Type": "application/json"
    },
    body: JSON.stringify(data)
});
```

---

## Backend Example (Node.js + Express)

```javascript
app.put("/api/update/:id", async (req, res) => {
    const data = await usermodel.findByIdAndUpdate(
        req.params.id,
        {
            Name: req.body.name,
            Email: req.body.mail,
            Age: req.body.age
        },
        { new: true }
    );

    if (data) {
        res.send({ statuscode: 1 });
    } else {
        res.send({ statuscode: 0 });
    }
});
```

### Explanation

- `app.put()` creates a PUT API route.
- `:id` is a route parameter that identifies the record to update.
- `findByIdAndUpdate()` updates the document in MongoDB.
- `req.params.id` gets the ID from the URL.
- `req.body` contains the updated data sent by the client.
- `{ new: true }` returns the updated document after modification.
- `statuscode: 1` indicates success.
- `statuscode: 0` indicates failure.

---

# Flag

A **flag** is a variable used to represent the current state of a program. It is usually a **boolean** value (`true` or `false`).

In React, a flag helps determine which action the component should perform.

### Example

- `flag = false` → **Add Mode**
- `flag = true` → **Update Mode**

---

## Syntax of Flag

```javascript
const [flag, setFlag] = useState(false);
```

---

## Example in React

```javascript
import { useState } from "react";

function App() {
    const [flag, setFlag] = useState(false);

    const handleSubmit = () => {
        if (flag) {
            console.log("Update Data");
        } else {
            console.log("Add Data");
        }
    };

    return (
        <div>
            <button onClick={handleSubmit}>
                {flag ? "Update" : "Add"}
            </button>
        </div>
    );
}

export default App;
```

### Output

- When `flag` is `false`, clicking the button performs the **Add** operation.
- When `flag` is `true`, clicking the button performs the **Update** operation.

---

**NAME : ADITI TANGRI**

**URN : 2302460**

**CRN : 2315004**
