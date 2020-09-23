---
title: "Events"
date: 2020-08-20T15:54:15+02:00
weight: 9
---

<!-- The Modal -->
<div id="myModal" class="modal">
  <span class="close">&times;</span>
  <img class="modal-content" id="img01">
  <div id="caption"></div>
</div>

{{<lead>}}
Events page is where custom events are listed. 
{{</lead>}}
<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="config-events" src="/config-events.png" alt="Events configuration">
    <figcaption>Fig 1. Events configuration</figcaption>
</figure>

Type of the event, number of recipients and if the event is enabled, are information displayed in the table. Events can be created <img src="/add_event_button.png">, duplicated <img  src="/duplicate_event.png">, edited <img src="/edit_event.png"> and deleted <img  src="/delete_event.png">. Events can be searched by name or filtered by endpoint by the filters provided.
<figure class="image_container">
    <img class="center_image myImg figure_resize2" onClick="reply_click(this)"  id="config_events_filters" src="/config_events_filters.png" alt="Events filter options">
    <figcaption>Fig 2. Events filter options</figcaption>
</figure>

## Add event
If you click on the "Add event" button <img src="/add_event_button.png"> "Add event" popup is opened.
<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="add_event" src="/add_event.png" alt="Add event">
    <figcaption>Fig 3. Add event</figcaption>
</figure>

As for the event it self, "NAME", "DESCRIPTION", "TYPE" info should be populated and the event should be enabled if you want it to take the set actions for the condition set.<br/>
There are two types of events, Alarms and Other. Alarms can be acknowledged and can became active and inactive depending of the latest value. Other type of event just gets archived when the condition is not met (See page Events for more details). 
<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="event_general" src="/event_general.png" alt="General event info">
    <figcaption>Fig 4. General event info</figcaption>
</figure>

#### Condition
Condition tab is preselected <img src="/condition_tab.png"> when you open the "Add event" popup. A condition must be set in order for the event to be created. You should choose one "ENDPOINT", and one or many tags from "TAG" list to create a condition, and compose the actual condition for tag's value, quality or time by choosing a relevant "OPERATOR" and desired "VALUE". <br/> If the custom event is created for many tags, the tag that will raise this event is the activation tag which name is used in the display of the name of the event, listed in the Events page.
<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="event_condition" src="/event_condition.png" alt="Event condition">
    <figcaption>Fig 5. Event condition</figcaption>
</figure>

After a condition is created it is listed in the table below and can be edited <img src="/edit_event.png"> and deleted <img  src="/delete_event.png">.
<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="condition_edit_mode" src="/condition_edit_mode.png" alt="Edit event condition">
    <figcaption>Fig 6. Edit event condition</figcaption>
</figure>

#### Actions
Actions can be defined in the tab "Actions" <img  src="/actions_tab.png">.
These are notifications that need to be sent in chosen ways to chosen recipients, with custom content, if the event condition is met.
<br/>
To create an Action, select type Notification from the "TYPE" dropdown. 
You can populate "CONTENT" and "VOICE MESSAGE TEXT" by choosing a template from the "TEMPLATE" dropdown, which is editable or by adding a text in the fields. "CONTENT" is required if you have "NOTIFY USING" "SMS", "Email" and "Push" enabled. "VOICE MESSAGE TEXT" is required if you have "NOTIFY USING" "Voice" enabled. You can play/stop the "VOICE MESSAGE TEXT" to check the whole message that will be played to the recipient in the call notification. <br/>
Recipients can be added one by one or as a recipient group from the "RECIPIENTS" dropdown.
<br/>
Notification can be repeated in the number of times set in the "REPEAT" textbox. In "INTERVAL (MIN)" you can define the interval between the notifications if they need to be repeated. In "PAUSE FOR NEXT ACTION (MIN)" you can define the interval between the actions if they need to be looped (see "EXECUTION" in "Advanced settings" for more details).
<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="add_action" src="/add_action.png" alt="Add action">
    <figcaption>Fig 7. Add action</figcaption>
</figure>

Actions added are listed in the table below and can be edited <img src="/edit_event.png"> and deleted <img  src="/delete_event.png">.
<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="edit_event_action" src="/edit_event_action.png" alt="Edit event action">
    <figcaption>Fig 8. Edit action</figcaption>
</figure>

#### Advanced settings
Advanced settings is where you can set the additional configuration for the event.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="advanced_settings" src="/advanced_settings.png" alt="Advanced settings"> 
    <figcaption>Fig 9. Advanced settings</figcaption>
</figure>

 In "GRACE PERIOD (MIN)" you can define the minutes to pass before this event becomes active after it is created. <br/>
 In "EXECUTION" you can define if actions should execute "Once" or many times in "Loop".<br/>
 "BREAK WHEN EVENT BECOMES" Inactive or Acknowledged refers to stopping the notifications set to be repeated and all actions set to be executed again.

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


// Get the <span> element that closes the modal
var span = document.getElementsByClassName("close")[0];

// When the user clicks on <span> (x), close the modal
span.onclick = function() { 
  modal.style.display = "none";
}
</script>