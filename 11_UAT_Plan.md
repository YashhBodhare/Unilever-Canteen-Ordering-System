# User Acceptance Testing Plan

## Purpose

Validate that the proposed canteen ordering service supports approved business processes and rules before a pilot or release. This is a test plan; no execution results or business sign-off were supplied.

## Roles

| Role | Responsibility |
|---|---|
| UAT lead / business representative | Coordinate test sessions, capture outcomes, manage defects |
| Employee testers | Validate sign-in, menu, cart, confirmation, status, and feedback |
| Canteen manager and kitchen representative | Validate menu administration and preparation summary |
| Delivery representative | Validate assignment and delivery status |
| HR/payroll representative | Validate eligibility, export, and reconciliation if payroll is in scope |
| IT / support | Prepare test environment, access, test data, and technical support |
| Product owner | Accept business readiness and approve release recommendation |

## Entry criteria

- Approved BRD scope and operating rules.
- Stable test environment and role-based test accounts.
- Representative menu, employee, order, and workstation test data.
- Payroll test interface and consent rules approved if in scope.
- Critical end-to-end requirements have passed system testing.
- UAT participants receive scenario instructions and defect logging guidance.

## Exit criteria

- All Must-priority UAT scenarios pass or have an approved workaround.
- No open severity-1 defect; severity-2 defects have an agreed disposition.
- Payroll totals reconcile for the approved test period if the integration is in scope.
- Canteen and delivery representatives confirm the operating handoffs.
- Product owner records acceptance, conditional acceptance, or rejection.

## UAT scenarios

| Test ID | Requirement | Scenario | Expected result |
|---|---|---|---|
| UAT-01 | FR-01 | Active employee signs in | Employee reaches the menu; access event is recorded. |
| UAT-02 | FR-01 | Inactive or ineligible user signs in | Ordering access is blocked with a clear message. |
| UAT-03 | FR-02 | Employee views a published menu | Correct date, canteen, item, description, price, and availability appear. |
| UAT-04 | FR-03, FR-05 | Employee changes cart and confirms before cutoff | Updated quantities and total are correct; one order reference is created. |
| UAT-05 | FR-04 | Employee attempts confirmation after cutoff | Service blocks order confirmation and explains the window is closed. |
| UAT-06 | FR-06 | Employee tries to edit confirmed order | Service prevents the change or follows an approved exception path with audit history. |
| UAT-07 | FR-07 | Manager views kitchen summary after cutoff | Summary totals match confirmed order lines and selected service location. |
| UAT-08 | FR-08 | Authorized manager publishes a menu | Menu appears to employees; actor and time are recorded. |
| UAT-09 | FR-09, FR-10 | Manager assigns delivery and associate updates status | Correct assignment and status history appear to permitted roles. |
| UAT-10 | FR-10 | Delivery associate records successful handoff | Order status changes to delivered with timestamp. |
| UAT-11 | FR-11 | Employee submits feedback for a delivered order | Feedback is stored against the correct order and access remains restricted. |
| UAT-12 | FR-12 | Manager runs a sales and demand report | Report matches source order data for the selected period. |
| UAT-13 | FR-14 | Reviewer checks audit history | Menu, order, and status events show actor and timestamp. |
| UAT-14 | FR-13 | Approved payroll file is accepted | Deduction totals match eligible confirmed orders and reconciliation completes. |
| UAT-15 | FR-13 | Payroll rejects an invalid employee or amount | Rejection is visible with reason and can be corrected without duplicate deduction. |
| UAT-16 | FR-15, NFR-04 to NFR-08 | User completes ordering on approved devices with access controls | Supported device flow works; unauthorized data remains unavailable. |

## Defect log fields

Test ID, date, tester, environment, role, actual result, expected result, severity, evidence, owner, status, retest result, and business disposition.

