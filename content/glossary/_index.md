---
title: "Glossary"
date: 2020-09-24T09:56:56+02:00
weight: 21
---

###### Account
Refers to one or more accounts within Qlarm, but typically the Tenant. Other types of accounts are User account.
###### Action
An activity to be carried out by the system when the condition of an event becomes true. An event may have multiple actions, and they can be executed once or repeatedly depending on configuration.
###### Action Type
A type of Action. Currently there is only Notification implemented, but in the future there will be a multitude of Action Types available.
###### Acknowledge (synonym: ACK)
An activity by a user or a recipient to confirm that they have seen an event and take responsibility to follow up on the corresponding event.
###### Alarm
An alarm is a type of event within Qlarm. It has a stricter set of parameters, and is acknowledgeable.
###### Asset
A collection of tags, events, states and attributes that belong to a single entity within the system. An asset provides context to the system. A sensor is typically not an asset, but a device that provides data on behalf of an asset.
E.g. a motor [asset] could have tags for Speed, Power, and Temperature; and static attributes Name, Weight, and Location; and have an event (alarm) defined for Overheating. Assets can share properties through templates.
###### Asset model
An hierarchical representation (model) of assets.
###### Channel
A method or mechanism of communicating with recipients. E.g. SMS text message, e-mail, voice phone call or push notifications.
###### Condition
A rule within an event that evaluates to true or false for the attributes of a tag (its value, quality, or time). Examples:
Condition: Room temperature is over 30 °C [RoomTemp > 30].
###### Context tag
The tag within an event that triggered the event.
###### Dashboard
A graphical representation of the real time content within Qlarm. The dashboard is composed of customizable widgets showing data like values, states, graphs.
###### Default dashboard
The dashboard configuration which loads when Dashboard page is opened.
###### Edge Client
The Qlarm Edge Client is an application (service) running on the local server of a customer. The Edge Client acts as an intermediary broker between the Qlarm platform and the local data source. The Edge Client will monitor an OPC UA server locally and forward data depending on the configuration and the customer's subscription.
###### Endpoint
A connection to a data source from where to get data. The endpoint can be of types OPC UA (using the Qlarm Edge Client); IoT Gateway (using MQTT directly). An endpoint belong to a tenant and have a separate Scope defined. Endpoints have a number of tags defined, and attributes like Location, Time Zone, Geographic properties.
###### Event
An occurrence (event) defined by a given condition and corresponding actions. Examples:
Condition: Room temperature is over 30 °C
Action: Send an SMS to the janitor.
###### Event Definition
The definition of an event with its name, conditions, actions, and parameters. Found under Qlarm -> Configuration -> Events.
###### Event Instance
When an event has been triggered, an Event Instance is created. The Event Instance will remain active until the event condition reverts to false. There can only be one Event Instance active at any time (see Tag Set).
An event instance can have these states:
Created - when the condition becomes true;
In Grace Period - a defined waiting period before any actions are executed;
Active - after the grace period and when the actions are executed;
Active & Unacknowledged - the user has not yet acknowledged the event instance;
Active & Acknowledged - the user has acknowledged the event instance;
Inactive - when the condition no longer is true (no actions executed if turning inactive during grace period);
Inactive & Unacknowledged - the condition is no longer true and the user has not acknowledged;
Archived - when event is inactive and no pending user activities pending (e.g. acknowledge);
###### Event Type
Events inherit some features by their type. Currently there are only two system defined types: Alarm and Other. Alarms can be acknowledged, Other can not. In the future more types can be created and customized by the user.
###### Grace period
The time in minutes to ignore an event's condition. The purpose is to filter out or allow a certain overshoot of a tag's value. This is an advanced setting of an event. 
###### Logs
Tracking information data about changes made to an entity (Event, Endpoint, etc.).
###### MQTT
A standard messaging protocol for Internet of Things (IoT). Used for IoT endpoints to communicate between Qlarm and the local gateway.
###### Notification
A message sent from Qlarm  to notify recipients through one or more channels (SMS, voice call, e-mail or push notification). Typically defined as an action on an event.
###### OPC server
OPC is an industrial automation communication protocol. An OPC server define items/tags that can be read by the Qlarm Edge Client and forwarded tothe  Qlarm platform.
###### Page size
The number of items (rows) to be listed in a table. There is a feature at the bottom of the table to browse to the next or previous pages. 
###### Permission
A restriction rule for User action.
###### Portal
The online web application of Qlarm found on app.qlarm.com.
###### Recipient
A person that can receive notifications from QLARM. A recipient is not necessarily a user, but can be.
###### Recipients Group
A group of recipients.
###### Report
A trending chart displaying values of one or more tags in time.
###### Role
A set of permissions providing or denying access to features or activities within the system. Users have one role per tenant.
###### Scope
A limitation of the data users have access to. An endpoint will be automatically created with a data access limitation called "scope". A user can have access to one or more scopes. A user can only access the data of the scopes they have access to. They will not see the Endpoints, Dashboards, or any other elements using data from other scopes. An administrator can define who has access to which scopes.
###### Site menu
The menu tree on the left side that organizes pages.
###### Site menu items
The items of the Site menu which are links to pages or submenus.
###### Subscription
An agreement and payment plan defining the features and capabilities of Qlarm for the customer. A subscription belongs to a tenant.
###### Tag
One specific data point. E.g. a temperature.
###### Tag Set
A group of tags defined within one event that share the same conditions and actions. Event instances are created individually for each tag.
###### Tenant (account)
A tenant is similar to a customer account, and often just referred to as the Account. A tenant defines the properties of the customer, the subscription, the endpoints and the users that have access to Qlarm.
###### Ticket
An issue from a person about the system provided to system support.
###### Time zone
Time zones are defined for both the user and the endpoint, as well as Qlarm internally handing all times as UTC (Coordinated Universal Time). Qlarm will always present data to the user in the user's time zone (and time format) when in the portal, unless explicitly instructed otherwise. This enables the possibility to compare data between endpoints in different time zones.
It is important to note that the time shown in notifications for recipients will be in the endpoint's time zone (and the tenants time format) as there are no time zones defined for recipients."
###### Trend
A chart that shows the historic values of one or more tags in the form of a graph. The x-axis is time and the y-axis the value.
###### Trigger 
The condition of an event is also called a trigger. When the condition is true the event has been triggered and an Event Instance is created.
###### User
A person whom have access to the Qlarm system. A user may have access to one or more tenants.
###### View 
One of the "pages" in the system providing a view/perspective to the data. E.g. Live View, Events View, History View, Trend View.
###### Widget
A configurable component on the dashboard which provides real-time values about tags, endpoints and the system.