# URL Shortener - Backend

This is the backend component of a URL Shortener application built with **Spring Boot**. It provides REST APIs for generating shortened URLs and redirecting them to the original URLs.

## Features

- Shortens long URLs via a RESTful endpoint
- Redirects short URLs to their original destination
- Basic input validation
- In-memory storage (can be extended to database)
- CORS enabled for frontend integration

## Technologies Used

- Java 17+
- Spring Boot
- Spring Web
- Maven

## API Endpoints

| Method | Endpoint           | Description                    |
|--------|--------------------|--------------------------------|
| POST   | `/api/shorten`     | Accepts a long URL, returns a short code |
| GET    | `/{shortCode}`     | Redirects to the original URL  |

## Example Request

### POST `/api/shorten`
```json
{
  "longUrl": "https://www.example.com/some/very/long/path"
}

Response

{
  "shortUrl": "http://localhost:8080/abc123"
}

Run the Project

# Build the project
mvn clean install

# Run the application
mvn spring-boot:run


Future Enhancements
Add database support (e.g., MySQL, PostgreSQL)

Add analytics (e.g., click count, timestamps)

User authentication and URL ownership.
