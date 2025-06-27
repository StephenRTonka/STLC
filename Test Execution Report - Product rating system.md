# **Test Execution Report**

**Feature:** Product Rating System  
 **Application:** GroceryMate  
 **Environment:** Test  
 **Browser:** Chrome  
 **Operating System:** Windows 10  
 **Tester:** Stephen Russell  
 **Date:** 20-06-2025

---

### **Test Case 1: Verify rating with 1 star (minimum valid value)**

| Step\# | Action | Expected Outcome | OK/NOK | URL | Link to issue |
| ----- | ----- | ----- | ----- | ----- | ----- |
| 1 | Navigate to GroceryMate product page | Product page loads | OK | [https://grocerymate.masterschool.com/store](https://grocerymate.masterschool.com/store) |  |
| 2 | Submit 1-star rating with no comment | Rating submitted successfully | OK |  |  |

---

### **Test Case 2: Verify rating with 5 stars and a comment**

| Step\# | Action | Expected Outcome | OK/NOK | URL | Link to issue |
| ----- | ----- | ----- | ----- | ----- | ----- |
| 1 | Submit 5-star rating with comment "Excellent\!" | Rating and comment submitted successfully | NOK |  | Bug \#1 |

---

### **Test Case 3: Verify submission with valid comment and rating (EP)**

| Step\# | Action | Expected Outcome | OK/NOK | URL | Link to issue |
| ----- | ----- | ----- | ----- | ----- | ----- |
| 1 | Submit 3-star rating with comment "Decent product" | Rating and comment saved and visible | NOK |  | Bug \#2 |

---

### **Test Case 4: Verify submission with only rating (no comment)**

| Step\# | Action | Expected Outcome | OK/NOK | URL | Link to issue |
| ----- | ----- | ----- | ----- | ----- | ----- |
| 1 | Submit 4-star rating with no comment | Rating submitted, no comment required | NOK |  | Bug \#3 |

---

### **Test Case 5: Submit without selecting a star rating**

| Step\# | Action | Expected Outcome | OK/NOK | URL | Link to issue |
| ----- | ----- | ----- | ----- | ----- | ----- |
| 1 | Leave stars unselected, add comment | Error: “Please select a rating.” | OK |  |  |

---

### **Test Case 6: Submit with invalid characters in comment**

| Step\# | Action | Expected Outcome | OK/NOK | URL | Link to issue |
| ----- | ----- | ----- | ----- | ----- | ----- |
| 1 | Submit 3-star rating with comment `alert('x')` | Error: “Invalid characters in comment.” | NOK |  | Bug \#4 |

---

### **Test Case 7: Update a previously submitted rating**

| Step\# | Action | Expected Outcome | OK/NOK | URL | Link to issue |
| ----- | ----- | ----- | ----- | ----- | ----- |
| 1 | Update rating from 3 stars to 5 stars with comment | Updated rating and comment reflected | OK |  |  |

