# Bug Report Examples

## BUG-001 - User Can Submit Checkout Form With Empty Phone Field

| Field | Value |
| --- | --- |
| Severity | Major |
| Priority | High |
| Environment | Web, Chrome, Windows 11 |
| Build | 1.0.0 |
| Status | Open |

## Preconditions

- User is logged in.
- Cart contains at least one product.
- Checkout page is opened.

## Steps To Reproduce

1. Open checkout page.
2. Fill all required fields except `Phone`.
3. Click `Place order`.

## Actual Result

Order is created successfully without phone number.

## Expected Result

Order is not created. Phone field is highlighted and validation message is displayed.

## Attachments

- Screenshot of checkout form.
- Network request payload.

---

## BUG-002 - Incorrect Error Message For Invalid OTP

| Field | Value |
| --- | --- |
| Severity | Minor |
| Priority | Medium |
| Environment | Android 14, Pixel 7 |
| Build | 2.4.1 |
| Status | Open |

## Preconditions

- User is logged in.
- User is on transfer confirmation screen.

## Steps To Reproduce

1. Enter invalid OTP `000000`.
2. Tap `Confirm`.

## Actual Result

Application shows `Something went wrong`.

## Expected Result

Application shows clear message: `Invalid confirmation code`.

## Attachments

- Screenshot of error message.
- Device logs.
