# MERN STACK
## DAY-33
## Date: 1 August 2026

# Project: PARKEASY - Parking Management System

# User Dashboard Development

The **User Dashboard** is developed to provide users with their personal parking information and activities in the **ParkEasy Parking Management System**.

## Purpose

- It allows users to view vehicle details, booking history, parking status, and available parking slots.
- It helps users manage their parking activities efficiently.
- Dashboard data is dynamically displayed using React state values.

---

# User Dashboard Features

The User Dashboard displays the following information:

## User Information

1. User Name
2. Email Address
3. Vehicle Number
4. Vehicle Type
5. Current Parking Status
6. Total Bookings
7. Available Parking Slots

---

# User Dashboard API Development

The User Dashboard API is created using Express.js to retrieve user-specific information.

- The API uses the logged-in user's ID to fetch user details from MongoDB.
- It retrieves user information, vehicle details, booking records, and available parking slots.
# API Endpoint
```
GET /user-dashboard/:id
```
# User Dashboard API Code
```
app.get("/user-dashboard/:id",async(req,res)=>{
    try{
        const user=await User.findById(req.params.id);

        const availableSlots=await Slot.countDocuments({
            status:"Available"
        });

        res.json({
            success:true,
            name:user.name,
            email:user.email,
            vehicle:user.vehicle,
            bookings:user.bookings,
            availableSlots
        });

    }catch(err){
        res.json({
            success:false,
            message:err.message
        });
    }
});
```
# User Dashboard Flow
```
User Login
     |
     v
Retrieve User ID from localStorage
     |
     v
UserDashboard Component
     |
     v
GET /user-dashboard/:id API
     |
     v
Fetch User Details from MongoDB
     |
     v
Count Available Parking Slots
     |
     v
Send User Dashboard Data
     |
     v
Display User Information and Activities
```

**Name : ADITI TANGRI**

**URN: 2302460**

**CRN: 2315004**
