# Room API Test Cases

## TC-001: Get Room by Valid ID

- *Objective:* Verify that the API returns room details for a valid room ID.
- *Preconditions:* The API is accessible and room ID 1 is valid.
- *Method:* GET
- *Endpoint:* /api/room/1
- *Expected Result:* The API returns 200 OK and the room details.
- *Actual Result:* The API returned 200 OK with the room details.
- *Status:* PASS

## TC-002: Verify Required Room Fields

- *Objective:* Verify that the response contains all required room fields.
- *Preconditions:* Room ID 1 is valid.
- *Method:* GET
- *Endpoint:* /api/room/1
- *Expected Result:* The response contains roomid, roomName, roomPrice, and type.
- *Actual Result:* All four fields were present in the response.
- *Status:* PASS

## TC-003: Verify Room Price

- *Objective:* Verify that the room price is a positive number.
- *Preconditions:* Room ID 1 is valid.
- *Method:* GET
- *Endpoint:* /api/room/1
- *Expected Result:* roomPrice is numeric and greater than zero.
- *Actual Result:* The response contained a positive numeric room price.
- *Status:* PASS

## TC-004: Investigate Invalid Room ID

- *Objective:* Investigate the API behavior for an invalid room ID.
- *Preconditions:* The expected behavior for an invalid ID must be confirmed.
- *Method:* GET
- *Endpoint:* /api/room/4
- *Expected Result:* The API returns the documented error response for an invalid room ID.
- *Actual Result:* The API returned 500 Internal Server Error.
- *Status:* UNDER INVESTIGATION

*Note:* The expected behavior for an invalid room ID has not yet been confirmed against the API specification. This result is not classified as a confirmed defect.

## Additional API Tests — Get All Rooms

*Endpoint:* GET /api/room/

| Test ID | Test Scenario | Expected Result | Actual Result | Status |
|---|---|---|---|---|
| TC-005 | Verify the rooms property exists and is an array | Response contains a rooms array | rooms property exists and is an array | PASS |
| TC-006 | Verify the response contains at least one room | The rooms array contains at least one room | Three rooms returned | PASS |
| TC-007 | Verify required fields for each room | Each room contains roomid, roomName, roomPrice, and type | Required fields are present in all returned rooms | PASS |
| TC-008 | Verify room field data types | roomid and roomPrice are numbers; roomName and type are strings | All validated field types match expectations | PASS |

*Execution notes:* These tests were executed in Postman against the room-list endpoint. All four tests passed during the recorded execution.

*Investigation note:* Individual room requests using GET /api/room/1, /2, and /3 returned 500 Internal Server Error during testing. The cause and expected behavior remain unconfirmed; this is recorded as an investigation item, not a confirmed defect.
