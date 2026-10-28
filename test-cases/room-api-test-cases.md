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
