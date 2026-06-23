# Session 2 Assignment - Test Organization

**Student Name:** Valkesh thuthgar  
**Course Module:** Test Organization, QA vs QC, Testing vs Debugging, and Test Plan  

---

### Task 1: Roles and Responsibilities (Tester vs Test Leader)

#### A. Software Tester (QA Engineer)
1. **Responsibilities:**
   * Reviewing requirements/HLR to identify ambiguity.
   * Writing detailed test scenarios, test cases, and preparing test data.
   * Executing test cases during builds and logging defects with clear steps to reproduce.
2. **Release Cycle Contribution Example:** During a release sprint, the tester actively executes regression test suites on the staging environment to ensure new bug fixes haven't broken existing features like Checkout or Payment.

#### B. Test Leader (Test Manager)
1. **Responsibilities:**
   * Defining the overall test strategy, writing the Master Test Plan, and estimating timelines.
   * Assigning tasks to the testing team and tracking daily execution metrics.
   * Acting as the primary point of contact for cross-functional alignment (Developers, Product Owners).
2. **Release Cycle Contribution Example:** Before the final deployment, the Test Leader reviews the open bug metrics, evaluates remaining quality risks, and formally signs off on the "Go/No-Go" release decision.

---

### Task 2: QA vs QC Comparison for Instagram

For an app like Instagram, **Quality Assurance (QA)** is a proactive, process-oriented approach performed *before and during* coding. It involves activities like setting coding standards, conducting design reviews, and planning workflows (e.g., establishing a process where no code can be merged into production without peer review and automated sanity checks) to prevent bugs from being introduced in the new Reels filter feature. On the other hand, **Quality Control (QC)** is a reactive, product-oriented approach performed *after* the coding is complete. It involves actual testing activities where a QA tester manually opens the Instagram build, applies the new Reels filter, checks for crashes, verifies the visual alignment, and logs defects to ensure the final product matches the specified requirements before public release.

---

### Task 3: Testing vs Debugging (Flipkart Shopping Cart Example)

When a critical bug is found in a Flipkart-style shopping cart feature (e.g., the cart total does not update when a item quantity is changed):

* **What the Tester Does (Testing):** The tester performs *Testing* by executing the steps, identifying the defect, analyzing the expected behavior ($100 \times 2 = \$200$) versus actual behavior (stuck at \$100), logging a detailed bug report with screenshots/console logs, and assigning it to the developer. The tester's job is to uncover and document the discrepancy without altering the source code.
* **What the Developer Does (Debugging):** The developer performs *Debugging* by taking the tester's bug report, analyzing the root cause within the source code (e.g., finding a missing event listener or a broken JavaScript loop variable like `cartTotal`), fixing the faulty logic, and running unit tests to ensure the specific code bug is eliminated.

---

### Task 4: Test Plan Skeleton for Food Delivery App (Order Tracking Feature)

#### 1. Test Plan ID
`TP_SWIGGY_TRACK_2026_V1`

#### 2. Feature Description
This feature enables real-time GPS-based tracking for customers after an order is placed. It includes live status updates ("Order Accepted", "Food Preparing", "Driver Dispatched"), showing the driver's real-time movement on an interactive map component, and sending contextual push notifications at key delivery milestones.

#### 3. Test Scope
* **In-Scope (What to test):**
  * Verification of live GPS coordinates updates on the map interface.
  * Validation of milestone status triggers based on delivery partner actions.
  * Functional testing of the "Call Driver" masking feature.
  * Handling network switches (e.g., moving from Wi-Fi to 5G while tracking).
* **Out-of-Scope (What not to test):**
  * Restaurant partner dashboard backend mechanics.
  * Payment gateway processing (as it happens before tracking initializes).

#### 4. Roles & Responsibilities
* **Test Leader:** Oversees overall validation velocity, approves the environment setup, and tracks blockages.
* **Functional Tester (Valkesh):** Responsible for designing end-to-end edge test cases, executing tracking cycles using mock GPS tools, and reporting defects.

#### 5. Test Environment
* **Mobile Hardware:** Android (Samsung Galaxy S23 - OS 14), iOS (iPhone 15 - OS 17)
* **Testing Tools:** Android Studio Emulator, Charles Proxy (for intercepting network traffic), Live Location Mocking Apps.
* **Build URL:** Staging Environment Sandboxed Build (`v4.12.0-RC1`)

#### 6. Test Deliverables
* Final Approved Test Plan Document.
* Comprehensive Test Cases Executed Sheet (Passed/Failed Metrics).
* Open & Resolved Bug Summary Logs.
* Final Quality Sign-Off Certificate.
