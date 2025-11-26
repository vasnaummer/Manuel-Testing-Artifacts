# Manual-Testing-Artifacts
Manual testing documentation including test scenarios, test cases, and bug reports

# Manual Testing Project

## Overview

This repository contains comprehensive manual testing documentation for the PrestaShop Demo e-commerce website. The project demonstrates practical QA skills including test case design, test execution, defect identification, and professional bug reporting.

## Application Under Test

**Website:** PrestaShop Demo  
**URL:** https://demo.prestashop.com/  
**Application Type:** E-commerce Platform  
**Testing Type:** Functional Testing

## Testing Summary

- **Total Test Cases:** 40
- **Test Cases Passed:** 37
- **Test Cases Failed:** 3
- **Pass Rate:** 92.5%
- **Critical Bugs Found:** 3

## Repository Contents

### Test Cases Document
Comprehensive Excel spreadsheet containing 40 detailed test cases covering:
- URL and browser compatibility testing
- User authentication (Login/Logout)
- Product search functionality
- Shopping cart operations
- Checkout process
- Guest user flows

**File:** `PrestaShop-Test-Cases.xlsx`

### Bug Reports
Professional bug reports for all failed test cases, including:
- Detailed steps to reproduce
- Expected vs Actual results
- Severity and Priority classification
- Impact analysis
- Suggested fixes

**Location:** `/Bug-Reports/PrestaShop-Bugs.md`

## Test Coverage

### Modules Tested

| Module | Test Cases | Status |
| --- | --- | --- |
| URL & Browser Testing | 6 | ✅ Pass |
| User Authentication | 3 | ❌ 1 Failed (TC-07) |
| Homepage Navigation | 6 | ✅ Pass |
| Product Details Page | 5 | ✅ Pass |
| Search Functionality | 6 | ❌ 1 Failed (TC-26) |
| Shopping Cart | 6 | ✅ Pass |
| Checkout Process | 5 | ✅ Pass |
| Order Placement | 3 | ❌ 1 Failed (TC-39) |

## Critical Bugs Identified

1. **BUG-TC07:** Login failure with valid credentials (Blocker)
2. **BUG-TC26:** Search returns results for 3-character input (Critical)
3. **BUG-TC39:** Place Order button unclickable after completing details (Critical)

## Skills Demonstrated

- Test case design and documentation
- Cross-browser testing (Chrome, Edge, Firefox)
- Mobile responsiveness testing
- Positive and negative test scenario creation
- Defect identification and reporting
- Severity and priority assessment
- Professional QA documentation practices

## Testing Approach

### Test Case Structure
Each test case includes:
- Test Case ID
- Test Method (Positive/Negative)
- Test Data
- Test Scenario
- Step-by-step reproduction steps
- Expected Result
- Actual Result
- Priority and Severity levels
- Status (Pass/Fail)
- Comments

### Bug Report Structure
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

## Tools Used

- Google Sheets (Test case documentation)
- Chrome DevTools (Debugging)
- Multiple browsers for compatibility testing

## Author

Created as part of software testing portfolio development.

**Date:** November 2025

## How to Use This Repository

1. Download `PrestaShop-Test-Cases.xlsx` to view complete test execution details
2. Review `/Bug-Reports/` folder for detailed defect documentation
3. Test cases can be reused as templates for similar e-commerce testing projects
