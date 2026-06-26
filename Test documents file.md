------------------------------------------------------------------
BUG ID: BUG_LOG_042
SUMMARY: App crashes on Swiggy cart page when clicking 'Apply Coupon' twice.
------------------------------------------------------------------
PRE-REQUISITES: User must have items added to the cart.

STEPS TO REPRODUCE:
1. Open the food delivery app and go to the Cart.
2. Click on the 'Apply Coupon' button.
3. Rapidly click the button for the second time before the network loads.

EXPECTED RESULT: The button should get disabled, or show an error message.
ACTUAL RESULT: App freezes completely and crashes with a "Not Responding" pop-up.

SEVERITY: High (Major functionality broken)
PRIORITY: High (Needs fix before release)
ENVIRONMENT: Android 14 (Samsung S23)
ATTACHMENTS: [Screenshot_Crash_Log.png]
------------------------------------------------------------------
