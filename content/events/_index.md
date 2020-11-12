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
The "[Events](/glossary#event)" page shows the current status and history of [Event Instances](/glossary#event-instance). The event lists can be filtered to display events in several different ways.
The "Event [View](/glossary#view)" tab lists the currently active events, and inactive events that have not been acknowledged.
The "History" tab lists all events that are both inactive and acknowledged.
<img src="/events-view-tabs.png" > <br />
The [Event Definitions](/glossary#event-definition) can be edited for each instance, and the [Logs](/glossary#logs) containing all the changes the event states pass through can be accessed.
{{</lead>}}

If the [Event Definition](/glossary#event-definition) obtains many [Tags](/glossary#tag), then the name displayed for the [Event Instances](/glossary#event-instance) is consisted of the [Tag](/glossary#tag)'s name dash ("-") the the name of the [Event Definition](/glossary#event-definition).
<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="events" src="/events.png" alt="Events">
    <figcaption>Fig 1. Events</figcaption>
</figure>

## Types of Events
There are two types of [Events](/glossary#event) defined in the system: [Alarm](/glossary#alarm) and Other.
<br />
The functional flow for the [Alarm](/glossary#alarm) type events is:
An [Event Instance](/glossary#event-instance) ([Alarm](/glossary#alarm)) is Created and then it gets the Creation Date.
<br />
If there is a [Grace Period](/glossary#grace-period) defined in the [Event Definition](/glossary#event-definition), then the [Event Instance](/glossary#event-instance) is Activated after the [Grace Period](/glossary#grace-period) expires. And if not it is activated right after it is created and then it gets the Activation Date.
<br />
If the new evaluation does not meet the [Alarm](/glossary#alarm) [Condition](/glossary#condition), the [Alarm](/glossary#alarm) gets Inactivated if it is not in a [Grace Period](/glossary#grace-period) (Inactive Date), on the other hand, if it is in a [Grace Period](/glossary#grace-period) it gets Archived (Archived Date).
<br />
Being active or inactive, [Event Instance](/glossary#event-instance) can be [Acknowledged](/glossary#acknowledge-synonym-ack) by a [Recipient](/glossary#recipient) (Acknowledged date).
<br />
Every time an [Condition](/glossary#condition) is met, before the creation of an [Event Instance](/glossary#event-instance), system finds the old inactive [Alarm](/glossary#alarm) for the [Event Definition](/glossary#event-definition) ([acknowledged](/glossary#acknowledge-synonym-ack) or not) and it archives it (Archived date).
<br />
[Event Definition](/glossary#event-definition) can be edited or deleted. In this case its instances gets Archived (Archived date).
<br />
The functional flow for the Other type [Events](/glossary#event) is:
An [Event Instance](/glossary#event-instance) is Created (Creation Date).
<br />
If there is a [Grace Period](/glossary#grace-period) defined in the [Event Definition](/glossary#event-definition), the [Event Instance](/glossary#event-instance) is Activated after this [Grace Period](/glossary#grace-period). And if not, it is activated right after it is created (Activation Date).
<br />
If the new evaluation does not meet the [Condition](/glossary#condition), the [Event Instance](/glossary#event-instance) gets Archived, (Archived Date).
<br />
[Event Definition](/glossary#event-definition) can be edited or deleted. In this case its instances gets Archived (Archived date).

## Columns
Columns for [Alarm](/glossary#alarm) type are:

- Creation time
- Activation time
- Inactive time
- Acknowledged time
- Archived time

Columns for Other type are:

- Creation time
- Activation time
- Archived time

Both types of [Event Instances](/glossary#event-instance) have State: They can be in [Grace Period](/glossary#grace-period) or not. This depends on the time elapsed since creation.

## Filters
The following filters are available for both Events and History tabs:
- "ENDPOINT FILTER" - the endpoint filter is preselected and is used to select [Event Instances](/glossary#event-instance) created for any of the [Tags](/glossary#tag) of the selected [Endpoint](/glossary#endpoint). 
- "TAG FILTER" - the tag filter is populated with the selected [Endpoint](/glossary#endpoint) [Tags](/glossary#tag) and is not preselected. It filters [Event Instances](/glossary#event-instance) for selected [Tag](/glossary#tag).
- "SEARCH FILTER" (by name) - filters the [Event Instances](/glossary#event-instance) with a name that contains the search string.
- "EVENT TYPE" - filters only the [Event Instances](/glossary#event-instance) from selected [Event Type](/glossary#event-type).
- "IN GRACE PERIOD" - if checked than only [Event Instances](/glossary#event-instance) that are in [Grace Period](/glossary#grace-period) will be displayed. If this is not the case, only the [Event Instances](/glossary#event-instance) that are not in a [Grace Period](/glossary#grace-period) will be listed.

In the Events tab there are also:  
- "EVENT STATE" - filters the [Event Instances](/glossary#event-instance) that have the selected event state.
- "ACKNOWLEDGED STATE" - filters the [Event Instances](/glossary#event-instance) that have the selected acknowledged state.
<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="Event_view_filters" src="/Event_view_filters.png" alt="Event view filter options">
    <figcaption>Fig 2. Event view filter options</figcaption>
</figure>

In the History tab there are also:  
- "DATE FILTER" - filters the [Event Instances](/glossary#event-instance) by creation date.
<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="History_filters" src="/History_filters.png" alt="History filter options">
    <figcaption>Fig 3. History filter options</figcaption>
</figure>

Depending on what is selected in the filters, you can have a different columns displayed: Column is not displayed if its data is not expected for a certain filter combination.

## Info in columns (cells population)
If data is not expected, "-" is displayed. <br />
If data is expected but not available, an empty cell is displayed.

## Events details
In Event view tab [Event](/glossary#event) details are provided and in order to be displayed you need to click the arrow at the beginning of the row.
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
Events listed in both Event view and History tab have [Logs](/glossary#logs). They can be reached by clicking "Logs" the row context menu. <img src="/events_view_logs_link.png"> 
<br />
[Logs](/glossary#logs) display tracking data about the event. What has happen, when and by who. There is also a possibility for a [User](/glossary#user) to add a custom log (a comment).
<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="events_view_logs" src="/events_view_logs.png" alt="Logs">
    <figcaption>Fig 5. Logs</figcaption>
</figure>

## Event view Actions
Event view events can be [acknowledged](/glossary#acknowledge-synonym-ack) by clicking the "ACK" button for the [Event Instance](/glossary#event-instance) row. A popup appears and you can confirm or cancel the acknowledgement. <img src="/events_view_ack_link.png" > 
<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="events_view_ack_popup" src="/events_view_ack_popup.png" alt="Acknowledge event">
    <figcaption>Fig 6. Acknowledge event</figcaption>
</figure>

## Event view Links
[Events](/glossary#event) are related to [Tags](/glossary#tag) which data can be visually presented in a chart in [Trend view](/glossary#view). Link to this page is available in "Trend" column of the "Event view" tab. <img src="/events_view_trend_link.png" >

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
