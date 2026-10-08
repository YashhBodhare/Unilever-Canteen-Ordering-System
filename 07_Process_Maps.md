# Process Maps

The maps below are clean portfolio reconstructions of the scenario's current and proposed processes. Confirm timing, roles, exception paths, and payroll scope with operational stakeholders.

## As-Is process

~~~mermaid
flowchart TD
    A([Lunch break begins]) --> B[Employee travels to canteen]
    B --> C[Employee joins queue]
    C --> D{Preferred item available?}
    D -->|Yes| E[Employee orders and pays using current method]
    D -->|No| F[Employee chooses another item or leaves without preferred meal]
    E --> G{Seat available?}
    G -->|Yes| H[Employee eats]
    G -->|No| I[Employee waits for a table]
    I --> H
    H --> J[Employee returns to workstation]
    E --> K[Canteen prepares based on walk-in demand]
    F --> L[Unsold food may remain]
    K --> L
    J --> M([Lunch journey ends])
~~~

## To-Be process

~~~mermaid
flowchart TD
    A([Menu published]) --> B[Employee signs in]
    B --> C[Employee views daily menu]
    C --> D[Employee builds and reviews cart]
    D --> E{Order window open and employee eligible?}
    E -->|No| X[Show reason and next step]
    E -->|Yes| F[Employee confirms order]
    F --> G[Service locks order and creates reference]
    G --> H[Manager reviews consolidated demand]
    H --> I[Kitchen prepares confirmed meals]
    I --> J[Manager assigns delivery work]
    J --> K[Delivery associate delivers to workstation]
    K --> L[Delivery status recorded]
    L --> M[Employee submits feedback]
    L --> N[Operational reports updated]
    G -. If approved .-> P[Monthly payroll export and reconciliation]
~~~

## Process controls

- The system applies the approved cutoff using a defined local time zone.
- Only eligible employees can confirm orders.
- Menu changes after order placement trigger a defined employee and kitchen process.
- The manager sees the authoritative confirmed order count.
- Delivery status and payroll export events are timestamped and auditable.
- The team agrees on a failed delivery, unavailable item, and payroll rejection process before launch.

## Improvement hypotheses

1. Capturing demand before preparation may improve quantity planning and reduce unsold meals.
2. Consolidated orders may reduce time spent at the counter and help the kitchen sequence work.
3. Workstation delivery may reduce employee travel and waiting, subject to delivery capacity.
4. Clear menu availability may reduce disappointment when a preferred item is unavailable.

These are hypotheses to test during a pilot, not measured outcomes.

