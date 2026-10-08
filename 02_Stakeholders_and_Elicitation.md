# Stakeholder Analysis and Elicitation

## Stakeholder register

Influence and interest are initial BA estimates from the scenario, not confirmed stakeholder ratings.

| Stakeholder | Primary interest or responsibility | Influence | Interest | Engagement approach |
|---|---|---:|---:|---|
| Employees | Find meals, place orders quickly, receive the correct order at the right workstation | Medium | High | Survey a broad employee sample; interview users with different work locations and lunch routines. |
| Canteen manager | Publish menus, see demand, coordinate kitchen and delivery, review operational reports | High | High | Process workshop; validate cutoff, order summaries, exceptions, and reports. |
| Chef / kitchen staff | Receive accurate preparation quantities and handle substitutions or unavailable items | Medium | High | Job shadowing and preparation walkthrough. |
| Delivery associates | Receive assigned orders and deliver them to correct locations | Medium | High | Route walkthrough and prototype review. |
| HR / payroll | Confirm employee eligibility and monthly deduction rules | High | Medium | Integration and policy interview; review reconciliation and exception flow. |
| IT / operational support | Identity, access, integration, hosting, support, monitoring, and maintenance | High | Medium | Technical discovery and security review. |
| Management / sponsor | Approve business outcomes, investment, scope, and rollout | High | Medium | Decision workshop and benefits review. |
| Project manager / product lead | Coordinate scope, milestones, risks, and decisions | High | High | Backlog refinement and decision log review. |
| Business analyst | Plan analysis, elicit and model needs, manage traceability, support validation | Medium | High | Maintain requirements and decision records. |
| Testers | Verify business rules, integrations, and end-to-end outcomes | Medium | Medium | Testability review and UAT planning. |
| Food suppliers | Provide supply and availability information if a future inventory interface is approved | Low / open | Low / open | Consult only if supplier or inventory scope is approved. |

## Stakeholder map

Use the following as a draft influence-interest map. Confirm placements with the sponsor and operational leads.

|  | **Higher interest** | **Lower or moderate interest** |
|---|---|---|
| **Higher influence** | Canteen manager; management/sponsor; HR/payroll; IT/operations; project/product lead | Executive stakeholders who approve outcomes but do not use the daily workflow |
| **Lower or moderate influence** | Employees; chefs; delivery associates; testers; business analyst | Suppliers unless procurement or inventory integration enters scope |

~~~mermaid
quadrantChart
    title Draft Stakeholder Influence and Interest
    x-axis Lower interest --> Higher interest
    y-axis Lower influence --> Higher influence
    quadrant-1 Manage closely
    quadrant-2 Keep satisfied
    quadrant-3 Monitor
    quadrant-4 Keep informed
    Canteen manager: [0.86, 0.82]
    Sponsor and management: [0.58, 0.94]
    HR and payroll: [0.48, 0.78]
    IT and operations: [0.58, 0.78]
    Employees: [0.88, 0.48]
    Kitchen staff: [0.82, 0.42]
    Delivery associates: [0.78, 0.38]
    Testers: [0.58, 0.42]
    Suppliers: [0.25, 0.22]
~~~

Ratings are analyst estimates for workshop validation.

## Draft RACI

R = responsible, A = accountable, C = consulted, I = informed. This draft assigns one accountable role per activity; confirm role names and decision rights before publication.

| Activity | Sponsor | Product / PM | BA | Canteen Manager | IT | HR / Payroll | Kitchen / Delivery | Employees | Test |
|---|---|---|---|---|---|---|---|---|---|
| Approve business outcomes and scope | A | R | C | C | C | C | I | I | I |
| Elicit and validate business requirements | I | A | R | C | C | C | C | C | C |
| Approve menu and order operating rules | I | C | R | A | C | I | C | C | I |
| Define payroll eligibility and deduction interface | I | C | C | I | R | A | I | I | C |
| Design and deliver the service | I | A | C | C | R | C | C | I | C |
| Execute UAT and recommend acceptance | I | A | C | C | C | C | C | C | R |
| Approve release readiness | A | R | C | C | C | C | I | I | C |

