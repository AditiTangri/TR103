# MERN STACK
## DAY-26
### DATE - 26 JULY 2026

# ParkEasy - Parking Management System

## Project Overview

ParkEasy is a smart parking management system developed using the MERN Stack.  
The main objective of this project is to provide an efficient and user-friendly platform that helps users find, reserve, and manage parking spaces easily.

The Home Page is the main interface of the application. It provides information about the parking system, displays available parking details, explains the working process, highlights important features, and allows users to proceed to the login page.

---

# Technology Used

## Frontend
- React.js
- React Router DOM
- JavaScript
- CSS

## Backend
- Node.js
- Express.js

## Database
- MongoDB

---

# Home Page UI Development

The Home Page is developed using React.js to create an interactive and informative landing page for the ParkEasy application.

The page introduces the smart parking solution and explains how users can search, reserve, and manage parking spaces efficiently.

React Router's `useNavigate()` hook is used for navigation between pages. It allows users to move from the Home Page to the Login Page when clicking the Get Started buttons.

The Home Page contains multiple sections:

- Navigation Bar
- Hero Section
- Parking Dashboard
- About Us Section
- How It Works Section
- Features Section
- Footer Section

---

# Navigation Bar

The navigation bar provides easy access to different sections of the website.

It contains:

- About Us
- How It Works
- Features
- Get Started Button

The navigation links allow users to directly move to specific sections of the same page.

The Get Started button redirects users to the login page.

---

# Hero Section

The Hero Section is the first section visible to users.

It contains:

- Application introduction
- Smart parking solution message
- Description about ParkEasy
- Get Started button

This section explains how ParkEasy helps users find and reserve parking spaces quickly.

---

# Parking Dashboard

The parking dashboard provides a visual representation of parking availability.

It displays:

- Parking lot name
- Availability status
- Number of available spaces
- Parking slot layout

The dashboard helps users understand the current parking availability in a simple format.

---

# About Us Section

The About Us section explains the purpose of the ParkEasy system.

It describes how the application transforms traditional parking into a smart digital parking solution.

The main objective is to connect drivers, vehicles, and parking spaces using modern technology.

---

# How It Works Section

This section explains the complete parking process in three simple steps.

## 1. Find a Slot

Users can search and identify available parking spaces according to their requirements.

## 2. Reserve Space

Users can book their preferred parking slot through the reservation system.

## 3. Park & Go

Users can reach the location and enjoy a smooth parking experience.

---

# Features Section

The Features section highlights the main functionalities provided by the ParkEasy system.

## Easy Booking

Users can reserve parking spaces quickly through a simple booking process.

## Smart Management

The system provides efficient management of parking spaces using digital technology.

## Secure Parking

The system provides a reliable and secure parking environment for vehicles.

---

# Footer Section

The footer provides a final call-to-action option for users.

It contains:

- Smart Parking message
- Start Now button

The Start Now button redirects users to the login page.

---

# Working

1. The `Home()` functional component is created to display the complete homepage of the ParkEasy application.

2. `useNavigate()` is imported from `react-router-dom` to handle page navigation.

3. When the user clicks the "Get Started" or "Start Now" button, the user is redirected to:

```
/login
```


4. The Home Page displays different sections using React JSX structure.

5. The parking dashboard provides information about available parking spaces.

6. Different sections are organized using CSS classes for better design and maintainability.

7. The page provides smooth navigation and improves user interaction.

8. Users can understand the parking system features before accessing the application.

---

# Purpose

The purpose of the ParkEasy Home Page is to provide users with a simple, attractive, and informative interface.

It helps users understand the smart parking system, explore available features, view parking information, and easily access the application through secure login

---
**NAME : ADITI TANGRI**

**URN: 2302460**

**CRN: 2315004**
