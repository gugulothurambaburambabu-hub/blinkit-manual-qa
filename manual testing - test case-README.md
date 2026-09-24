# README — Manual QA Testing

Independent manual testing project on the Blinkit grocery delivery app, covering core user flows: search, cart, checkout, payment, and order tracking.

## Approach
- Designed test cases covering happy paths, edge cases, and error states
- Executed each case manually on the live app
- Logged expected vs actual results and flagged mismatches as bugs

## Results
See [TEST_CASES.md](./TEST_CASES.md) for the full test case log, or [Blinkit_Manual_Test_Cases.xlsx](./Blinkit_Manual_Test_Cases.xlsx) for the spreadsheet version.

## Key bugs found
- Out-of-stock items can still be added to cart
- Order placement fails silently under poor network conditions

## Tech/Tools
Manual black-box testing, Excel/Markdown for documentation.
