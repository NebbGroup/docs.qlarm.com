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
<figure class="image_container">
    <img class="center_image" src="/event_view_screen.png" alt="Events page">
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
- "ENDPOINT FILTER" - <img src="/events_view_endpoint_filter.png"> This filter is preselected and it filters events for selected endpoint. 
- "TAG FILTER" - <img src="/events_view_tag_filter.png"> This filter is populated with the selected endpoint tags and is not preselected. It filters events for selected tag. 
- "SEARCH FILTER" (by name) - <img src="/events_view_search_filter.png"> This filters events by name that contains the search string.
- "EVENT TYPE" - <img src="/events_view_event_type_filter.png"> This filters only the events from selected type.
- "IN GRACE PERIOD" - <img src="/events_view_in_grace_filter.png"> If this is checked than only events that are in grace period will be displayed. Otherwise only the events that are not in a grace period are listed.

For Events tab we have 
- "EVENT STATE" - <img src="/events_view_event_state_filter.png"> This filters the events that have the selected event state.
- "ACKNOWLEDGED STATE" - <img src="/events_view_acknowledged_state_filter.png">This filters the events that have the selected acknowledged state.

- There is also "DATE FILTER" <img src="/events_view_date_filter.png"> that is available for the History tab, and it filters the events by creation date.

Depending on what is chosen in the filters we have a different display of columns: If data is expected for a column for a certain filter combination, than the column is displayed.

## Info in columns (cells population)
If data is not expected than "-" is displayed. <br />
If data is expected but not available then an empty cell is displayed.

## Events details
In Event view tab event details are provided and in order to be displayed click on the arrow at the beginning of the row.
If data is not expected than the label for a certain time is not displayed.<br />
If data is expected but not available then "-" is displayed.
<figure class="image_container">
    <img class="center_image" src="/event_details.png" alt="Events page">
    <figcaption>Fig 2. Event details</figcaption>
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
    <img class="center_image" src="/events_view_logs.png" alt="Events page">
    <figcaption>Fig 3. Logs</figcaption>
</figure>

## Event view Actions
Event view events can be acknowledged from this view by clicking the relevant row "ACK" button. <img src="/events_view_ack_link.png" > Than popup appears and we need to confirm if we acknowledge the event or we can cancel the acknowledgement.
<figure class="image_container">
    <img class="center_image" src="/events_view_ack_popup.png" alt="Events page">
    <figcaption>Fig 4. Acknowledge event</figcaption>
</figure>

## Event view Links
Event view events are related to tags which data can be visually presented in a chart in Trend view. Link to this page is available in Trend column. <img src="/events_view_trend_link.png" >

