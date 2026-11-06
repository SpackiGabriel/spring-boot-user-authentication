# Spring Boot User Authentication Service

This is a simple Spring Boot application that implements a user authentication service using Spring Security and JWT (JSON Web Tokens).

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

- Java Development Kit (JDK) 21
- Maven

### Installing

1. Clone the repository:

```bash
git clone https://github.com/SpackiGabriel/spring-boot-user-authentication.git
```

2. Navigate into the project directory:

```bash
cd spring-boot-user-authentication
```

3. Build the project using Maven:

```bash
mvn clean install
```

### Running the Application

You can run the application using Maven:

```bash
mvn spring-boot:run
```

The application will start at `http://localhost:8080`.

## Usage

Once the application is running, you can interact with it using any HTTP client such as cURL or Postman. Below are some example requests:

### Register a User

Send a POST request to `/auth/register` with a JSON body containing the user details:

```json
{
    "name": "Example User",
    "email": "exampleuser@example.com",
    "password": "examplepassword",
    "role": "USER"
}
```

### Authenticate User

Send a POST request to `/auth/login` with the user credentials:

```json
{
    "email": "exampleuser@example.com",
    "password": "examplepassword"
}
```

If the credentials are correct, you will receive a JWT token in the response.

### Access Protected Resource

To access a protected resource, include the JWT token in the `Authorization` header of your requests:

```makefile
Authorization: Bearer <JWT token>
```
### Built With

- Spring Boot - Framework for creating Spring applications
- Spring Web - Build web, including RESTful, applications using Spring MVC
- Spring Data JPA - Simplifies data access for relational databases
- Spring Security - Authentication and access control framework
- PostgreSQL - Open source object-relational database system
- Project Lombok - Java library that helps to reduce boilerplate code
- Auth0 Java JWT - Library for working with JSON Web Tokens (JWT) in Java
- Flyway - Database migration tool for java
