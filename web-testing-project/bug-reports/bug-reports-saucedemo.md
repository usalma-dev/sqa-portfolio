# Bug Reports — Sauce Demo Web Application

| Field | Details |
|---|---|
| **Date** | 16 May 2026 |
| **Application** | https://www.saucedemo.com |
| **Tester** | [U Salma] |

---

## BUG-001 — Product images are broken for problem_user

| Attribute | Details |
|---|---|
| **Bug ID** | BUG-001 |
| **Title** | All product images fail to load correctly for problem_user |
| **Module** | Product Listing |
| **Severity** | Major |
| **Priority** | High |
| **Status** | Open |
| **Reported by** | [U Salma] |
| **Date** | 16 May 2026 |
| **Environment** | Google Chrome 147.0.7727.138 (Official Build) (64-bit), Windows 11 Pro |

**Description:**
When logged in as `problem_user`, all product images on the inventory page display the same incorrect image (a dog/animal photo) instead of the actual product images shown for `standard_user`. This is a visual defect that breaks product recognition for the user.

**Steps to Reproduce:**
1. Go to https://www.saucedemo.com
2. Log in with username: `problem_user`, password: `secret_sauce`
3. Observe the product images on the Products page

**Expected Result:** Each product displays its own correct and relevant product image.

**Actual Result:** All products display the same wrong image (a dog photo). No product-specific images are shown.

**Screenshot:** Please see `screenshots/BUG-001-problem-user-images.png`

---

## BUG-002 — Add to Cart button does not work for some products (problem_user)

| Attribute | Details |
|---|---|
| **Bug ID** | BUG-002 |
| **Title** | "Add to cart" button unresponsive for certain products when logged in as problem_user |
| **Module** | Product Listing / Shopping Cart |
| **Severity** | Critical |
| **Priority** | High |
| **Status** | Open |
| **Reported by** | [U Salma] |
| **Date** | 16 May 2026 |
| **Environment** | Google Chrome 147.0.7727.138 (Official Build) (64-bit), Windows 11 Pro |

**Description:**
When logged in as `problem_user`, clicking "Add to cart" on certain products does not add them to the cart. The cart count does not increase and no error message is displayed, leaving the user with no feedback.

**Steps to Reproduce:**
1. Go to https://www.saucedemo.com
2. Log in as `problem_user` / `secret_sauce`
3. Click **Add to cart** on the "Sauce Labs Backpack"
4. Observe the cart icon

**Expected Result:** The cart badge updates to show 1 item added.

**Actual Result:** The cart count does not change. The item is not added.

**Screenshot:** Please see `screenshots/BUG-002-add-to-cart-broken.png`

---

## BUG-003 — Sort by Name (Z to A) does not work for problem_user

| Attribute | Details |
|---|---|
| **Bug ID** | BUG-003 |
| **Title** | Product sort dropdown does not reorder products for problem_user |
| **Module** | Product Listing / Sorting |
| **Severity** | Major |
| **Priority** | Medium |
| **Status** | Open |
| **Reported by** | [U Salma] |
| **Date** | 16 May 2026 |
| **Environment** | Google Chrome 147.0.7727.138 (Official Build) (64-bit), Windows 11 Pro |

**Description:**
When logged in as `problem_user` and selecting any sort option from the dropdown (e.g., "Name (Z to A)" or "Price (low to high)"), the product order on the page does not change. The sort function appears broken for this user type.

**Steps to Reproduce:**
1. Log in as `problem_user` / `secret_sauce`
2. On the Products page, click the sort dropdown
3. Select **Name (Z to A)**
4. Observe the product list order

**Expected Result:** Products reorder alphabetically from Z to A.

**Actual Result:** Product order remains unchanged. Sort has no effect.

**Screenshot:** Please see `screenshots/BUG-003-sort-broken.png`

---

## BUG-004 — Last Name field not functional during checkout (problem_user)

| Attribute | Details |
|---|---|
| **Bug ID** | BUG-004 |
| **Title** | Cannot type in the Last Name field on the Checkout form when logged in as problem_user |
| **Module** | Checkout |
| **Severity** | Critical |
| **Priority** | High |
| **Status** | Open |
| **Reported by** | [U Salma] |
| **Date** | 16 May 2026 |
| **Environment** | Google Chrome 147.0.7727.138 (Official Build) (64-bit), Windows 11 Pro |

**Description:**
During the checkout process, the Last Name field does not accept keyboard input for `problem_user`. Clicking the field and typing produces no result. The field remains empty regardless of input. This blocks the user from completing checkout entirely.

**Steps to Reproduce:**
1. Log in as `problem_user` / `secret_sauce`
2. Add any item to the cart
3. Go to the cart → Click **Checkout**
4. Click on the **Last Name** field
5. Try to type any text

**Expected Result:** Text typed by the user appears in the Last Name field.

**Actual Result:** Nothing appears. The field does not accept any input.

**Screenshot:** Please see `screenshots/BUG-004-last-name-field.png`
