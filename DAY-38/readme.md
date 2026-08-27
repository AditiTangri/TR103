# MERN Stack 
## Day 38

**Date:** 7 August 2026
**Project:** Parking Management System

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




**By:** Aditi Tangri
**URN:** 2302460
**CRN:** 2315004
