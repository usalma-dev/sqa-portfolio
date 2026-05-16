# Test Execution Report — Sauce Demo Web Application

| Field | Details |
|---|---|
| **Prepared by** | [U Salma] |
| **Date** | 16 May 2026 |
| **Application** | https://www.saucedemo.com |
| **Test Period** | 16 May 2026 |
| **Browser** | Google Chrome 147.0.7727.138 (Official Build) (64-bit) |
| **OS** | Windows 11 Pro |

---

## 1. Summary

| Metric | Count |
|---|---|
| Total Test Cases Written | 12 |
| Total Test Cases Executed | 12 |
| Passed | 10 |
| Failed | 2 |
| Blocked | 0 |
| Total Bugs Found | 4 |

---

## 2. Test Execution Results

| TC ID | Title | Result | Bug ID |
|---|---|---|---|
| TC-001 | Login with valid standard_user credentials | ✅ Pass | — |
| TC-002 | Login with locked_out_user | ✅ Pass | — |
| TC-003 | Login with wrong password | ✅ Pass | — |
| TC-004 | Login with empty fields | ✅ Pass | — |
| TC-005 | Logout | ✅ Pass | — |
| TC-006 | Products page loads correctly | ❌ Fail | BUG-001 |
| TC-007 | Sort by Price (low to high) | ❌ Fail | BUG-003 |
| TC-008 | Add single item to cart | ✅ Pass | — |
| TC-009 | Remove item from cart | ✅ Pass | — |
| TC-010 | Cart preserves items after navigation | ✅ Pass | — |
| TC-011 | Complete checkout successfully | ✅ Pass | — |
| TC-012 | Checkout with empty First Name | ✅ Pass | — |

> **Note:** TC-006 and TC-007 failures were observed specifically under the `problem_user` account. Standard user flows passed without issues.

---

## 3. Bug Summary

| Bug ID | Title | Severity | Priority | Status |
|---|---|---|---|---|
| BUG-001 | Product images broken for problem_user | Major | High | Open |
| BUG-002 | Add to Cart button unresponsive for problem_user | Critical | High | Open |
| BUG-003 | Sort dropdown has no effect for problem_user | Major | Medium | Open |
| BUG-004 | Last Name field does not accept input (problem_user) | Critical | High | Open |

---

## 4. Test Coverage

| Module | Test Cases | Passed | Failed |
|---|---|---|---|
| Login | 5 | 5 | 0 |
| Product List | 2 | 1 | 1 |
| Shopping Cart | 3 | 3 | 0 |
| Checkout | 2 | 1 | 1 |

---

## 5. Observations and Notes

- The `standard_user` account passes all test scenarios without defects. Core application functionality is working correctly.
- The `problem_user` account has multiple intentional (or unintentional) defects affecting images, cart behavior, sorting, and form input. These were fully documented as bugs.
- The `locked_out_user` account behaves as expected — access is blocked with a clear error message.
- No JavaScript console errors were found during `standard_user` testing via Chrome DevTools.
- All critical `standard_user` flows (login → browse → add to cart → checkout → confirmation) are functional.

---

## 6. Conclusion

Testing of the Sauce Demo application has been completed. The core e-commerce user journey functions correctly for standard users. Four defects were identified and documented, all related to the `problem_user` account. No blockers were found for the `standard_user` flow. The application is considered stable for standard use.
