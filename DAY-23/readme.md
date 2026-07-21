# MERN STACK  
# DAY-23
## Date: 21 July 2026

# GET Method

The **GET** method is used to retrieve data from the server. It does not modify or delete any data.

## Characteristics:

- Used to fetch data.
- Sends data through the URL (if parameters are needed).
- Should not change server data.
- Can be cached by browsers.
- Safe and idempotent (making the same request multiple times has the same effect).

## Example (Express):

```javascript
app.get("/api/getuser", async (req, res) => {
    const data = await usermodel.find();
    res.send(data);
});
```

## Example (React):

```javascript
const result = await fetch("http://localhost:9000/api/getuser");

const data = await result.json();

console.log(data);
```

## GET Method Flow:

```
Client
   |
   | GET Request
   |
   v
Server
   |
   | Fetch data from MongoDB
   |
   v
Client receives response
```

---

# DELETE Method

The **DELETE** method is used to remove a resource from the server.

## Characteristics:

- Used to delete existing data.
- Usually requires the unique ID of the resource.
- Idempotent (deleting the same resource multiple times should not create additional changes after it is removed).

## Example (Express):

```javascript
app.delete("/api/deluser/:id", async (req, res) => {

    const data = await usermodel.deleteOne({
        _id: req.params.id
    });

    if (data.deletedCount > 0) {
        res.send({
            statuscode: 1
        });
    } else {
        res.send({
            statuscode: 0
        });
    }
});
```

### Explanation:

- `:id` is a route parameter.
- `req.params.id` contains the ID sent in the URL.
- `deleteOne()` removes the matching document from MongoDB.

## Example (React):

```javascript
const dele = async (id) => {

    await fetch(`http://localhost:9000/api/deluser/${id}`, {
        method: "DELETE"
    });

};
```

---

# GET vs DELETE

| Feature | GET | DELETE |
|---------|-----|--------|
| Purpose | Retrieve data | Remove data |
| Database Change | No change | Deletes data |
| HTTP Method | GET | DELETE |
| Requires ID | Usually No | Usually Yes |
| Example URL | `/api/getuser` | `/api/deluser/:id` |
| Response | Data list/object | Success or error message |

---
**NAME: ADITI TANGRI**

**URN: 2302460**

**CRN: 2315004**



