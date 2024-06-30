# Spring Boot CRM

Spring Boot CRM is a simple Customer Relationship Management (CRM) application built using Spring Boot and Thymeleaf. It provides basic CRUD functionalities for managing customer data and incorporates Spring Security for authentication.

## Table of Contents

- [Features](#features)
- [Setup](#setup)
  - [Prerequisites](#prerequisites)
  - [Running the Application](#running-the-application)
- [Technologies Used](#technologies-used)
- [Project Structure](#project-structure)
- [Usage](#usage)
  - [Navigating the Application](#navigating-the-application)
  - [Managing Customers](#managing-customers)
  - [Authentication and Authorization](#authentication-and-authorization)

## Features

- **CRUD Operations**: Create, Read, Update, and Delete customer records.
- **Pagination and Sorting**: Display customers in a paginated and sortable data grid.
- **Search and Filter**: Search customers by various fields like name, city, and country.
- **Validation**: Includes basic validation for customer data inputs.
- **Authentication**: Integrates Spring Security for user authentication and authorization.
- **Role-based Access Control**: Supports roles for administrators, standard users, and read-only users.
- **Dynamic UI**: Uses Thymeleaf templates with Bootstrap for responsive and dynamic user interface.

## Setup

### Prerequisites

- Java 17 (or later)
- Gradle or Maven
- IDE (IntelliJ IDEA recommended)

### Running the Application

1. **Clone the repository**:
   ```bash
   git clone https://github.com/4d4r5h/crm-application.git
   cd crm-application
   ```

2. **Build and run using Gradle**:
   ```bash
   ./gradlew bootRun
   ```

   or

   **Build and run using Maven**:
   ```bash
   mvn spring-boot:run
   ```

3. Access the application at [http://localhost:8080](http://localhost:8080).

## Technologies Used

- Java 17
- Spring Boot 3
- Spring Security 6
- Thymeleaf
- Bootstrap
- H2 Database (in-memory)
- Lombok

## Project Structure

The project follows a typical Spring Boot structure:

- **src/main/java**: Contains Java source code.
  - `com.example.crm`: Main application package.
    - `config`: Configuration classes (SecurityConfig, WebMvcConfig).
    - `controllers`: MVC controllers (CustomerWebController, UserWebController).
    - `dto`: Data Transfer Objects (UserDTO).
    - `entities`: JPA entities (Customer, User).
    - `repositories`: Data repositories (CustomerRepository, UserRepository).
    - `security`: Security related classes (CustomUserDetails, CustomUserDetailsService).
    - `services`: Business logic services (CustomerService, UserService).
    - `init`: Initialization tasks (Bootstrap).
- **src/main/resources**: Contains application resources.
  - `application.properties`: Configuration properties.
  - `data.sql`: SQL script for initializing sample data (customers).
  - `schema.sql`: SQL script for database schema.
  - `templates`: Thymeleaf templates (customer, user).
  - `static`: Static resources (CSS, JS).

## Usage

### Navigating the Application

- **Home Page**: Welcome screen with links to manage customers and, for administrators, manage users.
- **Customer Management**: CRUD operations for managing customer records.
- **User Management**: For administrators only, manage user accounts including roles and permissions.

### Managing Customers

- **Listing Customers**: View a paginated list of customers with search and sort capabilities.
- **Adding Customers**: Create new customer records with validation checks.
- **Editing Customers**: Update existing customer details.
- **Deleting Customers**: Remove customer records from the database.

### Authentication and Authorization

- **Login**: Access the application using username and password (provided during startup for demo users).
- **Logout**: Securely log out of the application.