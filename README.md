# 🛒 TechMart E-Commerce App — Manual QA Testing Project

**Tested by:** Kushal Shrivastava  
**Date:** April 30, 2026  
**Build Version:** v1.0.3  
**Application:** TechMart E-Commerce Web App  

---

##  Project Overview

This project contains manually written and executed test cases for the **TechMart E-Commerce Web Application**. The goal is to verify the functionality, usability, and reliability of the application's core authentication modules — **Sign Up** and **Login**.

The testing covers positive scenarios, negative scenarios, edge cases, and UI validation checks.

---

##  Folder Structure

```
TechMart-QA-Testing-Project/
│
├── README.md
├── Test-Cases/
│   ├── SignUp_TestCases.xlsx       ← Test cases for Registration module
│   └── Login_TestCases.xlsx        ← Test cases for Login/Authentication module
└── Bug-Reports/
    └── Bug_Report.md               ← Bugs found during testing (Failed test cases)
```

---

##  Modules Tested

| Module | No. of Test Cases | Passed | Failed |
|---|---|---|---|
| Sign Up (Registration) | 13 | 10 | 3 |
| Login (Authentication) | 13 | 10 | 3 |
| **Total** | **26** | **20** | **6** |

---

##  Test Case Structure

Each test case follows this format:

| Field | Description |
|---|---|
| **Test Case ID** | Unique identifier (e.g., TC_001) |
| **Description** | What is being tested |
| **Steps** | Step-by-step actions to reproduce |
| **Expected Result** | What should happen |
| **Actual Result** | What actually happened |
| **Status** | Pass / Fail |

---

##  Bugs Found

Bugs were identified when the **Actual Result** did not match the **Expected Result**. All bugs are documented in detail in the [`Bug-Reports/Bug_Report.md`](Bug-Reports/Bug_Report.md) file.

### Quick Summary of Bugs:

**Sign Up Page:**
- TC_002 — Invalid email format was accepted (no validation error shown)
- TC_009 — Special characters in name were accepted without validation
- TC_010 — Submitting all empty fields only showed validation for Full Name field

**Login Page:**
- TC_003 — Login succeeded with invalid username and valid password
- TC_008 — Special characters accepted in username without validation
- TC_011 — Browser back button after login did not log out the user

---

##  Tools Used

- **Microsoft Excel** — Test case documentation
- **Manual Testing** — Functional and UI testing
- **GitHub** — Version control and project hosting

---

##  Types of Testing Performed

-  Functional Testing
-  Negative Testing
-  Boundary / Edge Case Testing
-  UI / Usability Testing
-  Input Validation Testing

---

##  About the Tester

**Kushal Shrivastava**  
Aspiring QA Engineer | Manual Testing  
 April 2026
