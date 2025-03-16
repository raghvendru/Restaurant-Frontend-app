# Restaurant Service Suite

## Overview

The Restaurant Service Suite is a collection of microservices designed to provide a comprehensive solution for managing restaurant operations. This suite includes services for managing restaurant listings, orders, user information, food catalogues, and service discovery.

## Components

### 1. Restaurant Listing Service
- **Description**: Manages the details of restaurants, including their names, locations, and menus.
- **Endpoints**:
  - `GET /restaurants`: Retrieve a list of all restaurants.
  - `POST /restaurants`: Add a new restaurant.
  - `PUT /restaurants/{id}`: Update restaurant details.
  - `DELETE /restaurants/{id}`: Remove a restaurant.

### 2. Order Service
- **Description**: Handles customer orders, including order creation, updates, and status tracking.
- **Endpoints**:
  - `GET /orders`: Retrieve a list of all orders.
  - `POST /orders`: Create a new order.
  - `PUT /orders/{id}`: Update order details.
  - `DELETE /orders/{id}`: Cancel an order.

### 3. User Information Service
- **Description**: Manages user profiles, preferences, and authentication.
- **Endpoints**:
  - `GET /users`: Retrieve a list of all users.
  - `POST /users`: Register a new user.
  - `PUT /users/{id}`: Update user information.
  - `DELETE /users/{id}`: Remove a user.

### 4. Food Catalogue Service
- **Description**: Manages the food items available in the restaurant, including descriptions and prices.
- **Endpoints**:
  - `GET /catalogue`: Retrieve the food catalogue.
  - `POST /catalogue`: Add a new food item.
  - `PUT /catalogue/{id}`: Update food item details.
  - `DELETE /catalogue/{id}`: Remove a food item.

### 5. Eureka Service
- **Description**: Service discovery for microservices, allowing them to find and communicate with each other.
- **Endpoints**:
  - `GET /eureka/apps`: Retrieve registered services.
  - `POST /eureka/apps`: Register a new service.
  - `DELETE /eureka/apps/{serviceId}`: Deregister a service.

### 6. Deployment Folder
- **Description**: Contains deployment scripts and configuration files for deploying the microservices.
- **Contents**:
  - Dockerfiles for each service.
  - Kubernetes configuration files (if applicable).
  - Scripts for CI/CD pipelines.

## Technologies Used

- **Java**: The primary programming language for the services.
- **Spring Boot**: Framework for building the microservices.
- **Docker**: Containerization for easy deployment.
- **Maven**: Build tool for managing dependencies and building the project.
- **Eureka**: Service discovery for microservices.
- **SonarQube**: Code quality and security analysis.

## Getting Started

### Prerequisites

- Java 17 or higher
- Maven
- Docker
- Git

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/raghvendru/Restaurant-Service.git
   cd Restaurant-Service
   ```

2. Build the project using Maven:
   ```bash
   mvn clean package -DskipTests
   ```

3. Run the application:
   ```bash
   java -jar target/restaurant-service.jar
   ```

### Docker Setup

To build and run the application using Docker:

1. Build the Docker image:
   ```bash
   docker build -t restaurant-service .
   ```

2. Run the Docker container:
   ```bash
   docker run -p 8080:8080 restaurant-service
   ```

## Usage

- Access the API at `http://localhost:8080/api`
- Use tools like Postman or curl to interact with the endpoints.

## Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature/YourFeature`).
3. Make your changes and commit them (`git commit -m 'Add some feature'`).
4. Push to the branch (`git push origin feature/YourFeature`).
5. Create a new Pull Request.



## Acknowledgments

- Thanks to all contributors and the open-source community for their support.
