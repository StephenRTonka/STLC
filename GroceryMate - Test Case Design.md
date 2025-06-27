### **1\. Product Rating System**

**Test Design Techniques**: Boundary Value Analysis (BVA), Equivalence Partitioning (EP), Error Guessing, Use Case Testing

### **Test Cases:**

1. **Boundary Value Analysis**:  
   * **Test Case**: Verify rating with 1 star (minimum valid value).  
     * **Input**: 1 star selected, no comment  
     * **Expected Outcome**: Rating submitted successfully.  
2. **Boundary Value Analysis**:  
   * **Test Case**: Verify rating with 5 stars (maximum valid value).  
     * **Input**: 5 stars selected, comment \= "Excellent\!"  
     * **Expected Outcome**: Rating and comment submitted successfully.  
3. **Equivalence Partitioning**:  
   * **Test Case**: Verify submission with valid comment and rating.  
     * **Input**: 3 stars, comment \= "Decent product"  
     * **Expected Outcome**: Rating and comment saved and visible.  
4. **Equivalence Partitioning**:  
   * **Test Case**: Verify submission with only rating (no comment).  
     * **Input**: 4 stars, comment \= empty  
     * **Expected Outcome**: Rating submitted, comment optional.  
5. **Error Guessing**:  
   * **Test Case**: Verify error when submitting without selecting a star rating.  
     * **Input**: No stars selected, comment \= "Nice"  
     * **Expected Outcome**: Error message: "Please select a rating."  
6. **Error Guessing**:  
   * **Test Case**: Verify error with invalid characters in comment.  
     * **Input**: 3 stars, comment \= "alert('x')"  
     * **Expected Outcome**: Error message: "Invalid characters in comment."  
7. **Use Case Testing**:  
   * **Test Case**: Verify update of a previously submitted rating.  
     * **Input**: Update from 3 stars to 5 stars  
     * **Expected Outcome**: Updated rating and comment reflected.

---

### **2\. Age Verification for Alcoholic Products**

**Test Design Techniques**: Boundary Value Analysis (BVA), Equivalence Partitioning (EP), Error Guessing, Use Case Testing

### **Test Cases:**

1. **Boundary Value Analysis**:  
   * **Test Case**: Verify access with age exactly 18\.  
     * **Input**: Age \= 18  
     * **Expected Outcome**: Access granted to alcohol category.  
2. **Boundary Value Analysis**:  
   * **Test Case**: Verify access denied with age 17\.  
     * **Input**: Age \= 17  
     * **Expected Outcome**: Error: "You must be 18+ to enter."  
3. **Equivalence Partitioning**:  
   * **Test Case**: Verify access with valid adult age.  
     * **Input**: Age \= 25  
     * **Expected Outcome**: Access granted.  
4. **Equivalence Partitioning**:  
   * **Test Case**: Verify denial with age under 18\.  
     * **Input**: Age \= 12  
     * **Expected Outcome**: Access denied with appropriate error.  
5. **Error Guessing**:  
   * **Test Case**: Verify system behavior with no input.  
     * **Input**: Empty age field  
     * **Expected Outcome**: Error: "Please enter your age."  
6. **Error Guessing**:  
   * **Test Case**: Verify system behavior with non-numeric input.  
     * **Input**: Age \= "eighteen"  
     * **Expected Outcome**: Error: "Enter a valid number."  
7. **Use Case Testing**:  
   * **Test Case**: Verify age modal appears when navigating to alcoholic products.  
     * **Input**: Click "Alcoholic Beverages" category  
     * **Expected Outcome**: Modal appears requesting age verification.  
8. **Use Case Testing**:  
   * **Test Case**: Verify age is stored and modal doesn’t reappear during session.  
     * **Input**: Age verified \= 19, revisit alcohol section  
     * **Expected Outcome**: No modal shown again in same session.

---

### **3\. Shipping Cost Changes**

**Test Design Techniques**: Boundary Value Analysis (BVA), Equivalence Partitioning (EP), Use Case Testing, Error Guessing

### **Test Cases:**

1. **Boundary Value Analysis**:  
   * **Test Case**: Verify shipping cost when order is exactly at free shipping threshold.  
     * **Input**: Order total \= $50 (threshold)  
     * **Expected Outcome**: Free shipping applied.  
2. **Boundary Value Analysis**:  
   * **Test Case**: Verify shipping cost when order is just below the threshold.  
     * **Input**: Order total \= $49.99  
     * **Expected Outcome**: Shipping fee applied.  
3. **Equivalence Partitioning**:  
   * **Test Case**: Verify free shipping for high order total.  
     * **Input**: Order total \= $75  
     * **Expected Outcome**: No shipping charge.  
4. **Equivalence Partitioning**:  
   * **Test Case**: Verify shipping charge for low order.  
     * **Input**: Order total \= $30  
     * **Expected Outcome**: Shipping fee added.  
5. **Use Case Testing**:  
   * **Test Case**: Verify shipping fee updates when item is removed.  
     * **Input**: Add items to $60, then remove to $45  
     * **Expected Outcome**: Shipping fee reapplied automatically.  
6. **Use Case Testing**:  
   * **Test Case**: Verify coupon discount affects shipping eligibility.  
     * **Input**: Cart \= $55, Coupon \= \-$10, Net \= $45  
     * **Expected Outcome**: Shipping fee added.  
7. **Error Guessing**:  
   * **Test Case**: Verify behavior with cart value of $0.  
     * **Input**: Empty cart  
     * **Expected Outcome**: Error or no checkout allowed.  
8. **Use Case Testing**:  
   * **Test Case**: Verify consistent shipping logic for guest vs. logged-in user.  
     * **Input**: Same cart under both scenarios  
     * **Expected Outcome**: Same shipping cost applied.

