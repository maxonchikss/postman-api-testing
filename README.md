# Postman API Testing

A project demonstrating REST API testing using Postman and JavaScript.

## Overview

This project contains a Postman collection for testing the [JSONPlaceholder](https://jsonplaceholder.typicode.com/) REST API. It covers common API testing scenarios, including retrieving resources, creating records, validating response structures, and handling requests to non-existent resources.

## Tech Stack

- **Postman** — API requests and automated test execution
- **JavaScript** — test assertions and response validation
- **REST API** — HTTP methods and status codes
- **JSON** — response structure and data type validation
- **Git and GitHub** — version control and project management

## Test Coverage

| Endpoint | Method | Test Scenarios |
|---|---|---|
| `/posts/1` | GET | Status code, response structure, required fields, data types, and resource ID |
| `/posts` | GET | Status code, response array, and object structure |
| `/posts` | POST | Creation status code and response field validation |
| `/posts/999999` | GET | Handling requests to non-existent resources |
| `/users/1` | GET | Status code, required fields, and data types |

## Testing Techniques

- HTTP status code validation
- JSON response structure validation
- Required field and data type checks
- Positive and negative test scenarios
- API response assertions using JavaScript
- Validation of resource creation and error handling

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

## Test Documentation

- **Test Cases:** `test-cases/test-cases.md`
- **Bug Reports:** `bug-reports/bug-reports.md`

## Notes

This is an educational portfolio project intended to demonstrate fundamental REST API testing skills.
