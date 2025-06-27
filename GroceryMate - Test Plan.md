## **1\. Analyze the Product**

### **Objective**

To validate the proper implementation of the new features on the MarketMate webshop, focusing on user experience, data validation, and accurate logic for shipping, ratings, and age restrictions.

### **New Features to Test**

* **Product Rating System**

* **Age Verification for Alcoholic Products**

* **Shipping Cost Logic**

### **User Base**

All registered and guest users of the webshop, including:

* Users under and over 18 years

* Buyers of general and restricted items

* Users on desktop and mobile devices

### **Hardware and Software Specifications**

* **Devices**: Smartphones, tablets, desktops

* **Operating Systems**: Windows, macOS, iOS, Android

* **Browsers**: Chrome, Safari, Firefox, Edge

* **Dependencies**: Backend APIs, UI components, Payment Gateway, User Profiles

---

## **2\. Test Strategy**

### **Scope**

✅ In Scope:

* Rating system for products (UI \+ backend)

* Age gate and verification for alcohol category

* Logic for free shipping threshold

❌ Out of Scope:

* Internal analytics for rating data

* Complex tax or currency calculations

* Backend data storage

### **Testing Types**

* Functional Testing

* UI/UX Testing

* Boundary Value Analysis (BVA)

* Security (for age verification bypass attempts)

* Regression Testing (for checkout flow)

### **Risks & Mitigation**

| Risk | Mitigation |
| ----- | ----- |
| Bypass of age gate | Add cookie \+ backend validation |
| Rating system abuse (spam reviews) | Limit reviews per product per user |
| Shipping rule logic conflicts | Test price thresholds, coupons, and edge cases |

---

## **3\. Test Objectives**

| Objective | Expected Outcome |
| ----- | ----- |
| Rating submission | User can rate products 1-5 stars and leave a comment |
| Age gate enforcement | Alcoholic category access blocked until age is verified |
| Shipping logic | Free shipping applies only when order total meets threshold |

---

## **4\. Test Criteria**

### **Suspension Criteria**

* Rating API unavailable

* Age true/false fails to render

* Checkout blocked due to shipping errors

### **Exit Criteria**

* All P1 and P2 defects closed

* ≥95% test case execution

* ≥90% pass rate

* Age verification works across all devices

* Ratings display and update correctly

---

## **5\. Resource Planning**

| Role | Name |
| ----- | ----- |
| QA Lead | Jane Smith |
| Functional Tester | John Doe |
| Regression Tester | Alice White |
| UAT Participant | Maria Green |

---

## **6\. Test Environment**

* Environments: DEV → TEST → PROD

* Devices: iPhone, Android phones, Chrome Desktop, Safari macOS

* Tools: Selenium and Pytest

---

## **7\. Schedule & Estimation**

| Activity | Start | End | Effort |
| ----- | ----- | ----- | ----- |
| Test Case Design | 20-Jun | 22-Jun | 16h |
| Functional Testing | 23-Jun | 26-Jun | 24h |
| Regression \+ UAT | 27-Jun | 28-Jun | 12h |

---

## **8\. Test Deliverables**

* Test Plan

* Test Cases

* Bug Reports

* Execution Log

* Sign off

