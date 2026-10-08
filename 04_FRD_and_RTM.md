# Functional Requirements and Traceability

## Functional requirements

Priority uses a draft MoSCoW recommendation: **Must**, **Should**, **Could**, or **Open**. The product owner must validate it.

| ID | Requirement | Priority | Acceptance summary |
|---|---|---|---|
| FR-01 | The service shall authenticate an employee and check eligibility before displaying employee-specific ordering functions. | Must | Active eligible employee can sign in; invalid or inactive identity receives a clear access message. |
| FR-02 | The service shall display the current daily menu with item name, description, price, category, and availability status. | Must | Employee sees only the published menu for the selected canteen/date. |
| FR-03 | The service shall allow an employee to add, remove, and adjust items in a draft cart. | Must | Cart quantities and total update accurately before confirmation. |
| FR-04 | The service shall prevent order confirmation after the approved daily cutoff. | Must | At or after cutoff, the service blocks new confirmation and explains the reason. Exact boundary time is an open decision. |
| FR-05 | The service shall show an order summary and obtain confirmation before submitting the order. | Must | Employee reviews items, quantity, amount, and payment method before confirmation. |
| FR-06 | The service shall prevent changes to a confirmed order unless an approved exception process permits them. | Must | Confirmed order is locked; authorized exception and audit history are recorded if policy allows changes. |
| FR-07 | The service shall provide canteen management with confirmed orders and totals grouped by menu item and fulfilment location. | Must | Manager can view and export or print the preparation list before kitchen handoff. |
| FR-08 | The service shall let authorized staff publish and update a daily menu and prices. | Must | Only authorized menu staff can publish; changes after orders exist are controlled and logged. |
| FR-09 | The service shall allow the manager to assign preparation and delivery work to operational staff. | Should | Assigned work displays relevant order and workstation details to permitted users. |
| FR-10 | The service shall record order status from confirmed through prepared and delivered. | Must | Status changes are timestamped and visible to permitted roles. |
| FR-11 | The service shall allow an employee to submit feedback for a completed order. | Should | Feedback is linked to the order without exposing it to unauthorized users. |
| FR-12 | The service shall generate reports on order volume, item demand, sales, system usage, and feedback. | Should | Report totals reconcile to order records for the selected period. |
| FR-13 | If payroll deduction is approved, the service shall send eligible monthly order totals to payroll and record accepted or rejected results. | Open | Reconciliation report identifies employee, period, amount, status, and exception reason. |
| FR-14 | The service shall record audit events for menu publication, order confirmation, status changes, and payroll export. | Should | Authorized reviewers can identify actor, event, and timestamp. |
| FR-15 | The service shall support the approved workplace access devices and accessibility requirements. | Open | Device/browser and accessibility acceptance criteria are approved before release. |

## Non-functional requirements

| ID | Quality area | Draft requirement | Measure to confirm |
|---|---|---|---|
| NFR-01 | Capacity | Support the expected employee population and peak ordering load. | Clarify whether 1,500 means registered employees, daily users, or concurrent sessions; then set load-test targets. |
| NFR-02 | Performance | Menu, cart, and order actions should complete within an agreed response time under expected load. | Product/IT to set percentile and threshold. |
| NFR-03 | Availability | Service should be available during menu viewing and ordering windows. | Agree uptime target and maintenance window. |
| NFR-04 | Security | Apply role-based access, secure authentication, least privilege, and audit logging. | Security review and access test. |
| NFR-05 | Privacy | Limit employee and payroll data to approved purposes and authorized roles. | Data inventory, retention period, and privacy review. |
| NFR-06 | Usability | Employees and operational staff can complete their key tasks using clear, consistent screens. | Usability test with representative users. |
| NFR-07 | Accessibility | Meet the organization's approved accessibility standard. | Standard and test method to be agreed. |
| NFR-08 | Maintainability | Use an architecture and technology stack supported by the organization's IT team. | Technology decision record. A specific Java constraint from a source version is unvalidated. |
| NFR-09 | Integration | Payroll and identity integrations handle failures, retries, duplicates, and reconciliation safely. | Interface contract and end-to-end test. |

## Business rules

| ID | Rule | Status |
|---|---|---|
| RULE-01 | Only active, eligible employees may place an order. | Draft; confirm source of employee status. |
| RULE-02 | An employee may order only from the menu published for the applicable service date and canteen. | Draft; confirm multi-canteen behavior. |
| RULE-03 | Order confirmation closes at the approved cutoff. The source commonly states 11:00 a.m. | Open: exact time zone, inclusive/exclusive boundary, and exception policy. |
| RULE-04 | Employees may edit a draft cart before confirmation. | Supported in source versions. |
| RULE-05 | A confirmed order cannot be edited or cancelled by the employee unless a business-approved exception is defined. | Draft; refund/cancellation handling is not consistent across sources. |
| RULE-06 | Payroll deduction applies only to employees enrolled in the approved deduction scheme, if this payment route is retained. | Open; consent, opt-out, and non-enrolled behavior need policy approval. |
| RULE-07 | Delivery is limited to approved employee workstations in the MVP. | Draft; source versions differ on what delivery locations are in scope. |
| RULE-08 | Only authorized canteen roles may create or publish menu changes. | Proposed control; validate role design. |

## Requirements traceability matrix

| Business need | BRD | Functional requirement | Story | UAT |
|---|---|---|---|---|
| Eligible employees can order a daily meal | BR-01 | FR-01, FR-02, FR-03, FR-05 | US-01, US-02, US-03 | UAT-01 to UAT-04 |
| Ordering closes before kitchen preparation | BR-01, BR-02 | FR-04, FR-07 | US-04, US-06 | UAT-05, UAT-07 |
| Canteen receives a reliable preparation view | BR-02 | FR-07, FR-08 | US-06, US-07 | UAT-07, UAT-08 |
| Meals reach the correct workstation | BR-03, BR-04 | FR-09, FR-10 | US-08 | UAT-09, UAT-10 |
| Employees can report order experience | BR-05 | FR-11 | US-09 | UAT-11 |
| Management can evaluate service performance | BR-05 | FR-12, FR-14 | US-10 | UAT-12, UAT-13 |
| Payroll deduction is accurate, if approved | BR-06 | FR-13, FR-14 | US-11 | UAT-14, UAT-15 |
| Service works for approved devices and access needs | BR-06 | FR-15, NFR-04 to NFR-08 | US-12 | UAT-16 |

## Requirement change control

Every proposed change should include the reason, affected stakeholder, priority, source or decision, impact on scope/process/data/integration/tests, approver, and updated trace links. Keep unresolved scope items in [Source Notes](10_Source_Notes.md) until a decision owner confirms them.

