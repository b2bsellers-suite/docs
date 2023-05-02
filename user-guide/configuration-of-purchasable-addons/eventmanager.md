---
description: 'Directory: custom/plugins/B2BSellersCore/addons/B2bEventManager'
---

# Eventmanager

With the Event Manager, sales staff can easily create and manage events. Customers can register in the store for free or paid events.

{% hint style="danger" %}
The Event Manager is available as an addon from version 1.1.0.
{% endhint %}

### **Features**

* Convenient participant management
  * Editing the participant data&#x20;
  * Overview of all participating events of a customer
  * Manually add a participant
  * Circular Mail to all Participants
* Filterable event overview for customer
* Participant overview for customer (customer can see other participants from the same company)
* Event detail page
* Waiting list function
* Various event attributes (language, format and difficulty)
* Events are linked to products. This allows the Shopware Core Checkout process to be used.
* Participant limit&#x20;
* Registration deadline (time limit to register for an event possible)



## **Actions of the sales staff**

The Sales Staff has the ability to create or manage events.

### Create event

In the menu, select Event Manager > Create Event. Note that each event must be assigned to an article (Shopware standard function).

{% hint style="info" %}
Multiple events can be assigned to one item.
{% endhint %}

<figure><img src="../../.gitbook/assets/image (26).png" alt=""><figcaption></figcaption></figure>

After creating the event, you will be redirected to the event management page. Alternatively, you can find the event management page under Event Manager -> Manage Events. Here you can make further settings for the event details, participants and descriptions.

{% hint style="info" %}
By default, the event is always created in "draft" mode. Depending on the settings in the Shopware admin area, it may still be necessary to change the event status so that the event is visible to customers. You can do this under Event Manager -> Manage Events -> Your Event.
{% endhint %}

### More Information

1.  Changing participant details

    Both participant information and document information can be adjusted or completed.
2. Participant management\
   The Sales Staff can manually add a customer to the event. An already registered participant can be set by Cusomer Stuff to the status Excluded, Canceled, Not Participated or Participated. Different statuses can be created in the Shopware Admin area.

<figure><img src="../../.gitbook/assets/image (6) (1).png" alt=""><figcaption><p>Participant management</p></figcaption></figure>

3. Event managment\
   The event can be customized or extended at any time. With a click on the magnifying glass icon you can edit the event details.

<figure><img src="../../.gitbook/assets/image (11).png" alt=""><figcaption><p>Event managment</p></figcaption></figure>

4. Circular Mail\
   The Sales Stuff can conveniently send email to all participants in the frontend.

<figure><img src="../../.gitbook/assets/image (3).png" alt=""><figcaption><p>Circular Mail</p></figcaption></figure>

5. Creation of event specifications\
   Sales Stuff can create and manage different event formats, venues, speakers and difficulty levels.

<figure><img src="../../.gitbook/assets/image (1) (1).png" alt=""><figcaption><p>Creation of event specifications</p></figcaption></figure>



## **Actions of the custom**

1. Overview of registered events\
   The participant can view an overview of all registered events. The overview page can also be filtered by various parameters such as format, level of difficulty, languages and search terms.

<figure><img src="../../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

2. Register colleagues for event\
   Customers can also purchase a ticket for employees of the same company. It is possible to purchase a ticket for several colleagues at the same time..

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

## **Configuration in Shopware Admin**

B2b settings -> Event-Manager settings

### Event status participants can register

By selecting one or more event statuses, you can define with which event statuses participants can register.

### Event category

The event category is linked in the customer dashboard. Here the user can be redirected to the selected category page by clicking the "Discover all Events" button.

### Event category URL



### Available Event Languages

Select the possible languages that the sales staff can store as event languages

### Event Backend
