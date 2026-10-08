# Business Requirements Document

## Document purpose

This BRD defines the business need, intended outcomes, scope, and high-level requirements for a proposed employee canteen ordering service. It is a portfolio analysis draft derived from the supplied training scenario.

## Business need

Employees experience a crowded lunch service and spend time waiting for food and seating. Canteen staff have limited advance visibility of demand, which can contribute to unavailable meal choices and unsold food. The business is considering an online ordering service that gives employees a menu and order channel before lunch and gives canteen staff a consolidated view of demand.

## Business objectives

| ID | Objective | Draft measure | Target stated in scenario | Owner to confirm |
|---|---|---|---|---|
| BO-01 | Reduce food waste | Discarded food quantity or value divided by a defined prepared-food baseline | At least 30% reduction within 6 months | Canteen manager / sponsor |
| BO-02 | Reduce canteen operating cost | Agreed operating cost categories compared over equivalent periods | 15% reduction within 12 months | Finance / sponsor |
| BO-03 | Increase effective work time | Change in lunch-related time away from work per participating employee | 30 additional minutes per employee per day within 3 months | Sponsor / HR |
| BO-04 | Improve meal access and satisfaction | Order completion, item availability, and post-order satisfaction | Target not supplied | Product / canteen manager |
| BO-05 | Improve operational planning | Daily demand available to the kitchen before preparation | Target not supplied | Canteen manager |

All targets are draft scenario targets, not achieved outcomes. BO-01 requires reconciliation with the alternative target phrasing in the source files.

## Scope

### In scope for the working MVP

- Employee access and eligibility checks.
- Daily menu and price display.
- Create, review, and confirm a lunch order before the approved cutoff.
- Canteen menu administration and order summaries.
- Kitchen preparation handoff.
- Delivery to employee workstations and completion status.
- Post-order feedback.
- Basic operational and management reporting.
- Payroll deduction only if the sponsor confirms it as a release requirement and HR/IT approves the design.

### Out of scope for the working MVP

- Breakfast service.
- Ordering by non-employees.
- Supplier procurement and vendor management.
- Canteen staff payroll administration.
- Refund processing and complex cancellation after confirmation.
- Third-party payment gateway unless payroll is rejected and an alternative is approved.
- SMS/email notifications, dietary recommendation, and delivery outside approved workstations.
- Full inventory management unless separately approved.

### Scope decisions still open

- Responsive mobile/tablet access.
- Whether two canteens share a menu and fulfilment model.
- Whether the employee may choose a delivery time or receives a standard lunch delivery window.
- Whether payroll deduction is mandatory, optional, or a later release.
- Whether inventory availability is shown to employees.

## Business requirements

| ID | Requirement | Rationale |
|---|---|---|
| BR-01 | The service shall let eligible employees order meals from a published daily menu before a business-approved cutoff. | Give the kitchen demand before preparation and reduce lunch congestion. |
| BR-02 | The service shall provide canteen management with a reliable consolidated view of confirmed demand. | Support quantity planning and preparation. |
| BR-03 | The service shall support delivery of confirmed meals to approved employee workstations. | Reduce the need for every employee to queue at the canteen. |
| BR-04 | The service shall record order status through preparation and delivery. | Give staff operational control and support issue resolution. |
| BR-05 | The service shall provide operational data to evaluate usage, menu demand, food waste, cost, and employee feedback. | Measure business outcomes and inform service decisions. |
| BR-06 | The solution shall protect employee and payroll-related information through approved access and data-handling controls. | Protect employee information and support trusted payroll processing. |

## Constraints and dependencies

- The service depends on accurate employee identity and active employment status.
- Payroll deduction depends on HR policy, employee consent/enrollment, and an approved payroll interface or controlled file exchange.
- Canteen staff need reliable devices and a defined process to publish menus and receive consolidated orders.
- Delivery requires current employee workstation or location information with appropriate access controls.
- The project needs an agreed operational baseline before benefit targets can be measured.

## Business risks

| Risk | Effect | Initial response |
|---|---|---|
| Payroll integration or deduction rules remain unclear | Incorrect deductions, delayed launch, or loss of employee trust | Confirm policy, consent, data contract, reconciliation, and exception ownership before build. |
| Cutoff is too early or too late for staff and kitchen | Low adoption or poor preparation readiness | Test cutoff with kitchen and employee schedules. |
| Delivery demand exceeds available capacity | Late or misplaced orders | Pilot route capacity and define assignment/priority rules. |
| Targets lack an agreed baseline | Benefits cannot be credibly measured | Define baseline period, formulas, and accountable metric owners. |
| Mobile access scope is unresolved | Some employees may not be able to use the service | Confirm workplace device access and accessibility needs in discovery. |

## Approval checklist

- Sponsor approves objectives and metric definitions.
- Canteen manager approves operating process and cutoff.
- HR/payroll approves eligibility, consent, deduction, and reconciliation rules.
- IT approves identity, privacy, access, and integration boundaries.
- Product owner approves MVP scope and prioritization.

