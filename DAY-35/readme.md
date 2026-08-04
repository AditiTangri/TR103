# MERN STACK
## DAY-35
## Date: 4 August 2026

# Project: PARKEASY - Parking Management System

# Book Slot and My Bookings Module Development

The **Book Slot** and **My Bookings** modules are developed to manage the complete parking reservation process in the **ParkEasy Parking Management System**.

## Purpose

- The **Book Slot** module allows users to select a parking slot, choose a booking date and time, and send a reservation request.
- The **My Bookings** module allows users to view and manage all their parking reservations.
- These modules are integrated with the user account system and store booking information inside the user's booking records in MongoDB.

---

# Book Slot Features

The Book Slot module collects the following booking details:

1. Parking Slot Number
2. Vehicle Number
3. Booking Date
4. Start Time
5. End Time
6. Booking Status

The booking request is initially created with **Pending** status and can later be **Approved** or **Rejected** by the administrator.

Before creating a booking, the system verifies:

1. User Vehicle Details
2. Slot Availability
3. Existing Bookings for the Selected Time
4. Vehicle Booking Conflicts

---

# My Bookings Features

The My Bookings module displays all booking records based on their current status:

1. Pending Requests
2. Approved Bookings
3. Completed Bookings
4. Cancelled / Rejected Bookings

Each booking record displays:

1. Slot Number
2. Booking Date
3. Booking Time
4. Vehicle Details
5. Booking Status

Users can cancel pending booking requests, and the system automatically updates the booking status and slot availability.

---

# Book Slot API Development

The **Book Slot API** is developed using **Express.js** to process parking reservation requests.

## API Endpoint

```http
PUT /book-slot/:userId
```

## Purpose

- Receives booking information from the frontend.
- Retrieves user details using the provided user ID.
- Checks booking conflicts before creating a reservation.
- Stores booking details in the user's booking array.

### User Retrieval

```javascript
User.findById(req.params.userId)
```

### Booking Validation

The API checks:

1. Same slot booking during the same time period.
2. Same vehicle having multiple bookings at the same time.

If no conflict exists, a new booking object is created and stored with **Pending** status.

---

# My Bookings API Development

The **My Bookings API** retrieves all booking records of the logged-in user.

## API Endpoint

```http
GET /my-bookings/:id
```

### User Retrieval

```javascript
User.findById(req.params.id)
```

### API Response

The response contains:

1. User Name
2. Booking Records

The frontend separates booking records according to their booking status.

---

# Cancel Booking API Development

The **Cancel Booking API** allows users to cancel pending parking requests.

## API Endpoint

```http
PUT /cancel-booking/:userId/:index
```

## Purpose

- Receives the User ID and Booking Index.
- Updates the selected booking status to **Cancelled**.
- Restores parking slot availability if no active booking exists for the same slot.

---

# Module Flow

```text
User Dashboard
      |
      v
Available Slots
      |
      v
Select Parking Slot
      |
      v
Book Slot Form
      |
      v
PUT /book-slot/:userId
      |
      v
Verify Slot & Vehicle Availability
      |
      v
Store Booking (Pending)
      |
      v
My Bookings Page
      |
      v
GET /my-bookings/:id
      |
      v
Display Booking Records
      |
      v
Cancel Booking (Optional)
      |
      v
PUT /cancel-booking/:userId/:index
      |
      v
Update Booking Status
```

---

# Working

1. The user selects an available parking slot from the **Available Slots** module.

2. The user enters the booking date, start time, and end time.

3. The frontend sends the booking request using the `PUT /book-slot/:userId` API.

4. The backend verifies user details, vehicle information, and slot availability.

5. If the booking is valid, the request is stored in MongoDB with **Pending** status.

6. The user can view all booking records through the **My Bookings** page.

7. The My Bookings module retrieves booking information using the `GET /my-bookings/:id` API.

8. Booking records are displayed according to their current status.

9. Users can cancel pending requests using the **Cancel Booking** option.

10. The cancellation request updates the booking status and refreshes the booking list automatically.

---


---

**Name : ADITI TANGRI**

**URN: 2302460**

**CRN: 2315004**
