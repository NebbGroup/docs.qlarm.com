---
title: "Event View"
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
The "Event View" page shows the current status and history of [Event Instances](/glossary#event-instance). The event lists can be filtered to display events in several different ways.
The "Event View" tab lists the currently active [Events](/glossary#event), and inactive Events that have not been acknowledged.
The "History" tab lists all Events that are both inactive and acknowledged.<br>
<img src="/events-view-tabs.png" > <br />
The [Event Definitions](/glossary#event-definition) can be edited for each instance, and the [Logs](/glossary#logs) containing all the changes the event states pass through can be accessed.
{{</lead>}}


## Types of Events
There are two [Event Types](/glossary#event-type) defined in the system: [Alarm](/glossary#alarm) and Other.
<br>
<br />
The functional flow for the Alarm type events is:<br>
An Event Instance (Alarm) is Created and assigned a Creation Date.
<br />
If there is a [Grace Period](/glossary#grace-period) defined in the Event Definition, then the Event Instance is Activated after the Grace Period expires. And if not it is activated right after it is created and then it gets the Activation Date.
<br />
If the new evaluation does not meet the Alarm [Condition](/glossary#condition), the Alarm gets Inactivated if it is not in a Grace Period (Inactive Date), on the other hand, if it is in a Grace Period it gets Archived (Archived Date).
<br />
Being active or inactive, Event Instance can be [Acknowledged](/glossary#acknowledge-synonym-ack) by a [Recipient](/glossary#recipient) (Acknowledged date).
<br />
Every time an Condition is met, before the creation of an Event Instance, system finds the old inactive Alarm for the Event Definition (acknowledged or not) and it archives it (Archived date).
<br />
Event Definition can be edited or deleted. In this case its instances gets Archived (Archived date).
<br />
<br>
The functional flow for the Other type Events is:<br>
An Event Instance is Created (Creation Date).
<br />
If there is a Grace Period defined in the Event Definition, the Event Instance is Activated after this Grace Period. And if not, it is activated right after it is created (Activation Date).
<br />
If the new evaluation does not meet the Condition, the Event Instance gets Archived, (Archived Date).
<br />
Event Definition can be edited or deleted. In this case its instances gets Archived (Archived date).

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

Both types of Event Instances have State: They can be in Grace Period or not. This depends on the time elapsed since creation.

## Filters
The following filters are available for both Events and History tabs:
- "ENDPOINT FILTER" - the endpoint filter is preselected and is used to select Event Instances created for any of the Tags of the selected [Endpoint](/glossary#endpoint). 
- "TAG FILTER" - the tag filter is populated with the selected Endpoint Tags and is not preselected. It filters Event Instances for selected Tag.
- "SEARCH FILTER" (by name) - filters the Event Instances with a name that contains the search string.
- "EVENT TYPE" - filters only the Event Instances from selected Event Type.
- "IN GRACE PERIOD" - if checked than only Event Instances that are in Grace Period will be displayed. If this is not the case, only the Event Instances that are not in a Grace Period will be listed.

In the Events tab there are also:  
- "EVENT STATE" - filters the Event Instances that have the selected event state.
- "ACKNOWLEDGED STATE" - filters the Event Instances that have the selected acknowledged state.
<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="Event_view_filters" src="/Event_view_filters.png" alt="Event view filter options">
    <figcaption>Fig 2. Event view filter options</figcaption>
</figure>

In the History tab there are also:  
- "DATE FILTER" - filters the Event Instances by creation date.
<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="History_filters" src="/History_filters.png" alt="History filter options">
    <figcaption>Fig 3. History filter options</figcaption>
</figure>

Depending on what is selected in the filters, you can have a different columns displayed: Column is not displayed if its data is not expected for a certain filter combination.

## Info in columns (cells population)
If the Event Definition contains many Tags, then the name displayed for the Event Instances consists of the Tags' names separated by dashes ("-") the the name of the Event Definition.
<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="events" src="/events.png" alt="Events">
    <figcaption>Fig 1. Events</figcaption>
</figure>
If data is not expected, "-" is displayed. <br />
If data is expected but not available, an empty cell is displayed.

## Events details
In Event view tab Event details are provided and in order to be displayed you need to click the arrow at the beginning of the row.
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
Events listed in both Event view and History tab have Logs. They can be reached by clicking "Logs" the row context menu. <img src="/events_view_logs_link.png"> 
<br />
Logs display tracking data about the event. What has happen, when and by who. There is also a possibility for a [User](/glossary#user) to add a custom log (a comment).
<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="events_view_logs" src="/events_view_logs.png" alt="Logs">
    <figcaption>Fig 5. Logs</figcaption>
</figure>

## Event view Actions
Event view events can be acknowledged by clicking the "ACK" button for the Event Instance row. A popup appears and you can confirm or cancel the acknowledgement. <img src="/events_view_ack_link.png" > 
<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="events_view_ack_popup" src="/events_view_ack_popup.png" alt="Acknowledge event">
    <figcaption>Fig 6. Acknowledge event</figcaption>
</figure>

## Event view Links
Events are related to Tags which data can be visually presented in a chart in Trend view. Link to this page is available in "Trend" column of the "Event view" tab. <img src="/events_view_trend_link.png" >

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
