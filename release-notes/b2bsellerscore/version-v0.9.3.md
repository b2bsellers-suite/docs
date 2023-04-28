---
description: 11.05.2022
---

# Version v0.9.3



#### Bugs

* BCS-554 Fixed bug which did not allow to reorder ordered items via Express Checkout
* BCS-547 Show error message at login if no admin and no rule is selected
* BCS-546 Shopware 6.4.11.\* compatibility
* BCS-541 Fixed a bug which always hid the prices when not logged in
* BCS-528 Fixed a bug when loading the current sales-channel context after persisting it resulted in switched the employee
* BCS-526 As Employee, if express-checkout isn't configure, it's not allowed to "express"-reorder
* BCS-523 Remove platform modal backdrop when component is destroyed
* BCS-521 as customer, I want to create the first employee and if the employee already exists, it returns an exception instead of a flash-message
* BCS-513 fixed buttons at "employee edit" page side by side
* BCS-503 if I'm logged in as employee with customer persistent cart setting "employeeBound", clone cart Error
* BCS-497 In the admin checkbox "Trade confirmation in registration" remove frontend button "Trade license\*".
* BCS-494 bug fixed which didn't allow employees to create custom products in the cart
* BCS-493 fixed a bug, which as sales rep logged in into employee, the topbar "back to sales portal" is sometimes not viewed
* BCS-479 Fixed session/sales-channel context problem for sales agents on login

#### Task

* BCS-551 Added the express checkout feature to the order history
* BCS-540 Added additional routes to switch the current active addresses instead of setting them as default and updated the address switch on the checkout confirm page
* BCS-522 Revert functionality: customer automatically login to the first employee admin
* BCS-520 add password recovery for employees
* BCS-515 if isn't any employee equal to "administrator", create an extra page after login, to set an employee instead of employee creation
* BCS-496 Add field to each employee "trackActivities" with default true
* BCS-475 Add multiple Translations to Storefront
* BCS-474 Repeat order as a quick order with recalculation of the order (availability, prices, etc.)
* BCS-470 In the Customer Migrate command, you can now also specify customer groups semicolon separated that should get B2B platform access.
* BCS-468 The "Department" field in Employees is no longer a required field
* BCS-464 if I'm logged in as sales rep, I don't know, where I'm. Show Name and Mail address in Account Menu (Header)
* BCS-423 Add missing translations at roles page
* BCS-418 Lot of small optimizations for the Employee Login
* BCS-416 Lot of small optimizations for the sales representative Login
* BCS-397 Customize express purchase ( f.e. select addresses, payment method, shipping method or make comments ...)
* BCS-245 Display the variants of the table listing in a modal instead of the table itself
