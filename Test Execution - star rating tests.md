### **Test Case 1: Verify rating with 1 star (minimum valid value)**

| Step\# | Action | Expected Outcome | OK/NOK | URL | Link to issue |
| ----- | ----- | ----- | ----- | ----- | ----- |
| 1 | Go to GroceryMate product detail page | Product page loads | OK | [https://grocerymate.masterschool.com/store](https://grocerymate.masterschool.com/store) |  |
| 2 | Select 1 star rating | 1 star selected | OK |  |  |
| 3 | Leave comment field empty | Comment field remains empty | OK |  |  |
| 4 | Submit rating | Rating submitted successfully | OK |  |  |
| 5 | Verify rating is visible in product reviews | 1 star rating shown without comment | OK |  |  |

### **Test Case 2: Verify rating with 5 stars (maximum valid value)**

| Step\# | Action | Expected Outcome | OK/NOK | URL | Link to issue |
| ----- | ----- | ----- | ----- | ----- | ----- |
| 1 | Go to GroceryMate product detail page | Product page loads | OK | [https://grocerymate.masterschool.com/store](https://grocerymate.masterschool.com/store) |  |
| 2 | Select 5 stars rating | 5 stars selected | OK |  |  |
| 3 | Enter comment "Excellent\!" | Comment entered | OK |  |  |
| 4 | Submit rating | Rating and comment submitted successfully | NOK |  | Bug \#1 |
| 5 | Observe error message | Error "User has already reviewed this item." shown | OK |  | Bug \#1 |

---

### **Test Case 3: Verify submission with valid comment and rating**

| Step\# | Action | Expected Outcome | OK/NOK | URL | Link to issue |
| ----- | ----- | ----- | ----- | ----- | ----- |
| 1 | Go to GroceryMate product detail page | Product page loads | OK | [https://grocerymate.masterschool.com/store](https://grocerymate.masterschool.com/store) |  |
| 2 | Select 3 stars rating | 3 stars selected | OK |  |  |
| 3 | Enter comment "Decent product" | Comment entered | OK |  |  |
| 4 | Submit rating | Rating and comment submitted successfully | NOK |  | Bug \#2 |
| 5 | Verify rating and comment visible | Rating visible; comment missing | NOK |  | Bug \#2 |

---

### **Test Case 4: Verify submission with only rating (no comment)**

| Step\# | Action | Expected Outcome | OK/NOK | URL | Link to issue |
| ----- | ----- | ----- | ----- | ----- | ----- |
| 1 | Go to GroceryMate product detail page | Product page loads | OK | [https://grocerymate.masterschool.com/store](https://grocerymate.masterschool.com/store) |  |
| 2 | Select 4 stars rating | 4 stars selected | OK |  |  |
| 3 | Leave comment empty | Comment field empty | OK |  |  |
| 4 | Submit rating | Rating submitted successfully | OK |  |  |
| 5 | Observe any error messages | No error expected | NOK (warn) |  | Bug \#3 |
| 6 | Error message "You have already reviewed this item." shown | Misleading error message | NOK (warn) |  | Bug \#3 |

---

### **Test Case 5: Verify error when submitting without selecting a star rating**

| Step\# | Action | Expected Outcome | OK/NOK | URL | Link to issue |
| ----- | ----- | ----- | ----- | ----- | ----- |
| 1 | Go to GroceryMate product detail page | Product page loads | OK | [https://grocerymate.masterschool.com/store](https://grocerymate.masterschool.com/store) |  |
| 2 | Do not select any star rating | No star rating selected | OK |  |  |
| 3 | Enter comment "Nice" | Comment entered | OK |  |  |
| 4 | Submit rating | Submission blocked with error message | OK |  |  |
| 5 | Verify error message | "Please select a rating." displayed | OK |  |  |

---

### **Test Case 6: Verify error with invalid characters in comment**

| Step\# | Action | Expected Outcome | OK/NOK | URL | Link to issue |
| ----- | ----- | ----- | ----- | ----- | ----- |
| 1 | Go to GroceryMate product detail page | Product page loads | OK | [https://grocerymate.masterschool.com/store](https://grocerymate.masterschool.com/store) |  |
| 2 | Select 3 stars rating | 3 stars selected | OK |  |  |
| 3 | Enter comment `alert('x')` | Comment entered | OK |  |  |
| 4 | Submit rating | Submission blocked with "Invalid characters" error | NOK |  | Bug \#4 |
| 5 | Observe error message | Error message displayed | NOK |  | Bug \#4 |
| 6 | Actual result shows only "You can only review once" message | No invalid character error shown | NOK |  | Bug \#4 |

---

### **Test Case 7: Verify update of a previously submitted rating**

| Step\# | Action | Expected Outcome | OK/NOK | URL | Link to issue |
| ----- | ----- | ----- | ----- | ----- | ----- |
| 1 | Go to GroceryMate product detail page | Product page loads | OK | [https://grocerymate.masterschool.com/store](https://grocerymate.masterschool.com/store) |  |
| 2 | Submit rating: 3 stars | 3 stars rating saved | OK |  |  |
| 3 | Update rating to 5 stars | 5 stars rating saved | OK |  |  |
| 4 | Verify updated rating is visible | New rating displayed | OK |  |  |

 