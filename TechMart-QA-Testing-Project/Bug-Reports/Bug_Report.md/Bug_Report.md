#  Bug Report — TechMart E-Commerce App

**Project:** TechMart E-Commerce Web Application  
**Tested by:** Kushal Shrivastava  
**Date:** April 30, 2026  
**Build Version:** v1.0.3  

---

##  Bug Report Summary

| Bug ID | Module | Test Case | Severity | Status |
|---|---|---|---|---|
| BUG_001 | Sign Up | TC_002 | High | Open |
| BUG_002 | Sign Up | TC_009 | Medium | Open |
| BUG_003 | Sign Up | TC_010 | High | Open |
| BUG_004 | Login | TC_003 | Critical | Open |
| BUG_005 | Login | TC_008 | Medium | Open |
| BUG_006 | Login | TC_011 | High | Open |

---

## 🔴 Sign Up Module Bugs

---

### BUG_001 — Invalid Email Format Accepted

| Field | Details |
|---|---|
| **Bug ID** | BUG_001 |
| **Test Case ID** | TC_002 |
| **Module** | Registration & Authentication (Sign Up) |
| **Description** | Invalid email format was accepted and account was created |
| **Severity** | High |
| **Priority** | High |

**Steps to Reproduce:**
1. Open the TechMart app
2. Navigate to the Sign Up page
3. Enter valid input in all fields but enter an invalid email (e.g., `kushalgmail.com`)
4. Click "Create Account"

**Expected Result:**  
System should show error: *"Enter a valid email address"*

**Actual Result:**  
Account was created and user was redirected to Home Page (no validation error shown)

**Impact:**  
Users can register with invalid email addresses, which will cause issues with email communication, password recovery, and account verification.

---

### BUG_002 — Special Characters in Name Field Accepted

| Field | Details |
|---|---|
| **Bug ID** | BUG_002 |
| **Test Case ID** | TC_009 |
| **Module** | Registration & Authentication (Sign Up) |
| **Description** | Special characters in the Full Name field were accepted without validation |
| **Severity** | Medium |
| **Priority** | Medium |

**Steps to Reproduce:**
1. Open the TechMart app
2. Navigate to the Sign Up page
3. Enter special characters (e.g., `@#$%^&*`) in the Full Name field
4. Enter valid data in all other fields
5. Click "Create Account"

**Expected Result:**  
Should show a validation error OR reject invalid input (special characters should not be allowed in a name field)

**Actual Result:**  
Account was created and user was redirected to Home Page without any error

**Impact:**  
Invalid names can corrupt user data and cause display/formatting issues across the application.

---

### BUG_003 — Empty Form Submission Shows Only One Validation Message

| Field | Details |
|---|---|
| **Bug ID** | BUG_003 |
| **Test Case ID** | TC_010 |
| **Module** | Registration & Authentication (Sign Up) |
| **Description** | Submitting all empty fields only displayed validation message for the Full Name field |
| **Severity** | High |
| **Priority** | High |

**Steps to Reproduce:**
1. Open the TechMart app
2. Navigate to the Sign Up page
3. Leave all fields empty
4. Click "Create Account"

**Expected Result:**  
Validation messages should be displayed for **all** required fields

**Actual Result:**  
Only the "Full Name" field displayed a validation message; other required fields showed no error

**Impact:**  
Users are not informed about all missing required fields, leading to a poor user experience and incomplete form submissions.

---

## 🔴 Login Module Bugs

---

### BUG_004 — Login Succeeded with Invalid Username  [CRITICAL]

| Field | Details |
|---|---|
| **Bug ID** | BUG_004 |
| **Test Case ID** | TC_003 |
| **Module** | User Authentication (Login) |
| **Description** | User was able to login successfully with an invalid username and valid password |
| **Severity** | Critical |
| **Priority** | Critical |

**Steps to Reproduce:**
1. Open the TechMart app
2. Enter an **invalid/unregistered username** in the username field
3. Enter a **valid password**
4. Click "Login"

**Expected Result:**  
Login should be denied

**Actual Result:**  
Login was successful — user was able to access the application with an invalid username

**Impact:**  
This is a **critical security vulnerability**. Unauthorized users can gain access to the application. This must be fixed immediately before deployment.

---

### BUG_005 — Special Characters Accepted in Username Field

| Field | Details |
|---|---|
| **Bug ID** | BUG_005 |
| **Test Case ID** | TC_008 |
| **Module** | User Authentication (Login) |
| **Description** | Special characters were accepted in the username field without any validation message |
| **Severity** | Medium |
| **Priority** | Medium |

**Steps to Reproduce:**
1. Open the TechMart app
2. Enter special characters (e.g., `!@#$%`) in the username field
3. Enter any password
4. Click "Login"

**Expected Result:**  
System should not accept special characters in the username field and should display a validation message

**Actual Result:**  
System allowed special characters; no validation message was displayed

**Impact:**  
Could expose the application to injection attacks and unexpected behavior.

---

### BUG_006 — Browser Back Button After Login Does Not Log Out User

| Field | Details |
|---|---|
| **Bug ID** | BUG_006 |
| **Test Case ID** | TC_011 |
| **Module** | User Authentication (Login) |
| **Description** | After logging in, clicking the browser back button does not log out the user |
| **Severity** | High |
| **Priority** | High |

**Steps to Reproduce:**
1. Open the TechMart app
2. Enter valid username and password
3. Click "Login"
4. After successful login, click the **browser back button**

**Expected Result:**  
User should be logged out and redirected to the Login page

**Actual Result:**  
User remained logged in and was redirected to the Home page

**Impact:**  
This is a **session management issue**. On shared or public devices, another person could access the account simply by pressing the back button after the original user thinks they've navigated away.

---

## 📊 Bug Severity Summary

| Severity | Count |
|---|---|
| 🔴 Critical | 1 |
| 🟠 High | 3 |
| 🟡 Medium | 2 |
| 🟢 Low | 0 |
| **Total** | **6** |

---

*Report prepared by: Kushal Shrivastava | April 30, 2026*
