# Postman API Testing

A project demonstrating REST API testing with Postman and JavaScript.

## Overview

The collection targets [JSONPlaceholder](https://jsonplaceholder.typicode.com/), a public mock REST API. It covers resource retrieval, simulated record creation, response validation, and handling a request for a non-existent resource.

## Tech Stack

- **Postman** — sending HTTP requests and running the collection
- **JavaScript** — automated assertions
- **REST API / HTTP** — methods and status codes
- **JSON** — response structure and data type validation
- **Git and GitHub** — version control

## Test Coverage

| Endpoint | Method | Coverage |
|---|---|---|
| `/posts/1` | GET | Status code, content type, required fields, data types, resource ID |
| `/posts` | GET | Status code, non-empty array, post structure |
| `/posts` | POST | Creation status code, submitted fields, response ID |
| `/posts/999999` | GET | Not-found status and empty response object |
| `/users/1` | GET | Status code, required user fields, data types and ID |

The collection contains **15 assertions** across five requests. Run the current collection in Postman to generate and verify the latest execution results.

## Testing Techniques

- HTTP status code validation
- JSON response and field validation
- Data type checks
- Positive and negative scenarios
- Request body and response data comparison
- Automated assertions using Postman scripts

## Project Structure

```text
postman-api-testing/
├── postman/
│   └── JSONPlaceholder.postman_collection.json
├── test-cases/
│   └── test-cases.md
├── bug-reports/
│   └── bug-reports.md
├── .gitignore
└── README.md
```

## Getting Started

1. Clone the repository:

   ```bash
   git clone https://github.com/maxonchikss/postman-api-testing.git
   ```

2. Open Postman and import `postman/JSONPlaceholder.postman_collection.json`.
3. Open the collection and select **Run**.
4. Review the result of each request and its assertions.

## Test Documentation

- [Test Cases](test-cases/test-cases.md)
- [Bug Report Documentation](bug-reports/bug-reports.md)

## Limitations

JSONPlaceholder is a mock API. A successful `POST /posts` response simulates record creation; the new record is not persisted in a real database.

This project is intended to demonstrate foundational REST API testing skills.
