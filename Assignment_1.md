# Session 1 Assignment - Manual Testing Basics

**Student Name:** Valkesh thuthgar 
**Course Module:** Basics of Testing: Errors, Bugs, Defects, and Risks  

---

### Task 1: UI/UX Defect Observation on Flipkart Homepage
After reviewing the Flipkart homepage, here are 3 observed layout and functional discrepancies classified as defects:

1. **Misaligned Banner Text on Mobile Viewport:** 
   * *Description:* The promotional offer text overlaps with the adjacent product image when viewed on smaller screen sizes.
   * *Justification:* It violates the UX design standard and impacts readability, hence it is a defect.
2. **Delayed Response on Category Dropdown (Hover Latency):** 
   * *Description:* Hovering over the "Electronics" category takes more than 1.5 seconds to render the submenu dropdown.
   * *Justification:* Expected performance response should be under 300ms. High latency directly degrades user experience.
3. **Broken Links in Footer Section:** 
   * *Description:* Clicking on certain links under the "Policy" section in the footer redirects to a 404 Error page.
   * *Justification:* Any broken hyperlink that fails to route the user to the expected content is a functional defect.

---

### Task 2: Definitions and Real-World Examples

#### 1. Error
* **Explanation:** An error is a human mistake made by a programmer or designer during the coding or requirement phase that leads to an incorrect system implementation.
* **Real-World Example (IRCTC):** A developer accidentally types an incorrect logical condition in the age validation code, allowing users to enter a negative number as their age.

#### 2. Bug
* **Explanation:** A bug is an anomaly or fault found in the software application *during the internal testing phase* by the QA team before the product goes live.
* **Real-World Example (Instagram):** While testing a beta version, the QA tester notices that applying a specific filter causes the app to crash instantly.

#### 3. Defect
* **Explanation:** A defect is a deviation from client requirements found in the software *by end-users or clients in the production environment* after the release.
* **Real-World Example (Paytm):** A user tries to transfer money, the amount is deducted from the bank, but the app screen permanently freezes without showing a success banner.

---

### Task 3: App Failure Analysis - PhonePe Payment Failure

* **Observed Incident:** During peak hours, a UPI transaction on PhonePe gets stuck on the "Processing" screen and eventually fails.
* **Analysis of Possible Causes:**
  * **Human Error:** A developer might have failed to write proper exception handling code for timeout scenarios, leaving the UI hanging instead of throwing a clear retry message.
  * **Technical Limitation:** The banking server's API gateway can handle only a limited number of concurrent requests per second. When traffic spikes, the technical infrastructure hits its threshold capacity.
  * **Process Gap:** The product team might not have scheduled structural Load and Stress testing before releasing the mega-cashback campaign, which caused unexpected traffic management gaps.

---

### Task 4: Risk Analysis for a Food Delivery App (e.g., Swiggy)

1. **Performance Risk (Server Crash under Load):**
   * *Impact:* If thousands of users open the app simultaneously during dinner hours (8 PM - 10 PM), the server might crash. Users will face infinite loading loops, unable to place orders, causing heavy revenue and trust loss.
2. **Security Risk (Data Breach & Payment Fraud):**
   * *Impact:* If user payment tokens, saved credit cards, or location coordinates are not encrypted, hackers can steal sensitive user data, leading to severe legal and financial liabilities.
3. **Usability Risk (Complex Checkout Flow):**
   * *Impact:* If the checkout button is hidden or the address selection flow is confusing, users (especially elderly users) will get frustrated, abandon their carts, and switch to competitor apps.

---

### Task 5: Classification Matrix - Movie Ticket Booking

| Item | Classification | Justification / Reasoning |
| :--- | :--- | :--- |
| **(a) The 'Book Now' button does not respond on mobile.** | **Defect** | This is a live functional failure. The feature is completely broken in the mobile environment, which deviates directly from expected application behavior. |
| **(b) There is no logout option.** | **Defect** | This is a requirement omission defect. A standard user management system must strictly include a secure logout mechanism to protect session data. |
| **(c) The app sometimes loads slowly during IPL match days.** | **Risk** | This is an active performance risk. The application has not broken down completely yet, but high concurrent user traffic during specific events poses a future threat to app stability. |
