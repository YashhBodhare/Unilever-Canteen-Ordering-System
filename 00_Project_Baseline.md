# Project Baseline

## Executive summary

The case describes a workplace canteen serving a large office population. Employees concentrate lunch breaks around noon, while limited seating and a manual, walk-in service create queues. Employees may not find their preferred meals, and the canteen may prepare food that remains unsold. The proposed service lets eligible employees view a daily menu and place lunch orders before a defined cutoff. Canteen staff prepare grouped orders and delivery associates take meals to employee workstations. Payroll deduction and management reporting appear in the source scenario, but their implementation boundaries need confirmation.

## Problem statement

Employees spend a material part of their lunch period travelling to and waiting at the canteen. The canteen has limited seating and relies on walk-in demand, which makes it harder to plan quantities and provide each employee's preferred meal. The business needs a controlled ordering and fulfilment process that improves access to lunch and gives canteen management better demand information.

## Scenario facts and draft targets

| Item | Value stated in supplied materials | Treatment in this case study |
|---|---:|---|
| Office population | About 1,500 employees | Scenario input. Confirm whether this means registered users or expected concurrent use. |
| Canteens | 2 | Scenario input. Confirm whether both use one service and menu. |
| Seating | About 150 per canteen at a time | Scenario input. |
| Lunch window | Most employees prefer noon to 1 p.m. | Scenario input. |
| Lunch duration | About 60 minutes, including travel and waiting | Scenario input. |
| Queue and table wait | About 30 to 35 minutes | Scenario input. Measurement method is not supplied. |
| Food waste | One source gives a 25% baseline; target language varies | Baseline and denominator require confirmation. See [Source Notes](10_Source_Notes.md). |
| Waste reduction | At least 30% within 6 months in multiple versions | Draft target. Confirm whether relative reduction or percentage-point change. |
| Operating cost | Reduce by 15% within 12 months | Draft target. Cost categories and baseline period require approval. |
| Effective work time | Increase by 30 minutes per employee per day within 3 months | Draft target. Define measurement and eligible population. |

## Proposed outcomes and measures

1. Reduce employee time spent waiting for lunch service. Measure queue time before and after launch using an agreed sample and comparable lunch periods.
2. Reduce unsold food. Record prepared quantity, sold quantity, and discarded quantity by item and day.
3. Reduce canteen operating cost. Agree which labor, food, delivery, and technology costs count before calculating a change.
4. Improve employee experience. Use a short post-order satisfaction question and monitor order completion issues.
5. Improve demand visibility. Give canteen management a daily order summary before food preparation begins.

The numerical targets above come from the training case and are not independently validated. Do not present them as achieved results.

## Proposed product boundary

### Working MVP scope, pending business approval

- Employee identity verification and access to the ordering service.
- Daily menu publication with item descriptions and prices.
- Employee cart creation, review, and order confirmation before the cutoff.
- A controlled order cutoff so the kitchen can prepare the confirmed demand.
- Canteen manager view of confirmed orders and a preparation summary.
- Delivery assignment and delivery completion status for workstations.
- Employee feedback after fulfilment.
- Basic usage, sales, menu popularity, and fulfilment reports.
- Payroll deduction for employees enrolled in the agreed scheme, subject to interface and reconciliation approval.

### Working exclusions, pending business approval

- Breakfast ordering.
- Orders by visitors, former employees, or other external users.
- Supplier procurement, vendor management, and full inventory management.
- Canteen staff payroll and payment administration.
- Refunds and complex post-confirmation cancellations.
- SMS/email notifications and dietary recommendation features for the first release.
- Delivery to locations other than approved employee workstations.

Responsive access on mobile or tablet is unresolved in the sources. Treat it as an open requirement rather than an exclusion until the sponsor confirms it.

## Draft solution outline

The employee selects a menu item, adds it to a cart, checks the total, and confirms before the daily order cutoff. The service locks the confirmed order and makes a consolidated preparation list available to canteen management. Kitchen staff prepare the orders. The manager assigns delivery tasks, and delivery staff update each order as delivered. Employees can provide feedback after delivery. If payroll deduction is approved, monthly order totals are sent to the payroll process with reconciliation and exception handling.

## Success conditions

- A business owner approves the problem statement, target definitions, MVP scope, and release measures.
- HR/payroll and IT agree on employee eligibility, data exchange, error handling, and reconciliation.
- Canteen staff validate cutoff timing, menu publication, preparation summaries, and delivery capacity.
- The solution passes security, accessibility, performance, and UAT reviews before launch.

