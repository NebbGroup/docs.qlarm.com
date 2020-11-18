---
title: "Event Configuration"
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
The Events configuration page is where [Event Definitions](/glossary#event-definition) are listed and where you can configure your own Event Definition. The Event Definition is about malicious time, quality and value of a sensor that need to be detected and [Event](/glossary#event) to be raised. Raising the Event takes [Actions](/glossary#action) in place which is notifying [Recipients](/glossary#recipient) in many forms with feedback options.
{{</lead>}}

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="config-events" src="/config-events.png" alt="Events configuration">
    <figcaption>Fig 1. Events configuration</figcaption>
</figure>

Type of the Event Definition, number of Recipients and if the event definition is enabled, are information displayed in the table. Event Definitions can be created <img src="/add_event_button.png">, duplicated <img  src="/duplicate_event.png">, edited <img src="/edit_event.png"> and deleted <img  src="/delete_event.png">. Event Definitions can be searched by name or filtered by [Endpoint](/glossary#endpoint) by the filters provided.

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

As for the Event Definition it self, "NAME", "DESCRIPTION", "TYPE" info should be populated and the event should be enabled if you want it to take the set Actions for the [Condition](/glossary#condition) set.<br/>
There are two types of Event Definitions: [Alarm](/glossary#alarm) and Other. Alarms can be [acknowledged](/glossary#acknowledge-synonym-ack) and can became active and inactive depending of the latest value. Other type of Event Definition just gets archived when the Condition is not met (See page Events for more details). 
<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="event_general" src="/event_general.png" alt="General event info">
    <figcaption>Fig 4. General event info</figcaption>
</figure>

#### Condition
"Condition" tab is preselected <img src="/condition_tab.png"> when you open the "Add event" popup. A Condition must be set in order for the Event Instance to be created. You should choose one "ENDPOINT", and one or many [Tags](/glossary#tag) from "TAG" list to create a Condition, and compose the actual Condition for Tag's value, quality or time by choosing a relevant "OPERATOR" and desired "VALUE". <br/> If the Event Definition is created for many Tags, the Tag that will raise this Event is the Activation Tag which name is used in the display of the name of the [Event Instance](/glossary#event-instance), listed in the ["Events" page](/events).
<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="event_condition" src="/event_condition.png" alt="Event condition">
    <figcaption>Fig 5. Event condition</figcaption>
</figure>

After a Condition is created it is listed in the table below and can be edited <img src="/edit_event.png"> and deleted <img  src="/delete_event.png">.
<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="condition_edit_mode" src="/condition_edit_mode.png" alt="Edit event condition">
    <figcaption>Fig 6. Edit event condition</figcaption>
</figure>

#### Actions
Actions can be defined in the tab "Actions" <img  src="/actions_tab.png">.
These are [notifications](/glossary#notification) that need to be sent in chosen ways to chosen Recipients, with custom content, if the Event Definition Condition is met.
<br/>
To create an "action", select type "Notification" from the "TYPE" dropdown. 
You can populate "CONTENT" and "VOICE MESSAGE TEXT" by choosing a template from the "TEMPLATE" dropdown, which is editable or by adding a text in the fields. "CONTENT" is required if you have "NOTIFY USING" "SMS", "Email" and "Push" enabled. "VOICE MESSAGE TEXT" is required if you have "NOTIFY USING" "Voice" enabled. You can play/stop the "VOICE MESSAGE TEXT" to check the whole message that will be played to the Recipient in the Call Notification. <br/>
Recipients can be added one by one or as a [Recipients Group](/glossary#recipient-group) from the "RECIPIENTS" dropdown.
<br/>
Notification can be repeated in the number of times set in the "REPEAT" textbox. In "INTERVAL (MIN)" you can define the interval between the notifications if they need to be repeated. In "PAUSE FOR NEXT ACTION (MIN)" you can define the interval between the Actions if they need to be looped (see "EXECUTION" in "Advanced settings" for more details).
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
Advanced settings is where you can set the additional configuration for the Event Definition.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="advanced_settings" src="/advanced_settings.png" alt="Advanced settings"> 
    <figcaption>Fig 9. Advanced settings</figcaption>
</figure>

 In "GRACE PERIOD (MIN)" you can define the minutes to pass before this Event Instance becomes active after it is created. <br/>
 In "EXECUTION" you can define if Actions should execute "Once" or many times in "Loop".<br/>
 "BREAK WHEN EVENT BECOMES" Inactive or Acknowledged refers to stopping the notifications set to be repeated and all Actions set to be executed again.

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