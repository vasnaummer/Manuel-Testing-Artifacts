# Bug Reports: ParaBank Banking Application

## Testing Information
**Application:** ParaBank  
**URL:** https://parabank.parasoft.com/parabank/index.htm  
**Tested By:** [Your Name]  
**Testing Period:** November 2025  
**Total Bugs Found:** 13

---

## Critical Registration Form Validation Issues

### Bug #1: Name Field Accepts Numbers

**Bug ID:** BUG-PB04  
**Related Test Case:** PB-04  
**Severity:** Major  
**Priority:** High  
**Status:** Open

**Module:** User Registration - Form Validation

**Description:**  
The first name field accepts numeric values, which should be restricted to alphabetic characters only for a valid name.

**Steps to Reproduce:**
1. Navigate to https://parabank.parasoft.com/parabank/index.htm
2. Click Register link
3. Enter numbers (e.g., "12345") in First Name field
4. Fill remaining required fields with valid data
5. Click Register button

**Expected Result:**  
System should display validation error: "Please enter a valid name (letters only)"

**Actual Result:**  
User is able to register successfully with numbers in the name field

**Impact:**  
Data integrity issue - Invalid customer records with numeric names in database

---

### Bug #2: Name Field Accepts Special Characters

**Bug ID:** BUG-PB05  
**Related Test Case:** PB-05  
**Severity:** Major  
**Priority:** High  
**Status:** Open

**Module:** User Registration - Form Validation

