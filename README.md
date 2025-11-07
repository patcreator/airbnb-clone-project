# airbnb-clone-project


A full-stack Airbnb clone 
This project replicates core features of Airbnb, including property listings, booking management, user authentication, and responsive design.


# Team Roles
Software developer (Backend Developer)

# Technology Stack
- OpenAPI Standard: The backend APIs are documented using the OpenAPI standard to ensure clarity and ease of integration.
- Django: A high-level Python web framework used for building the RESTful API.
- Django REST Framework: Provides tools for creating and managing RESTful APIs.
- PostgreSQL: A powerful relational database used for data storage.
- GraphQL: Allows for flexible and efficient querying of data.
- Celery: For handling asynchronous tasks such as sending notifications or processing payments.
- Redis: Used for caching and session management.
- Docker: Containerization tool for consistent development and deployment environments.
- CI/CD Pipelines: Automated pipelines for testing and deploying code changes.
# Database Design
- Users
  - Id
  - Username
  - Email
  - Password
- Properties
  - Id
  - Name
  - Description
  - Location
  - Price
  - Status
- Bookings
   - Id
   - User
   - Property
   - Start Date/Time
   - End Date/Time
   - Status
- Reviews
  - Id
  - user
  - Starts
  - Comment
  - Attachment
- Payments
  - Id
  - Booking
  - Payment method
  - Paid Amount
  - Status
  - Type of Payment
## Relationship
  User -> Booking (1 - M)
  User -> review (1 - M)
  Payment -> booking (1-M)
  Properties -> booking (M-1)
# Feature Breakdown
1. API Documentation
OpenAPI Standard: The backend APIs are documented using the OpenAPI standard to ensure clarity and ease of integration.
Django REST Framework: Provides a comprehensive RESTful API for handling CRUD operations on user and property data.
GraphQL: Offers a flexible and efficient query mechanism for interacting with the backend.
2. User Authentication
  Register new users, authenticate, and manage user profiles.
4. Property Management
   Create, update, retrieve, and delete property listings.
5. Booking System
    Make, update, and manage bookings, including check-in and check-out details.
6. Payment Processing
    Handle payment transactions related to bookings.
7. Review System
    Post and manage reviews for properties.
8. Database Optimizations
Indexing: Implement indexes for fast retrieval of frequently accessed data.
Caching: Use caching strategies to reduce database load and improve performance.
  
 
