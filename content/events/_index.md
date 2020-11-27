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
The "Events" page shows the current status and history of [Event Instances](/glossary#event-instance). The event lists can be filtered to display events in several different ways.
The "Event View" tab lists the currently active [Events](/glossary#event), and inactive Events that have not been acknowledged.
The "History" tab lists all Events that are both inactive and acknowledged.<br>
The [Event Definitions](/glossary#event-definition) can be edited for each instance, and the [Logs](/glossary#logs) containing all the changes the event states pass through can be accessed.
{{</lead>}}

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="events" src="/events.png" alt="Events">
    <figcaption>Fig 1. Events</figcaption>
</figure>

## Types of Events
There are two [Event Types](/glossary#event-type) defined in the system: [Alarm](/glossary#alarm) and Other.
<br>
<br />
The functional flow for the Alarm type of Events is:<br>
An Event Instance (Alarm) is Created and assigned a Creation Date.
<br />
If there is a [Grace Period](/glossary#grace-period) defined in the Event Definition, the Event Instance is Activated after the Grace Period expires. If no Grace Period is defined, it is activated immediately.
<br />
If the new evaluation does not meet the Alarm [Condition](/glossary#condition), the Alarm is Inactivated if it is not in a Grace Period (Inactive Date). If it is in a Grace Period it is Archived.
<br />
Both active and inactive Event Instances can be [Acknowledged](/glossary#acknowledge-synonym-ack) by a [Recipient](/glossary#recipient).
<br />
Every time a Condition is met, before the creation of an Event Instance, system finds the old inactive Alarm for the Event Definition (acknowledged or not) and archives it .
<br />
Event Definitions can be edited or deleted. In this case its instances are Archived.
<br />
<br>
The functional flow for the Other type of Events is:<br>
An Event Instance is Created.
<br />
If there is a [Grace Period](/glossary#grace-period) defined in the Event Definition, the Event Instance is Activated after the Grace Period expires. If no Grace Period is defined, it is activated immediately.
<br />
If the new evaluation does not meet the Condition, the Event Instance are Archived.
<br />
Event Definition can be edited or deleted. In this case its instances are Archived.

## Columns
Columns common for all Event Types are:

| Column Name | Value |
|---------|---------|
| State | Active or Inactive |
| Timer | Time elapsed since Activation |
| Type | Alarm or Other
| Creation Time | Timestamp for creation| 
| Active Time | Timestamp for transition to Active state |
| Inactive Time | Timestamp for transition to Inactive state | 
| Ack Time | Timestamp for Acknowledgement of Alarm |
| Trend | Link to trend view | 
| Actions | Button for Acknowledging Alarm | 


## Filters
The following filters are available for both Events and History tabs:
- "ENDPOINT FILTER" - the endpoint filter is preselected and is used to select Event Instances created for any of the Tags of the selected [Endpoint](/glossary#endpoint). 
- "TAG FILTER" - the tag filter is populated with the selected Endpoint Tags and is not preselected. It filters Event Instances for selected Tag.
- "SEARCH FILTER" (by name) - filters the Event Instances with a name that contains the search string.
- "EVENT TYPE" - filters only the Event Instances from selected Event Type.
- "IN GRACE PERIOD" - If checked, only Event Instances that are in Grace Period will be displayed . 

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

## Info in columns 
If the Event Definition contains many Tags, then the name displayed for the Event Instances consists of the Tags' names separated by dashes ("-") <br>
If data is not expected, "-" is displayed. <br />
If data is expected but not available, an empty cell is displayed.

## Event details
Details are provided for all Event Instances in the "Event View". Clicking the arrow at the beginning of each row expands the row to show all associated Event Details.
If data is not expected, the label for a certain time is not displayed.<br />
If data is expected but not available, "-" is displayed.
<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="event_details" src="/event_details.png" alt="Event details">
    <figcaption>Fig 4. Event details</figcaption>
</figure>

## Sorting
Clicking on a column header will sort the table data by the selected column.

## Editing Event Instances
Events listed in the Event view tab can be edited by clicking "Edit" in the row context menu. This will take the user to the [Event Configuration](/configuration/events) page and open the specific Event Definition for editing.
<img src="/events_view_edit_link.png">

## Logs
Events listed in both Event view and History tab have Logs. They can be reached by clicking "Logs" the row context menu. <img src="/events_view_logs_link.png"> 
<br />
The Log for each instance contains information on changes in the State of the event, which [User](/glossary#user) initiated the change, and at what time the change occured.There is also a possibility for the User to add a custom log in the form of a comment.
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
