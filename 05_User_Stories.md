# User Stories and Acceptance Criteria

This is a draft backlog derived from the scenario. Story points, owners, sprint assignments, and delivery status should be set by the delivery team after refinement. They are intentionally not fabricated here.

| ID | Epic | User story | Priority |
|---|---|---|---|
| US-01 | Employee access | As an eligible employee, I want to sign in with my work identity so that only authorized employees can place orders. | Must |
| US-02 | Menu | As an employee, I want to view the current menu, descriptions, prices, and availability so that I can choose a meal before ordering. | Must |
| US-03 | Cart and confirmation | As an employee, I want to add items, adjust quantities, review the total, and confirm so that my order is accurate. | Must |
| US-04 | Order cutoff | As an employee, I want to know the daily order deadline so that I understand when I can still place an order. | Must |
| US-05 | Order history | As an employee, I want to view my confirmed order and status so that I know whether it is being prepared or delivered. | Should |
| US-06 | Kitchen preparation | As a canteen manager, I want a consolidated order list grouped by item so that the kitchen can prepare the right quantities. | Must |
| US-07 | Menu administration | As an authorized menu manager, I want to publish and update the daily menu so that employees see current choices and prices. | Must |
| US-08 | Delivery | As a delivery associate, I want to see my assigned deliveries and update their status so that orders reach the correct workstations. | Must |
| US-09 | Feedback | As an employee, I want to leave feedback after delivery so that the canteen can identify service issues. | Should |
| US-10 | Reporting | As a manager, I want reports on order volume, item demand, sales, and feedback so that I can review service performance. | Should |
| US-11 | Payroll | As an enrolled employee, I want eligible meal charges recorded for payroll deduction so that I can use the approved payment arrangement. | Open |
| US-12 | Support and accessibility | As a user, I want clear, accessible screens and a support route so that I can complete an order or get help when something fails. | Open |

## Acceptance criteria

### US-01 Employee sign-in

~~~gherkin
Scenario: Eligible employee signs in
  Given the employee has an active eligible work identity
  When the employee completes authentication
  Then the service grants access to the employee ordering functions

Scenario: Ineligible identity attempts to order
  Given the identity is inactive or not eligible
  When authentication or eligibility validation completes
  Then the service denies ordering access and displays a clear next step
~~~

### US-02 Daily menu

~~~gherkin
Scenario: Employee views a published menu
  Given a menu is published for the selected service date and canteen
  When the employee opens the menu
  Then each available item shows its name, description, price, category, and availability

Scenario: No menu is published
  Given no menu is available for the selected date
  When the employee opens the menu
  Then the service explains that ordering is unavailable and provides the next expected update if known
~~~

### US-03 Cart and confirmation

~~~gherkin
Scenario: Employee confirms a valid order before cutoff
  Given the order window is open
  And the cart contains available items
  When the employee reviews and confirms the order
  Then the service creates one confirmed order with the correct items and total
  And the service displays an order reference and next-step status

Scenario: Employee changes a draft cart
  Given the employee has not confirmed the order
  When the employee changes an item or quantity
  Then the cart and total update before confirmation
~~~

### US-04 Cutoff

~~~gherkin
Scenario: Employee attempts to confirm after cutoff
  Given the approved daily cutoff has passed
  When the employee attempts to confirm an order
  Then the service blocks confirmation and explains that the order window is closed
~~~

### US-06 Kitchen summary

~~~gherkin
Scenario: Manager reviews confirmed demand
  Given the ordering window has closed
  When the manager opens the preparation summary
  Then the service displays confirmed quantities grouped by menu item
  And the summary includes the approved fulfilment location details
~~~

### US-07 Menu administration

~~~gherkin
Scenario: Authorized manager publishes a menu
  Given the user has menu-management permission
  When the user enters valid items, descriptions, prices, and availability and publishes
  Then the menu becomes visible for the selected date and canteen
  And the service records who published it and when
~~~

### US-08 Delivery status

~~~gherkin
Scenario: Delivery associate completes an assigned delivery
  Given an order is assigned to the delivery associate
  When the associate marks the order delivered
  Then the service records the delivery status and timestamp
  And the employee can see the completed status
~~~

## Refinement questions

- What item customization is allowed, and how does the kitchen see it?
- Can employees place multiple orders in one day or across two canteens?
- Is order edit allowed until confirmation only, or until the cutoff?
- What is the cancellation and unavailable-item policy after confirmation?
- Is a delivery time selected by the employee or assigned by operations?
- Does payroll deduction require explicit employee consent, and what happens when a deduction is rejected?
- What story-point scale and estimation team will be used?

