# BUG-003 – API validates quantity as 0 (zero) and returns 200 OK when adding product to kit

## Preconditions
- Urban Grocers API is available.
- An existing kit is available (e.g., Kit ID 3).
- A valid product is available to be added (e.g., Product ID 70).

## Steps to Reproduce
1. Open Postman.
2. Configure a POST request to {{baseUrl}}/api/v1/kits/3/products.
3. Set the request header Content-Type: application/json.
4. In the request body (JSON), insert:
   - productId: 70
   - quantity: 0
5. Send the request.

## Expected Result
- Status code: 400 Bad Request.
- A clear validation error message indicating that quantity with value 0 (zero) is invalid.

## Actual Result
- Status code: 200 OK.
- The API successfully adds the product to the specified kit.

## Environment
- Urban Grocers REST API

Evidence (request and response details) is attached in Jira.
