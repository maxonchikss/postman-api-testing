# Test Cases

**Project:** JSONPlaceholder API Testing  
**Environment:** `https://jsonplaceholder.typicode.com`  
**Tool:** Postman  
**Test data:** Public mock API data

## Execution Summary

The project author reported a successful local collection run: **15 passed, 0 failed**. Re-run the collection before relying on this result after any changes.

## Test Cases

| ID | Scenario | Preconditions | Steps | Expected Result |
|---|---|---|---|---|
| TC-API-001 | Retrieve a post by ID | API is reachable | Send `GET /posts/1` | `200 OK`; JSON response contains `userId`, `id`, `title`, `body`; fields have expected types; `id = 1` |
| TC-API-002 | Retrieve all posts | API is reachable | Send `GET /posts` | `200 OK`; response is a non-empty array; post objects contain expected fields |
| TC-API-003 | Create a post | API is reachable | Send `POST /posts` with a JSON body containing `title`, `body`, and `userId` | `201 Created`; response contains the submitted values and a numeric `id` |
| TC-API-004 | Request a non-existent post | API is reachable | Send `GET /posts/999999` | `404 Not Found`; response body is an empty JSON object |
| TC-API-005 | Retrieve a user by ID | API is reachable | Send `GET /users/1` | `200 OK`; response contains `id`, `name`, `username`, and `email`; `id = 1`; field types are valid |

## Test Data

### TC-API-001
- Request: `GET /posts/1`
- Expected post ID: `1`

### TC-API-003
```json
{
  "title": "API testing portfolio",
  "body": "Created by a Postman test",
  "userId": 1
}
```

### TC-API-004
- Request: `GET /posts/999999`
- Purpose: verify handling of a non-existent resource.

## Scope Notes

- These test cases cover basic positive and negative API scenarios.
- The collection validates responses; it does not test authentication, rate limiting, load, or a production database.
- JSONPlaceholder simulates `POST` creation and does not persist the created resource.
