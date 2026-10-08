# Gap Analysis and Solution Evaluation

## Current-to-future gap analysis

| Area | Current situation in scenario | Desired capability | Gap | Proposed response |
|---|---|---|---|---|
| Ordering | Employees order in person during a concentrated lunch period | Eligible employees place orders before kitchen preparation | No advance capture of demand | Online daily menu, cart, confirmation, and cutoff control |
| Demand planning | Canteen sees demand as employees arrive | Manager sees confirmed quantities in advance | Kitchen lacks a reliable consolidated forecast | Preparation summary grouped by item and canteen |
| Menu availability | Employees may find preferred items unavailable | Menu and availability visible before the employee travels | Choice and availability are uncertain | Publish daily menu and define unavailable-item policy |
| Queue and seating | Employees wait for food and a table | More employees can collect or receive meals without joining the same queue | Limited seating and concentrated arrival | Workstation delivery or organized pickup; capacity requires pilot validation |
| Fulfilment | Manual coordination is described | Assigned delivery with visible status | Handoffs and delivery completion may not be traceable | Delivery queue, assignment, status events, and exception path |
| Payment | Conventional methods and payroll are both mentioned | Approved payment with reconciliation | Payment model and interface are unclear | Decide payroll vs gateway; define consent, data flow, and reconciliation |
| Reporting | Management wants usage and performance visibility | Reports on orders, sales, demand, satisfaction, and waste | Measures and data ownership are not defined | Define report catalogue and baseline metrics |
| Access and security | Employee-only system is expected | Role-based access with protected employee data | Authentication, authorization, privacy, and audit details are incomplete | Security and privacy requirements plus role design |

## Root-cause analysis

The source materials include a fishbone framing. The following 5 Whys chain is a draft hypothesis based on the stated scenario, not validated research.

**Problem:** Employees wait a long time for lunch and the canteen may waste food.

1. Why do employees wait? Many employees seek lunch in the same period and order in person.
2. Why does in-person demand cause delays? The canteens have limited seating and counter capacity relative to peak demand.
3. Why is demand difficult to plan? The kitchen receives limited advance information about individual meal choices.
4. Why is advance information limited? The current process relies on walk-in ordering and does not capture confirmed demand early enough.
5. Why does the process rely on walk-ins? No shared ordering workflow connects employees, menu publication, kitchen preparation, delivery, and payment.

**Working cause to validate:** The process lacks a reliable, timely demand signal and coordinated fulfilment workflow. Validate through observation, order data, interviews, and waste records.

## Solution options

| Option | Description | Advantages | Limitations / risks |
|---|---|---|---|
| A. Improve current walk-in process | Adjust counter queues, lunch waves, signage, and seating management | Lower technology change; can be piloted quickly | Does not provide pre-order demand or workstation delivery; may not resolve meal availability |
| B. Internal online ordering service | Employee menu, pre-order, canteen preparation dashboard, delivery status, and approved payment integration | Addresses the connected ordering and fulfilment needs in the scenario | Requires product build, identity/access, operational change, payroll integration decision, and delivery capacity |
| C. Third-party food ordering platform | Use an existing ordering provider, configured for the office | May reduce custom development effort | Supplier capability, fees, employee data, payroll fit, menu control, and integration are unknown |

## Qualitative evaluation

Scores are analyst estimates for discussion only: 1 = weak fit, 5 = strong fit. Validate weights and scores with sponsor, canteen, IT, and HR/payroll.

| Criterion | Weight | A. Process improvement | B. Internal service | C. Third-party platform |
|---|---:|---:|---:|---:|
| Advance demand capture | 25% | 1 | 5 | 4 |
| Employee ordering convenience | 20% | 2 | 4 | 4 |
| Canteen preparation visibility | 20% | 2 | 5 | 3 |
| Payroll and identity fit | 15% | 3 | 3 | 2 |
| Delivery workflow fit | 10% | 1 | 4 | 3 |
| Cost and implementation certainty | 10% | 4 | 2 | 3 |
| **Weighted score (draft)** | **100%** | **2.0** | **4.1** | **3.3** |

The internal service scores well against the stated process needs, but the comparison does not include verified costs, delivery capacity, technical feasibility, privacy review, or vendor proposals. It is not an approved recommendation.

