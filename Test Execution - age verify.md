### **Test Case 1: Verify access with age exactly 18**

| Step\# | Action | Expected Outcome | OK/NOK | URL | Link to issue |
| ----- | ----- | ----- | ----- | ----- | ----- |
| 1 | Go to GroceryMate product detail page | Homepage/product page loads | OK | [https://grocerymate.masterschool.com/store](https://grocerymate.masterschool.com/store) |  |
| 2 | Click on "Alcoholic Beverages" category | Age verification modal appears | NOK |  | Bug \#5 |
| 3 | Attempt to enter age: 18 | Age input field visible | NOK |  | Bug \#5 |
| 4 | Submit | Access granted after age check | NOK |  | Bug \#5 |

---

### **Test Case 2: Verify access denied with age 17**

| Step\# | Action | Expected Outcome | OK/NOK | URL | Link to issue |
| ----- | ----- | ----- | ----- | ----- | ----- |
| 1 | Go to Alcoholic Beverages category | Age verification modal appears | NOK | [https://grocerymate.masterschool.com/store](https://grocerymate.masterschool.com/store) | Bug \#5 |
| 2 | Enter age: 17 | Input field present and accepts input | NOK |  | Bug \#5 |
| 3 | Submit | Error shown: "You must be 18+ to enter" | NOK |  | Bug \#5 |

---

### **Test Case 3: Verify access with valid adult age (25)**

| Step\# | Action | Expected Outcome | OK/NOK | URL | Link to issue |
| ----- | ----- | ----- | ----- | ----- | ----- |
| 1 | Go to Alcoholic Beverages category | Age modal appears | NOK | [https://grocerymate.masterschool.com/store](https://grocerymate.masterschool.com/store) | Bug \#5 |
| 2 | Enter age: 25 | Age input accepted | NOK |  | Bug \#5 |
| 3 | Submit | Access granted | NOK |  | Bug \#5 |

---

### **Test Case 4: Verify denial with age under 18 (age \= 12\)**

| Step\# | Action | Expected Outcome | OK/NOK | URL | Link to issue |
| ----- | ----- | ----- | ----- | ----- | ----- |
| 1 | Go to Alcoholic Beverages category | Age modal appears | NOK | [https://grocerymate.masterschool.com/store](https://grocerymate.masterschool.com/store) | Bug \#5 |
| 2 | Enter age: 12 | Age input accepted | NOK |  | Bug \#5 |
| 3 | Submit | Access denied with age-related error | NOK |  | Bug \#5 |

---

### **Test Case 5: Verify system behavior with no input**

| Step\# | Action | Expected Outcome | OK/NOK | URL | Link to issue |
| ----- | ----- | ----- | ----- | ----- | ----- |
| 1 | Go to Alcoholic Beverages category | Age modal appears | NOK | [https://grocerymate.masterschool.com/store](https://grocerymate.masterschool.com/store) | Bug \#5 |
| 2 | Leave age field empty | Input field remains empty | NOK |  | Bug \#5 |
| 3 | Submit | Error: "Please enter your age." shown | NOK |  | Bug \#5 |

---

### **Test Case 6: Verify system behavior with non-numeric input**

| Step\# | Action | Expected Outcome | OK/NOK | URL | Link to issue |
| ----- | ----- | ----- | ----- | ----- | ----- |
| 1 | Go to Alcoholic Beverages category | Age modal appears | NOK | [https://grocerymate.masterschool.com/store](https://grocerymate.masterschool.com/store) | Bug \#5 |
| 2 | Enter age: "eighteen" | Invalid input flagged | NOK |  | Bug \#5 |
| 3 | Submit | Error: "Enter a valid number." shown | NOK |  | Bug \#5 |

---

### **Test Case 7: Verify age modal appears when navigating to alcoholic products**

| Step\# | Action | Expected Outcome | OK/NOK | URL | Link to issue |
| ----- | ----- | ----- | ----- | ----- | ----- |
| 1 | Go to GroceryMate homepage | Homepage loads | OK | [https://grocerymate.masterschool.com/store](https://grocerymate.masterschool.com/store) |  |
| 2 | Click "Alcoholic Beverages" | Modal appears requesting age input | NOK |  | Bug \#5 |

---

### **Test Case 8: Verify age is stored and modal doesn’t reappear during session**

| Step\# | Action | Expected Outcome | OK/NOK | URL | Link to issue |
| ----- | ----- | ----- | ----- | ----- | ----- |
| 1 | Go to Alcoholic Beverages category | Age modal appears | NOK | [https://grocerymate.masterschool.com/store](https://grocerymate.masterschool.com/store) | Bug \#5 |
| 2 | Enter age: 19 | Age stored | NOK |  | Bug \#5 |
| 3 | Submit | Access granted | NOK |  | Bug \#5 |
| 4 | Navigate away and return to Alcoholic Beverages | Modal does **not** reappear during session | NOK |  | Bug \#5 |

---

### **Summary of Execution – Age Verification Feature**

| Test Case ID | Description | Status | Notes |
| ----- | ----- | ----- | ----- |
| 1 | Access with age 18 | Fail | No modal, unrestricted access |
| 2 | Access denied with age 17 | Fail | No modal, age not collected |
| 3 | Access with age 25 | Fail | No modal shown |
| 4 | Denial with age 12 | Fail | No validation performed |
| 5 | No age input | Fail | No input field displayed |
| 6 | Non-numeric input (e.g., "eighteen") | Fail | No validation triggered |
| 7 | Age modal appears when visiting alcohol category | Fail | Modal does not appear |
| 8 | Age stored and modal suppressed during session revisit | Fail | Feature not functional |

