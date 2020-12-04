---
title: "Creating Events"
date: 2020-11-27T15:45:28+01:00
weight: 11
---

<!-- The Modal -->
<div id="myModal" class="modal">
  <span class="close">&times;</span>
  <img class="modal-content" id="img01">
  <div id="caption"></div>
</div>

{{<lead>}}
The Event configuration page is accessed from the Configuration > Events menu option, and is where all [Event Definitions](/glossary#event-definition) are listed and where you can create and edit your own event definitions. An event definition defines the specific tags the system should supervise. Setting conditions on tags enables the Event to become active and notifications to be raised whenever the value of those tags exceed some defined boundaries. The event definition also enables you to define which [Recipients](/glossary#recipient) the notifications are to be sent, and whether to notify them via email, phone or push notifications.
{{</lead>}}

<figure class="image_container">
    <img class="center_image figure_resize1" onClick="reply_click(this)"  id="configure_events_menu" src="/configure_events_menu.png" alt="Event configuration menu">
    <figcaption>Fig 1. Accessing the event configuration view</figcaption>
</figure>

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="config-events" src="/config-events.png" alt="Events configuration">
    <figcaption>Fig 2. Event configuration view</figcaption>
</figure>

The event definition table provides several details for each event definition. The event type, number of recipients and the definition's enabled/disabled state are displayed. event definitions can be created <img src="/add_event_button.png">, duplicated <img  src="/duplicate_event.png">, edited <img src="/edit_event.png"> and deleted <img  src="/delete_event.png">. event definitions can be searched by name or filtered by [Endpoint](/glossary#endpoint) by the filters provided.

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

As for the event definition itself, "NAME", "DESCRIPTION", "TYPE" info should be populated and the event should be enabled if you want it to take the set actions for the [Condition](/glossary#condition) set.<br/>
There are two types of event definitions: [Alarm](/glossary#alarm) and Other. Alarms can be [acknowledged](/glossary#acknowledge-synonym-ack) and can became active and inactive depending of the latest value. Event definitions of type "Other" just gets archived when the condition is not met. 
<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="event_general" src="/event_general.png" alt="General event info">
    <figcaption>Fig 4. General event info</figcaption>
</figure>

#### Condition
"Condition" tab is preselected <img src="/condition_tab.png"> when you open the "Add event" popup. A condition must be set in order for the event instance to be created. You should choose one "ENDPOINT", and one or many [Tags](/glossary#tag) from "TAG" list to create a condition, and compose the actual condition for tag's value, quality or time by choosing a relevant "OPERATOR" and desired "VALUE". <br/> If the event definition is created for many tags, the tag that will raise this event is the activation tag which name is used in the display of the name of the [Event Instance](/glossary#event-instance), listed in the [Event View](/events) page.
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
These are [Notifications](/glossary#notification) that need to be sent in chosen ways to chosen recipients, with custom content, if the event definition condition is met.
<br/>
To create an "action", select type "Notification" from the "TYPE" dropdown. 
You can populate "CONTENT" and "VOICE MESSAGE TEXT" by choosing a template from the "TEMPLATE" dropdown, which is editable or by adding a text in the fields. "CONTENT" is required if you have "NOTIFY USING" "SMS", "Email" and "Push" enabled. "VOICE MESSAGE TEXT" is required if you have "NOTIFY USING" "Voice" enabled. You can play/stop the "VOICE MESSAGE TEXT" to check the whole message that will be played to the Recipient in the Call Notification. <br/>
Recipients can be added one by one or as a [Recipients Group](/glossary#recipient-group) from the "RECIPIENTS" dropdown.
<br/>
Notifications can be repeated in the number of times set in the "REPEAT" textbox. In "INTERVAL (MIN)" you can define the interval between the notifications if they need to be repeated. In "PAUSE FOR NEXT ACTION (MIN)" you can define the interval between the Actions if they need to be looped (see "EXECUTION" in "Advanced settings" for more details).
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
Advanced settings is where you can set the additional configuration for the event definition.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="advanced_settings" src="/advanced_settings.png" alt="Advanced settings"> 
    <figcaption>Fig 9. Advanced settings</figcaption>
</figure>

 In "GRACE PERIOD (MIN)" you can define the minutes to pass before this Event Instance becomes active after it is created. <br/>
 In "EXECUTION" you can define if Actions should execute "Once" or many times in "Loop".<br/>
 "BREAK WHEN EVENT BECOMES" inactive or acknowledged refers to stopping the notifications set to be repeated and all actions set to be executed again.

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