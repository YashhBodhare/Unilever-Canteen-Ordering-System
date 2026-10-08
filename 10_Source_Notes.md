# Source Notes and Decision Log

## Source inventory

The source files are training or assignment materials and identify different submitters. This repository uses them as scenario references. It does not reproduce the source documents.

| Ref | Source title | Named submitter | Format |
|---|---|---|---|
| S1 | Canteen Order System for a Simplilearn project for CBAP | Nava Timsina | PDF |
| S2 | Canteen Ordering System for Unilever, Project 1 | Sanjali Sanyal | PDF |
| S3 | Unilever Canteen Management System | Rekha Tiwari | PowerPoint |
| S4 | Canteen Ordering System for Unilever, CBAP project | Mahesh Kulkarni | PowerPoint |

Before publishing, confirm which parts are your own work and whether source documents may be redistributed. Do not present another submitter's original diagrams or prose as your own. The artifacts in this repository are a newly structured analysis of the scenario and must still be validated as a portfolio case study.

## Decision log

| ID | Decision or question | Conflicting or missing evidence | Working treatment | Decision owner | Status |
|---|---|---|---|---|---|
| DEC-01 | Is pre-ordering in scope? | It is central in proposed flows; one source lists pre-order as out of scope. | Assume same-day pre-order for the draft To-Be process. | Sponsor / Product Owner | Open |
| DEC-02 | What is the payment model? | Sources mention no payment gateway and monthly payroll deduction. | Treat payroll as conditional, with integration and consent to be approved. | HR/Payroll / Sponsor | Open |
| DEC-03 | Is inventory management in scope? | Feature lists mention inventory/order forecasting; other scope lists exclude inventory and vendor management. | Include order demand summary only; exclude full inventory and supplier procurement. | Canteen Manager / Product Owner | Open |
| DEC-04 | What does the food waste target mean? | A 30% reduction target conflicts with a 25% baseline and below-15% target. | Preserve both as unconfirmed scenario statements; define formula and baseline. | Sponsor / Finance / Canteen Manager | Open |
| DEC-05 | What is the cutoff rule? | Sources state before 11 a.m., by 11 a.m., and kitchen list at 11 a.m. | Use an 11 a.m. draft cutoff, but define whether confirmation at 11:00 is allowed. | Canteen Manager | Open |
| DEC-06 | Are mobile and tablet access included? | A source lists mobile/tablet access as out of scope; other materials propose a web/mobile service. | Mark device coverage open and validate employee access needs. | Product Owner / IT | Open |
| DEC-07 | Is the order editable after confirmation? | Sources consistently allow edits before checkout and prohibit changes after confirmation; cancellation/refund scope differs. | Lock confirmed orders; define an authorized exception process before launch. | Sponsor / Canteen Manager | Open |
| DEC-08 | Can employees select a delivery date/time? | Scenario mentions a specified time/date, while other flows assume same-day lunch delivery. | Use the same service date and standard delivery window for draft; validate. | Canteen Manager / Product Owner | Open |
| DEC-09 | What does 1,500-user capacity mean? | The source says scalable for 1,500 users but does not define concurrency. | Treat 1,500 as employee population only until load expectations are specified. | IT | Open |
| DEC-10 | What are the realized benefits? | No pilot or post-launch results were supplied. | State targets and hypotheses only; do not claim outcomes. | Sponsor | Open |

## Assumptions register

- The service is intended for employees at one office location described in the training scenario.
- Workstation delivery is the target fulfilment model for the draft MVP.
- The exact implementation technology remains a technical decision; the Java mention is not treated as an approved constraint.
- No survey, interview, workshop, UAT execution, or production deployment is evidenced in the supplied files.
- Any numerical solution evaluation in this pack is illustrative analyst scoring, not stakeholder-approved evidence.

