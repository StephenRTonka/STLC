### **Test Execution Report** 

**Feature:** Product Rating System  
 **Application:** GroceryMate  
 **Environment:** Test  
 **Browser:** Chrome  
 **Operating System:** Windows 10  
 **Tester:** Stephen Russell  
 **Date:** 20-06-2025

### **Bug Report**

**Title:** User prevented from submitting a valid new rating due to “already reviewed” error

**Priority:** High  
 **Reporter:** Stephen Russell  
 **Date:** 20-06-2025

**Environment:** Test  
 **Application:** GroceryMate  
 **Page:** Product Detail / Rating Submission  
 **Browser:** Chrome  
 **Operating System:** Windows 10

**Steps to Reproduce:**

1. Navigate to GroceryMate product detail page.

2. Submit a 5-star rating with comment "Excellent\!" for a product.

3. Attempt to submit another rating for the same product with the same or a different user account.

**Expected Result:**  
 Rating and comment should be accepted if not previously submitted by the same user.

**Actual Result:**  
 Error message displayed: "User has already reviewed this item." even with different user accounts. Submission blocked.

**Screenshots/Attachments:**  
 bug screenshot \- (i will add the screenshots later)

**Additional Information:**  
 This restricts valid new reviews and may be caused by session or user identification logic errors.

---

### **Bug Report**

**Title:** User comments not saved or displayed with product ratings

**Priority:** Medium  
 **Reporter:** Stephen Russell  
 **Date:** 20-06-2025

**Environment:** Test  
 **Application:** GroceryMate  
 **Page:** Product Detail / Rating Submission  
 **Browser:** Chrome  
 **Operating System:** Windows 10

**Steps to Reproduce:**

1. Navigate to GroceryMate product detail page.

2. Submit a rating (e.g., 3 stars) with a comment like "Decent product".

3. Check the product reviews after submission.

**Expected Result:**  
 Both rating and comment should be saved and visible under product reviews.

**Actual Result:**  
 Only the rating is visible; the comment is missing or not displayed.

**Screenshots/Attachments:**  
 bug screenshot \- (i will add the screenshots later)

**Additional Information:**  
 Likely a backend or UI bug that prevents user comments from being stored or rendered.

---

### **Bug Report**

**Title:** Misleading “already reviewed” error message shown despite successful rating submission

**Priority:** Low  
 **Reporter:** Stephen Russell  
 **Date:** 20-06-2025

**Environment:** Test  
 **Application:** GroceryMate  
 **Page:** Product Detail / Rating Submission  
 **Browser:** Chrome  
 **Operating System:** Windows 10

**Steps to Reproduce:**

1. Submit a rating (e.g., 4 stars) without a comment on a product.

2. Observe the feedback messages post submission.

**Expected Result:**  
 Successful submission without any error message.

**Actual Result:**  
 Rating is saved but an error message "You have already reviewed this item." is displayed erroneously.

**Screenshots/Attachments:**  
 bug screenshot \- (i will add the screenshots later)

**Additional Information:**  
 Confusing for users and should be corrected for better UX.

---

### **Bug Report**

**Title:** Invalid character input in comments not detected or blocked, posing security risk

**Priority:** Critical  
 **Reporter:** Stephen Russell  
 **Date:** 20-06-2025

**Environment:** Test  
 **Application:** GroceryMate  
 **Page:** Product Detail / Rating Submission  
 **Browser:** Chrome  
 **Operating System:** Windows 10

**Steps to Reproduce:**

1. Navigate to GroceryMate product detail page.

2. Submit a rating (e.g., 3 stars) with comment: `alert('x')`

3. Observe any validation or error messages.

**Expected Result:**  
 An error message should prevent submission due to invalid characters (script injection attempt).

**Actual Result:**  
 No validation error shown; submission blocked only by "You can only review this product once." message, ignoring invalid input.

**Screenshots/Attachments:**  
 bug screenshot \- (i will add the screenshots later)

**Additional Information:**  
 Lack of input sanitization may lead to cross-site scripting (XSS) vulnerabilities.

---

**Feature:** Age Verification for Alcoholic Products  
 **Application:** GroceryMate  
 **Environment:** Test  
 **Browser:** Chrome  
 **Operating System:** Windows 10  
 **Tester:** Stephen Russell  
 **Date:** 27-06-2025

---

### **Bug Report**

**Title:** Age verification modal does not appear when accessing alcoholic products  
 **Priority:** Critical  
 **Reporter:** Stephen Russell  
 **Date:** 27-06-2025  
 **Environment:** Test  
 **Application:** GroceryMate  
 **Page:** Alcoholic Beverages Category  
 **Browser:** Chrome  
 **Operating System:** Windows 10

