# API Testing with Postman

This mini project demonstrates basic API testing using Postman.

##  What I learned

- Sending GET requests
- Sending POST requests
- Working with JSON body
- Writing tests using JavaScript
- Validating status codes

## Tools

- Postman

##  Test Scenarios

### GET Request
- Fetch data from API
- Validate status code = 200

### POST Request
- Send data using JSON body
- Validate status code = 201

##  Example Tests

```javascript
pm.test("Successful POST request", function () {
    pm.expect(pm.response.code).to.be.oneOf([200, 201]);
});
