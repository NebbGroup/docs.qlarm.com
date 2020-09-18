---
title: "Events"
date: 2020-08-20T15:30:04+02:00
weight: 4
pre: ""
---

{{<lead>}}
Event view is listing the current and the past events in tabs Events and History, respectively. 
<img src="/events-view-tabs.png" > <br />
Sorting on column and various filtering are provided for both tabs. Events tab events have details provided in collapsible row and can be edited. Both Events and History data have Logs.
{{</lead>}}

If the event optains many tags then the name displayed for the event is consisted of the tag name dash ("-") the the name of the custom event.
<figure class="image_container">
    <img class="center_image" src="/events.png" alt="Events">
    <figcaption>Fig 1. Events</figcaption>
</figure>

## Types of Events
There are two types of alarms defined in the system now: Alarm and Other.
<br />
The functional flow for the Alarm type events is:
An event instance (Alarm) is Created and then it gets the Creation Date.
<br />
If there is a grace period defined in the Custom Event, then the event instance is Activated after this grace period. And if not it is activated right after it is created and then it gets the Activation Date.
<br />
If the reason for the Alarm is gone (the new evaluation does not satisfy the Alarm condition, e.g. the freezer got cold enough again) than the Alarm gets Inactivated if it is in a grace period and then it gets the Inactive Date and Archived if it is in a grace period and then it gets the Archived Date.
<br />
If the Alarm is Acknowledged by a user, active or inactive, then it gets the Acknowledged date.
<br />
Every time a real-world alarm happens, before the creation of an alarm in the system, we find the old inactive alarms for the Custom Event (acknowledged or not) and we archive them, then they get the Archived date.
<br />
Custom Event can be edited or deleted. Alarms that happen because of it are Archived, then they get the Archived date.
<br />
The functional flow for the Other type events is:
An event instance (Event) is Created and then it gets the Creation Date.
<br />
If there is a grace period defined in the Custom Event, then the event instance is Activated after this grace period. And if not it is activated right after it is created and then it gets the Activation Date.
<br />
If the reason for the Event is gone (the new evaluation does not satisfy the Event condition) than the Event gets Archived, then it gets the Archived Date.
<br />
Custom Event can be edited or deleted. Alarms that happen because of it are Archived, then they get the Archived date.

## Columns
According to the explanation above, for Alarm we can expect:

- Creation time
- Activation time
- Inactive time
- Acknowledged time
- Archived time

And for Other type of event we can expect:

- Creation time
- Activation time
- Archived time

They both have State : In grace period or not, and that only depend of the time passed since creation.

## Filters
There are filters on this page mutual for both tabs (Events and History):
- "ENDPOINT FILTER" - This filter is preselected and it filters events for selected endpoint. 
- "TAG FILTER" - This filter is populated with the selected endpoint tags and is not preselected. It filters events for selected tag. 
- "SEARCH FILTER" (by name) - This filters events by name that contains the search string.
- "EVENT TYPE" - This filters only the events from selected type.
- "IN GRACE PERIOD" - If this is checked than only events that are in grace period will be displayed. Otherwise only the events that are not in a grace period are listed.

For Events tab we also have: 
- "EVENT STATE" - This filters the events that have the selected event state.
- "ACKNOWLEDGED STATE" - This filters the events that have the selected acknowledged state.
<figure class="image_container">
    <img class="center_image" src="/Event_view_filters.png" alt="Event view filter options">
    <figcaption>Fig 2. Event view filter options</figcaption>
</figure>

For History tab we also have:
- "DATE FILTER" - This filters the events by creation date.
<figure class="image_container">
    <img class="center_image" src="/History_filters.png" alt="History filter options">
    <figcaption>Fig 3. History filter options</figcaption>
</figure>

Depending on what is chosen in the filters we have a different display of columns: If data is expected for a column for a certain filter combination, than the column is displayed.

## Info in columns (cells population)
If data is not expected than "-" is displayed. <br />
If data is expected but not available then an empty cell is displayed.

## Events details
In Event view tab event details are provided and in order to be displayed click on the arrow at the beginning of the row.
If data is not expected than the label for a certain time is not displayed.<br />
If data is expected but not available then "-" is displayed.
<figure class="image_container">
    <img class="center_image" src="/event_details.png" alt="Events details">
    <figcaption>Fig 4. Event details</figcaption>
</figure>

## Sorting
Sorting by clicking on a column name in the tables in both tabs is provided.

## Event view Edit
Events listed in the Event view tab can be edited by clicking the row context menu and than chose "Edit".
<img src="/events_view_edit_link.png">

## Logs
Events listed in both Event view and History tab have logs provided. They can be reached by clicking the row context menu and than choose "Logs". <img src="/events_view_logs_link.png"> 
<br />
Logs display tracking data about the event. What has happen, when and by who. There is also a possibility for a user to add a custom log (a comment).
<figure class="image_container">
    <img class="center_image" src="/events_view_logs.png" alt="Logs">
    <figcaption>Fig 5. Logs</figcaption>
</figure>

## Event view Actions
Event view events can be acknowledged from this view by clicking the relevant row "ACK" button. <img src="/events_view_ack_link.png" > Than popup appears and we need to confirm if we acknowledge the event or we can cancel the acknowledgement.
<figure class="image_container">
    <img class="center_image" src="/events_view_ack_popup.png" alt="Acknowledge event">
    <figcaption>Fig 6. Acknowledge event</figcaption>
</figure>

## Event view Links
Event view events are related to tags which data can be visually presented in a chart in Trend view. Link to this page is available in Trend column. <img src="/events_view_trend_link.png" >

