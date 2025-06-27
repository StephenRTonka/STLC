

### 

### **Test Case 1: Verify shipping cost when order is exactly at free shipping threshold ($20)**

| Step\# | Action | Expected Outcome | OK/NOK | URL | Link to issue |
| ----- | ----- | ----- | ----- | ----- | ----- |
| 1 | Log in or continue as guest | Access to store | OK | [https://grocerymate.masterschool.com/store](https://grocerymate.masterschool.com/store) |  |
| 2 | Add items to cart totaling exactly $20.00 | Cart shows $20 subtotal | OK |  |  |
| 3 | Proceed to checkout | Free shipping applied and confirmation displayed | NOK |  | Bug \#6 |

---

### **🐞 Bug Report: Bug \#6**

**Title:** No confirmation or shipping summary displayed after completing order

**Priority:** High  
 **Reporter:** Stephen Russell  
 **Date:** 27-06-2025

**Environment:** Test  
 **Application:** GroceryMate  
 **Page:** Checkout flow  
 **Browser:** Chrome  
 **Operating System:** macOS

**Steps to Reproduce:**

1. Go to [https://grocerymate.masterschool.com/store](https://grocerymate.masterschool.com/store)

2. Add items to cart totaling exactly $20

3. Proceed to checkout and attempt to place the order

**Expected Result:**  
 A confirmation screen should appear with a clear success message and a shipping cost breakdown (free or applied).

**Actual Result:**  
 After submitting the order, **no confirmation screen** appears. There is **no feedback** regarding success, failure, shipping, or total. The user is left without any clear indication of the result.

**Screenshots/Attachments:**  
 To be added manually.

**Additional Info:**  
 This affects not only the verification of shipping logic, but also the general order confirmation flow. It may also impact user trust and repeat purchases.

---

### **Test Case 8: Verify consistent shipping logic for guest vs. logged-in user**

| Step\# | Action | Expected Outcome | OK/NOK | URL | Link to issue |
| ----- | ----- | ----- | ----- | ----- | ----- |
| 1 | Log in and create cart with $20 total | Free shipping applied | NOK | [https://grocerymate.masterschool.com/store](https://grocerymate.masterschool.com/store) | Bug \#6 |
| 2 | Log out and try to recreate same cart as guest | Same shipping logic expected | **NOK** (Blocked) | User is redirected to login page | Bug \#7 |

## **Shipping Cost Changes – Execution Summary**

| Test Case ID | Description | Status | Notes |
| ----- | ----- | ----- | ----- |
| TC1 | Free shipping at $20 threshold | **Fail** | No confirmation or shipping info shown |
| TC2 | Shipping fee at $19.99 | **Fail** | Same issue — checkout lacks summary or feedback |
| TC3 | Free shipping for $75 order | **Fail** | No visible indication of shipping logic or final pricing |
| TC4 | Shipping charge for $10 order | **Fail** | Cannot verify due to missing checkout confirmation |
| TC5 | Shipping updates after item removal ($60 → $15) | **Fail** | No update or summary displayed |
| TC6 | Coupon brings $25 cart to $15 → shipping should apply | **Fail** | Discounted total accepted, but no shipping info visible |
| TC7 | Empty cart checkout prevented | **Fail** | No explicit error message or block observed; unclear behavior |
| TC8 | Compare guest vs. logged-in user shipping logic | **Fail** | In both cases, shipping fee logic could not be observed or confirmed |

