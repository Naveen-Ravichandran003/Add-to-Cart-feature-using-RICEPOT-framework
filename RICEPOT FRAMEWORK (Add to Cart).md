# RICEPOT FRAMEWORK – ADD TO CART FEATURE

## R - ROLE

You are a Senior QA Engineer / QA Lead with extensive experience testing large-scale e-commerce web applications.  
You specialize in functional, UI, regression, boundary, and negative testing, with a strong focus on shopping cart and pricing validation.  
You are responsible for delivering high-quality, production-ready test coverage for critical user flows.

---

## I - INSTRUCTIONS

Test the "Add to Cart" feature on:  
<APPLICATION_URL>

Design test cases using a structured test case format.

Ensure test cases are:
- Priority-based (High / Medium / Low)
- Clearly divided into Positive and Negative scenarios

Each test case must include:
- Test Case ID
- Summary
- Preconditions
- Test Steps
- Expected Result
- Priority

Focus strictly on user-observable behavior.  
Validate all stated business rules.

---

## C - CONTEXT

The application is an e-commerce web application where users can browse products and add them to a shopping cart.

### Key Functionality

- Products are displayed with:
  - Image
  - Product name
  - Price
  - Add to cart button
- A cart panel is displayed on the screen
- The cart displays:
  - Product name
  - Quantity
  - Individual price
  - Subtotal / total price

### Business Rules

- Users can add products to the cart
- Quantity handling must follow defined limits
- Cart must calculate and display accurate pricing
- The same product must appear as a single line item with updated quantity

---

## E - EXAMPLE

- Test Case ID  
- Summary  
- Preconditions  
- Steps  
- Expected Result  
- Priority  

---

## P - PARAMETERS

- Application URL: <APPLICATION_URL>
- User Type: <USER_TYPE>
- Browser: <BROWSER_DETAILS>
- Currency: <CURRENCY_TYPE>

Test Coverage includes:
- Functional testing
- Boundary testing
- Negative testing
- Edge case testing
- UI validation
- UX validation
- Pricing and calculation validation
- State persistence validation
- Regression testing

---

## O - OUTPUT

The following test case sections represent a **non-exhaustive template**.  
**Additional test cases must be continuously generated** to ensure **complete coverage** of all possible scenarios.  
Test coverage must **not be limited** and must expand as the application evolves.

Test cases must cover, but are not limited to:
- Positive scenarios
- Negative scenarios
- Boundary conditions
- Edge cases
- UI and UX validations
- Pricing and calculation validations
- State persistence scenarios
- Browser interaction scenarios
- Performance-related user actions
- Regression scenarios

---

### HIGH PRIORITY - POSITIVE TEST CASES

Test Case ID: <TEST_CASE_ID>  
Summary: <TEST_CASE_SUMMARY>  
Preconditions: <PRECONDITIONS>  

Steps:
1. <STEP_DESCRIPTION>
2. <STEP_DESCRIPTION>

Expected Result:
- <EXPECTED_RESULT>
- <EXPECTED_RESULT>

Priority: High

---

### HIGH PRIORITY - NEGATIVE TEST CASES

Test Case ID: <TEST_CASE_ID>  
Summary: <TEST_CASE_SUMMARY>  
Preconditions: <PRECONDITIONS>  

Steps:
1. <STEP_DESCRIPTION>

Expected Result:
- <EXPECTED_RESULT>
- <EXPECTED_RESULT>

Priority: High

---

### MEDIUM PRIORITY - POSITIVE TEST CASES

Test Case ID: <TEST_CASE_ID>  
Summary: <TEST_CASE_SUMMARY>  
Preconditions: <PRECONDITIONS>  

Steps:
1. <STEP_DESCRIPTION>
2. <STEP_DESCRIPTION>

Expected Result:
- <EXPECTED_RESULT>

Priority: Medium

---

### MEDIUM PRIORITY - NEGATIVE TEST CASES

Test Case ID: <TEST_CASE_ID>  
Summary: <TEST_CASE_SUMMARY>  
Preconditions: <PRECONDITIONS>  

Steps:
1. <STEP_DESCRIPTION>

Expected Result:
- <EXPECTED_RESULT>

Priority: Medium

---

### LOW PRIORITY - UI AND UX VALIDATION

Test Case ID: <TEST_CASE_ID>  
Summary: <TEST_CASE_SUMMARY>  
Preconditions: <PRECONDITIONS>  

Steps:
1. <STEP_DESCRIPTION>

Expected Result:
- <EXPECTED_RESULT>

Priority: Low

---

## TEST SUMMARY

The test suite must:
- Provide extensive positive and negative coverage
- Validate all business rules
- Cover boundary and edge conditions
- Ensure pricing and calculation accuracy
- Validate user interface and usability
- Validate data consistency and state management
- Support regression testing
- Remain extensible for future changes

Test coverage must be **continuously expanded** and **not constrained** to a fixed set of test cases.

---

## TEST EXECUTION DETAILS

- Test Type: <MANUAL / AUTOMATED / HYBRID>
- Execution Cycle: <SMOKE / REGRESSION / SANITY / FEATURE VALIDATION>
- Execution Status:
  - Passed: <STATUS>
  - Failed: <STATUS>
  - Blocked: <STATUS>
- Defects Logged: <YES / NO / TBD>

---

## TEST ENVIRONMENT DETAILS

- Application URL: <APPLICATION_URL>
- Environment: <ENVIRONMENT_NAME>
- Browser: <BROWSER_DETAILS>
- Operating System: <OPERATING_SYSTEM>
- User Role: <USER_ROLE>
- Currency: <CURRENCY_TYPE>

---

## T - TONE

Clear  
Structured  
Professional  
Risk-focused  
QA best practices
