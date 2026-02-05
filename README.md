# API Test Cases — Urban Grocers

This document presents a selected set of **manual API test cases** executed
for the **Urban Grocers** application.

The test cases focus on validating HTTP methods, status codes, request/response
payloads, and error handling using REST principles.

Only a representative subset of test cases is included for portfolio purposes.

---

## TC-API-001 — Retrieve product list successfully (GET)

**Endpoint**  
`GET /api/v1/products`

**Preconditions**
- API is available
- Valid base URL is configured

**Steps**
1. Send a GET request to the products endpoint.
2. Observe the response status code and response body.

**Expected Result**
- Status code **200 OK** is returned.
- Response body contains a list of products.
- Product attributes are returned in JSON format.

---

## TC-API-002 — Create a new order successfully (POST)

**Endpoint**  
`POST /api/v1/orders`

**Preconditions**
- API is available
- Valid request payload is prepared

**Steps**
1. Send a POST request with valid order data in the request body.
2. Observe the response.

**Expected Result**
- Status code **201 Created** is returned.
- The order is created successfully.
- The response body contains the created order details.

---

## TC-API-003 — Validate error when creating order with invalid payload (POST)

**Endpoint**  
`POST /api/v1/orders`

**Preconditions**
- API is available
- Invalid or incomplete request payload is prepared

**Steps**
1. Send a POST request with invalid data in the request body.
2. Observe the response status code and message.

**Expected Result**
- Status code **400 Bad Request** is returned.
- An error message is displayed indicating invalid input.

---

## TC-API-004 — Retrieve non-existing resource (GET)

**Endpoint**  
`GET /api/v1/products/{id}`

**Preconditions**
- API is available
- A non-existing product ID is used

**Steps**
1. Send a GET request using a non-existing product ID.
2. Observe the response.

**Expected Result**
- Status code **404 Not Found** is returned.
- The response indicates that the resource does not exist.

---

## Tools & Techniques
- REST API testing
- HTTP methods (GET, POST)
- Status code validation
- Request and response body validation
- Manual API testing (Postman)

---

## 📎 Additional Documentation
The complete set of API test cases was originally documented in spreadsheet
format during the project execution and is included in this repository
for reference.