**Steps to Reproduce:**

1. Navigate to GroceryMate store.

2. Click on “Alcoholic Beverages” category.

**Expected Result:**  
 Age verification modal should appear requesting user to input age and restrict access if under 18\.

**Actual Result:**  
 No modal or age input field appears; unrestricted access to alcoholic products is granted.

**Screenshots/Attachments:**  
 bug screenshot \- (I will add the screenshots later)

**Additional Information:**  
 This poses a serious compliance risk by allowing unrestricted access to alcohol regardless of age.

---

### **Bug Report**

**Title:** No validation or error on empty age input or non-numeric values  
 **Priority:** High  
 **Reporter:** Stephen Russell  
 **Date:** 27-06-2025  
 **Environment:** Test  
 **Application:** GroceryMate  
 **Page:** Alcoholic Beverages Age Verification  
 **Browser:** Chrome  
 **Operating System:** Windows 10

**Steps to Reproduce:**

1. Attempt to input no age or enter non-numeric text (e.g., “eighteen”) if the modal appeared (note: modal does not appear, but if it did).

**Expected Result:**  
 Validation errors should appear: “Please enter your age.” or “Enter a valid number.”

**Actual Result:**  
 No modal or input field exists; no validation errors triggered.

**Screenshots/Attachments:**  
 bug screenshot \- (I will add the screenshots later)

**Additional Information:**  
 Validation logic is missing or not triggered, which makes age verification ineffective.

---

### **Bug Report**

**Title:** Age is not stored during session; modal does not reappear on revisits  
 **Priority:** Medium  
 **Reporter:** Stephen Russell  
 **Date:** 27-06-2025  
 **Environment:** Test  
 **Application:** GroceryMate  
 **Page:** Alcoholic Beverages Category  
 **Browser:** Chrome  
 **Operating System:** Windows 10

**Steps to Reproduce:**

1. Verify age modal appears on first visit (does not appear currently).

2. Navigate away and revisit alcohol category.

**Expected Result:**  
 Age verification modal should not reappear during the same session after successful verification.

**Actual Result:**  
 Modal never appears initially; no age stored or remembered during session.

**Screenshots/Attachments:**  
 bug screenshot \- (I will add the screenshots later)

**Additional Information:**  
 Session management for age verification is not implemented or broken.

---

**Feature:** Shipping Cost Changes  
 **Application:** GroceryMate  
 **Environment:** Test  
 **Browser:** Chrome  
 **Operating System:** Windows 10  
 **Tester:** Stephen Russell  
 **Date:** 27-06-2025

---

### **Bug Report**

**Title:** No confirmation or shipping cost summary displayed after checkout  
 **Priority:** Critical  
 **Reporter:** Stephen Russell  
 **Date:** 27-06-2025  
 **Environment:** Test  
 **Application:** GroceryMate  
 **Page:** Checkout / Order Confirmation  
 **Browser:** Chrome  
 **Operating System:** Windows 10

**Steps to Reproduce:**

1. Add items to cart totaling $20 (free shipping threshold).

2. Proceed to checkout and complete the order.

**Expected Result:**  
 A confirmation page or message should appear showing order success, total price, and shipping cost details.

**Actual Result:**  
 No confirmation page or shipping summary is displayed; user receives no feedback on order completion or shipping charges.

**Screenshots/Attachments:**  
 bug screenshot \- (I will add the screenshots later)

**Additional Information:**  
 This affects the ability to verify shipping fee application and negatively impacts user experience and trust.

---

### **Bug Report**

**Title:** Guest users cannot add products to cart; redirected to sign-in page  
 **Priority:** Medium  
 **Reporter:** Stephen Russell  
 **Date:** 27-06-2025  
 **Environment:** Test  
 **Application:** GroceryMate  
 **Page:** Storefront / Product Page  
 **Browser:** Chrome  
 **Operating System:** Windows 10

**Steps to Reproduce:**

1. Visit GroceryMate store without logging in.

2. Attempt to add products to the cart.

**Expected Result:**  
 Guest users should be able to add items to cart and proceed to checkout or guest checkout.

**Actual Result:**  
 Guests are immediately redirected to the sign-in page, preventing cart interaction or shipping logic testing.

**Screenshots/Attachments:**  
 bug screenshot \- (I will add the screenshots later)

**Additional Information:**  
 Prevents testing of shipping cost consistency between guest and logged-in users and limits guest user experience.

