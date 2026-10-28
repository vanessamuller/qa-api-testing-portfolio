**QA API Testing Portfolio**

**Project Overview**
This Project demostrates my practical skills in manual API testing using Postman. It includes test case design, response validation, test documentation, and investigation of unexpected API behaviour.
The goal is to apply QA fundamentals to real API and document the testying process in a structured, professional format.

**Tools & Technologies**
- Postman - API requests and response validation
- REST API - HTTP methods, status codes, and JSON responses
- GitHub - Project documentation and version control

**Project Scope**
The current scope focuses on testing the room details endpoint:

GET /api/room/{id}

Testing activities include:
- Validating successful API responses
- Verifying required response fields
- Checking data types and room price values
- Investigating API Behavior for an invalid room
- Documenting test cases and execution results

**Test Documentation**

The project includes the following test cases:

| Test Case ID | Description | Status |
|---|---|---|
| TC-001 | Retrieve room details using a valid ID | Pass |
| TC-002 | Verify requires room fields | Pass |
| TC-003 | Verify room price is valid | Pass |
| TC-004 | Investigate response for an invalid room ID | Under investigation |

Findings
During testing, the API returned 500 Internal Server Eoor when requesting room ID 4.

The expected behavior for an invalid room ID has not yet been confirmed against the API specification. This finding is documented for further investigatioin rather than being classified as a confirmed defect.

## How to Run the API Tests

1. Download the Postman collection JSON file from this repository.
2. Open Postman.
3. Select *Import* and upload the downloaded JSON file.
4. Open the QA API Practice collection.
5. Select a request and click *Send*.
6. Review the response status, response body, and test results.

## API Base URL

https://automationintesting.online

## Notes

This is a learning project using a public practice API. Results may vary if the API changes or becomes unavailable.
**Project Status**
In Progress
Furure improvements will include additional API scenarios, expanded test coverage, execution evidence, and introductory automated testing.

**Author**
QA learner building practical sill in a API  testing, test case design defect investigation, and test documentation

## Project Structure

- test-cases/room-api-test-cases.md — Manual test cases and execution results.
- QA API Practice — Postman collection containing API requests and automated tests.

## Test Coverage

The current API tests validate:

- Response structure and the rooms property.
- Presence of room data.
- Required fields for each room.
- Data types for room fields.

## Current Findings

The room-list endpoint (GET /api/room/) returned three rooms during testing, and all four automated checks passed.

Individual room requests (GET /api/room/{id}) returned 500 Internal Server Error during testing. This behavior remains under investigation.
