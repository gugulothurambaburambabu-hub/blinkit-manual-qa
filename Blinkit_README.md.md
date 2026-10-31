# Blinkit Android App: Manual Test Case Suite

Independent manual QA testing project covering the core user flows of the Blinkit quick-commerce Android app, with a focus on search, cart, and checkout.

> This is an independent practice project and is not affiliated with Blinkit.

## Objective
To design and execute a structured manual test suite covering functional, UI, negative, and boundary scenarios for a real-world quick-commerce application, and to document findings using standard QA artifacts (test cases, priority classification, and defect reports).

## Test Environment

| Item | Details |
|---|---|
| Application | Blinkit (Android) |
| App Version | 1.0.15 |
| Device | Vivo Y20 (V2029) |
| Operating System | Android 12 |
| Test Date | 29 October 2026 |
| Test Type | Manual, black-box |
| Defect Tracking | JIRA |

## Test Cases

| Test Case ID | Module | Test Scenario | Test Steps | Expected Result | Actual Result | Status | Priority |
|---|---|---|---|---|---|---|---|
| TC_01 | Search | Verify product search using headphones | 1. Open the Blinkit app.<br>2. Enter "headphones" in the search bar.<br>3. Tap Search. | Relevant headphone products should be displayed. | Relevant products were displayed in the search results. | Pass | High |
| TC_02 | Cart | Verify adding an out-of-stock product | 1. Open the Blinkit app.<br>2. Search for an out-of-stock product.<br>3. Attempt to add it to the cart. | The application should prevent the unavailable product from being added to the cart. | The application allowed the out-of-stock item to be added to the cart. | Fail | High |
| TC_03 | Quantity | Verify quantity limit validation | 1. Search for an available product.<br>2. Add it to the cart.<br>3. Increase the quantity beyond available stock. | The application should prevent quantities above available stock and display an appropriate message. | A message was displayed when the requested quantity exceeded the available stock. | Pass | High |
| TC_04 | Place Order | Verify order behavior during a network error | 1. Add a product to the cart.<br>2. Proceed to checkout.<br>3. Simulate a network interruption where safely possible.<br>4. Attempt to place the order. | The application should handle the network error and communicate the order status correctly. | The order was not placed during the network interruption, but the application did not display any message informing the user of the failure. | Fail | Medium |
| TC_05 | Payment | Verify payment screen loading time | 1. Open the Blinkit app.<br>2. Add a product to the cart.<br>3. Proceed to checkout.<br>4. Measure the time required for the payment screen to open. | The payment screen should open within the defined performance requirement. | The payment screen opened within the expected time. | Pass | High |
| TC_06 | Login | Verify login with a valid mobile number and OTP | 1. Open the login screen.<br>2. Enter a valid mobile number.<br>3. Request an OTP.<br>4. Enter the received OTP.<br>5. Submit the login form. | The user should be authenticated and redirected to the home screen. | The user was authenticated and redirected to the home screen. | Pass | High |
| TC_07 | Login | Verify login with an invalid OTP | 1. Open the login screen.<br>2. Enter a valid mobile number.<br>3. Request an OTP.<br>4. Enter an incorrect OTP.<br>5. Submit the form. | The application should reject the invalid OTP and display an appropriate error message. | An error message was displayed, and login was not completed. | Pass | High |
| TC_08 | Login | Verify mobile number validation | 1. Open the login screen.<br>2. Enter a mobile number containing fewer than 10 digits.<br>3. Tap Continue. | The application should validate the mobile number and prevent submission. | The application displayed a validation message and prevented submission. | Pass | Medium |
| TC_09 | Location | Verify current location using GPS | 1. Open the Blinkit app.<br>2. Grant location permission if requested.<br>3. Select the current-location option.<br>4. Check the displayed delivery area. | The application should identify the current location and display the corresponding delivery area. | The application detected the current location and displayed the corresponding area. | Pass | High |
| TC_10 | Location | Verify an unserviceable delivery location | 1. Open the location selection screen.<br>2. Enter an address outside the supported delivery area.<br>3. Confirm the location. | The application should notify the user if delivery is unavailable at that address. | The application displayed a message indicating that delivery was unavailable for the selected location. | Pass | Medium |
| TC_11 | Search | Verify search for a nonexistent product | 1. Open the Blinkit app.<br>2. Tap the search bar.<br>3. Enter xyzabc123.<br>4. Submit the search. | The application should display a suitable no-results message. | No matching products were displayed. | Pass | Medium |
| TC_12 | Search | Verify search using special characters | 1. Open the Blinkit app.<br>2. Enter a query containing special characters.<br>3. Submit the search.<br>4. Observe the application response. | The application should handle the query without crashing or displaying a technical error. | The application remained responsive and displayed an appropriate search response. | Pass | Low |
| TC_13 | Product Details | Verify product details | 1. Search for an available product.<br>2. Open the product details screen.<br>3. Check the product name, image, price, and availability. | Product information should be displayed clearly and consistently. | The product details were displayed on the product screen. | Pass | Medium |
| TC_14 | Cart | Verify adding an available product to the cart | 1. Search for an in-stock product.<br>2. Tap Add to Cart.<br>3. Open the cart.<br>4. Verify the selected product. | The product should be added to the cart, and the cart count should update correctly. | The product was added to the cart, and the cart count increased. | Pass | High |
| TC_15 | Cart | Verify removing a product from the cart | 1. Add a product to the cart.<br>2. Open the cart.<br>3. Remove the selected product.<br>4. Check the cart contents and total. | The product should be removed, and the cart total should be recalculated. | The product was removed, and the cart total was updated. | Pass | High |
| TC_16 | Cart | Verify cart total for three products | 1. Add three products to the cart.<br>2. Record their prices and quantities.<br>3. Calculate the expected subtotal.<br>4. Compare it with the displayed subtotal. | The subtotal should equal the sum of product prices multiplied by their quantities. Applicable charges should be calculated separately. | The displayed subtotal matched the calculated product total. | Pass | High |
| TC_17 | Cart | Verify cart persistence after reopening the app | 1. Add a product to the cart.<br>2. Close the application.<br>3. Reopen the application.<br>4. Navigate to the cart. | The cart should behave according to the application's documented persistence rules. | The cart contents remained available after reopening the application. | Pass | Medium |
| TC_18 | Coupon | Verify applying a valid coupon | 1. Add eligible products to the cart.<br>2. Open the coupon section.<br>3. Enter a valid coupon code.<br>4. Tap Apply.<br>5. Verify the discount. | The application should accept the coupon and apply the eligible discount. | The coupon was accepted, and the applicable discount was displayed. | Pass | Medium |
| TC_19 | Coupon | Verify applying an invalid or expired coupon | 1. Add a product to the cart.<br>2. Open the coupon section.<br>3. Enter an invalid or expired coupon code.<br>4. Tap Apply. | The application should reject the coupon and display an appropriate message. | The coupon was rejected, and an error message was displayed. | Pass | Medium |
| TC_20 | Bill Details | Verify delivery fees and final bill | 1. Add products to the cart.<br>2. Proceed to checkout.<br>3. Review the subtotal and applicable charges.<br>4. Verify the final payable amount. | The bill should display applicable charges and the correct final payable amount. | The bill displayed the subtotal, applicable charges, and final payable amount. | Pass | High |
| TC_21 | Checkout | Verify changing the delivery address during checkout | 1. Add a product to the cart.<br>2. Proceed to checkout.<br>3. Open the delivery address section.<br>4. Select another eligible saved address.<br>5. Review the checkout details. | The selected address should be updated, and applicable delivery information should be recalculated. | The selected delivery address was updated on the checkout screen. | Pass | High |
| TC_22 | Payment | Verify payment using UPI | 1. Add a product to the cart.<br>2. Proceed to checkout.<br>3. Select UPI as the payment method.<br>4. Complete an authorized transaction.<br>5. Verify the payment and order status. | The application should display the correct payment outcome and order status. | The payment was successful, and order confirmation was displayed. | Pass | High |
| TC_23 | Payment | Verify cancelled or failed payment | 1. Proceed to checkout.<br>2. Select a payment method.<br>3. Cancel the payment or simulate failure using an approved method.<br>4. Return to the application.<br>5. Check the payment and order status. | The application should handle payment cancellation or failure and display the correct status without incorrectly confirming the order. | The application displayed a payment failure or cancellation message and did not incorrectly confirm the order. | Pass | High |
| TC_24 | Order Tracking | Verify order tracking | 1. Place a test order.<br>2. Open the orders section.<br>3. Select the relevant order.<br>4. Open the tracking screen.<br>5. Check the displayed status. | The application should display the order status and relevant tracking information. | The order status and tracking information were displayed. | Pass | High |
| TC_25 | Cancellation | Verify order cancellation before dispatch | 1. Place a test order.<br>2. Open the order details.<br>3. Check whether cancellation is available.<br>4. Cancel the order if permitted.<br>5. Verify the updated order status. | If cancellation is allowed at that stage, the application should confirm cancellation and update the order status. | The application confirmed cancellation and updated the order status. | Pass | Medium |

## Defects Logged

| Bug ID | Title | Related TC | Severity | Priority | Status | JIRA Link | Screenshot |
|---|---|---|---|---|---|---|---|
| BUG_01 | Out-of-stock product can still be added to the cart | TC_02 | Major | High | Open | | |
| BUG_02 | No error message shown when order placement fails due to network interruption | TC_04 | Minor | Medium | Open | | |

## Test Execution Summary

| Metric | Count |
|---|---|
| Total Test Cases | 25 |
| Passed | 23 |
| Failed | 2 |
| Blocked | 0 |
| Pass Percentage | 92% |

## Author
**Gugulothu Rambabu**
Manual QA Tester (Fresher) | [LinkedIn](https://linkedin.com/in/rambabu-naik-372027387)
