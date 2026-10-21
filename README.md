# Postman API Testing — JSONPlaceholder

A QA portfolio project demonstrating REST API testing with Postman, JavaScript assertions, and test documentation.

## Project overview

The collection tests the public [JSONPlaceholder](https://jsonplaceholder.typicode.com/) API. It covers successful responses, response structure and data types, simulated resource creation, and a non-existing resource.

> **Important:** JSONPlaceholder is a demo API. Write operations are simulated and do not persist data like a production service.

## Tech stack

- **Postman** — API requests and test execution
- **JavaScript** — automated response assertions
- **REST / HTTP / JSON** — API fundamentals
- **Git and GitHub** — version control and project delivery

## Repository structure

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

## Test coverage

| Request | Scenario | Main checks |
|---|---|---|
| `GET /posts/1` | Existing post | `200 OK`, JSON, required fields, data types, ID |
| `GET /posts` | List posts | `200 OK`, non-empty array, object structure |
| `POST /posts` | Create post (simulated) | `201 Created`, submitted fields, generated ID |
| `GET /posts/999999` | Non-existing post | `404 Not Found`, empty JSON object |
| `GET /users/1` | Existing user | `200 OK`, ID, name, username, email |

## Getting started

1. Install [Postman Desktop](https://www.postman.com/downloads/).
2. Download or clone this repository.
3. In Postman, select **Import**.
4. Import `postman/JSONPlaceholder.postman_collection.json`.
5. Open the imported collection and send a request.
6. Review the **Test Results** section below the response.

The collection uses a `baseUrl` variable set to `https://jsonplaceholder.typicode.com`.

## Running the automated checks

Each request includes JavaScript tests in its **Scripts → Post-response** section. To execute the entire collection:

1. Select the collection.
2. Click **Run**.
3. Run the requests in sequence.
4. Review passed and failed assertions in the Collection Runner.

For repeatable local or CI runs, the collection can also be executed with [Newman](https://learning.postman.com/docs/collections/using-newman-cli/command-line-integration-with-newman/), Postman's command-line collection runner.

## Test design approach

The project demonstrates:
- positive and negative scenarios;
- HTTP status-code validation;
- JSON response and schema-like field validation;
- data type and value assertions;
- validation of collection responses;
- readable test names and documented expected results.

## Test documentation

- [Test cases](test-cases/test-cases.md)
- [Bug report examples and reporting rules](bug-reports/bug-reports.md)

The bug-report file contains templates and hypothetical examples only. No real defects are claimed against JSONPlaceholder.

## Limitations

- This is a public demo service, not a production application.
- Some write operations are simulated.
- The project does not claim authentication, authorization, load, security, or database-persistence coverage.
- Execution results should be recorded only after running the collection.

## Author

QA Engineering portfolio project.

Feedback and suggestions are welcome.
