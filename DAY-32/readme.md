# MERN STACK
## DAY-32
## Date: 31 July 2026

# Project: PARKEASY - Parking Management System

# Admin Dashboard Development

The **Admin Dashboard** is developed to provide administrators with complete control and monitoring of the **ParkEasy Parking Management System**.

## Purpose

- It allows administrators to view parking statistics, user information, and booking activities.
- It helps in managing and monitoring the complete parking system efficiently.
- Dashboard data is dynamically displayed using React state values.

---

# Admin Dashboard Features

The Admin Dashboard displays the following information:

## Parking Statistics

1. Total Parking Slots
2. Available Slots
3. Reserved Slots
4. Maintenance Slots
5. Total Users
6. Pending Booking Requests

## Parking Overview

The Parking Overview section displays:

1. Approved Bookings
2. Cancelled Bookings
3. Current Vehicles Parked

---

## Admin Dashboard API Development

The Admin Dashboard API is created using Express.js to provide complete system statistics.

- The API retrieves user and parking slot information from MongoDB.
- It calculates booking and parking statistics based on database records.

```
app.get("/admin-dashboard", async(req,res)=>{

try{
const users = await User.find();
const slots = await Slot.find();
let pendingBookings = 0;
let approvedBookings = 0;
let cancelledBookings = 0;
let currentParking = 0;
users.forEach(user=>{
user.bookings.forEach(booking=>{
if(booking.status==="Pending")
pendingBookings++;
if(booking.status==="Approved")
approvedBookings++;
if(booking.status==="Cancelled")
cancelledBookings++;
if(booking.status==="Approved")
currentParking++;
});
});
res.json({
totalSlots:slots.length,
availableSlots:
slots.filter(s=>s.status==="Available").length,
reservedSlots:
slots.filter(s=>s.status==="Reserved").length,
maintenanceSlots:
slots.filter(s=>s.status==="Maintenance").length,
totalUsers:users.length,

pendingBookings,

approvedBookings,

cancelledBookings,

currentParking

});
}
catch(err){
res.status(500).json({
message:err.message
});
}
});
```

## Admin Dashboard Flow
```
Admin Panel
     |
     v
AdminDashboard Component
     |
     v
GET /admin-dashboard API
     |
     v
Fetch Users and Slots from MongoDB
     |
     v
Calculate Statistics
     |
     v
Send Dashboard Data
     |
     v
Display Dashboard Cards

```

---
**NAME: ADITI TANGRI**

**URN: 2302460**

**CRN: 2315004**
