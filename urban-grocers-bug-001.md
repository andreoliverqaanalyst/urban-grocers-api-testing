# BUG-001 – ClientDeliveryCost returned as 0 for Order and Go when weight exceeds 6kg

## Preconditions
- Urban Grocers API is available.

## Steps to Reproduce
1. Open Postman.
2. Configure a POST request to {{baseUrl}}/order-and-go/v1/delivery.
3. Set the request header Content-Type: application/json.
4. In the request body (JSON), insert:
   - deliveryTime: 9
   - productsCount: 10
   - productsWeight: 6.1
5. Send the request.

## Expected Result
- Status code: 200 OK
- Response:
  - isItPossibleToDeliver: true
  - hostDeliveryCost: 5
  - clientDeliveryCost: 9

## Actual Result
- Status code: 200 OK
- Response:
  - isItPossibleToDeliver: true
  - hostDeliveryCost: 5
  - clientDeliveryCost: 0

## Environment
- Urban Grocers REST API

Evidence (request and response details) is attached in Jira.
