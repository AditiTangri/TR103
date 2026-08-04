# MERN STACK
## DAY-30
## Date: 29 July 2026

# Project: PARKEASY - Parking Management System

# Signup API Development

The **Signup API** is developed to allow new users to register in the **ParkEasy Parking Management System**.

- The Signup API is created using **Express.js** and connected with MongoDB through the **User model**.
- The API handles new user registration requests using the **POST method**.
- User registration data is received from the frontend in JSON format.

---

# API 
```
app.post("/signup",async(req,res)=>{
    try{
        const exist=await User.findOne({email:req.body.email});

        if(exist)
            return res.json({success:false,message:"Email already exists"});

        const user=new User(req.body);
        await user.save();

        res.json({
            success:true,
            message:"Account Created Successfully"
        });

    }catch(err){
        res.json({success:false,message:err.message});
    }
});
```

## Signup API Flow
```
Frontend
    |
    | User Registration Data
    |
    v
POST /signup API
    |
    v
Check Email in MongoDB
    |
    +----------------+
    |                |
Email Exists    New Email
    |                |
    v                v
Return Error    Create User
                    |
                    v
               Save Data
                    |
                    v
          Account Created Successfully
```

--- 

**NAME: ADITI TANGRI**

**URN : 2302460**

**CRN: 2315004**
