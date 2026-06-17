# BUG-002 — Cart total does not update when quantity is increased

| Field | Detail |
|---|---|
| **Bug ID** | BUG-002 |
| **Reported by** | Hassan Ali Raza |
| **Date** | 2026-01-14 |
| **Environment** | Windows 11, Chrome 121, ShopEase build v2.4.0 |
| **Module** | Cart / Checkout |
| **Severity** | High |
| **Priority** | High |
| **Status** | Open |

---

## Preconditions
- User is logged in
- One item ("Wireless Mouse", $25.00) is in the cart with quantity 1

## Steps to Reproduce
1. Open the cart
2. Change the item quantity from 1 to 3 using the quantity selector
3. Observe the line total and the order total

## Expected Result
- Line total updates to `$75.00` (3 × $25.00)
- Order total updates to `$75.00`

## Actual Result
- The quantity field shows `3`
- The line total and order total remain at `$25.00`
- The correct total only appears after manually refreshing the page

## Evidence
*Screenshot showing quantity = 3 with order total still $25.00 would be attached here.*

## Additional Notes
The total recalculates correctly on a full page reload, suggesting the front-end is not re-triggering the total calculation on quantity change. Backend order value is correct once submitted.