**Description:**  
The first name field accepts special characters (e.g., @, #, $, %), which should be restricted.

**Steps to Reproduce:**
1. Navigate to registration page
2. Enter special characters (e.g., "@#$%") in First Name field
3. Fill remaining fields with valid data
4. Click Register

**Expected Result:**  
Validation error should prevent registration

**Actual Result:**  
Registration succeeds with special characters in name

**Impact:**  
Database contains invalid customer names, potential security risk for SQL injection

---

### Bug #3: Address Field Accepts Numbers Only

**Bug ID:** BUG-PB06  
**Related Test Case:** PB-06  
**Severity:** Major  
**Priority:** High  
**Status:** Open

**Module:** User Registration - Address Validation

**Description:**  
Address field accepts only numeric values without any alphabetic characters.

**Steps to Reproduce:**
1. Navigate to registration page
2. Enter only numbers (e.g., "123456") in Address field
3. Complete remaining fields
4. Click Register

**Expected Result:**  
System should require alphanumeric address format

**Actual Result:**  
Registration completes with numeric-only address

**Impact:**  
Invalid addresses stored, potential mail delivery failures

---

### Bug #4: Address Field Accepts Special Characters

**Bug ID:** BUG-PB07  
**Related Test Case:** PB-07  
**Severity:** Major  
**Priority:** High  
**Status:** Open

**Module:** User Registration - Address Validation

**Description:**  
Address field accepts special characters without proper validation.

**Steps to Reproduce:**
1. Navigate to registration page
2. Enter special characters in Address field
3. Complete registration

**Expected Result:**  
Limited special characters should be allowed (comma, period, hyphen only)

**Actual Result:**  
All special characters accepted

**Impact:**  
Data quality issues, address parsing problems

---

### Bug #5: Single Character Address Accepted

**Bug ID:** BUG-PB08  
**Related Test Case:** PB-08  
**Severity:** Major  
**Priority:** High  
**Status:** Open

**Module:** User Registration - Address Validation

**Description:**  
System allows registration with a single character in the address field.

**Steps to Reproduce:**
1. Navigate to registration page
2. Enter single character (e.g., "A") in Address field
3. Complete registration

**Expected Result:**  
Minimum address length should be enforced (at least 5 characters)

**Actual Result:**  
Registration succeeds with 1-character address

**Impact:**  
Meaningless addresses in database

---

### Bug #6: ZIP Code Exceeding Limit Accepted

**Bug ID:** BUG-PB10  
**Related Test Case:** PB-10  
**Severity:** Critical  
**Priority:** High  
**Status:** Open

**Module:** User Registration - ZIP Code Validation

**Description:**  
System accepts ZIP codes exceeding standard length (typically 5 or 10 digits for US ZIP codes).

**Steps to Reproduce:**
1. Navigate to registration page
2. Enter ZIP code with 15+ digits
3. Complete registration

**Expected Result:**  
Error message: "ZIP code must be 5 or 9 digits"

**Actual Result:**  
Registration completes with invalid ZIP length

**Impact:**  
Critical - Invalid ZIP codes prevent mail delivery, address verification failures

---

### Bug #7: ZIP Code Accepts Letters

**Bug ID:** BUG-PB11  
**Related Test Case:** PB-11  
**Severity:** Critical  
**Priority:** High  
**Status:** Open

**Module:** User Registration - ZIP Code Validation

**Description:**  
ZIP code field accepts alphabetic characters instead of numeric-only validation.

**Steps to Reproduce:**
1. Navigate to registration page
2. Enter letters (e.g., "ABCDE") in ZIP Code field
3. Complete registration

**Expected Result:**  
Validation error: "ZIP code must contain numbers only"

**Actual Result:**  
System accepts letters in ZIP code

**Impact:**  
Critical - Address verification systems fail, shipping issues

---

### Bug #8: ZIP Code Accepts Special Characters

**Bug ID:** BUG-PB12  
**Related Test Case:** PB-12  
**Severity:** Critical  
**Priority:** High  
**Status:** Open

**Module:** User Registration - ZIP Code Validation

**Description:**  
ZIP code field accepts special characters (@, #, $, etc.).

**Steps to Reproduce:**
1. Navigate to registration page
2. Enter special characters in ZIP Code field
3. Complete registration

**Expected Result:**  
Only numeric characters and hyphen allowed

**Actual Result:**  
All special characters accepted

**Impact:**  
Critical - Database integrity issue, address validation failures

---

### Bug #9: SSN Field Accepts Letters

**Bug ID:** BUG-PB14  
**Related Test Case:** PB-14  
**Severity:** Critical  
**Priority:** High  
**Status:** Open

**Module:** User Registration - SSN Validation

**Description:**  
Social Security Number field accepts alphabetic characters instead of numeric-only.

**Steps to Reproduce:**
1. Navigate to registration page
2. Enter letters in SSN field
3. Complete registration

**Expected Result:**  
Validation error: "SSN must be numeric (XXX-XX-XXXX format)"

**Actual Result:**  
Registration succeeds with letters in SSN

**Impact:**  
Critical - Invalid SSN records, compliance violation, identity verification failures

---

### Bug #10: SSN Field Accepts Special Characters

**Bug ID:** BUG-PB15  
**Related Test Case:** PB-15  
**Severity:** Critical  
**Priority:** High  
**Status:** Open

**Module:** User Registration - SSN Validation

**Description:**  
SSN field accepts special characters without validation.

**Steps to Reproduce:**
1. Navigate to registration page
2. Enter special characters in SSN field
3. Complete registration

**Expected Result:**  
Only numbers and hyphens allowed (XXX-XX-XXXX)

**Actual Result:**  
All special characters accepted

**Impact:**  
Critical - Regulatory compliance issue (GDPR, PCI-DSS), data security risk

---

### Bug #11: Phone Number Invalid Format Accepted

**Bug ID:** BUG-PB16  
**Related Test Case:** PB-16  
**Severity:** Critical  
**Priority:** High  
**Status:** Open

**Module:** User Registration - Phone Validation

**Description:**  
Phone number field accepts invalid formats without proper validation.

**Steps to Reproduce:**
1. Navigate to registration page
2. Enter invalid phone format (letters, special characters, wrong length)
3. Complete registration

**Expected Result:**  
Validation for standard phone format (e.g., XXX-XXX-XXXX)

**Actual Result:**  
Any format accepted

**Impact:**  
Critical - Unable to contact customers, SMS/OTP delivery failures

---

### Bug #12: Username Accepts Invalid Characters

**Bug ID:** BUG-PB18  
**Related Test Case:** PB-18  
**Severity:** Critical  
**Priority:** High  
**Status:** Open

**Module:** User Registration - Username Validation

**Description:**  
Username field allows invalid characters that could cause system issues.

**Steps to Reproduce:**
1. Navigate to registration page
2. Enter special characters/spaces in username
3. Complete registration

**Expected Result:**  
Username should allow only alphanumeric and underscore

**Actual Result:**  
Invalid characters accepted

**Impact:**  
Critical - Login issues, database query problems, potential security vulnerability

---

### Bug #13: Single Character Password Accepted

**Bug ID:** BUG-PB20  
**Related Test Case:** PB-20  
**Severity:** Critical  
**Priority:** High  
**Status:** Open

**Module:** User Registration - Password Security

**Description:**  
System allows registration with single-character password, violating security best practices.

**Steps to Reproduce:**
1. Navigate to registration page
2. Enter single character (e.g., "a") in Password field
3. Enter same in Confirm Password
4. Complete registration

**Expected Result:**  
Password minimum length enforcement (at least 8 characters)

**Actual Result:**  
Single-character password accepted

**Impact:**  
Critical - Severe security vulnerability, accounts easily compromised, brute force attack risk

---

### Bug #14: Password Length Limit Not Enforced

**Bug ID:** BUG-PB21  
**Related Test Case:** PB-21  
**Severity:** Critical  
**Priority:** High  
**Status:** Open

**Module:** User Registration - Password Security

**Description:**  
System allows extremely long passwords exceeding reasonable limits.

**Steps to Reproduce:**
1. Navigate to registration page
2. Enter password with 1000+ characters
3. Complete registration

**Expected Result:**  
Maximum password length enforced (typically 128 characters)

**Actual Result:**  
No maximum length restriction

**Impact:**  
Critical - Database performance issues, potential denial of service, buffer overflow risk

---

## Summary Table

| Bug ID | Module | Issue | Severity | Status |
| --- | --- | --- | --- | --- |
| BUG-PB04 | Name Validation | Accepts numbers | Major | Open |
| BUG-PB05 | Name Validation | Accepts special chars | Major | Open |
| BUG-PB06 | Address Validation | Accepts numbers only | Major | Open |
| BUG-PB07 | Address Validation | Accepts special chars | Major | Open |
| BUG-PB08 | Address Validation | Single character allowed | Major | Open |
| BUG-PB10 | ZIP Code | Exceeds length limit | Critical | Open |
| BUG-PB11 | ZIP Code | Accepts letters | Critical | Open |
| BUG-PB12 | ZIP Code | Accepts special chars | Critical | Open |
| BUG-PB14 | SSN Validation | Accepts letters | Critical | Open |
| BUG-PB15 | SSN Validation | Accepts special chars | Critical | Open |
| BUG-PB16 | Phone Validation | Invalid format accepted | Critical | Open |
| BUG-PB18 | Username | Invalid chars accepted | Critical | Open |
| BUG-PB20 | Password Security | Single char password | Critical | Open |
| BUG-PB21 | Password Security | No max length | Critical | Open |

**Total Critical Issues:** 11  
**Total Major Issues:** 5

**Recommendation:** The registration form has severe validation failures across all input fields. Complete input validation overhaul required before production deployment. These issues pose significant security and data integrity risks.
