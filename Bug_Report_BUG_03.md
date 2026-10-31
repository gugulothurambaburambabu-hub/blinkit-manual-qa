# Bug Report: BUG_03

| Field | Details |
|---|---|
| Bug ID | BUG_03 |
| Title | Payment screen shows a higher amount (Rs. 205) than the checkout payable amount (Rs. 200) |
| Related Test Case | TC_22 |
| Module | Payment |
| Application | Blinkit (Android), version 1.0.15 |
| Device / OS | Vivo Y20 (V2029), Android 12 |
| Severity | Major |
| Priority | High |
| Status | Open |
| Reported By | Gugulothu Rambabu |
| Date Reported | 29 October 2026 |

## Steps to Reproduce
1. Open the Blinkit app and add a product to the cart.
2. Proceed to checkout and note the final payable amount.
3. Select UPI as the payment method.
4. Compare the amount on the payment screen with the checkout amount.

## Expected Result
The amount on the payment screen should match the final payable amount shown at checkout.

## Actual Result
The checkout screen showed Rs. 200, but the payment screen showed Rs. 205. The extra Rs. 5 was not explained on the checkout screen.

## Impact
The user may be charged more than the amount they agreed to at checkout, which affects trust and could lead to complaints or abandoned orders.

## Attachments
Screenshot of the checkout screen: add file name here
Screenshot of the payment screen: add file name here

Back to the [test case suite](README.md).
