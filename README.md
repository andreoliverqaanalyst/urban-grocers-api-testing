# Urban Grocers – API Testing Project

This repository contains API testing artifacts developed during the QA Bootcamp, focusing on validating business rules, data integrity, and error handling for the **Urban Grocers** backend services.

The tests were executed using REST API requests, validating responses, status codes, and business logic related to order creation, delivery availability, and pricing calculations.

---

## 🔍 Scope of Testing

- Product quantity validation
- Delivery availability rules
- Delivery cost calculation based on weight and service type
- API error handling and response consistency

---

## Selected Bug Reports

Below are three representative API bugs identified during the testing process. These issues were selected to demonstrate critical validation gaps, business rule violations, and backend error handling problems.

---

###  BUG-001 – Empty string in `quantity` parameter causes 500 error (integer overflow)

**Description:**  
When an empty string is sent in the `quantity` parameter while adding a product to a kit via API, the system returns an unexpected **500 Internal Server Error**, indicating an integer overflow instead of handling the input validation properly.

**Impact:**  
This issue reveals missing input validation and can cause system instability or crashes when invalid data is submitted.

📎 *Evidence (request, response, and logs) is attached in Jira.*

---

### BUG-002 – API returns `"isItPossibleToDeliver": true` outside service operating hours

**Description:**  
The API incorrectly returns `"isItPossibleToDeliver": true` for delivery requests made outside the service’s operating hours.

**Impact:**  
This behavior violates business rules and may allow users to place orders that cannot be fulfilled, causing operational and customer experience issues.

📎 *Evidence (request and response payloads) is attached in Jira.*

---

### BUG-003 – `clientDeliveryCost` returned as 0 for Order and Go when weight exceeds 6kg

**Description:**  
For **Order and Go** service type, when the total order weight exceeds **6kg**, the API incorrectly returns `clientDeliveryCost` as **0**, instead of applying the correct delivery fee.

**Impact:**  
This bug can result in financial loss due to incorrect pricing calculation.

📎 *Evidence (request scenarios and API responses) is attached in Jira.*

---

## 🛠 Tools & Technologies

- REST API testing
- JSON
- HTTP status code validation
- Business rules validation
- Jira (bug tracking and evidence management)

---

## 📌 Notes

- All bugs were reported and tracked in Jira.
- Test evidence, including request/response payloads, screenshots, and logs, is available as Jira attachments.
- This repository highlights real-world API testing scenarios and common backend validation issues.

---
