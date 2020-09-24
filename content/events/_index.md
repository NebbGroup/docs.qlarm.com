---
title: "Events"
date: 2020-08-20T15:30:04+02:00
weight: 4
pre: ""
---

<!-- The Modal -->
<div id="myModal" class="modal">
  <span class="close">&times;</span>
  <img class="modal-content" id="img01">
  <div id="caption"></div>
</div>

{{<lead>}}
Event view lists the current and the past events in tabs Events and History.
<img src="/events-view-tabs.png" > <br />
Sort on column and various filtering are provided for both tabs. Current events have details provided in collapsible row. Events can be edited and have Logs.
{{</lead>}}

If the event obtains many tags, then the name displayed for the event is consisted of the tag name dash ("-") the the name of the custom event.
<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="events" src="/events.png" alt="Events">
    <figcaption>Fig 1. Events</figcaption>
</figure>

## Types of Events
There are two types of events defined in the system: Alarm and Other.
<br />
The functional flow for the Alarm type events is:
An event instance (Alarm) is Created and then it gets the Creation Date.
<br />
If there is a grace period defined in the Custom Event, then the event instance is Activated after the grace period expires. And if not it is activated right after it is created and then it gets the Activation Date.
<br />
If the new evaluation does not meet the Alarm condition, the Alarm gets Inactivated if it is not in a grace period (Inactive Date), on the other hand, if it is in a grace period it gets Archived (Archived Date).
<br />
Being active or inactive, event can be Acknowledged by a user (Acknowledged date).
<br />
Every time an event condition is met, before the creation of an event instance, system finds the old inactive alarm for the Custom Event (acknowledged or not) and it archives it (Archived date).
<br />
Custom Event can be edited or deleted. In this case its instances gets Archived (Archived date).
<br />
The functional flow for the Other type events is:
An event instance is Created (Creation Date).
<br />
If there is a grace period defined in the Custom Event, the event instance is Activated after this grace period. And if not, it is activated right after it is created (Activation Date).
<br />
If the new evaluation does not meet the Event condition, the Event gets Archived, (Archived Date).
<br />
Custom Event can be edited or deleted. In this case its instances gets Archived (Archived date).

## Columns
Columns for Alarm type are:

- Creation time
- Activation time
- Inactive time
- Acknowledged time
- Archived time

Columns for Other type are:

- Creation time
- Activation time
- Archived time

Both types of Events have State: They can be in grace period or not. This depends on the time elapsed since creation.

## Filters
The following filters are available for both Events and History tabs:
- "ENDPOINT FILTER" - the endpoint filter is preselected and is used to select events created for any of the tags of the selected endpoint. 
- "TAG FILTER" - tag filter is populated with the selected endpoint tags and is not preselected. It filters events for selected tag.
- "SEARCH FILTER" (by name) - filters the events with a name that contains the search string.
- "EVENT TYPE" - f only the events from selected type.
- "IN GRACE PERIOD" - If checked than only events that are in grace period will be displayed. If this is not the case, only the events that are not in a grace period will be listed.

For Events tab we also have: 
- "EVENT STATE" - filters the events that have the selected event state.
- "ACKNOWLEDGED STATE" - filters the events that have the selected acknowledged state.
<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="Event_view_filters" src="/Event_view_filters.png" alt="Event view filter options">
    <figcaption>Fig 2. Event view filter options</figcaption>
</figure>

For History tab we also have:
- "DATE FILTER" - filters the events by creation date.
<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="History_filters" src="/History_filters.png" alt="History filter options">
    <figcaption>Fig 3. History filter options</figcaption>
</figure>

Depending on what is selected in the filters, you can have a different columns displayed: Column is not displayed if its data is not expected for a certain filter combination.

## Info in columns (cells population)
If data is not expected, "-" is displayed. <br />
If data is expected but not available, an empty cell is displayed.

## Events details
In Event view tab event details are provided and in order to be displayed you need to click the arrow at the beginning of the row.
If data is not expected, the label for a certain time is not displayed.<br />
If data is expected but not available, "-" is displayed.
<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="event_details" src="/event_details.png" alt="Event details">
    <figcaption>Fig 4. Event details</figcaption>
</figure>

## Sorting
Clicking on a column header will sort the table data by the column clicked.

## Event view Edit
Events listed in the Event view tab can be edited by clicking "Edit" in the row context menu.
<img src="/events_view_edit_link.png">

## Logs
Events listed in both Event view and History tab have logs. They can be reached by clicking "Logs" the row context menu. <img src="/events_view_logs_link.png"> 
<br />
Logs display tracking data about the event. What has happen, when and by who. There is also a possibility for a user to add a custom log (a comment).
<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="events_view_logs" src="/events_view_logs.png" alt="Logs">
    <figcaption>Fig 5. Logs</figcaption>
</figure>

## Event view Actions
Event view events can be acknowledged by clicking the "ACK" button for the event row. A popup appears and you can confirm or cancel the acknowledgement. <img src="/events_view_ack_link.png" > 
<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="events_view_ack_popup" src="/events_view_ack_popup.png" alt="Acknowledge event">
    <figcaption>Fig 6. Acknowledge event</figcaption>
</figure>

## Event view Links
Events are related to tags which data can be visually presented in a chart in Trend view. Link to this page is available in Trend column of the Event view tab. <img src="/events_view_trend_link.png" >

<script>
// Get the modal
var modal = document.getElementById("myModal");

var modalImg = document.getElementById("img01");
var captionText = document.getElementById("caption");
function reply_click(img)
{
    modal.style.display = "block";
    modalImg.src = img.src;
    captionText.innerHTML = img.alt;
}

modal.onclick = function() { 
  modal.style.display = "none";
}

document.addEventListener('keyup', function(e) {
    if (e.keyCode == 27) {
        modal.style.display = "none";
    }
});
</script>
