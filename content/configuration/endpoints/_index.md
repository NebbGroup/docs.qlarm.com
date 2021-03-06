---
title: "Endpoints"
date: 2020-08-20T15:54:44+02:00
weight: 12
---

<!-- The Modal -->
<div id="myModal" class="modal">
  <span class="close">&times;</span>
  <img class="modal-content" id="img01">
  <div id="caption"></div>
</div>

{{<lead>}}
The Endpoints configuration page contains all of the accessible [Endpoints](/glossary#endpoint) and their associated nodes. An 
Endpoint is a logical representation of [OPC server](/glossary#opc-server) in the context of Qlarm environment, providing necessary data to manage an OPC server. Endpoints are the starting point of the main functional flow in the system, the messaging flow. All properties of an Endpoint should be configured to respond to the necessity of the flow. Starting from configuration of the Endpoint (its OPC server with [Tags](/glossary#tag) associated) via [Event Definitions](/glossary#event-definition) to [Events](/glossary#event) raised and [Notifications](/glossary#notification) send to [Recipients](/glossary#recipient), Endpoints are the main trade for all of these entities. Monitoring pages like Live, Events, Notifications can all be filtered by Endpoint.
{{</lead>}}

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="endpoints_configuration" src="/endpoints_configuration.png" alt="Endpoints configuration">
    <figcaption>Fig 1. Endpoints configuration</figcaption>
</figure>

Upon opening the Endpoints configuration the [User](/glossary#user) is greeted with a list of the accessible Endpoints which can be filtered by entering a keyword in the Search Filter.

Each Endpoint is displayed with basic information: Name, Location, Status; and additional information: Date Time Format, IoT Device Name, Description, Type, [Time Zone](/glossary#time-zone), Time Format and Number of Tags. The Date Time and Time format shows the format preference for the Date Time and Time for the Notifications that show up in the Notifications [View](/glossary#view). The Time Zone shows the time zone in which the Endpoint operates. Type shows the type of the Endpoint. IoT Device Name and Descriptions may contain additional naming information for the specific Endpoint. Most of this information can be edited by clicking the <img src="/edit_button.png" alt="New Dashboard button"> button, separately for each Endpoint. You can edit Name, Date Time Format, IoT Device Name, Description, [Time Zone and Time Format. Additionally, in this mode there is more information about a specific Endpoint: Unique Identifier, Keywords, Update frequency, Geographical Coordinates, Geo Location and IP Address. You can also set the specific Endpoint to be the Default endpoint which will enable every information associated with it to appear first in any table content. When a specific Endpoint is not set as default the "Set Default" button is blank <img src="/set_default_blank.png" alt="New Dashboard button">, otherwise it is coloured <img src="/set_default_primary.png" alt="New Dashboard button">. 

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="edit_endpoint" src="/edit_endpoint.png" alt="Endpoint edit mode">
    <figcaption>Fig 2. Endpoint edit mode<figcaption>>
</figure>

<img src="/log_button.png" alt="New Dashboard button"> contains the [Logs](/glossary#logs) for any changes associated with the specific Endpoint.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="logs" src="/logs.png" alt="Endpoint logs">
    <figcaption>Fig 3. Endpoint logs<figcaption>
</figure>

The Status Label displays if the Endpoint is <img src="/online_status.png" alt="online status"> or <img src="/offline_status.png" alt="offline status">. 

By clicking the <img src="/tag_button.png" alt="New Dashboard button"> button the User can view the table of associated Tags for that endpoint. For each known Tag the table displays its Name, Description, OPC UA URL, Value Type, Precision, Deadband, Unit, Enable Live Data, Logs, Enable Status. 

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="tags" src="/tags.png" alt="tags">
    <figcaption>Fig 4. Endpoint tags<figcaption>
</figure>

By clicking on the <img src="/edit_recipient_button.png" alt="online status"> button you can change the [Actions](/glossary#action) for the specific Tag listed in the table, upon which an "Edit tag" form appears. Also, by selecting multiple Tags and clicking on the <img src="/change_button.png" alt="New Dashboard button"> button you can apply changes to all the selected Tags. 

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="edit_tag" src="/edit_tag.png" alt=" Edit tag">
    <figcaption>Fig 5. Edit tag<figcaption>
</figure>

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="edit_tags" src="/edit_tags.png" alt="Edit selected tags">
    <figcaption>Fig 6. Edit selected tags<figcaption>
</figure>

The User can add a new Tag by clicking on the <img src="/add_tag_button.png" alt="online status"> button, upon which an "Add tag" form appears which requires information to be provided.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="add_tag" src="/add_tag.png" alt="Add tag form">
    <figcaption>Fig 7. Add tag form<figcaption>
</figure>

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