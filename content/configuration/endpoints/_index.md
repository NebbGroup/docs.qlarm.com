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
The Endpoints configuration page contains all of the accessible endpoints and their associated nodes. 
Endpoint is logical representation of OPC server in the context of Qlarm environment, providing necessary data to manage an OPC server. Endpoints are the starting point of the main functional flow in the system, the messaging flow. All properties of an endpoint should be configured to respond to the necessity of the flow. Starting from configuration of the endpoint (its OPC server with tags associted) via custom event definitions to events raised and notifications send to recipients, endpoints are the main thrade for all of these entities. Monotoring pages like Live, Events, Notifications can all be filtered by endpoint.
{{</lead>}}

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="endpoints_configuration" src="/endpoints_configuration.png" alt="Endpoints configuration">
    <figcaption>Fig 1. Endpoints configuration</figcaption>
</figure>

Upon opening the Endpoints configuration the user is greeted with a list of the accessible endpoints which can be filtered by entering a keyword in the Search Filter.

Each Endpoint is displayed with basic information: Name, Location, Status; and additional information: Date Time Format, IoT Device Name, Description, Type, Time Zone, Time Format and Number of Tags. The Date Time and Time format shows the format preference for the Date Time and Time for the notifications that show up in the Notifications View. The Time Zone shows the time zone in which the Endpoint operates. Type shows the type of the Endpoint. IoT Device Name and Descriptions may contain additional naming information for the specific Endpoint. Most of this information can be edited by clicking the <img src="/edit_button.png" alt="New Dashboard button"> button, separately for each Endpoint. You can edit Name, Date Time Format, IoT Device Name, Description, Time Zone and Time Format. Additionally, in this mode there is more information about a specific endpoint: Unique Identifier, Keywords, Update frequency, Geographical Coordinates, Geo Location and IP Address. You can also set the specific Endpoint to be the default endpoint which will enable every information associated with it to appear first in any table content. When a specific endpoint is not set as default the "Set Default" button is blank <img src="/set_default_blank.png" alt="New Dashboard button">, otherwise it is coloured <img src="/set_default_primary.png" alt="New Dashboard button">. 

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="edit_endpoint" src="/edit_endpoint.png" alt="Endpoint edit mode">
    <figcaption>Fig 2. Endpoint edit mode<figcaption>>
</figure>

<img src="/log_button.png" alt="New Dashboard button"> contains the logs for any changes associated with the specific Endpoint.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="logs" src="/logs.png" alt="Endpoint logs">
    <figcaption>Fig 3. Endpoint logs<figcaption>
</figure>

The Status Label displays if the Endpoint is <img src="/online_status.png" alt="online status"> or <img src="/offline_status.png" alt="offline status">. 

By clicking the <img src="/tag_button.png" alt="New Dashboard button"> button the user the view the table of associated tags for that endpoint. For each known tag the table displays its Name, Description, OPC UA URL, Value Type, Precision, Deadband, Unit, Live Data View, Log View, Enable status. 

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="tags" src="/tags.png" alt="tags">
    <figcaption>Fig 4. Endpoint tags<figcaption>
</figure>

By clicking on the <img src="/edit_recipient_button.png" alt="online status"> button you can change the actions for the specific tag listed in the table, upon which an edit tag form appears. Also, by selecting multiple tags and clicking on the <img src="/change_button.png" alt="New Dashboard button"> button you can apply changes to all the selected tags. 

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="edit_tag" src="/edit_tag.png" alt=" Edit tag">
    <figcaption>Fig 5. Edit tag<figcaption>
</figure>

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="edit_tags" src="/edit_tags.png" alt="Edit selected tags">
    <figcaption>Fig 6. Edit selected tags<figcaption>
</figure>

The user can add a new tag by clicking on the <img src="/add_tag_button.png" alt="online status"> button, upon which an add tag form appears which requires information to be provided.

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