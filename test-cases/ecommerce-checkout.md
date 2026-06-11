# E-commerce Checkout Test Cases

## TC-CHECKOUT-001 - Add Product To Cart

| Field | Value |
| --- | --- |
| Priority | High |
| Type | Smoke, Functional |
| Preconditions | Product is available and in stock |
| Test data | Product: wireless headphones |
| Status | Not run |

| Step | Action | Expected result |
| --- | --- | --- |
| 1 | Open product page | Product details are displayed |
| 2 | Click `Add to cart` | Product is added to cart |
| 3 | Open cart | Product is displayed in cart |
| 4 | Check quantity and price | Quantity is `1`, price matches product page |

## TC-CHECKOUT-002 - Change Product Quantity In Cart

| Field | Value |
| --- | --- |
| Priority | Medium |
| Type | Functional, Regression |
| Preconditions | Cart contains one product |
| Test data | Quantity: `2` |
| Status | Not run |

| Step | Action | Expected result |
| --- | --- | --- |
| 1 | Open cart | Cart page is displayed |
| 2 | Increase quantity to `2` | Quantity is updated |
| 3 | Check total price | Total price is recalculated correctly |
| 4 | Refresh page | Updated quantity is saved |

## TC-CHECKOUT-003 - Remove Product From Cart

| Field | Value |
| --- | --- |
| Priority | High |
| Type | Functional |
| Preconditions | Cart contains at least one product |
| Test data | Any product |
| Status | Not run |

| Step | Action | Expected result |
| --- | --- | --- |
| 1 | Open cart | Cart page is displayed |
| 2 | Click `Remove` for product | Product is removed |
| 3 | Check cart state | Empty cart message is displayed |
| 4 | Check cart counter | Counter is `0` |

## TC-CHECKOUT-004 - Checkout With Valid Delivery Address

| Field | Value |
| --- | --- |
| Priority | High |
| Type | Functional, End-to-end |
| Preconditions | User is logged in, cart contains product |
| Test data | Valid city, street, house, phone number |
| Status | Not run |

| Step | Action | Expected result |
| --- | --- | --- |
| 1 | Open checkout page | Checkout form is displayed |
| 2 | Fill delivery address | Fields accept values |
| 3 | Select delivery method | Delivery price is displayed |
| 4 | Select payment method | Payment method is selected |
| 5 | Click `Place order` | Order is created, confirmation page is displayed |

## TC-CHECKOUT-005 - Checkout With Empty Required Fields

| Field | Value |
| --- | --- |
| Priority | High |
| Type | Negative, Validation |
| Preconditions | Cart contains product |
| Test data | Empty required fields |
| Status | Not run |

| Step | Action | Expected result |
| --- | --- | --- |
| 1 | Open checkout page | Checkout form is displayed |
| 2 | Leave required fields empty | Fields remain empty |
| 3 | Click `Place order` | Order is not created |
| 4 | Check validation messages | Required fields are highlighted with clear messages |
