# **Test Execution Report**

**Feature:** Age Verification for Alcoholic Products  
 **Application:** GroceryMate  
 **Environment:** Test  
 **Browser:** Chrome  
 **Operating System:** Windows 10  
 **Tester:** Stephen Russell  
 **Date:** 27-06-2025

---

### **Test Case 1: Verify access with age exactly 18**

| Step\# | Action | Expected Outcome | OK/NOK | URL | Link to issue |
| ----- | ----- | ----- | ----- | ----- | ----- |
| 1 | Navigate to GroceryMate store | Storefront loads | OK | [https://grocerymate.masterschool.com/store](https://grocerymate.masterschool.com/store) |  |
| 2 | Click on “Alcoholic Beverages” category | Age verification modal appears | NOK |  | Bug \#5 |
| 3 | Enter age \= 18 | Access granted to alcoholic items | NOK |  | Bug \#5 |

---

### **Test Case 2: Verify access denied with age 17**

| Step\# | Action | Expected Outcome | OK/NOK | URL | Link to issue |
| ----- | ----- | ----- | ----- | ----- | ----- |
| 1 | Navigate to GroceryMate store | Storefront loads | OK | [https://grocerymate.masterschool.com/store](https://grocerymate.masterschool.com/store) |  |
| 2 | Click on “Alcoholic Beverages” category | Age verification modal appears | NOK |  | Bug \#5 |
| 3 | Enter age \= 17 | Error: “You must be 18+ to enter.” | NOK |  | Bug \#5 |

---

### **Test Case 3: Verify access with valid adult age (25)**

| Step\# | Action | Expected Outcome | OK/NOK | URL | Link to issue |
| ----- | ----- | ----- | ----- | ----- | ----- |
| 1 | Navigate to GroceryMate store | Storefront loads | OK | [https://grocerymate.masterschool.com/store](https://grocerymate.masterschool.com/store) |  |
| 2 | Click on “Alcoholic Beverages” category | Age verification modal appears | NOK |  | Bug \#5 |
| 3 | Enter age \= 25 | Access granted to alcoholic items | NOK |  | Bug \#5 |

---

### **Test Case 4: Verify denial with age under 18 (12)**

| Step\# | Action | Expected Outcome | OK/NOK | URL | Link to issue |
| ----- | ----- | ----- | ----- | ----- | ----- |
| 1 | Navigate to GroceryMate store | Storefront loads | OK | [https://grocerymate.masterschool.com/store](https://grocerymate.masterschool.com/store) |  |
| 2 | Click on “Alcoholic Beverages” category | Age verification modal appears | NOK |  | Bug \#5 |
| 3 | Enter age \= 12 | Access denied with appropriate error | NOK |  | Bug \#5 |

---

### **Test Case 5: Verify system behavior with no input**

| Step\# | Action | Expected Outcome | OK/NOK | URL | Link to issue |
| ----- | ----- | ----- | ----- | ----- | ----- |
| 1 | Navigate to GroceryMate store | Storefront loads | OK | [https://grocerymate.masterschool.com/store](https://grocerymate.masterschool.com/store) |  |
| 2 | Click on “Alcoholic Beverages” category | Age verification modal appears | NOK |  | Bug \#5 |
| 3 | Leave age input empty | Error: “Please enter your age.” | NOK |  | Bug \#5 |

---

### **Test Case 6: Verify system behavior with non-numeric input**

| Step\# | Action | Expected Outcome | OK/NOK | URL | Link to issue |
| ----- | ----- | ----- | ----- | ----- | ----- |
| 1 | Navigate to GroceryMate store | Storefront loads | OK | [https://grocerymate.masterschool.com/store](https://grocerymate.masterschool.com/store) |  |
| 2 | Click on “Alcoholic Beverages” category | Age verification modal appears | NOK |  | Bug \#5 |
| 3 | Enter age \= “eighteen” (non-numeric input) | Error: “Enter a valid number.” | NOK |  | Bug \#5 |

---

### **Test Case 7: Verify age modal appears when navigating to alcoholic products**

| Step\# | Action | Expected Outcome | OK/NOK | URL | Link to issue |
| ----- | ----- | ----- | ----- | ----- | ----- |
| 1 | Navigate to GroceryMate store | Storefront loads | OK | [https://grocerymate.masterschool.com/store](https://grocerymate.masterschool.com/store) |  |
| 2 | Click on “Alcoholic Beverages” category | Age verification modal appears | NOK |  | Bug \#5 |

---

### **Test Case 8: Verify age is stored and modal doesn’t reappear during session**

| Step\# | Action | Expected Outcome | OK/NOK | URL | Link to issue |
| ----- | ----- | ----- | ----- | ----- | ----- |
| 1 | Navigate to GroceryMate store | Storefront loads | OK | [https://grocerymate.masterschool.com/store](https://grocerymate.masterschool.com/store) |  |
| 2 | Click on “Alcoholic Beverages” category | Age verification modal appears (once) | NOK |  | Bug \#5 |
| 3 | Navigate away and revisit Alcoholic Beverages | Modal does not reappear during session revisit | NOK |  | Bug \#5 |

---

