# airbnb-clone-project

## Overview
The Airbnb Clone project aims to replicate the core functionalities of Airbnb, providing a robust backend for managing user interactions, property listings, bookings, payments, and reviews. The project is designed to be scalable, secure, and efficient, leveraging modern technologies to ensure a seamless experience for users and hosts.

## Tech Stack
Django
PostgreSQL
GraphQL
Redis
Docker
Celery

## Team Roles
Backend Developer: Designs and implements API endpoints, database schemas, and business logic to support core functionalities like user management, bookings, and payments.

Database Administrator: Oversees database design, indexing, and optimization to ensure efficient data storage and retrieval.

DevOps Engineer: Manages deployment, monitoring, and scaling of backend services, ensuring high availability and performance.

QA Engineer: Tests backend functionalities to ensure they meet quality standards and perform reliably under various conditions.

## Tech Stack
Django: A Python web framework used for building secure and scalable RESTful APIs.

Django REST Framework: Provides tools for creating and managing RESTful APIs with support for CRUD operations.

PostgreSQL: A relational database for storing user, property, booking, and payment data.

GraphQL: Enables flexible and efficient data querying, reducing over- or under-fetching of data.

Celery: Handles asynchronous tasks like sending notifications or processing payments.

Redis: Supports caching and session management to improve performance.

Docker: Ensures consistent development and deployment environments through containerization.

CI/CD Pipelines: Automates testing and deployment to streamline development and ensure code quality.

## Database Design
Users

id: Unique identifier for each user.
email: User’s email for authentication and communication.
name: User’s full name for profile display.
password: Hashed password for secure authentication.
created_at: Timestamp for user registration.


Properties:

id: Unique identifier for each property.
host_id: Foreign key linking to the user who owns the property.
title: Name or title of the property.
location: Address or coordinates of the property.
price_per_night: Cost of renting the property per night.


Bookings:

id: Unique identifier for each booking.
property_id: Foreign key linking to the booked property.
user_id: Foreign key linking to the user making the booking.
check_in_date: Start date of the booking.
check_out_date: End date of the booking.


Reviews:

id: Unique identifier for each review.
property_id: Foreign key linking to the reviewed property.
user_id: Foreign key linking to the user posting the review.
rating: Numerical rating (e.g., 1-5 stars).
comment: Text description of the review.


Payments:

id: Unique identifier for each payment.
booking_id: Foreign key linking to the associated booking.
amount: Payment amount.
status: Payment status (e.g., pending, completed).
created_at: Timestamp of the payment.

## Relationships
A User can own multiple Properties (one-to-many).
A Property can have multiple Bookings and Reviews (one-to-many).
A Booking belongs to one User and one Property (many-to-one).
A Review is associated with one User and one Property (many-to-one).
A Payment is linked to one Booking (one-to-one).

## Feature Breakdown
User Management: Allows users to register, authenticate, and manage profiles, ensuring secure access to the platform.

Property Management: Enables hosts to create, update, and delete property listings, making it easy to manage rental offerings.

Booking System: Facilitates property reservations, including check-in/check-out details, providing a seamless booking experience.

Payment Processing: Handles secure payment transactions for bookings, ensuring trust and reliability.

Review System: Allows users to post and view property reviews, enhancing transparency and user confidence.

Data Optimization: Implements indexing and caching to improve data retrieval speed and reduce database load.

API Documentation: Provides clear REST and GraphQL API documentation, simplifying integration for developers.