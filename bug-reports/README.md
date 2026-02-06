# Urban Grocers – API Bug Reports

This folder contains a curated set of API bug reports identified during the QA Bootcamp project for **Urban Grocers**.  
The reported issues focus on **input validation**, **business rule enforcement**, and **delivery cost calculation** within the backend services.

The bugs were documented based on real API testing scenarios using Postman and were tracked and managed through Jira.

---

## Scope of Reported Issues

The bug reports in this folder cover the following areas:

- Delivery availability validation based on service operating hours
- Incorrect delivery cost calculation based on order weight
- Missing input validation for product quantity when adding items to kits

---

## Bug Reports Overview

### BUG-001 – ClientDeliveryCost returned as 0 for Order and Go when weight exceeds 6kg
Identifies an issue where the API returns an incorrect client delivery cost when the total order weight exceeds the defined limit for the Order and Go service.

### BUG-002 – API returns "isItPossibleToDeliver": true outside service operating hours
Highlights a business logic flaw where the API allows delivery outside the official service operating hours.

### BUG-003 – API validates quantity as 0 (zero) and returns 200 OK when adding product to kit
Demonstrates missing input validation, allowing invalid quantity values and returning a successful response instead of a client error.

---

## Tools & Technologies

- REST API testing
- Postman
- HTTP status code validation
- JSON request and response analysis
- Jira (bug tracking and evidence management)

---

##  Test Evidence

- All bugs were reported and tracked in **Jira**.

## 📝 Notes

- The bug reports were selected to represent common and critical backend validation issues.
- This folder is intended to demonstrate practical API testing skills and real-world QA documentation standards.

---

