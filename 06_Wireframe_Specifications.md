# Wireframe Specifications

These screen specifications translate requirements into low-fidelity design guidance. They are not production UI designs. A designer should validate layout, accessibility, and content with users.

## Employee journey screens

| Screen | Main content | Actions | Validation and error states |
|---|---|---|---|
| Sign in | Work identity sign-in, help link, eligibility message | Sign in, get help | Invalid credentials, inactive employee, identity service unavailable |
| Daily menu | Service date/canteen, menu categories, item name, description, price, availability | Add item, view details, search/filter if approved | No published menu, item unavailable, price missing |
| Cart | Selected items, quantities, item totals, order total, cutoff reminder | Change quantity, remove item, continue browsing, proceed | Empty cart, item became unavailable, total recalculated |
| Review and confirm | Final order summary, payment/deduction method, delivery location, terms | Confirm order, return to cart | Cutoff passed, employee not enrolled in required payment option, invalid location |
| Order status | Order reference, confirmed/preparing/ready/delivered status, delivery location | View details, contact support | Status delayed, order not found, service unavailable |
| Feedback | Order reference, satisfaction rating, optional comment | Submit feedback | Duplicate feedback policy, inappropriate or empty input handling |

## Operations screens

| Screen | Main content | Actions | Validation and error states |
|---|---|---|---|
| Menu management | Date, canteen, categories, item, description, price, availability | Save draft, publish, edit | Missing price, invalid date, unauthorized user, menu already locked |
| Preparation dashboard | Confirmed orders, counts by item, special notes, service location | Export/print summary, assign preparation | Late changes, duplicate order, quantity mismatch |
| Delivery queue | Assigned orders, employee, workstation, route grouping, order status | Accept assignment, mark picked up/delivered, raise exception | Wrong location, delivery failed, order not present |
| Manager reports | Orders, demand by item, sales totals, feedback, waste measure if captured | Filter period/canteen, export | Incomplete data, payroll reconciliation outstanding |
| Payroll reconciliation | Employee reference, period, order total, export status, rejection reason | Review, export, reconcile exceptions | Duplicate export, rejected employee, invalid total |

## Navigation flow

~~~mermaid
flowchart LR
    A[Sign in] --> B[Daily menu]
    B --> C[Cart]
    C --> B
    C --> D[Review order]
    D -->|Edit| C
    D -->|Confirm before cutoff| E[Order status]
    D -->|Cutoff passed| B
    E --> F[Feedback]
~~~

## Design decisions to validate

- Browser access versus native mobile application.
- Whether menu selection is filtered by canteen, floor, or delivery zone.
- Whether dietary and allergen information is included in the first release.
- How payroll enrollment and consent appear in the employee journey.
- How a delivery associate confirms a handoff without exposing unnecessary employee data.
- How cancellation, item substitution, and failed delivery are handled.

