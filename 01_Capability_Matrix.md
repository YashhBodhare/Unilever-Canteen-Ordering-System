# BA Capability Matrix

This matrix maps the four website tabs to evidence in this repository. Each card has a suggested GitHub destination. The **Evidence status** column distinguishes supplied-source evidence from newly drafted analysis and activities that have not happened.

## Core BA Capabilities

| Website card | Portfolio description | Evidence link | Evidence status |
|---|---|---|---|
| Stakeholder Analysis | Identified employee, canteen, kitchen, delivery, payroll, IT, and management interests and responsibilities. | [Stakeholders and Elicitation](02_Stakeholders_and_Elicitation.md) | Stakeholder roles appear in sources; influence and engagement detail is an analyst draft. |
| Requirements Elicitation | Prepared questions to confirm employee, canteen, payroll, and support needs. | [Interview and Survey Guide](02_Stakeholders_and_Elicitation.md#elicitation-plan) | Questionnaire is drafted. No completed interview or survey evidence was supplied. |
| Requirements Analysis | Structured the business, functional, non-functional, and transition requirements and connected them to tests. | [FRD and RTM](04_FRD_and_RTM.md) | Source requirements exist; normalized register and traceability are drafted here. |
| Process Improvement | Compared the manual canteen journey with an online ordering and workstation-delivery concept. | [Process Maps](07_Process_Maps.md) | As-Is and future-state concepts appear in source files; maps here are reconstructed for clarity. |
| Solution Evaluation | Compared process options against user, canteen, integration, and operational needs. | [Gap Analysis and Solution Evaluation](09_Gap_Analysis_and_Solution_Evaluation.md) | Qualitative analyst draft. Cost and technical feasibility data remain unavailable. |
| Business Case Development | Framed expected benefits and measures around waiting time, food waste, operating cost, and employee experience. | [Project Baseline](00_Project_Baseline.md) | Training-case targets are included; no cost model, ROI, or realized benefit data was supplied. |

## Techniques & Methods

| Website card | Portfolio description | Evidence link | Evidence status |
|---|---|---|---|
| Stakeholder Interviews | Created an interview guide for employees, canteen managers, kitchen staff, delivery, HR/payroll, and IT. | [Interview and Survey Guide](02_Stakeholders_and_Elicitation.md#interview-guide) | Guide drafted; interviews not evidenced. |
| 5 Whys Analysis | Traced queueing and food waste to demand timing, limited seating, walk-in ordering, and menu availability. | [Gap Analysis](09_Gap_Analysis_and_Solution_Evaluation.md#root-cause-analysis) | Hypotheses derived from the scenario; validate with stakeholders and operational data. |
| MoSCoW Prioritisation | Proposed a first-release priority for ordering, menu, fulfilment, payroll, reporting, and later enhancements. | [FRD and RTM](04_FRD_and_RTM.md#prioritisation) | Draft prioritisation; sponsor approval is open. |
| Gap Analysis | Compared current walk-in service with the proposed online order and delivery process. | [Gap Analysis](09_Gap_Analysis_and_Solution_Evaluation.md#gap-analysis) | Analyst draft based on supplied scenario. |
| Facilitated Workshops | Prepared a workshop agenda to validate scope, order rules, payroll, fulfilment, and success measures. | [Miro Board Plan](12_Miro_Board_Plan.md) | Workshop plan only; no workshop completion evidence supplied. |
| Root-Cause Analysis | Used the case's fishbone analysis and developed testable causes for queueing and waste. | [Gap Analysis](09_Gap_Analysis_and_Solution_Evaluation.md#root-cause-analysis) | Fishbone is present in a source version; cause validation remains open. |

## BA Deliverables

| Website card | Portfolio description | Evidence link | Evidence status |
|---|---|---|---|
| Business Requirements Document | Defined business need, outcomes, scope, assumptions, and success measures. | [BRD](03_BRD.md) | Reconstructed portfolio draft. |
| User Stories | Converted employee and operational needs into a prioritized backlog. | [User Stories](05_User_Stories.md) | Analyst draft; review with product and delivery teams. |
| Acceptance Criteria | Added testable conditions for core ordering and fulfilment stories. | [User Stories](05_User_Stories.md) | Analyst draft. |
| Requirements Traceability Matrix | Linked business needs to functional requirements, stories, and UAT scenarios. | [FRD and RTM](04_FRD_and_RTM.md#requirements-traceability-matrix) | Analyst draft. |
| Business Rules | Clarified employee eligibility, cutoff, order confirmation, payroll enrollment, and delivery boundaries. | [FRD and RTM](04_FRD_and_RTM.md#business-rules) | Derived draft; unresolved rules are marked. |
| UAT Scenarios | Prepared role-based tests for menu, ordering, cutoff, kitchen processing, delivery, payroll, and reporting. | [UAT Plan](11_UAT_Plan.md) | Test plan drafted; execution and sign-off not evidenced. |

## Models & Diagrams

| Website card | Portfolio description | Evidence link | Evidence status |
|---|---|---|---|
| As-Is Process Map | Mapped the walk-in lunch journey and its queue and availability pain points. | [Process Maps](07_Process_Maps.md#as-is-process) | Source map exists; Mermaid version is reconstructed. |
| To-Be Process Map | Mapped online ordering, kitchen preparation, workstation delivery, and feedback. | [Process Maps](07_Process_Maps.md#to-be-process) | Future-state source map exists; Mermaid version is reconstructed. |
| BPMN Diagram | Modelled the proposed order fulfilment with roles, events, tasks, and decision points. | [Models and BPMN](08_Models_and_BPMN.md#bpmn-style-to-be-process) | Draft BPMN-style model; convert and validate in a BPMN editor before claiming BPMN 2.0 conformance. |
| Use-Case Diagram | Showed how employees and operational roles interact with the canteen service. | [Models and BPMN](08_Models_and_BPMN.md#use-case-view) | Analyst draft. |
| Stakeholder Map | Mapped stakeholder interest and influence for engagement planning. | [Stakeholders and Elicitation](02_Stakeholders_and_Elicitation.md#stakeholder-map) | Analyst draft; validate influence ratings. |
| Wireframe | Specified the key employee and operations screens and their states. | [Wireframe Specifications](06_Wireframe_Specifications.md) | Screen specification drafted; visual mockups need design-team review. |

## Using the matrix on the website

After publishing to GitHub, replace each relative path with its repository URL. Link each capability card to the specific evidence file. Link “Explore the Complete BA Case Study” to the repository README. Keep evidence-status language on the page when a card describes a plan or a draft rather than completed research or testing.

