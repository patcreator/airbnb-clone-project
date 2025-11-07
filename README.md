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
 ##  API Security
Security is a **core priority** of this project to ensure user trust, protect sensitive data, and maintain platform integrity.  
### Key Security Measures

1. **Authentication**
   - Implemented via **NextAuth.js** and **JWT tokens** for secure session handling.
   - Ensures only registered and verified users can access restricted features.

   **Why it’s crucial:**  
   Prevents unauthorized access to user data, bookings, and payment information.

2. **Authorization**
   - Role-based access control (e.g., admin, host, guest).
   - Restricts critical actions like property deletion or booking management to authorized users only.

   **Why it’s crucial:**  
   Protects resources from malicious or accidental misuse and ensures data integrity.

3. **Rate Limiting & Throttling**
   - Limits the number of API requests per IP or user within a specific time frame.
   - Helps mitigate brute-force attacks and API abuse.

   **Why it’s crucial:**  
   Prevents service overloads and protects against denial-of-service (DoS) attacks.

4. **Data Encryption**
   - All sensitive data (e.g., passwords, payment details) is encrypted using industry standards (bcrypt, TLS).
   - Environment variables are securely managed via `.env` files.

   **Why it’s crucial:**  
   Ensures sensitive data remains protected in transit and at rest.

5. **Input Validation & Sanitization**
   - All API endpoints validate user input to prevent SQL injection and XSS attacks.

   **Why it’s crucial:**  
   Keeps the application safe from data corruption and malicious payloads.

6. **Secure Payments**
   - Payments processed through trusted gateways (e.g., Stripe or PayPal).
   - No credit card data is stored on our servers.

   **Why it’s crucial:**  
   Maintains compliance with PCI-DSS and ensures safe user transactions.

 ##  CI/CD Pipeline

Continuous Integration (CI) and Continuous Deployment (CD) are automated workflows that ensure consistent, reliable, and rapid development and delivery of the application.

### What is CI/CD?
- **Continuous Integration (CI):** Automatically builds and tests code changes whenever developers push updates to the repository.
- **Continuous Deployment (CD):** Automatically deploys tested and verified code to the production or staging environment.

### Why it’s Important
-  **Improves code quality:** Every commit is tested automatically to detect bugs early.  
-  **Faster deployments:** Automates build and deployment steps, reducing manual effort.  
-  **Consistent environments:** Ensures production mirrors development using containers or configuration files.  
-  **Enhanced reliability:** Automated tests and deployment checks reduce human error.  

### Tools Used
- **GitHub Actions** – Automates build, test, and deploy workflows directly from GitHub.  
- **Docker** – Creates consistent environments using containerized services.  
- **Vercel / Render** – Handles automatic deployments when changes are pushed to the main branch.  
- **Jest / Cypress** – Used for unit and end-to-end testing during the CI phase.

