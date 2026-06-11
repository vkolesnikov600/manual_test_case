# API Profile Test Cases

## TC-API-PROFILE-001 - Get Current User Profile

| Field | Value |
| --- | --- |
| Priority | High |
| Type | API, Smoke |
| Preconditions | User is authorized |
| Test data | Valid bearer token |
| Status | Not run |

| Step | Action | Expected result |
| --- | --- | --- |
| 1 | Send `GET /api/profile` with valid token | Response status is `200 OK` |
| 2 | Check response body | Body contains `id`, `email`, `name` |
| 3 | Validate field types | Field types match API documentation |
| 4 | Check response time | Response time is within accepted limit |

## TC-API-PROFILE-002 - Get Profile Without Token

| Field | Value |
| --- | --- |
| Priority | High |
| Type | API, Negative, Security |
| Preconditions | Endpoint is available |
| Test data | No authorization header |
| Status | Not run |

| Step | Action | Expected result |
| --- | --- | --- |
| 1 | Send `GET /api/profile` without token | Response status is `401 Unauthorized` |
| 2 | Check response body | Error code/message is returned |
| 3 | Check sensitive data | Profile data is not returned |

## TC-API-PROFILE-003 - Update Profile With Valid Data

| Field | Value |
| --- | --- |
| Priority | High |
| Type | API, Functional |
| Preconditions | User is authorized |
| Test data | Name: `Vladislav`, phone: valid phone number |
| Status | Not run |

| Step | Action | Expected result |
| --- | --- | --- |
| 1 | Send `PATCH /api/profile` with valid body | Response status is `200 OK` |
| 2 | Check response body | Updated fields are returned |
| 3 | Send `GET /api/profile` | Updated data is saved |

## TC-API-PROFILE-004 - Update Profile With Invalid Email Format

| Field | Value |
| --- | --- |
| Priority | Medium |
| Type | API, Negative, Validation |
| Preconditions | User is authorized |
| Test data | Email: `wrong-email-format` |
| Status | Not run |

| Step | Action | Expected result |
| --- | --- | --- |
| 1 | Send `PATCH /api/profile` with invalid email | Response status is `400 Bad Request` |
| 2 | Check validation message | Email validation error is returned |
| 3 | Send `GET /api/profile` | Previous email remains unchanged |
