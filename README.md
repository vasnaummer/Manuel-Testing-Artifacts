# Manual Testing Portfolio

## Overview

This repository contains comprehensive manual testing documentation for three different applications across e-commerce, banking, and recipe platform domains. The project demonstrates practical QA skills including test planning, test case design, test execution, defect identification, and professional bug reporting.

---

## Testing Summary

### Overall Portfolio Statistics
- **Total Test Cases Executed:** 118
- **Total Bugs Found:** 22
- **Applications Tested:** 3 (E-commerce, Banking, Recipe Platform)
- **Testing Types:** Functional, Security, Form Validation, Cross-browser, Mobile Responsiveness
- **Pass Rate:** 81.4%

### Project Breakdown

| Project | Test Cases | Pass Rate | Critical Bugs | Status |
| --- | --- | --- | --- | --- |
| PrestaShop (E-commerce) | 40 | 92.5% | 3 | ✅ Complete |
| ParaBank (Banking) | 23 | 43.5% | 13 | ✅ Complete |
| Allrecipes (Recipe Platform) | 55 | 89.1% | 6 | ✅ Complete |

---

## Repository Contents

### Project 1: PrestaShop E-Commerce Testing

**Application:** PrestaShop Demo  
**URL:** https://demo.prestashop.com/  

**Documentation:**
- **Test Cases:** `PrestaShop-Test-Cases.xlsx` (40 test cases)
- **Bug Reports:** `/Bug-Reports/PrestaShop-Bugs.md` (3 critical bugs)

**Testing Focus:**
- URL and browser compatibility testing
- User authentication (Login/Logout)
- Product search functionality
- Shopping cart operations
- Checkout process
- Guest user flows

**Key Findings:**
- Login failure with valid credentials (Blocker)
- Search returns results for incomplete input (Critical)
- Place Order button unclickable (Critical)

---

### Project 2: ParaBank Banking Application Testing

**Application:** ParaBank  
**URL:** https://parabank.parasoft.com/parabank/index.htm  

**Documentation:**
- **Test Cases:** `ParaBank-Test-Cases.xlsx` (23 test cases)
- **Bug Reports:** `/Bug-Reports/ParaBank-Bugs.md` (13 critical bugs)

**Testing Focus:**
- User registration form validation
- Name and address field validation
- ZIP code format validation
- SSN (Social Security Number) security
- Phone number validation
- Password security requirements

**Key Findings:**
- Critical security vulnerabilities in password validation
- SSN field accepts invalid formats (letters, special characters)
- ZIP code validation completely missing
- Phone number format not validated
- Multiple input validation failures across registration form

---

### Project 3: Allrecipes Website Testing

**Application:** Allrecipes  
**URL:** https://www.allrecipes.com/  

**Documentation:**
- **Test Plan:** `Allrecipes-Test-Plan.pdf`
- **Test Cases:** `Allrecipes-Test-Cases.xlsx` (55 test cases across 9-10 modules)
- **Test Execution Report:** `Allrecipes-Test-Execution-Report.xlsx`
- **Bug Reports:** Included in Test Cases Excel (Sheet 2)
- **Test Scenarios:** `/Test-Scenarios/Allrecipes-Test-Scenarios.md`

**Testing Focus:**
- URL validation and deep linking
- User registration and authentication
- Recipe search and filtering
- Recipe details page functionality
- User favorites management
- Rating and review system
- Navigation and menu links
- Mobile responsiveness
- Cross-browser compatibility
- Image loading and UI elements

**Test Modules Covered:**
1. URL Testing
2. User Registration
3. User Login
4. Recipe Search
5. Recipe Details
6. Favorites Feature
7. Rating & Review
8. Navigation
9. UI/Responsiveness
10. Cross-browser Testing

**Results:**
- Total Test Cases: 55
- Passed: 49
- Failed: 6
- Pass Rate: 89.1%

**Key Findings:**
- 6 bugs documented with severity classification
- Complete test execution report with metrics
- Professional test plan documentation

---

## Bug Reports

Professional bug reports for all failed test cases across all projects:

**Location:**
- `/Bug-Reports/PrestaShop-Bugs.md` (3 bugs)
- `/Bug-Reports/ParaBank-Bugs.md` (13 bugs)
- `Allrecipes-Test-Cases.xlsx` - Sheet 2 (6 bugs)

Each bug report includes:
- Bug ID linked to Test Case
- Severity and Priority classification
- Detailed description
- Preconditions
- Step-by-step reproduction steps
- Expected vs Actual results
- Impact analysis
- Environment details (Browser, OS)
- Suggested fixes

---

## Skills Demonstrated

### Testing Skills
- Test planning and strategy
- Test case design and documentation
- Test execution and reporting
- Positive and negative test scenario creation
- Cross-browser testing (Chrome, Edge, Firefox)
- Mobile responsiveness testing
- Security testing (password policies, sensitive data)
- Form validation testing
- Defect identification and tracking

### Documentation Skills
- Professional test plan creation
- Detailed test case documentation
- Bug report writing with industry standards
- Test execution reports
- Excel/Sheets proficiency
- Test scenario creation

### Technical Skills
- Understanding of SDLC and STLC
- Severity and priority assessment
- Test coverage analysis
- Functional testing
- UI/UX testing
- Domain knowledge (E-commerce, Banking, Web Applications)

---

## Test Documentation Structure

### Test Plan Components
- Test objectives and scope
- Testing approach and methodology
- Test environment requirements
- Entry and exit criteria
- Test deliverables
- Risk assessment

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

### Test Execution Report
- Test execution summary
- Pass/Fail statistics
- Defect summary
- Test coverage metrics
- Test cycle duration
- Environment details

---

## Tools Used

- **Test Management:** Google Sheets, Microsoft Excel
- **Documentation:** Google Docs, Markdown
- **Testing Tools:** Chrome DevTools, Browser Developer Tools
- **Browsers:** Chrome, Edge, Firefox
- **Version Control:** GitHub

---

## How to Use This Repository

1. **Review Test Plans:** Start with `Allrecipes-Test-Plan.pdf` to understand testing approach
2. **View Test Cases:** Download Excel files to see detailed test case documentation
3. **Check Bug Reports:** Review `/Bug-Reports/` folder and Excel sheets for defect documentation
4. **Analyze Metrics:** Review test execution reports for quality metrics
5. **Reuse Templates:** Test cases and bug reports can be adapted for similar projects

---

## Portfolio Highlights

✅ **Complete Testing Lifecycle:** Test planning → Test case design → Execution → Bug reporting  
✅ **Multi-Domain Experience:** E-commerce, Banking, Recipe/Content platforms  
✅ **Professional Documentation:** Test plans, test cases, execution reports, bug reports  
✅ **Quality Metrics:** Clear pass rates, bug classification, test coverage  
✅ **Real Bugs Found:** 22 actual defects identified across 3 applications  
✅ **Comprehensive Coverage:** 118 test cases covering functional, security, and UI testing  

---

## Author

Created as part of software testing portfolio development.

**Date:** July 2025  
**Contact:** github.com/vasnaummer

---

## Project Statistics

| Metric | Value |
| --- | --- |
| Total Projects | 3 |
| Total Test Cases | 118 |
| Total Bugs Found | 22 |
| Average Pass Rate | 81.4% |
| Critical Bugs | 8 |
| Major Bugs | 12 |
| Minor Bugs | 2 |
| Test Execution Time | [Add if available] |

---

*This repository demonstrates professional software testing skills suitable for manual QA tester, software tester, and QA analyst positions.*
