# 🏠 Project Features and Functionalities – Airbnb Clone

This repository contains the backend implementation of an Airbnb-style rental marketplace as part of the ALX Full Stack Engineering program.

The backend supports user authentication, property listings, bookings, payments, reviews, messaging, and admin functionality

## 🧾 Overview

This project replicates the backend logic of Airbnb

---

## 🔑 Core Functionalities

### 1. **User Management**

- Register as guest or host
- Login via email/password or OAuth (Google/Facebook)
- Update profile details and upload photos

### 2. **Property Listings**

- Hosts can create, update, and delete listings
- Properties include title, description, location, price, availability, and amenities

### 3. **Search & Filtering**

- Search by location, price range, guest count, and amenities
- Pagination support for large datasets

### 4. **Booking System**

- Guests book properties based on available dates
- Prevent double bookings using date validation
- Booking status tracking: pending, confirmed, canceled

### 5. **Payment Integration**

- Support for Stripe and PayPal
- Multi-currency transactions
- Automatic payouts to hosts after successful stays

### 6. **Reviews & Ratings**

- Users can leave ratings (1–5 stars) and feedback
- Reviews are tied to actual bookings to ensure authenticity
- Hosts can respond to reviews

### 7. **Messaging System**

- In-app messaging between guests and hosts
- Messages stored securely in the database

### 8. **Admin Dashboard**

- Manage users, properties, bookings, and payments
- Monitor activity logs and resolve disputes

---

### Entities

- **User**: Stores guest and host profiles
- **Property**: Rental listings created by hosts
- **Booking**: Reservation records
- **Payment**: Transaction details
- **Review**: User feedback
- **Message**: Communication between users

## Technology Stack

- **Backend Framework:** Django REST Framework  
- **Database:** PostgreSQL, MySQL  
- **APIs:** RESTful and GraphQL endpoints  
- **Caching:** Redis
- **Deployment:** Docker, CI/CD Pipelines