## Elicitation plan

The source pack provides a training scenario and proposed requirements, but it does not contain evidence of completed interviews, workshops, or a field survey. The plan below is ready for execution and should not be described as completed research.

| Activity | Participants | Purpose | Output |
|---|---|---|---|
| Employee survey | Employees across floors and work patterns | Understand ordering habits, menu needs, device access, preferred delivery, and willingness to use payroll deduction | Response dataset and summarized themes |
| Employee interviews | A small, varied set of employees | Explore order exceptions, accessibility, trust, and current lunch journey | Interview notes and validated user needs |
| Canteen observation | Canteen manager and BA | Measure queue, order, seating, preparation, and waste points at peak and off-peak times | Current-state observations and baseline measures |
| Operations workshop | Manager, chef, delivery associate, product, IT, HR/payroll | Validate To-Be process, cutoff, order grouping, handoffs, exception handling, and scope | Approved process map and decision log |
| Payroll / IT discovery | HR/payroll and IT | Confirm eligibility source, data exchange, security, reconciliation, and failure handling | Interface requirements and risks |

## Interview guide

### Employee questions

1. Walk me through your most recent lunch break at the office. Where did time get spent?
2. How do you decide what to eat, and what happens when your preferred item is unavailable?
3. What would make you trust an online canteen order and workstation delivery?
4. What information would you need before confirming an order?
5. How should the service handle an unavailable item, a late delivery, or a wrong order?
6. Which device would you use at work, and are there access or accessibility constraints?
7. Would monthly payroll deduction be acceptable? What information or controls would you expect?

### Canteen and fulfilment questions

1. How are the daily menu, quantities, prices, and substitutions decided today?
2. What is the latest time the kitchen can receive a reliable order count?
3. How should orders be grouped for preparation and delivery?
4. Which workstation details can delivery staff access, and how should they confirm delivery?
5. What exceptions create the most rework or food waste?
6. Which daily and monthly reports would change a decision?

### HR, payroll, and IT questions

1. What source confirms that a person is an eligible active employee?
2. What consent or enrollment step is required before payroll deduction?
3. What data can the ordering service send to payroll, and how are rejected records corrected?
4. What access roles, audit history, retention, and support controls are required?
5. What capacity, availability, performance, and device support targets must the team meet?

## Stakeholder survey questionnaire

**Purpose:** Understand demand and workflow needs for a proposed employee canteen ordering service. This questionnaire is ready to distribute; no respondent data or results are included in this repository.

1. How often do you use an office canteen for lunch? (Daily / 3-4 days a week / 1-2 days a week / Rarely / Never)
2. How long does your current lunch journey usually take, including travel and waiting? (Under 20 / 20-30 / 31-45 / 46-60 / Over 60 minutes)
3. What is the most difficult part of getting lunch at work? (Queue / Seating / Menu availability / Payment / Travel / Other)
4. Would you use a service to order lunch before the rush and receive it at your workstation? (Definitely / Probably / Unsure / Probably not / Definitely not)
5. Which ordering device would you prefer? (Work computer / Personal phone / Work phone / Either computer or phone / Other)
6. What menu information do you need before ordering? (Item name / Description / Price / Ingredients / Dietary or allergen details / Availability / Other)
7. When should the order cutoff occur to give the kitchen enough preparation time? (Before 10 a.m. / 10-10:30 / 10:30-11 / After 11 / Depends on menu)
8. Would you accept monthly payroll deduction for orders? (Yes / No / Need more information)
9. What should happen if an item becomes unavailable after you order? (Choose a substitute / Contact me / Remove item and adjust total / Cancel full order / Other)
10. What delivery confirmation would you expect? (Order status / Delivery message / Direct handoff / Other)
11. How important is the ability to edit an order before the cutoff? (Very important / Somewhat important / Not important)
12. What would prevent you from using this service? (Open response)
13. What change would make your lunch experience better? (Open response)

## Survey reporting guardrail

When responses are collected, report the actual sample size, dates, distribution method, and limitations. Do not present invented or simulated responses as real stakeholder research.

