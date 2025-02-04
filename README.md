# STC-System
# Secure Trading Capturing System

## Project Overview

The Secure Trading Capturing System is a scalable and secure application designed to handle trading transactions with robust user authentication, token-based security mechanisms, and RESTful API integration. It ensures seamless transaction management, role-based access control, and efficient client-server communication.

---

## System Components

1. **Client Frontend**:
   - Built using modern JavaScript frameworks like Vue.js or React.js.
   - Manages user interactions and authentication (e.g., login, token storage).
   - Communicates with the backend for secure data exchange.

2. **Client Backend**:
   - Developed with Spring Boot (Java).
   - Implements business logic, user authentication, and secure communication with the authentication server.
   - Manages token validation and session handling.

3. **Authentication Server**:
   - Implements OAuth 2.0 or JWT for secure user authentication.
   - Handles login requests and generates tokens.
   - Redirects the user to the client application with authorization tokens.

4. **Database**:
   - **MySQL** for storing user details, roles, permissions, and transaction data.
   - Ensures data integrity and supports efficient query operations.

---

## Core Features

1. **User Authentication and Authorization**:
   - Users log in through the frontend, which sends credentials to the authentication server.
   - The authentication server validates credentials and returns a JWT token.
   - The frontend stores the token locally for subsequent API requests.

2. **Transaction Management**:
   - Backend provides APIs for capturing and managing transaction data.
   - APIs are protected by Spring Security to allow access only to authenticated users.

3. **Role-Based Access Control**:
   - Configured via Spring Security for managing roles and permissions.
   - Different user roles determine access to specific APIs or functionalities.

4. **Secure Communication**:
   - All communication between the frontend and backend is secured via HTTPS.
   - Sensitive data is encrypted both in transit and at rest.

5. **System Monitoring and Logging**:
   - Logs user activities and error information.
   - Includes performance monitoring and auditing features.

---

## Technology Stack

- **Frontend**: Vue.js / React.js
- **Backend**: Spring Boot + Spring Security
- **Database**: MySQL
- **Authentication**: OAuth 2.0 / JWT
- **Deployment**: Docker (supports deployment on AWS, Heroku, etc.)

---

## System Flow

1. The user initiates a login request from the frontend.
2. The frontend sends the login request to the authentication server.
3. The authentication server validates the credentials and returns a redirect URL with an authorization code.
4. The frontend exchanges the authorization code for an access token via the backend.
5. The backend retrieves the access token from the authentication server.
6. The frontend stores the access token in local storage for subsequent API calls.
7. The backend validates the token for every API request using Spring Security.

---

## Development Plan

1. **Requirement Analysis and Design** (1 Week):
   - Define functional modules and technology stack.
   - Design database models and system architecture.

2. **Frontend Development** (2 Weeks):
   - Implement the login interface and token management.
   - Design the user transaction management pages.

3. **Backend Development** (3 Weeks):
   - Configure Spring Security for authentication and authorization.
   - Develop RESTful APIs for transaction management.

4. **Integration and Testing** (2 Weeks):
   - Integrate frontend and backend, test for functionality and security.
   - Perform performance optimization and bug fixes.

5. **Deployment and Launch** (1 Week):
   - Configure Docker and deploy to cloud servers.
   - Enable monitoring and logging for production.

---

## How to Run Locally

### Prerequisites

- Node.js and npm (for the frontend)
- Java (JDK 11 or higher)
- MySQL
- Docker (optional for deployment)

### Steps

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/ZhenrongQu/STC-System.git
   cd STC-System
