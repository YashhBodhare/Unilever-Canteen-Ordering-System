# Models and BPMN

## System context

~~~mermaid
flowchart LR
    Employee[Employee] -->|Identity, menu request, order, feedback| COS((Canteen Ordering Service))
    COS -->|Menu, confirmation, status| Employee
    Manager[Canteen Manager] -->|Menu, assignments, updates| COS
    COS -->|Demand summary, reports| Manager
    Kitchen[Kitchen Staff] <-->|Preparation list, completion| COS
    Delivery[Delivery Associate] <-->|Assigned orders, delivery status| COS
    HR[HR / Payroll] <-->|Eligibility, deduction data, reconciliation| COS
    IT[IT / Support] <-->|Access, monitoring, support| COS
~~~

## Use-case view

~~~mermaid
flowchart LR
    Employee[Employee] --> Login((Sign in))
    Employee --> Menu((View menu))
    Employee --> Order((Create and confirm order))
    Employee --> Status((View order status))
    Employee --> Feedback((Submit feedback))
    Manager[Canteen Manager] --> Publish((Manage menu))
    Manager --> Summary((Review preparation summary))
    Manager --> Assign((Assign fulfilment))
    Kitchen[Kitchen Staff] --> Prepare((Prepare orders))
    Delivery[Delivery Associate] --> Complete((Record delivery))
    Payroll[HR / Payroll] --> Reconcile((Reconcile deductions))
    Manager --> Reports((Review reports))
~~~

## Draft entity relationship model

~~~mermaid
erDiagram
    EMPLOYEE ||--o{ ORDER : places
    EMPLOYEE ||--o| PAYROLL_ENROLLMENT : has
    EMPLOYEE ||--o{ FEEDBACK : submits
    ORDER ||--|{ ORDER_LINE : contains
    MENU ||--|{ MENU_ITEM : lists
    MENU_ITEM ||--o{ ORDER_LINE : selected_as
    ORDER ||--o{ ORDER_STATUS_EVENT : has
    DELIVERY_ASSIGNMENT }o--|| ORDER : fulfils
    EMPLOYEE ||--o{ DELIVERY_ASSIGNMENT : receives
    PAYROLL_EXPORT ||--o{ PAYROLL_LINE : contains
    ORDER ||--o| PAYROLL_LINE : contributes_to
~~~

### Data notes

- `EMPLOYEE` should use a minimum necessary identifier and approved workstation location reference.
- `ORDER` needs service date, canteen, total, payment route, and current status.
- `ORDER_LINE` preserves the ordered item name and price at confirmation to support audit and reconciliation.
- `PAYROLL_EXPORT` and `PAYROLL_LINE` apply only if payroll deduction is approved.
- The model is conceptual. Keys, retention, history, and integration ownership need technical design.

## BPMN-style To-Be process

This is a readable BPMN-style draft expressed in Mermaid. Recreate it in a BPMN editor and validate pools, lanes, events, gateways, messages, and exception flows before describing it as a formal BPMN 2.0 model.

~~~mermaid
flowchart LR
    subgraph Employee
        A([Start]) --> B[Sign in and view menu]
        B --> C[Build and confirm cart]
    end
    subgraph Ordering_Service
        C --> D{Eligible and before cutoff?}
        D -->|No| E[Display rejection reason]
        D -->|Yes| F[Create confirmed order]
        F --> G[Update order status]
    end
    subgraph Canteen_Operations
        F --> H[Consolidate demand]
        H --> I[Prepare meals]
        I --> J[Assign delivery]
    end
    subgraph Delivery
        J --> K[Deliver to workstation]
        K --> L[Record delivery outcome]
    end
    subgraph Payroll_if_approved
        F -. Monthly cycle .-> M[Export eligible totals]
        M --> N{Payroll accepts file?}
        N -->|Yes| O[Reconcile accepted totals]
        N -->|No| P[Resolve rejected records]
    end
    L --> Q([End])
~~~

## Stakeholder influence and interest

See the stakeholder table and draft influence-interest placements in [Stakeholders and Elicitation](02_Stakeholders_and_Elicitation.md#stakeholder-map). Keep placement ratings out of a public claim of stakeholder approval until participants validate them.

