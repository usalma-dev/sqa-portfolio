# Test Plan — Sauce Demo Web Application

| Field | Details |
|---|---|
| **Document Version** | 1.0 |
| **Date** | 16 May 2026 |
| **Prepared by** | U Salma |
| **Application** | Sauce Demo — https://www.saucedemo.com |
| **Status** | Final |

---

## 1. Introduction

Sauce Demo is a demo e-commerce web application built specifically for practicing testing. It simulates a real online shopping experience including login, product browsing, cart management, and checkout. This test plan defines the scope, approach, and resources for manual functional testing of the application.

---

## 2. Scope

### In Scope
- Login and logout functionality
- Product listing page (sorting, display)
- Product detail page
- Add to cart / Remove from cart
- Shopping cart page
- Checkout flow (personal info, order summary, order confirmation)
- Form field validation
- UI consistency checks

### Out of Scope
- Payment gateway processing
- Backend / database layer
- API testing
- Performance and load testing
- Mobile browsers

---

## 3. Test Objectives

- Verify that all standard user flows work correctly end to end
- Confirm that locked-out users cannot access the application
- Identify visual and functional defects introduced by `problem_user`
- Ensure form validation works on checkout
- Confirm the cart maintains correct item counts and prices

---

## 4. Testing Types

Test Type

| Smoke Testing | Confirm the app is stable and login works before deeper testing |
| Functional Testing | Verify each feature works according to expected behavior |
| Negative Testing | Test with invalid inputs and locked accounts |
| UI Testing | Check for broken images, misaligned elements, incorrect text |
| Regression Awareness | Note any areas where `problem_user` behavior differs from `standard_user` |

---

## 5. Test Environment

| Item | Details |
|---|---|
| URL | https://www.saucedemo.com |
| Browser | Google Chrome 147.0.7727.138 (Official Build) (64-bit) |
| OS | Windows 11 Pro |
| Device | Desktop |
| Tools | Chrome DevTools, Snipping Tool |
| Test Data | Credentials provided by the application (please see README) |

---

## 6. Entry and Exit Criteria

### Entry Criteria
- Application is accessible at the URL
- All test cases are written and ready
- Tester has valid credentials

### Exit Criteria
- All planned test cases have been executed
- All found bugs are documented with full defect attributes
- Test report is completed

---

## 7. Defect Management

All defects will be documented with the following attributes:

| Attribute | Description |
|---|---|
| Bug ID | Unique identifier |
| Title | Short description of the defect |
| Module | Feature area where the bug was found |
| Steps to Reproduce | Numbered steps to trigger the bug |
| Expected Result | What should happen |
| Actual Result | What actually happens |
| Severity | Critical / Major / Average / Minor |
| Priority | High / Medium / Low |
| Screenshot | Visual evidence |

### Defect Lifecycle
Open → Assigned → In Progress → Fixed → Re-tested → Closed
(If fix is invalid: Re-tested → Reopened)

---

## 8. Risks and Mitigations

| Risk | Mitigation |
|---|---|
| Demo app may be reset between sessions | Re-verify environment before each session |
| No backend access | Focus on front-end functional and UI testing |
