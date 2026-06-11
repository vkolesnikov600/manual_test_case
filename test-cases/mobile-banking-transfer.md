# Mobile Banking Transfer Test Cases

## TC-MOB-BANK-001 - Transfer Between Own Accounts

| Field | Value |
| --- | --- |
| Priority | High |
| Type | Smoke, Functional |
| Preconditions | User is logged in, user has two active accounts |
| Test data | Amount: `1000`, currency: account currency |
| Status | Not run |

| Step | Action | Expected result |
| --- | --- | --- |
| 1 | Open `Transfers` section | Transfer options are displayed |
| 2 | Select `Between own accounts` | Transfer form is displayed |
| 3 | Select source and target accounts | Accounts are selected |
| 4 | Enter valid amount | Amount is accepted |
| 5 | Confirm transfer | Success screen is displayed |
| 6 | Check balances | Source and target balances are updated correctly |

## TC-MOB-BANK-002 - Transfer With Amount Greater Than Balance

| Field | Value |
| --- | --- |
| Priority | High |
| Type | Negative, Functional |
| Preconditions | User is logged in |
| Test data | Amount greater than available balance |
| Status | Not run |

| Step | Action | Expected result |
| --- | --- | --- |
| 1 | Open transfer form | Form is displayed |
| 2 | Select source account | Account is selected |
| 3 | Enter amount greater than balance | Amount is entered |
| 4 | Tap `Continue` | Transfer is blocked |
| 5 | Check message | Insufficient funds message is displayed |

## TC-MOB-BANK-003 - Transfer Confirmation By OTP

| Field | Value |
| --- | --- |
| Priority | High |
| Type | Security, Functional |
| Preconditions | User is logged in, OTP confirmation is enabled |
| Test data | Valid transfer data, valid OTP |
| Status | Not run |

| Step | Action | Expected result |
| --- | --- | --- |
| 1 | Fill transfer form with valid data | Continue button is enabled |
| 2 | Tap `Continue` | OTP screen is displayed |
| 3 | Enter valid OTP | OTP is accepted |
| 4 | Confirm operation | Transfer is completed |
| 5 | Check operation history | Transfer appears in transaction history |

## TC-MOB-BANK-004 - Invalid OTP During Transfer

| Field | Value |
| --- | --- |
| Priority | High |
| Type | Negative, Security |
| Preconditions | OTP confirmation screen is displayed |
| Test data | Invalid OTP: `000000` |
| Status | Not run |

| Step | Action | Expected result |
| --- | --- | --- |
| 1 | Enter invalid OTP | OTP field accepts digits |
| 2 | Tap `Confirm` | Transfer is not completed |
| 3 | Check error message | Invalid OTP message is displayed |
| 4 | Check retry option | User can request a new OTP or retry within allowed limit |

## TC-MOB-BANK-005 - Transfer Form After Network Loss

| Field | Value |
| --- | --- |
| Priority | Medium |
| Type | Mobile, Negative |
| Preconditions | User is on transfer confirmation screen |
| Test data | Disable internet connection |
| Status | Not run |

| Step | Action | Expected result |
| --- | --- | --- |
| 1 | Fill transfer form | Transfer data is entered |
| 2 | Disable internet connection | Device is offline |
| 3 | Tap `Confirm` | Operation is not completed |
| 4 | Check message | Clear network error is displayed |
| 5 | Restore internet connection | User can retry operation |
