# MERN STACK
# DAY-31
## Date: 30 July 2026

# Project: PARKEASY - Parking Management System

# Login API Development

The **Login API** is developed to authenticate registered users in the **ParkEasy Parking Management System**.

- The Login API verifies the email and password entered by the user with the user data stored in the MongoDB database.
- The API is created using **Express.js** with a **POST request**.

---

# API 

```
app.post("/login",async(req,res)=>{
    try{
        const {email,password}=req.body;

        const user=await User.findOne({
            email,
            password
        });

        if(!user)
            return res.json({
                success:false,
                message:"Invalid Email or Password"
            });

        res.json({
            success:true,
            user
        });

    }catch(err){
        res.json({
            success:false,
            message:err.message
        });
    }
});
```

## LOGIN API FLOW
Frontend
   |
   |  Email + Password
   |
   v
POST /login API
   |
   v
Check User Data in MongoDB
   |
   +----------------+
   |                |
 Match Found     Not Found
   |                |
   v                v
Login Success   Invalid Credentials
   |
   v
Return User Details


---
**NAME : ADITI TANGRI**

**URN : 2302460**

**CRN : 2315004**
