## **The Software**

Online grocery shopping platform, with the following existing functions:

* Browse and search for grocery products

* Add products to the shopping cart

* Checkout and pay for orders

* User registration and login

* Categories for different types of products (e.g., fruits, vegetables, dairy, etc.)

* User profile management

* Basic order tracking

## **New Features**

---

### **1\. Product Rating System**

**Requirement**:

* Users should be able to rate products with a 5-star system and optionally leave written feedback.

**Questions**:

1. Who can rate a product — any user or only users who purchased the product?

2. Is the rating system limited to whole stars (1–5), or can users select half-star ratings (e.g., 4.5)?

3. What is the maximum character count for written feedback?

4. Should ratings and reviews be moderated (e.g., profanity filter, inappropriate content)?

5. Where will the ratings and feedback be displayed (e.g., product page, user profile)?

6. Can a user update or delete their rating after submission?

**Detailed Requirement**:

* Logged-in users who have purchased a product can leave a rating from 1 to 5 stars (whole numbers only). Users may also optionally include a written review (up to 500 characters).

* The product detail page should display an average star rating and a list of reviews, showing the username, star rating, and feedback.

* Users can edit or delete their rating and review at any time from their order history or product page.

* A profanity filter must be applied to all submitted feedback.

* Star ratings should contribute to the product's average score, updated dynamically as new ratings are added.

---

### **2\. Age Verification for Alcoholic Products**

**Vague Requirement**:

* Alcoholic products require age verification. A true/false Boolean should ask if the user is 18+ before they can access alcoholic products.

**Questions**:

1. How should the user's age be verified — by self-declaration entering date of birth?

2. Should the age verification happen every time, or can it be stored in the session?

3. What happens if the user indicates they are under 18?

4. Are there any legal disclaimers or terms to display on the age verification modal?

5. Is there a separate category/page for alcoholic products?

**Detailed Requirement**:

* When a user attempts to access the "Alcoholic Products" category, a dialog should appear prompting the user to input their date of birth.

* If the user's age is 18 or older, they are granted access to the category for the duration of the session.

* If the user is under 18 or enters a date indicating they are under 18, access to the category is denied and an appropriate message is shown.

* A disclaimer should be displayed indicating the legal restriction and purpose of data use.

* The Boolean True/False must prevent interaction with the rest of the website until a valid response is submitted.

---

### **3\. Shipping Cost Changes**

**Vague Requirement**:

* Free shipping for orders above a certain amount. Orders below this amount will incur a shipping fee.

**Questions**:

1. What is the minimum order amount required for free shipping?

2. What is the exact shipping fee for orders below the threshold?

3. Will the free shipping threshold vary by region or product type?

4. Where should the shipping cost be displayed during the checkout process?

5. Will the system display a message prompting users to add more items for free shipping?

**Detailed Requirement**:

* Users will receive free shipping on orders with a subtotal of €50 or more.

* Orders with a subtotal below €50 will incur a flat shipping fee of €4.99.

* During checkout, the shipping cost should be clearly listed in the cost summary.

* If a user’s cart subtotal is under €50, the cart page and checkout screen should display a dynamic message suggesting how much more needs to be added to qualify for free shipping.

* The shipping cost logic should automatically update if items are added or removed from the cart.

