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

The ecpected behavior for an invalid room ID has not yet been confirmed against the API specification. This finding is documented for further investigatioin rather than being classified as a confirmed defect.

**Project Status**
In Progress
Furure improvements will include additional API scenarios, expanded test coverage, execution evidence, and introductory automated testing.

**Author**
QA learner building practical sill in a API  testing, test case design defect investigation, and test documentation
