# Lab 2: Product Catalogue REST API

[![CI](https://github.com/p3ter-dev/Lab-2/actions/workflows/ci.yml/badge.svg)](https://github.com/p3ter-dev/Lab-2/actions/workflows/ci.yml)

A Spring Boot-based REST API for managing a product catalogue. This project implements full CRUD operations, robust request validation, standardized error handling (RFC 9457), and automated testing.

## Setup Instructions

### Prerequisites
- Java 21 installed on your machine
- Git

### Running the Application Locally
1. Clone the repository and navigate into the project directory.
2. Run the application using the included Maven wrapper.

On **Windows**:
```cmd
.\mvnw.cmd spring-boot:run
```

On **macOS / Linux**:
```bash
./mvnw spring-boot:run
```

3. The application will start on port `8080` connected to an in-memory H2 database.

## API Documentation (Swagger)

This project uses OpenAPI (Swagger) to automatically generate interactive API documentation. 

Once the application is running, you can view the Swagger UI here:  
👉 **[http://localhost:8080/swagger-ui.html](http://localhost:8080/swagger-ui.html)**

## API Endpoints

The API is exposed under the `/api/v1/products` base path.

| Method | Endpoint | Description |
|--------|----------|-------------|
| `GET` | `/api/v1/products` | Retrieve a list of all products |
| `GET` | `/api/v1/products/{id}` | Retrieve a specific product by its ID |
| `POST` | `/api/v1/products` | Create a new product |
| `PUT` | `/api/v1/products/{id}` | Update an existing product by its ID |
| `DELETE` | `/api/v1/products/{id}` | Delete a product by its ID |

## Testing

To run the automated MockMvc and Context Load test suite, run the following command:

```cmd
.\mvnw.cmd clean test
```
