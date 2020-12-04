---
title: "Viewing Tags"
date: 2020-11-30T14:19:36+01:00
weight: 9

---


{{<lead>}}



<figure class="image_container">
    <img class="center_image figure_resize1" onClick="reply_click(this)"  id="live_view" src="/live_menu.png" alt="Live view">
    <figcaption >Fig 1. Live view menu option</figcaption>
</figure>

The Live page provides an exhaustive list of all enabled [Tags](/glossary#tag) in you system. The list details the Tags' latest values, any [Events](/glossary#event) associated with the Tags, and provides a link to the Tags' trend [view](/glossary#view). 
Several filtering functions enable you to narrow down the list selection to show only Tags of interest. 
{{</lead>}}

<!-- The Modal -->
<div id="myModal" class="modal">
  <span class="close">&times;</span>
  <img class="modal-content" id="img01">
  <div id="caption"></div>
</div>

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="live_view" src="/live_view.png" alt="Live view">
    <figcaption >Fig 1. Live view</figcaption>
</figure>

The table lists all the Tags for selected [Endpoints](/glossary#endpoint) that are enabled and set for Live View (for more details see [Endpoints section](/configuration/endpoints)). The table shows the name, last value, last change time, associated active [Event Instances](/glossary#event-instance) and Trend View link for each Tag. You can filter the content in the table by activating the Search, Time or Endpoint filters.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="live_filter_options" src="/live_filter_options.png" alt="Live View filters options">
    <figcaption >Fig 2. Live View filters options</figcaption>
</figure>

In the Search filter you can search by one or more keywords and filter your Tag results. In the Time filter the [User](/glossary#user) can filter the Tags from a given time period predefined in the drop down list, or by entering a specific time period by clicking the  <img src="/options_button.png" alt="options button" class = "logo_resize"> button. In the Endpoint filter the user can filter the Tags by their Endpoints. Usually, the Tags are enabled to constantly receive information. To view these changes the user must refresh the content in the table by clicking the <img src="/refresh_button.png" alt="refresh button" class = "logo_resize"> button.

<img src="/event_description.png" alt="event description" class = "logo_resize"> describes the icons that are displayed for every Active Event column.

| Symbol                                                                                 | Description                       |
| -------------------------------------------------------------------------------------- | --------------------------------- |
| <img src="/ua-a-e.png" alt="Unacknowledged and active event">    | Unacknowledged and active event   |
| <img src="/ua-ia-e.png" alt="Unacknowledged and inactive event"> | Unacknowledged and inactive event |
| <img src="/a-a-e.png" alt="Acknowledged and active event">       | Acknowledged and active event     |

By clicking the Active event icon in the table, Qlarm will redirect the user to the Active Event Instance for that specific Tag.

<img src="/trend_button.png" alt="trend button" class = "logo_resize"> redirects the user to the trend view for that specific Tag.

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