# MERN STACK
## DAY-36
## Date: 5 August 2026

# Project: PARKEASY - Parking Management System

# Parking Slot Management

The **Parking Slot Management** module is developed to allow administrators to manage all parking slots in the **ParkEasy Parking Management System**.

## Purpose

- It enables administrators to add new parking slots.
- It allows administrators to update parking slot status.
- It allows administrators to delete parking slots.
- It helps monitor parking slot availability efficiently.
- The module is implemented using **React.js** for the frontend and **Express.js** with **MongoDB** for backend operations.

---

# Parking Slot Management Features

The module provides the following features:

1. Add New Parking Slot
2. Update Parking Slot Status
3. Delete Parking Slot
4. View All Parking Slots
5. Monitor Slot Availability
6. Display Success Messages

---


---

# Parking Slot Management APIs

## Add Parking Slot

### API Endpoint

```http
POST /slots
```

### Purpose

- Adds a new parking slot to the database.
- Stores the slot number with the default status as **Available**.

---

## Update Parking Slot

### API Endpoint

```http
PUT /slots/:id
```

### Purpose

- Updates the status of an existing parking slot.
- Allows administrators to switch a slot between:
  - Available
  - Maintenance

- If a slot is marked as **Maintenance**, all active bookings for that slot are automatically cancelled.

---

## Delete Parking Slot

### API Endpoint

```http
DELETE /slots/:id
```

### Purpose

- Deletes a parking slot from the system.
- Cancels all related bookings associated with the deleted slot.
- Updates booking records to maintain data consistency.

---

## Create Demo Slots

### API Endpoint

```http
GET /create-slots
```

### Purpose

- Creates predefined demo parking slots for testing purposes.
- Inserts sample parking slot records into the database.

---

# Parking Slot Management Flow

```text
Administrator
      |
      v
Parking Slot Management
      |
      +-------------------------------+
      |               |               |
      v               v               v
Add Slot      Update Slot Status   Delete Slot
      |               |               |
      |               |               |
 POST /slots     PUT /slots/:id   DELETE /slots/:id
      |               |               |
      |               |               |
      +------- Update MongoDB --------+
                      |
                      v
          Refresh Dashboard Statistics
                      |
                      v
          Display Success Message
```

---

# Working

1. The `SlotManagement()` component is created to manage all parking slot operations.

2. The component loads parking slot data from the `GET /slots` API when the page is opened.

3. Administrators can add new parking slots using the `POST /slots` API.

4. Before adding a parking slot, the system checks whether the slot number already exists.

5. The `PUT /slots/:id` API updates the status of a parking slot between **Available** and **Maintenance**.

6. If a slot is changed to **Maintenance**, all active bookings for that slot are cancelled automatically.

7. The `DELETE /slots/:id` API removes a parking slot and cancels all related bookings.

8. Dashboard summary cards are updated automatically after every operation.

9. Success messages are displayed to notify administrators of completed actions.

10. The Parking Slot Management module provides an efficient way to maintain parking slot availability and ensure proper management of parking resources.

---


**Name : ADITI TANGRI**

**URN: 2302460**

**CRN: 2315004**
