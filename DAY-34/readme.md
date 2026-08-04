# MERN STACK
## DAY-34
## Date: 3 August 2026

# Project: PARKEASY - Parking Management System

# Available Parking Slots Module Development

The **Available Parking Slots Module** is developed to allow users to view and select available parking spaces in the **ParkEasy Parking Management System**.

## Purpose

- It helps users find suitable parking slots according to their preferred date and time.
- It prevents booking conflicts by checking already reserved slots during the selected time period.
- It allows users to search, select, and request parking slots easily.
- The module provides real-time availability information for better parking management.

---

# Available Parking Slots Features

The Available Parking Slots Module provides the following features:

1. View Available Parking Slots
2. Search Specific Parking Slots
3. Select Required Parking Slot
4. Enter Booking Date and Time Details
5. Send Booking Request
6. View Selected Slot and Timing Information

---


---

# Working

1. The `AvailableSlots()` component is created to display available parking spaces.

2. The component sends a request to the `/slots` API using Fetch API.

3. The backend retrieves parking slot details from the Slot collection.

4. The system checks user booking records to identify unavailable slots.

5. The API filters booked slots according to the selected date and time.

6. Available slot details are sent back to the frontend.

7. The received slot data is displayed using React state.

8. Users can search, select, and request a parking slot.

9. The booking confirmation form displays selected slot and timing details.

10. After successful booking, the available slots list is updated automatically.

---


---

**Name : ADITI TANGRI**

**URN: 2302460**

**CRN: 2315004**
