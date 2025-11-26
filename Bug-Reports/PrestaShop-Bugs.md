# Bug Reports: PrestaShop Demo Website

## Testing Information
**Application:** PrestaShop Demo (https://demo.prestashop.com/)  
**Tested By:** [Your Name]  
**Testing Period:** November 2025  
**Total Bugs Found:** 3

---

## Bug #1: Login Failure with Valid Credentials

**Bug ID:** BUG-TC07  
**Related Test Case:** TC-07  
**Severity:** Blocker  
**Priority:** High  
**Status:** Open

**Module:** User Authentication

**Description:**  
User is unable to login using valid email and password. System displays "Authentication failed" error message.

**Preconditions:**
- User has valid credentials (email: anonymous@gmail.com, password: 200720emin)
- User is on the PrestaShop demo homepage

**Steps to Reproduce:**
1. Open browser
2. Navigate to https://demo.prestashop.com/#/en/front
3. Click on Sign In button
4. Enter email: anonymous@gmail.com
5. Enter password: 200720emin
6. Click Login button

**Expected Result:**  
User should successfully login and be redirected to their account dashboard

**Actual Result:**  
System displays error message "Authentication failed" and user remains on login page

**Impact:**  
Critical - Users cannot access their accounts, blocking all authenticated features including order history, wishlist, and checkout

**Environment:**
- Browser: Chrome/Edge/Firefox (tested on all)
- OS: Windows
- Date Found: November 2025

**Suggested Fix:**  
Verify authentication credentials in database. Check if demo credentials have expired or been deactivated.

---

## Bug #2: Search Function Returns Results for Incomplete Input

**Bug ID:** BUG-TC26  
**Related Test Case:** TC-26  
**Severity:** Critical  
**Priority:** High  
**Status:** Open

**Module:** Search Functionality

**Description:**  
Search function displays product results when user enters only 3 characters (letters, numbers, or combination), but should not display results for such short queries.

**Preconditions:**
- User is on PrestaShop homepage
- Search bar is visible

**Steps to Reproduce:**
1. Open browser
2. Navigate to https://demo.prestashop.com/#/en/front
3. Click on search bar
4. Enter any 3 characters (e.g., "abc", "123", or "a1b")
5. Press Enter or click search icon

**Expected Result:**  
System should display message "Please enter at least 4 characters to search" or similar validation message. No product results should be displayed.

**Actual Result:**  
System displays product results matching the 3-character input, potentially showing irrelevant results.

**Impact:**  
High - Users may get too many irrelevant search results, degrading search experience and making it difficult to find desired products.

**Environment:**
- Browser: Chrome
- OS: Windows
- Date Found: November 2025

**Suggested Fix:**  
Implement minimum character validation (4+ characters) before executing search query. Display helpful error message for inputs shorter than minimum.

---

## Bug #3: Place Order Button Unclickable After Completing All Details

**Bug ID:** BUG-TC39  
**Related Test Case:** TC-39  
**Severity:** Critical  
**Priority:** High  
**Status:** Open

**Module:** Checkout - Order Placement

**Description:**  
The "Place Order" button remains unclickable even after user fills all mandatory checkout details. No error message is displayed, preventing order completion.

**Preconditions:**
- User has added product(s) to cart
- User has entered valid shipping address
- User has proceeded to checkout page

**Steps to Reproduce:**
1. Open browser
2. Navigate to https://demo.prestashop.com/#/en/front
3. Select any product
4. Click "Add to Cart"
5. Enter valid shipping address
6. Click "Proceed to Checkout"
7. Fill all mandatory fields with valid data
8. Attempt to click "Place Order" button

**Expected Result:**  
"Place Order" button should become clickable after all mandatory fields are filled. Clicking it should process the order and display confirmation message.

**Actual Result:**  
"Place Order" button remains disabled/unclickable. No error message appears. User cannot complete purchase.

**Impact:**  
Critical - Complete checkout failure. Users cannot place orders, resulting in 100% cart abandonment and revenue loss.

**Environment:**
- Browser: Chrome/Edge/Firefox
- OS: Windows
- Date Found: November 2025

**Suggested Fix:**  
1. Check JavaScript validation logic for "Place Order" button
2. Verify all form field validations are properly connected
3. Ensure button state changes when all conditions are met
4. Add clear error messages if validation fails

---

## Summary

| Bug ID | Module | Severity | Status |
| --- | --- | --- | --- |
| BUG-TC07 | Login | Blocker | Open |
| BUG-TC26 | Search | Critical | Open |
| BUG-TC39 | Checkout | Critical | Open |

**Total Critical/Blocker Issues:** 3  

**Recommendation:** These bugs severely impact core user flows (authentication, search, purchase). Immediate fix required before production deployment.
