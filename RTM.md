# Requirements Traceability Matrix (RTM): Blinkit Android App

Blinkit's official requirements are not public, so the requirements below are self-defined from the app's visible features. Each one is mapped to the test cases that cover it and to any defects found.

| Req ID | Requirement | Test Case IDs | Defect IDs | Result |
|---|---|---|---|---|
| REQ_01 | User can search for products, including invalid and special-character searches | TC_01, TC_11, TC_12 | None | Pass |
| REQ_02 | Product details are displayed correctly | TC_13 | None | Pass |
| REQ_03 | User can add, remove and keep items in the cart; unavailable items cannot be added | TC_02, TC_14, TC_15, TC_17 | BUG_01 | Fail |
| REQ_04 | Quantity cannot exceed available stock | TC_03 | None | Pass |
| REQ_05 | Cart subtotal and final bill are calculated correctly | TC_16, TC_20 | None | Pass |
| REQ_06 | Valid coupons are applied and invalid coupons are rejected | TC_18, TC_19 | None | Pass |
| REQ_07 | User can log in with a mobile number and OTP, with input validation | TC_06, TC_07, TC_08 | None | Pass |
| REQ_08 | Location and delivery address are detected, validated and changeable | TC_09, TC_10, TC_21 | None | Pass |
| REQ_09 | Order placement handles network errors and informs the user | TC_04 | BUG_02 | Fail |
| REQ_10 | Payment screen shows the correct amount and handles failed or cancelled payments | TC_05, TC_22, TC_23 | BUG_03 | Fail |
| REQ_11 | User can track a placed order | TC_24 | None | Blocked |
| REQ_12 | User can cancel an order before dispatch | TC_25 | None | Blocked |

## Coverage Summary

| Metric | Count |
|---|---|
| Total requirements | 12 |
| Requirements with test coverage | 12 |
| Total test cases mapped | 25 |
| Requirements passed | 7 |
| Requirements failed | 3 |
| Requirements blocked | 2 |

Back to the [test case suite](README.md).
