# Product Requirements Document

## Product summary

The proposed canteen ordering service gives eligible employees a way to review the daily menu and confirm a lunch order before an approved cutoff. Canteen staff receive a consolidated preparation view and coordinate workstation delivery. The product also supports operational reporting and, if approved, payroll deduction.

## Product vision

Make office lunch easier to plan and access while giving canteen staff a more reliable view of meal demand.

## Users

- Employees who order lunch.
- Menu managers who publish daily choices and prices.
- Canteen managers who coordinate preparation and delivery.
- Kitchen staff who prepare meals from confirmed demand.
- Delivery associates who complete workstation handoffs.
- HR/payroll and IT teams who manage eligibility, integration, and support.
- Managers who review service reports.

## Product goals

1. Let eligible employees place a clear, accurate lunch order before the operational cutoff.
2. Give the kitchen an authoritative preparation summary.
3. Track fulfilment through delivery.
4. Capture data needed to evaluate queue time, food waste, cost, and satisfaction.
5. Protect employee information and any payroll data.

## MVP features

| Feature | User value | Release priority |
|---|---|---|
| Employee access | Prevent non-eligible users from ordering | Must |
| Daily menu | Let employees see current meals and prices | Must |
| Cart and confirmation | Reduce order errors and capture demand early | Must |
| Order cutoff | Give the kitchen time to prepare | Must |
| Preparation summary | Group confirmed orders for kitchen work | Must |
| Delivery assignment and status | Help fulfil workstation orders and record completion | Must |
| Menu management | Keep menu details current | Must |
| Feedback and basic reports | Review service issues and demand | Should |
| Payroll deduction | Support the proposed payment route | Open pending HR/payroll decision |

## Product non-goals for the working MVP

Full supplier procurement, kitchen staff payroll, breakfast, external-user ordering, advanced inventory, automated refund processing, SMS/email messaging, and dietary recommendation features are excluded unless later approved.

## Success measures

Use the training-case targets in [Project Baseline](00_Project_Baseline.md) as draft measures. The product team must define the baseline, calculation, reporting owner, observation period, and target approval before using them as committed goals.

## Release approach

1. Validate requirements, payroll choice, device access, menu and delivery rules.
2. Prototype the employee and operational flows and test usability.
3. Build and test the MVP with one canteen or a limited employee group if operationally feasible.
4. Pilot and measure queue time, order completion, waste, and satisfaction.
5. Decide whether to expand based on approved exit criteria and operational capacity.

## Dependencies and risks

See [BRD](03_BRD.md) and [Source Notes](10_Source_Notes.md). Main dependencies are employee identity, menu accuracy, kitchen readiness, delivery capacity, payroll policy, and an agreed benefits baseline.

