---
title: "User Settings"
date: 2020-08-20T16:06:59+02:00
weight: 14
---

<!-- The Modal -->
<div id="myModal" class="modal">
  <span class="close">&times;</span>
  <img class="modal-content" id="img01">
  <div id="caption"></div>
</div>

{{<lead>}}
The User settings contains basic settings that apply to the whole application when viewing different content on different pages.
{{</lead>}}

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="user_settings" src="/user_settings.png" alt="User Settings">
    <figcaption >Fig 1. User Settings</figcaption>
</figure>

The "Page size" drop down list enables the user to select the number of values in each table. The "Language" drop down list enables the user to select the general language of the application. The "Time Zone" drop down list enables the user to select the time zone for the whole application. The "Date Time Format" drop down list enables the user to select the dates format. The "Time Format" drop down list lest the user set the time format.

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
</script>