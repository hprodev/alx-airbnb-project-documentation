# Backend Requirement Specifications – Airbnb Clone

## Overview

This document outlines the technical and functional requirements for key backend features of the Airbnb Clone project.

It ensures clarity on what needs to be implemented, tested, and documented during development.

---

## 1. User Authentication

### API Endpoints

- `POST /auth/register` – Registers a new user (guest or host)
- `POST /auth/login` – Authenticates an existing user

### Input/Output

- **Input:** Full name, email, password, role
- **Output:** JWT token and success message with user details

### Validation Rules

- Passwords must be hashed before storage
- Email addresses must be unique across all users
- Role-based access control should be enforced

---

## 2. Property Management

### API Endpoints

- `POST /properties` – Adds a new property listing
- `GET /properties/{property_id}` – Retrieves detailed information about a specific property

### Input/Output

- **Input:** Property name, description, price per night, location
- **Output:** JSON response containing full property details

### Constraints & Performance Optimization

- All property searches should support filtering by location and price range
- The system should use indexing on fields like `location` and `price_per_night` for faster queries
- Only authenticated hosts can create or edit their listings

---

## 3. Booking System

### API Endpoints

- `POST /bookings` – Creates a new booking for a property
- `PUT /bookings/{booking_id}` – Updates the status of an existing booking

### Input/Output

- **Input:** Property ID, user ID, start date, end date
- **Output:** Booking confirmation or error if dates are unavailable

### Validation & Security

- The system must ensure no overlapping bookings occur for the same property
- A successful payment must be confirmed before a booking is finalized
- Users should only be able to book properties that are currently available
