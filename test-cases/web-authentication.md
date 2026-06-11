# Web Authentication Test Cases

## TC-AUTH-001 - Successful Login With Valid Credentials

| Field | Value |
| --- | --- |
| Priority | High |
| Type | Smoke, Functional |
| Preconditions | User account exists and is active |
| Test data | Email: `user@example.com`, password: valid password |
| Status | Not run |

| Step | Action | Expected result |
| --- | --- | --- |
| 1 | Open the login page | Login form is displayed |
| 2 | Enter a valid email | Email field accepts the value |
| 3 | Enter a valid password | Password is masked |
| 4 | Click `Login` | User is redirected to the account dashboard |
| 5 | Check user menu | User name or email is displayed |

## TC-AUTH-002 - Login With Incorrect Password

| Field | Value |
| --- | --- |
| Priority | High |
| Type | Negative, Functional |
| Preconditions | User account exists |
| Test data | Email: `user@example.com`, password: `wrongPassword123` |
| Status | Not run |

| Step | Action | Expected result |
| --- | --- | --- |
| 1 | Open the login page | Login form is displayed |
| 2 | Enter a valid email | Email field accepts the value |
| 3 | Enter an incorrect password | Password is masked |
| 4 | Click `Login` | Error message is displayed |
| 5 | Check current page | User stays on the login page |

## TC-AUTH-003 - Email Validation On Login Form

| Field | Value |
| --- | --- |
| Priority | Medium |
| Type | Validation, Negative |
| Preconditions | Login page is available |
| Test data | `userexample.com`, `user@`, `@example.com` |
| Status | Not run |

| Step | Action | Expected result |
| --- | --- | --- |
| 1 | Open the login page | Login form is displayed |
| 2 | Enter invalid email format | Field shows validation state |
| 3 | Enter any password | Password field accepts the value |
| 4 | Click `Login` | Request is not sent, validation message is displayed |

## TC-AUTH-004 - Password Recovery Request

| Field | Value |
| --- | --- |
| Priority | Medium |
| Type | Functional |
| Preconditions | User account exists |
| Test data | Email: `user@example.com` |
| Status | Not run |

| Step | Action | Expected result |
| --- | --- | --- |
| 1 | Open the login page | Login form is displayed |
| 2 | Click `Forgot password?` | Password recovery page is opened |
| 3 | Enter registered email | Email field accepts the value |
| 4 | Click `Send recovery link` | Success message is displayed |
| 5 | Check mailbox | Recovery email is received |

## TC-AUTH-005 - Logout From Account

| Field | Value |
| --- | --- |
| Priority | High |
| Type | Smoke, Regression |
| Preconditions | User is logged in |
| Test data | Active user session |
| Status | Not run |

| Step | Action | Expected result |
| --- | --- | --- |
| 1 | Open user menu | Menu is displayed |
| 2 | Click `Logout` | Session is closed |
| 3 | Open account dashboard URL directly | User is redirected to login page |
