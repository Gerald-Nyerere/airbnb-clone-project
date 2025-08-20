# AirBnB Clone Project

## Overview
The backend for the Airbnb Clone project is designed to provide a robust and scalable foundation for managing user interactions, property listings, bookings, and payments. This backend will support various functionalities required to mimic the core features of Airbnb, ensuring a smooth experience for users and hosts.

## Project Goals
- Develop features for property listing creation, updates, and retrieval.
- Implement a secure system for user registration, authentication, and profile management.
- Create a booking mechanism for users to reserve properties and manage booking details..
- Gain proficiency in CI/CD pipelines for automated deployment.
- Connect the backend to a database.
- Deploy the application in a production environment.

## Tech Stack
- Python
- GraphQL
- PostgreSQL
- CI/CD pipeline
- Redis
- Docker
- Django

## Team Roles
### 1. Backend Developer
- Responsible for implementing API endpoints, database schemas, and business logic.
### 2. Database Administrator
- Manages database design, indexing, and optimizations.
### 3. DevOps Engineer: 
- Handles deployment, continuous integration/continuous delivery (CI/CD), and server maintenance. 
- Ensures smooth application deployment and monitors system performance in production.
### 4. UI/UX Designer
- Designs the application layout, color schemes, and interaction flows. 
- Focuses on creating an intuitive and visually appealing user interface.
### 5. QA Engineer 
- Ensures the backend functionalities are thoroughly tested and meet quality standards.

### 7. Project Manager
- Coordinates the team, manages timelines, assigns tasks, and ensures the project meets deadlines and requirements.
- Acts as the main communication link between stakeholders and developers.

## Technology Stack
### 1. Django
- A high-level Python web framework used for building the RESTful API.
### 2. Django REST Framework 
- Provides tools for creating and managing RESTful APIs.
### 3. PostgreSQL 
- A powerful relational database used for data storage.
### 4. GraphQL 
- Allows for flexible and efficient querying of data.
### 5. Celery 
- For handling asynchronous tasks such as sending notifications or processing payments.
### 6. Redis 
Used for caching and session management.
### 7. Docker
- Containerization tool for consistent development and deployment environments.
### 8. CI/CD Pipelines
- Automated pipelines for testing and deploying code changes.

## Database Design

### 1. Users
- `id` (Primary Key)
- `name`: Full name of the user.
- `email`: Contact email, unique for each user.
- `password`: Encrypted password for authentication.
- `role`: Defines whether the user is a host or a guest.

### 2. Properties
- `id` (Primary Key).
- `title`: Name or title of the property.
- `description`: Detailed description of the property.
- `price_per_night`: Cost per night for booking.
- `owner_id` (Foreign Key): References the `Users` table

### 3. Bookings
- `id` (Primary Key): 
- `property_id` (Foreign Key): References the `Properties` table.
- `user_id` (Foreign Key): References the `Users` table
- `start_date`: Start date of the booking.
- `end_date`: End date of the booking.
- `status` (pending, confirmed, canceled).

### 4. Reviews
- `id` (Primary Key)
- `property_id` (Foreign Key): References the `Properties` table.
- `user_id` (Foreign Key) References the `Users` table 
- `rating` (e.g., 1–5).
- `comment`: Text feedback from the guest.

### 5. Payments
- `id` (Primary Key )
- `booking_id` (Foreign Key): References the `Bookings` table.
- `amount`: Payment amount for the booking.
- `payment_date`: Date of payment.
- `status`: (e.g., completed, pending).

## Feature Breakdown

### 1. User Management
- Handles user registration, authentication, and profile management. 
- Ensures users can securely sign up, log in, and manage their personal information, enabling personalized experiences.

### 2. Property Management
- Allows hosts to add, update, and manage property listings. 
- Includes property details, images, and pricing, forming the core of the AirBnB-like experience.

### 3. Booking System
- Enables guests to browse available properties, make reservations, and manage bookings.
- Ensures a smooth and efficient process for securing stays and handling availability.

### 4. Search and Filter
- Provides users with advanced search capabilities based on location, price range, and amenities. 
- Improves user experience by making it easier to find suitable properties quickly.

### 5. Reviews and Ratings
- Allows guests to leave feedback and ratings for properties. 
- Adds trust and transparency, helping future guests make informed decisions.

### 6. Payment Integration
- Facilitates secure payment transactions between guests and hosts. 
- It ensures a seamless booking experience by integrating reliable payment gateways.

### 7. Continuous Integration and Deployment (CI/CD)
- Automates code testing, building, and deployment using GitHub Actions.
- Ensures continuous integration of new features while minimizing errors.