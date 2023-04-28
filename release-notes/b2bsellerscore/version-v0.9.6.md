---
description: 'Release date: 20.10.2022'
---

# Version v0.9.6

## Release Notes

{% hint style="info" %}
Here you'll find our Blog post with detailed description and developer infos: \
\
DE => [https://www.b2b-sellers.com/de/release-news-produkt-updates-im-oktober-2022/](https://www.b2b-sellers.com/de/release-news-produkt-updates-im-oktober-2022/)\
... or ... \
EN =>  [https://www.b2b-sellers.com/en/release-news-product-updates-october-2022/](https://www.b2b-sellers.com/en/release-news-product-updates-october-2022/)
{% endhint %}

#### Bugs

BCS-986 First admin creation on frontend fails

BCS-835 Sales employee creation in admin

BCS-843 Assigned employees can be removed from a budget

BCS-823 Cart errors are not persisted when the persistant cart functionality is active

BCS-815 Added getter and setter methodes for all Translation Entity Classes

BCS-814 Fixed the variant list pop up bug in grid view on product listing

BCS-812 Unable to change the payment method in the b2b platform

BCS-811 Toggling the employee individual login link doesn't work

BCS-810 Entity translation fields are empty on languages other then the ones that are shipped with B2bSellers

BCS-809 Employee Route Bug

BCS-807 When Express Checkout is turned off, you don't get a notification in the shopping cart to fill the settings.

BCS-805 Exploded View Product Detailpage error "Argument 1 must be of the type string, null given"

BCS-792 The product detail page throws an error of the product already bought subscriber for B2C customers

BCS-791 The platform menu links don't work when logging in with a language other than german

BCS-788 fixed empty selected label at administration on add new customer access to an employee

BCS-787 fix employee autocomplete search in Administration

BCS-784 Provision of property search

BCS-776 fix error on product detail page, if b2b offer is active. config statusIdsWhereProductsCanBeAdded is null

BCS-774 Only show customer in sales agents customer list with same sales-channel

BCS-769 fix failure Mailsender Check at test-data-creation

BCS-768 /account/login can be open, if b2bsellers login screen is active. Now redirected to B2Bsellers Login Screen

BCS-757 show fallback sales representative profile picture if not set

BCS-747 Quick order via CSV file Article summation

BCS-744 Order requests are not automatically ordered but only as soon as the assigned contact person has processed them.

BCS-697 Offer table sorting to newest first

BCS-688 Fixed search for company on sales representative perspective for customer list

BCS-687 Activity product detail modal loading and content adjustments

BCS-686 Customer individual prices dont apply for a quanity of 1

BCS-660 add cart products to order list - not working

BCS-646 From order lists, products can be added to the shopping cart and requested as a quote

BCS-638 If there is no purchase authorization, the system redirects to the dashboard

BCS-608 Provision of several exploded views

BCS-567 Budget order confirmation recipient may be empty.

BCS-458 A bonus is credited directly with an order request

BCS-360 In the bonus program, the bonus is only credited when a certain payment status has been reached.

#### New Features&#x20;

BCS-872 Successfully tested on Shopware Version 6.4.16

BCS-801 Added Languages: NL, DK, PL

BCS-366 Share register link on employee creation

BCS-203 new addon: set a discount percentage for individual customers

BCS-750 Account extension - users without admin can view your role

#### Issues

BCS-813 Combining the sales agent customer list endpoints

BCS-797 Add possibility to exclude hard links (controller-names) in closed store

BCS-790 Change Naming from "my collection" to "my ordered assortment" at product-lists

BCS-789 company selection at start vue-watcher

BCS-781 Fix error "undefined array key b2b\_platform\_access" on checkout order, if customer isn't a b2b customer

BCS-777 show global roles at employee pages in administration

BCS-771 Copper/Brass fehler obwohl in config hinterlegt (emm oder stecker express zu testen)

BCS-770 Reload Admin Page after Addon activate/deactivate, because EntityDefinitions don't update after activate/deactivate

BCS-767 added new column price\_lock (default: true) at offer\_items, to show open/closed lock at every item

BCS-764 Fix in admin, that the link to the customer in the customer price list works again

BCS-756 show message if no addon config is empty on b2b config page

BCS-755 oppertunity to set perffered customer to null on the profile detail page

BCS-751 Show error message when items cannot be added from the product list to the shopping cart

BCS-746 Display of an error message if there is no sufficient authorization for quick ordering

BCS-745 Optimization of the express checkout order request

BCS-742 Optimized e-mail template for order request

BCS-735 show users list at roles page

BCS-720 delete the bonus in an order repeat

BCS-703 Tracking of the ordered sums on the budget

BCS-701 Multiple budget allocation

BCS-694 Cost centers show orders already placed

BCS-692 The total orders of the cost centers are displayed

BCS-664 Improvments on order list listing page to export products via csv or add to cart

BCS-649 Offer function Product lock only possible after product selection

BCS-606 add an loader icon at contact-selection after select an customer

BCS-573 Refactoring and optimization of the B2bProductLists plugin

BCS-506 The detail buttons of the orders were adapted to mobile for the offer plugin
