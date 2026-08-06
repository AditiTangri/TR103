

# **Project:** ParkEasy – Parking Management System  
# DAY-37 
**Date:** 6 August 2026

---

# Overview

The **Booking Management** module enables administrators to manage all parking booking requests submitted by users. It provides a centralized dashboard for viewing booking information, approving or rejecting booking requests, and monitoring completed and cancelled bookings.

The frontend is developed using **React.js**, while the backend is built with **Express.js** and **MongoDB**. Booking information is fetched dynamically using REST APIs, allowing administrators to perform booking operations in real time.

---

# Objectives

- View all parking booking requests.
- Approve pending booking requests.
- Reject pending booking requests.
- Monitor approved, completed, and cancelled bookings.
- Automatically refresh booking data after every update.
- Release parking slots when bookings are cancelled or rejected.

---



# REST APIs

## 1. Get All Bookings

### Endpoint

```
GET /all-bookings
```

### Description

Retrieves booking records of all registered users from MongoDB.

Each booking contains:

- User Name
- Vehicle Number
- Slot Number
- Booking Date
- Booking Time
- Booking Status

### Response Example

```json
[
  {
    "userId": "64ab12345",
    "name": "Rahul Sharma",
    "vehicleNumber": "PB10AB1234",
    "slotNumber": "A12",
    "date": "2026-08-06",
    "time": "10:00 AM",
    "status": "Pending"
  }
]
```

---

## 2. Update Booking Status

### Endpoint

```
PUT /booking-status/:userId/:index
```

### Description

Updates the status of a selected booking request.

Supported actions:

- Approve
- Reject

If rejected or cancelled, the parking slot becomes available again.

### Request Example

```json
{
    "status": "Approved"
}
```

### Response

```json
{
    "message": "Booking status updated successfully."
}
```

---

# Features

- Displays all booking requests.
- Shows booking information in separate sections.
- Displays user details.
- Displays slot details.
- Displays booking date and time.
- Displays vehicle number.
- Shows booking status.
- Approve pending bookings.
- Reject pending bookings.
- Automatically refreshes booking records.
- Releases parking slots after rejection or cancellation.

---

# Booking Sections

## Pending Requests

Contains booking requests waiting for administrator approval.

Actions available:

- Approve
- Reject

---

## Approved Bookings

Displays bookings approved by the administrator.

---

## Completed Parking

Displays bookings where parking has been completed successfully.

---

## Cancelled / Rejected Bookings

Displays cancelled or rejected booking requests.

The corresponding parking slot becomes available for future bookings.

---

# Workflow

### Step 1

The `BookingManagement()` component loads.

↓

### Step 2

`GET /all-bookings` API is called.

↓

### Step 3

The backend retrieves booking records from MongoDB.

↓

### Step 4

Booking data is stored using `useState()`.

↓

### Step 5

Bookings are displayed in different sections.

↓

### Step 6

Administrator clicks **Approve** or **Reject**.

↓

### Step 7

`PUT /booking-status/:userId/:index` API updates booking status.

↓

### Step 8

If rejected or cancelled:

- Booking status changes.
- Parking slot becomes available.

↓

### Step 9

Booking list refreshes automatically.

↓

### Step 10

Administrator views the latest booking records.

---





---

# API Flow

```
React Frontend
      │
      ▼
GET /all-bookings
      │
      ▼
Express Server
      │
      ▼
MongoDB
      │
      ▼
Booking Records
      │
      ▼
React Dashboard
```

---

## Status Update Flow

```
Admin Clicks Approve / Reject
            │
            ▼
PUT /booking-status/:userId/:index
            │
            ▼
Update MongoDB
            │
            ▼
Release Slot (If Rejected)
            │
            ▼
Refresh Booking List
```

---
**NAME: ADITI TANGRI**

**URN: 2302460**

**CRN: 2315004**
