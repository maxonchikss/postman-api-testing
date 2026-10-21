# Test Cases — JSONPlaceholder API

**Environment:** `https://jsonplaceholder.typicode.com`  
**Format:** REST API / JSON  
**Note:** Expected results describe the behavior currently provided by this demo API.

| ID | Title | Preconditions | Steps / Test data | Expected result |
|---|---|---|---|---|
| TC-001 | Get an existing post | API is reachable | Send `GET /posts/1` | `200 OK`; response is JSON object with `userId`, `id`, `title`, `body`; ID equals `1` |
| TC-002 | Get the list of posts | API is reachable | Send `GET /posts` | `200 OK`; response is a non-empty array; each item has the expected post fields |
| TC-003 | Create a post | API is reachable | Send `POST /posts` with valid JSON containing `title`, `body`, `userId` | `201 Created`; response contains submitted fields and an ID; persistence is not expected |
| TC-004 | Request a non-existing post | API is reachable | Send `GET /posts/999999` | `404 Not Found`; response body is an empty JSON object |
| TC-005 | Get an existing user | API is reachable | Send `GET /users/1` | `200 OK`; response contains `id`, `name`, `username`, `email`; ID equals `1` |

## Execution record

Fill this section after running the collection in Postman.

| Date | Collection run | Passed | Failed | Notes |
|---|---|---:|---:|---|
| TBD | Not run yet | — | — | Record actual results after execution |
