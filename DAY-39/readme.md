# MERN Stack 
## Day 39

**Date:** 8 August 2026
**Project:** ParkEasy — Parking Management System

---

#  Vehicle Management

The **Vehicle Management** module allows administrators to monitor and manage vehicles entering and exiting the parking area.

It enables administrators to:

* View vehicle details
* Search vehicles
* Filter records by date
* Manage vehicle entry and exit operations
* Track parking status

### React Hooks Used

* `useState()` is used to manage vehicle data, search values, selected dates, and filtered vehicle records.
* `useEffect()` is used to automatically load vehicle details when the page is opened.

The Vehicle Management module communicates with the backend using REST APIs to retrieve and update vehicle information.

---

## Vehicle Management APIs

### 1. Get All Vehicles

**Method:** `GET`

```http
/vehicles
```

**Purpose:**

* Retrieves all vehicle booking records from the database.
* Fetches owner details, vehicle number, vehicle type, slot details, booking date, timing, and parking status.
* Displays complete vehicle information in the administrator panel.

---

### 2. Vehicle Entry

**Method:** `PUT`

```http
/vehicle-entry/:userId/:index
```

**Purpose:**

* Records vehicle entry when an approved booking vehicle arrives at the parking area.
* Checks whether the booking has been approved before allowing entry.
* Validates the booking date and time.
* Updates the entry time.
* Changes the parking status to `Parked`.

---

### 3. Vehicle Exit

**Method:** `PUT`

```http
/vehicle-exit/:userId/:index
```

**Purpose:**

* Records vehicle exit after the vehicle leaves the parking area.
* Calculates parking duration using entry and exit time.
* Updates the booking status to `Completed`.
* Changes the parking status from `Parked` to `Exited`.

---

## Vehicle Management Working

1. The `VehicleManagement()` component is created to manage vehicle monitoring operations.

2. The component loads all vehicle records using:

   ```http
   GET /vehicles
   ```

3. Vehicle information is displayed in a table containing:

   * Owner
   * Vehicle number
   * Vehicle type
   * Slot
   * Date
   * Time
   * Booking status
   * Parking status

4. The search feature allows administrators to find vehicles using their vehicle numbers.

5. Date filtering allows administrators to view vehicle records for a specific date.

6. The **Today** button automatically selects the current date and displays today's vehicle records.

7. The **Vehicle Entry** button sends a request to:

   ```http
   PUT /vehicle-entry/:userId/:index
   ```

8. The backend validates the booking approval, date, and time before allowing vehicle entry.

9. The **Vehicle Exit** button updates vehicle exit details using:

   ```http
   PUT /vehicle-exit/:userId/:index
   ```

10. After entry or exit operations, vehicle records are refreshed automatically.

11. The Vehicle Management module helps administrators track parking activity and maintain accurate vehicle movement records.

---

# Admin Profile Management

The **Admin Profile Management** module allows administrators to view and update their account information.

It enables administrators to edit profile details such as:

* Name
* Email address

The profile update process communicates with the backend using REST APIs.

---

## Admin Profile API

### Update Admin Profile

**Method:** `PUT`

```http
/update-admin/:id
```

**Purpose:**

* Updates administrator profile information in the database.
* Modifies the administrator's name and email.
* Saves updated profile information permanently in MongoDB.

---

##  Admin Profile Working

12. The `AdminProfile()` component is created to manage administrator profile details.

13. The admin user ID is retrieved from `localStorage` after login.

14. Existing administrator details are loaded using:

```http
GET /user-dashboard/:id
```

15. Profile information is displayed inside a profile card interface.

16. Administrators can edit their name and email fields.

17. The **Save Profile** button sends updated information to:

```http
PUT /update-admin/:id
```

18. The backend verifies the administrator record before updating the details.

19. Updated profile information is stored in MongoDB.

20. A success message is displayed after successful profile modification.

21. The Admin Profile Management module provides a simple and secure way for administrators to maintain their account information.

---



**By:** Aditi Tangri
**URN:** 2302460
**CRN:** 2315004
