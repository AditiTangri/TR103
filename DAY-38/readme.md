# MERN Stack 
## Day 38

**Date:** 7 August 2026
**Project:** ParkEasy — Parking Management System

---

## Vehicle Profile

The **Vehicle Profile** module allows users to add and update their vehicle details. The saved vehicle number and vehicle type are automatically used while booking a parking slot.

### APIs Used

#### 1. Get Vehicle Details

**Method:** `GET`

```http
/user-dashboard/:id
```

**Purpose:**
Retrieves the user's profile and registered vehicle details.

---

#### 2. Update Vehicle Details

**Method:** `PUT`

```http
/update-vehicle/:id
```

**Request Body:**

```json
{
  "number": "PB10AB1234",
  "type": "Car"
}
```

**Purpose:**
Updates the user's registered vehicle information.

---

# 🧾 Parking Bills

The **Parking Bills** module displays bills for completed parking bookings.

Each bill contains:

* Slot number
* Date
* Parking time
* Vehicle number
* Parking duration
* Total parking charges
* Payment status

### API Used

**Method:** `GET`

```http
/my-bills/:userId
```

**Purpose:**
Retrieves all completed parking bills of the logged-in user.

### Response

```json
{
  "success": true,
  "bills": [
    {
      "bookingId": 1,
      "slot": "A-101",
      "date": "2026-08-04",
      "time": "09:00 - 11:00",
      "vehicle": "PB10AB1234",
      "duration": 2,
      "amount": 100,
      "status": "Paid"
    }
  ]
}
```

---

## Working

The Parking Bills module works as follows:

1. The page fetches completed parking bills using:

   ```http
   GET /my-bills/:userId
   ```

2. Only bookings with **Completed** status are displayed.

3. Parking charges are calculated using:

   ```text
   Parking Charges = Duration × ₹50 per hour
   ```

4. Each completed booking is displayed as a **parking receipt**.

5. The payment status is displayed as **Paid**.

---



**By:** Aditi Tangri
**URN:** 2302460
**CRN:** 2315004
