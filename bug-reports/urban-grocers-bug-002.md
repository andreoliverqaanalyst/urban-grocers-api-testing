# BUG-002 – API returns "isItPossibleToDeliver": true outside service operating hours

## Preconditions
- Urban Grocers API is available.

## Steps to Reproduce
1. Open Postman.
2. Configure a POST request to {{baseUrl}}/order-and-go/v1/delivery.
3. Set the request header Content-Type: application/json.
4. Test the following delivery times:
   - 07:59
   - 08:00
   - 22:00
   - 22:01
5. In the request body (JSON), insert:
   - deliveryTime: 07:59
   - productsCount: 5
   - productsWeight: 2
6. Send the request.

## Expected Result
- Status code: 200 OK.
- The response indicates:
  - isItPossibleToDeliver: false

## Actual Result
- Status code: 200 OK.
- The response indicates:
  - isItPossibleToDeliver: true

The comparison between expected and actual results for all tested scenarios (07:59, 08:00, 22:00, 22:01) is detailed in the attachments.

## Environment
- Urban Grocers REST API

Evidence (request and response details for all scenarios) is attached in Jira.
