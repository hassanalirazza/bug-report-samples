# BUG-003 — Search crashes when special characters are entered

| Field | Detail |
|---|---|
| **Bug ID** | BUG-003 |
| **Reported by** | Hassan Ali Raza |
| **Date** | 2026-01-16 |
| **Environment** | Android 14, ShopEase mobile app v3.1.0 |
| **Module** | Product Search |
| **Severity** | Critical |
| **Priority** | High |
| **Status** | Open |

---

## Preconditions
- User has the ShopEase mobile app installed and open
- User is on the product search screen

## Steps to Reproduce
1. Tap the search bar
2. Enter the following string: `%%%<>{}`
3. Tap **Search**

## Expected Result
The app handles the input gracefully — either returning "No results found" or ignoring invalid characters. The app remains stable.

## Actual Result
The app freezes for ~3 seconds and then crashes back to the device home screen. Reopening the app is required to continue.

## Evidence
*Screen recording of the crash and the crash log (stack trace) would be attached here.*

## Additional Notes
Reproducible 5/5 times on Android. Suspected unhandled exception when parsing special characters in the search query. Input sanitization appears to be missing on the search field.
