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
Endpoint is a logical representation of [OPC server](/glossary#opc-server) in the context of Qlarm environment, providing necessary data to manage an OPC server. Endpoints are the starting point of the main functional flow in the system, the messaging flow. All properties of an Endpoint should be configured to respond to the necessity of the flow. Starting from configuration of the Endpoint (its OPC server with [Tags](/glossary#tag) associated) via [Event Definitions](/glossary#event-definition) to [Events](/glossary#event) raised and [Notifications](/glossary#notification) send to [Recipients](/glossary#recipient), Endpoints are the main trade for all of these entities.
{{</lead>}}

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="endpoints_configuration" src="/endpoints-list.png" alt="Endpoints configuration">
    <figcaption>Fig 1. Endpoints configuration</figcaption>
</figure>

Upon opening the Endpoints configuration the [User](/glossary#user) is greeted with a list of the accessible Endpoints which can be filtered by entering a keyword in the Search Filter.

Each Endpoint is displayed with basic information: Name, Location, Status; and additional information: IoT Device Name, Description, Type, and Number of Tags. Type shows the type of the Endpoint (IoT Gateway or OPC UA Server). IoT Device Name and Descriptions may contain additional naming information for the specific Endpoint. Most of these information can be edited by clicking the  <img src="/edit-btn.png" alt="Edit endpoint"> button, separately for each Endpoint. You can edit Name, Location, IoT Device Name and Description. Additionally, in this mode there is more information about a specific Endpoint: Update frequency (ms), Device primary connection string, Device secondary connection string, Date Time Format, Time Format, [Time Zone](/glossary#time-zone), Longitude, Latitude, Geo Location (GeoName), Place named by (Nominatim), Keywords. If OPC UA Server Type is selected you can set OPC UA Server URL, IP Address and OPC UA Device info. IoT Device Name is the name of the device from the IoT Hub. Device primary connection string and Device secondary connection string are the connection strings for the IoT Device which is created when the Endpoint is created and you can expect these fields to be populated after the Endpoint is created. You can easily copy them and use them for your needs. This name is unique and is always prefixed with the low key tenant name and underscore. The Time Zone shows the time zone in which the Endpoint operates. Longitude, Latitude, Geo Location (GeoName), Place named by (Nominatim) can be easily populated by choosing a place on the map or inserting Longitude and Latitude. They provide additional info for endpoint location. For OPC UA Server type an installation package can be downloaded right after the Endpoint is created on click on the “Download” button  in the header of the Endpoint panel <img src="/download-btn.png" alt="Download installation package">. You can also set the specific Endpoint to be the Default endpoint which will enable every information associated with it to appear first in any table content.  When a specific Endpoint is not set as default the "Set Default" button is <img src="/set-default.png" alt="New Dashboard button">, otherwise it is <img src="/remove-default.png" alt="New Dashboard button">. 

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="edit_endpoint" src="/add_endpoint.png" alt="Endpoint add mode">
    <figcaption>Fig 2. Endpoint add mode - OPC UA Server<figcaption>
</figure>

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="edit_endpoint" src="/edit-endpoint.png" alt="Endpoint edit mode">
    <figcaption>Fig 3. Endpoint edit mode - IoT Gateway<figcaption>
</figure>

<img src="/logs-icon.png" alt="New Dashboard button"> contains the [Logs](/glossary#logs) for any changes associated with the specific Endpoint.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="logs" src="/logs.png" alt="Endpoint logs">
    <figcaption>Fig 4. Endpoint logs<figcaption>
</figure>

The Status Label displays if the Endpoint is <img src="/online-status.png" alt="online status"> or <img src="/offline-status.png" alt="offline status">. 

Create asset button <img src="/make-asset.png" alt="Make asset button"> enables creating an asset for the chosen endpoint and its tags, which will be visible in the Assets page in shape of a graph after its creation.

By clicking the <img src="/tagsBtn.png" alt="New Dashboard button"> button the User can view the table of associated Tags for that endpoint. For each known Tag the table displays its Name, Description, OPC UA URL, Value Type, Precision, Deadband, Unit, Enable Live Data, Logs, Enable Status and Is Writable information. 

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="tags" src="/tags-view.png" alt="tags">
    <figcaption>Fig 5. Endpoint tags<figcaption>
</figure>

By clicking on the <img src="/edit-btn.png" alt="online status"> button you can change the [Actions](/glossary#action) for the specific Tag listed in the table, upon which an "Edit tag" form appears. Also, by selecting multiple Tags and clicking on the <img src="/change-button.png" alt="New Dashboard button"> button you can apply changes to all the selected Tags.
By clicking on the <img src="/delete-tag.png" alt="online status"> button you can delete the specific Tag listed in the table, upon which an “Confirm” form appears. Also, by selecting multiple Tags and clicking ont the <img src="/delete-tags.png" alt="New Dashboard button"> button you can apply changes to all the selected Tags.
By clicking "Back" button <img src="/back-btn.png" alt="back to endpoints"> you can go back to the Endpoints view.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="edit_tag" src="/editTag-form.png" alt=" Edit tag">
    <figcaption>Fig 6. Edit tag<figcaption>
</figure>

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="edit_tags" src="/edit-multiple-tags.png" alt="Edit selected tags">
    <figcaption>Fig 7. Edit selected tags<figcaption>
</figure>

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="delete_tags" src="/confirm-delete-tag.png" alt="Confirm delete tag">
    <figcaption>Fig 8. Confirm form for delete tag(s)<figcaption>
</figure>

The User can add a new Tag by clicking on the <img src="/addTag-button.png" alt="online status"> button, upon which an "Add tag" form appears which requires information to be provided. 
'Deadband' and 'Precision' input fields are visible only for tag of int, float and string value type. For boolean value type tags instead of 'Deadband' and 'Precision', there are fields for 'State true' and 'State false'.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="add_tag" src="/addTag-form.png" alt="Add tag form">
    <figcaption>Fig 8. Add tag form<figcaption>
</figure>

The User (Super Admin) can add a multiple Tags by clicking on the <img src="/import-tags-btn.png" alt="online status"> button, than on Import Tags <img src="/import-export-tags-btn.png" alt="online status"> upon which an “Tags Importing” form appears which have a template and downloading it user should add a multiple tags using excel file. In the excel file for string and boolean value type are not required ‘Deadband’ and ‘Precision’. The ‘Engineering Unit’ and ‘Engineering Icon’ are not required for all value types and also ‘StateTrue’ and ‘StateFalse’ are required only for boolean value type. While importing tags are in progress user should see a progress bar and when importing is done user should be notified with Success Message.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="import_tags" src="/importing-tags-modal.png" alt="Import multiple tags form">
    <figcaption>Fig 9. Tag Importing form<figcaption>
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