# Manual Testing Project

## Overview

This repository contains comprehensive manual testing documentation for two applications: PrestaShop e-commerce platform and ParaBank banking system. The project demonstrates practical QA skills including test case design, test execution, defect identification, and professional bug reporting across different application domains.

## Testing Summary

### Overall Portfolio Statistics
- **Total Test Cases Executed:** 63
- **Total Bugs Found:** 16
- **Applications Tested:** 2 (E-commerce + Banking)
- **Testing Types:** Functional, Security, Form Validation

### Project Breakdown

| Project | Test Cases | Pass Rate | Critical Bugs |
| --- | --- | --- | --- |
| PrestaShop (E-commerce) | 40 | 92.5% | 3 |
| ParaBank (Banking) | 23 | 43.5% | 13 |

---

## Repository Contents

### Project 1: PrestaShop E-Commerce Testing

**Application:** PrestaShop Demo  
**URL:** https://demo.prestashop.com/  
**File:** `PrestaShop-Test-Cases.xlsx`

**Testing Focus:**
- URL and browser compatibility testing
- User authentication (Login/Logout)
- Product search functionality
- Shopping cart operations
- Checkout process
- Guest user flows

**Results:**
- Total Test Cases: 40
- Pass Rate: 92.5%
- Bugs Found: 3 critical issues

**Critical Bugs:**
1. BUG-TC07: Login failure with valid credentials (Blocker)
2. BUG-TC26: Search returns results for 3-character input (Critical)
3. BUG-TC39: Place Order button unclickable after completing details (Critical)

---

### Project 2: ParaBank Banking Application Testing

**Application:** ParaBank  
**URL:** https://parabank.parasoft.com/parabank/index.htm  
**File:** `ParaBank-Test-Cases.xlsx`

**Testing Focus:**
- User registration form validation
- Name and address field validation
- ZIP code format validation
- SSN (Social Security Number) validation
- Phone number validation
- Password security requirements

**Results:**
- Total Test Cases: 23
- Pass Rate: 43.5%
- Bugs Found: 13 critical validation issues

**Key Findings:**
- Critical security vulnerabilities in password validation
- SSN field accepts invalid formats
- ZIP code validation completely missing
- Phone number format not validated
- Name fields accept numbers and special characters

---

## Bug Reports

Professional bug reports for all failed test cases from both projects are available in the `/Bug-Reports/` folder:

- **PrestaShop-Bugs.md** - 3 critical e-commerce bugs
- **ParaBank-Bugs.md** - 13 critical validation and security bugs

Each bug report includes:
- Bug ID linked to Test Case
- Severity and Priority
- Detailed description
- Preconditions
- Steps to reproduce
- Expected vs Actual results
- Impact analysis
- Environment details
- Suggested fixes

---

## Skills Demonstrated

- Test case design and documentation
- Cross-browser testing (Chrome, Edge, Firefox)
- Mobile responsiveness testing
- Positive and negative test scenario creation
- Security testing (password policies, sensitive data validation)
- Form validation testing
- Defect identification and reporting
- Severity and priority assessment
- Professional QA documentation practices

---

## Test Case Structure

Each test case includes:
- Test Case ID
- Test Method (Positive/Negative)
- Test Data
- Test Scenario
- Step-by-step reproduction steps
- Expected Result
- Actual Result
- Priority and Severity levels
- Status (Pass/

