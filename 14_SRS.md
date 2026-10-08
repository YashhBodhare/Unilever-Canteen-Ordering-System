# Software Requirements Specification

## 1. Introduction

This SRS describes the proposed software behavior and quality needs for an employee canteen ordering service. It is a portfolio-level draft and does not prescribe a technology stack. The Java implementation mentioned in one source version requires validation by the organization’s IT team.

## 2. System context

The service connects employees, canteen management, kitchen staff, delivery associates, and potentially HR/payroll. It receives employee identity and eligibility information, presents a published menu, records confirmed orders, supports preparation and delivery, and provides operational reports.

## 3. User classes

| User class | Main permissions |
|---|---|
| Employee | View menu, manage draft cart, confirm order, view own order status, submit feedback |
| Menu manager | Create, update, and publish menu items and prices |
| Canteen manager | View confirmed demand, coordinate preparation, assign delivery, review reports |
| Kitchen staff | View permitted preparation information and update preparation status if included |
| Delivery associate | View assigned delivery details and update delivery status |
| HR/payroll user | Review eligible payroll exports and reconciliation exceptions if integration is approved |
| IT/support administrator | Manage access, monitoring, and support without unnecessary access to order details |
| Management user | View aggregate business reports |

## 4. Functional requirements

The detailed requirements are maintained in [FRD and RTM](04_FRD_and_RTM.md). The core system shall:

1. Authenticate users and enforce permissions by role.
2. Display a menu for the selected service date and canteen.
3. Allow an eligible employee to maintain a draft cart and confirm before cutoff.
4. prevent late confirmations and display the policy-defined reason.
5. Store an immutable confirmed order snapshot for preparation and audit.
6. Provide menu administration and a consolidated preparation view.
7. Support assignment and status tracking through delivery.
8. Accept feedback for a completed order.
9. Generate operational reports from authoritative order data.
10. Exchange monthly totals with payroll only after integration and consent rules are approved.

## 5. External interface requirements

| Interface | Information exchanged | Status / design need |
|---|---|---|
| Employee identity source | Employee identifier and active/eligible status | Source system and authentication method to be selected by IT. |
| Payroll system | Employee reference, period, amount, export status, rejection code | Conditional scope. Define secure transport, file/API format, deduplication, retries, and reconciliation. |
| Menu operations interface | Menu item, description, price, category, availability, service date/canteen | Role-based access and audit history required. |
| Employee browser/device | Menu, cart, confirmation, order status, feedback | Supported browsers, mobile/tablet scope, and accessibility standard need approval. |
| Reporting/export | Aggregate orders, sales, item demand, feedback, and approved waste measures | Define authorized recipients and data minimization. |

## 6. Data requirements

Core entities include Employee reference, Menu, Menu Item, Order, Order Line, Order Status Event, Delivery Assignment, Feedback, and conditional Payroll Export/Payroll Line. Store only required personal data. Retention, deletion, and audit periods require privacy and records-policy approval.

## 7. Quality requirements

- Capacity: validate expected registered users, peak concurrent sessions, and order burst before setting load targets.
- Performance: establish measurable response-time thresholds for menu, cart, and confirmation.
- Availability: define coverage during menu and ordering windows.
- Security: enforce authentication, least privilege, role-based access, secure integration, and audit logging.
- Privacy: limit personal and payroll data to approved purposes and roles.
- Usability and accessibility: test with representative employees and operations users against an approved standard.
- Reliability: prevent duplicate order confirmation and duplicate payroll deductions.
- Maintainability: choose supported technology with IT; do not treat the legacy Java suggestion as approved without review.

## 8. Business rules and constraints

See [FRD and RTM](04_FRD_and_RTM.md#business-rules). The cutoff boundary, cancellation policy, payroll eligibility, mobile support, and delivery window remain open decisions.

## 9. Verification approach

Map each requirement to system, integration, security, usability, performance, and UAT coverage as appropriate. The business acceptance scenarios are listed in [UAT Plan](11_UAT_Plan.md). Technical thresholds must be agreed before the team can declare non-functional requirements testable.

