# API Testing Project – JSONPlaceholder

##  Project Overview

This project demonstrates API testing using Postman on a sample REST API. It covers fundamental concepts of API testing including request validation, response validation, negative testing, and handling edge cases.

The goal of this project is to showcase practical QA skills in testing RESTful APIs and validating different scenarios in a structured and professional way.

---

##  Tools & Technologies

* Postman
* REST API
* JavaScript (Postman test scripts)

---

##  API Used

This project uses **JSONPlaceholder**, a free fake REST API for testing and prototyping.

⚠️ **Important Note:**
JSONPlaceholder is a mock API:

* It does NOT persist data
* POST, PUT, DELETE requests do not actually modify the database
* IDs returned in POST requests are fake and not retrievable later

Because of this limitation, static IDs are used for request chaining instead of dynamic ones.

---

##  Collection Structure

### 🔹 GET Requests

* Get all users
* Validate:

  * Status code (200)
  * Response format (array)
  * Required fields (id, name, email)
  * Data types
  * Email format
  * Response time

---

### 🔹 POST Requests

* Create new user
* Validate:

  * Status code (201)
  * Response contains name and id
  * Response format (JSON)
  * Response time
  * Data correctness

---

### 🔹 Negative Testing

* Invalid data (empty name)
* Empty request body
* Wrong data types (number instead of string)
* Special characters
* Edge cases (long input)

⚠️ Note: API accepts all inputs due to lack of validation

---

### 🔹 GET by ID (Chaining Requests)

* Retrieve user using `userId` from environment
* Validations:

  * Status code (200)
  * ID exists and is a number
  * Name exists

⚠️ Static ID is used because API does not persist created users

---

### 🔹 PUT Request

* Update user data
* Validate:

  * Status code (200)
  * Updated name is correct

---

### 🔹 DELETE Request

* Delete user
* Validate:

  * Status code (200)

---

##  Environment Variables

The project uses environment variables for flexibility:

```
baseUrl = https://jsonplaceholder.typicode.com
userId = 1
```

* `baseUrl`: API base endpoint
* `userId`: Static ID used for chaining requests

---

##  Test Coverage

This project includes:

* Functional testing
* Data validation
* Schema validation (basic)
* Negative testing
* Edge case testing
* Performance check (response time)

---

##  Limitations

Due to the nature of JSONPlaceholder:

* No real database operations occur
* Cannot fully test real-world scenarios like authentication, authorization, or data persistence
* Chaining requests is simulated using static values

---

##  Future Improvements

* Test a real API advanced testing
* Integrate with CI/CD pipeline
* Expand test coverage (headers, security, etc.)

---

##  Conclusion

This project demonstrates a solid foundation in API testing using Postman. It includes structured test cases, validations, and different testing scenarios, making it suitable for showcasing QA skills in a portfolio or CV.
