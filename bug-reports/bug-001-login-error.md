# BUG-001 — Login fails with valid credentials on Safari

| Field | Detail |
|---|---|
| **Bug ID** | BUG-001 |
| **Reported by** | Hassan Ali Raza |
| **Date** | 2026-01-12 |
| **Environment** | macOS Sonoma, Safari 17.2, ShopEase build v2.4.0 |
| **Module** | Authentication / Login |
| **Severity** | High |
| **Priority** | High |
| **Status** | Open |

---

## Preconditions
- User has a registered, active account
- User is on the ShopEase login page in Safari

## Steps to Reproduce
1. Open the login page in Safari
2. Enter a valid email: `user@shopease.com`
3. Enter the correct password: `Valid@123`
4. Click the **Login** button

## Expected Result
User is authenticated and redirected to the dashboard.

## Actual Result
The page reloads and the login form is cleared. The user remains on the login page with no error message. The same credentials log in successfully on Chrome and Firefox.

## Evidence
*Screenshot of the cleared login form after submission would be attached here. Browser console shows a CORS-related warning on the auth request (log reference attached).*

## Additional Notes
Issue is reproducible only on Safari. Suspected browser-specific handling of the authentication request.
