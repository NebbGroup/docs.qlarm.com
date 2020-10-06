---
title: "Live"
date: 2020-08-20T15:29:58+02:00
weight: 3
pre: ""
---

{{<lead>}}
The Live page lists all enabled [Tags](/glossary#tag). You can easily make a quick check of the [Tags](/glossary#tag) last values and [Events](/glossary#event) raised for a [Tag](/glossary#tag). You can filter the [Tags](/glossary#tag) by [Endpoint](/glossary#endpoint) and search a [Tag](/glossary#tag) by name. You can also filter the [Tags](/glossary#tag) changed in certain period of time.
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

The table lists all the [Tags](/glossary#tag) for selected [Endpoints](/glossary#endpoint) that are enabled and set for [Live View](/glossary#view) (for more details go to Endpoints section). The table shows the name, last value, last change time, associate active [Event Instances](/glossary#event-instance) and [Trend View](/glossary#view) link for each [Tag](/glossary#tag). You can filter the content in the table by activating the Search, Time or Endpoint filters.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="live_filter_options" src="/live_filter_options.png" alt="Live View filters options">
    <figcaption >Fig 2. Live View filters options</figcaption>
</figure>

In the Search filter you can search by one or more keywords and filter your [Tag](/glossary#tag) results. In the Time filter the [User](/glossary#user) can filter the [Tags](/glossary#tag) from a given time period predefined in the drop down list, or by entering a specific time period by clicking the  <img src="/options_button.png" alt="options button" class = "logo_resize"> button. In The Endpoint filter the [User](/glossary#user) can filter the [Tags](/glossary#tag) by their [Endpoints](/glossary#endpoint). Usually, the [Tags](/glossary#tag) are enabled to constantly receive information. To view these changes the [User](/glossary#user) must refresh the content in the table by clicking the <img src="/refresh_button.png" alt="refresh button" class = "logo_resize"> button.

<img src="/event_description.png" alt="event description" class = "logo_resize"> describes the icons that are displayed for every Active Event column.

- <img src="/ua-a-e.png" alt="Unacknowledged and active event" class = "logo_resize"> - Unacknowledged and active event
- <img src="/ua-ia-e.png" alt="Unacknowledged and inactive event" class = "logo_resize"> - Unacknowledged and inactive event
- <img src="/a-a-e.png" alt="Acknowledged and active event" class = "logo_resize"> - Acknowledged and active event

By clicking the Active event icon in the table, QLARM will redirect the [User](/glossary#user) to the Active [Event Instances](/glossary#event-instance) for that specific [Tag](/glossary#tag).

<img src="/trend_button.png" alt="trend button" class = "logo_resize"> redirects the [User](/glossary#user) to the [Trend View](/glossary#view) for that specific [Tag](/glossary#tag).

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