# Test Cases — Sauce Demo Web Application

| Field | Details |
|---|---|
| **Prepared by** | [U Salma] |
| **Date** | 16 May 2026 |
| **Application** | https://www.saucedemo.com |
| **Modules Covered** | Login, Product List, Cart, Checkout |

---

## Module 1: Login

### TC-001 — Successful Login with Valid Credentials

| Field | Details |
|---|---|
| **Test Case ID** | TC-001 |
| **Title** | Login with valid standard_user credentials |
| **Priority** | High |
| **Type** | Positive / Functional |

**Steps:**
1. Go to https://www.saucedemo.com
2. Enter `standard_user` in the Username field
3. Enter `secret_sauce` in the Password field
4. Click the **Login** button

**Expected Result:** User is redirected to the Products page (`/inventory.html`). Page title shows "Products".
**Status:** [ ]

---

### TC-002 — Login with Locked Out User

| Field | Details |
|---|---|
| **Test Case ID** | TC-002 |
| **Title** | Login attempt with locked_out_user account |
| **Priority** | High |
| **Type** | Negative / Functional |

**Steps:**
1. Go to https://www.saucedemo.com
2. Enter `locked_out_user` in the Username field
3. Enter `secret_sauce` in the Password field
4. Click **Login**

**Expected Result:** Login is rejected. Error message shown: *"Epic sadface: Sorry, this user has been locked out."*
**Status:** [ ]

---

### TC-003 — Login with Wrong Password

| Field | Details |
|---|---|
| **Test Case ID** | TC-003 |
| **Title** | Login with correct username but incorrect password |
| **Priority** | High |
| **Type** | Negative / Functional |

**Steps:**
1. Go to https://www.saucedemo.com
2. Enter `standard_user` in the Username field
3. Enter `wrongpassword` in the Password field
4. Click **Login**

**Expected Result:** Login fails. Error message shown: *"Epic sadface: Username and password do not match any user in this service."*
**Status:** [ ]

---

### TC-004 — Login with Empty Fields

| Field | Details |
|---|---|
| **Test Case ID** | TC-004 |
| **Title** | Login attempt with both fields empty |
| **Priority** | Medium |
| **Type** | Negative / Validation |

**Steps:**
1. Go to https://www.saucedemo.com
2. Leave both Username and Password fields empty
3. Click **Login**

**Expected Result:** Error message shown: *"Epic sadface: Username is required."*
**Status:** [ ]

---

### TC-005 — Logout

| Field | Details |
|---|---|
| **Test Case ID** | TC-005 |
| **Title** | Successfully log out from an active session |
| **Priority** | High |
| **Type** | Positive / Functional |

**Steps:**
1. Log in as `standard_user` (see TC-001)
2. Click the hamburger menu icon (top left)
3. Click **Logout**

**Expected Result:** User is redirected back to the login page. Session is ended.
**Status:** [ ]

---

## Module 2: Product List

### TC-006 — Products Page Loads Correctly

| Field | Details |
|---|---|
| **Test Case ID** | TC-006 |
| **Title** | All products display with name, image, price, and Add to Cart button |
| **Priority** | High |
| **Type** | Positive / Functional |

**Steps:**
1. Log in as `standard_user`
2. Observe the Products page

**Expected Result:** 6 products are displayed. Each has a name, description, price, product image, and an "Add to cart" button.
**Status:** [ ]

---

### TC-007 — Sort Products by Price (Low to High)

| Field | Details |
|---|---|
| **Test Case ID** | TC-007 |
| **Title** | Sorting products by Price (low to high) reorders the list correctly |
| **Priority** | Medium |
| **Type** | Positive / Functional |

**Steps:**
1. Log in as `standard_user`
2. On the Products page, click the sort dropdown (default shows "Name (A to Z)")
3. Select **Price (low to high)**

**Expected Result:** Products are reordered so the cheapest item appears first and the most expensive last.
**Status:** [ ]

---

## Module 3: Shopping Cart

### TC-008 — Add Single Item to Cart

| Field | Details |
|---|---|
| **Test Case ID** | TC-008 |
| **Title** | Adding one product updates the cart icon count to 1 |
| **Priority** | High |
| **Type** | Positive / Functional |

**Steps:**
1. Log in as `standard_user`
2. Click **Add to cart** on any product

**Expected Result:** The cart icon in the top right shows a badge with the number **1**.
**Status:** [ ]

---

### TC-009 — Remove Item from Cart

| Field | Details |
|---|---|
| **Test Case ID** | TC-009 |
| **Title** | Removing a product from the cart updates the cart count correctly |
| **Priority** | High |
| **Type** | Positive / Functional |

**Steps:**
1. Log in as `standard_user`
2. Add one product to the cart
3. Click **Remove** on the same product

**Expected Result:** The cart badge disappears (count returns to 0). The button returns to "Add to cart".
**Status:** [ ]

---

### TC-010 — Cart Preserves Items After Navigation

| Field | Details |
|---|---|
| **Test Case ID** | TC-010 |
| **Title** | Items added to cart remain there after navigating away and back |
| **Priority** | High |
| **Type** | Positive / Functional |

**Steps:**
1. Log in as `standard_user`
2. Add 2 products to the cart
3. Click on a product to go to its detail page
4. Click the back button or the cart icon

**Expected Result:** Cart still shows 2 items. Nothing was lost during navigation.
**Status:** [ ]

---

## Module 4: Checkout

### TC-011 — Complete Checkout Successfully

| Field | Details |
|---|---|
| **Test Case ID** | TC-011 |
| **Title** | Full checkout flow completes and shows confirmation |
| **Priority** | High |
| **Type** | Positive / Functional |

**Steps:**
1. Log in as `standard_user`
2. Add any product to the cart
3. Click the cart icon → Click **Checkout**
4. Enter First Name: `Test`, Last Name: `User`, Zip Code: `1207`
5. Click **Continue**
6. Click **Finish**

**Expected Result:** A confirmation page appears with the message *"Thank you for your order!"*
**Status:** [ ]

---

### TC-012 — Checkout with Empty First Name Field

| Field | Details |
|---|---|
| **Test Case ID** | TC-012 |
| **Title** | Checkout form shows error when First Name is left blank |
| **Priority** | High |
| **Type** | Negative / Validation |

**Steps:**
1. Log in as `standard_user`
2. Add any product to the cart
3. Click cart icon → Click **Checkout**
4. Leave First Name empty
5. Fill in Last Name and Zip Code
6. Click **Continue**

**Expected Result:** Error message shown: *"Error: First Name is required"*
**Status:** [ ]
