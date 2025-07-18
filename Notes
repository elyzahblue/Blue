Bugs Found (These are covered in the tests code written, expect the tests to fail)
1. GET todoitems/{id}
  Input: non-existing valid id
  Actual Result: Returns 404 NotFound
  Expected Result: Should return 200 OK with response body = empty/null
2. POST todoitems
  Input: existing Id (duplicate)
  Actual Result: Returns 500 Internal Server Error
  Expected Result: Should return 409 Conflict with error message in response body
3. PUT todoitems
  Input: valid request, existing item to update
  Actual Result: Returns 204 NoContent
  Expected Result: Should return 200 OK
4. PUT todoitems
  Input: valid request, new item to create
  Actual Result: Returns 204 NoContent
  Expected Result: Should return 201 Created
5. DELETE todoitems
  Input: Valid request, existing ID
  Actual Result: Returns 200 OK but still deletes the file 
  Expected Result: Should return 204 Content
  Note: Did not write a failing test for this as 200 OK is acceptable for now. Negotiable.

NFR Findings/Recommendations:
1. Security
  - Implement rate limiting access in header to prevent DoS attacks for multiple simultaneous calls
  - Add authentication and session token to limit access to the endpoints
  - Add validation of user inputs to protect against SQL injection
2. Logging
  - Add logging to monitor APIs
3. Increased performance and reduced latency
  - Support caching of APIs
  - Support indexing to optimize database
  - Implement filtering, sorting and pagination for GET that returns a large sets of data
4. API versioning
  - add version in uri to support backward compatability
5. Documentation
  - Add documentation in code
  - Add complete documentation in swagger
