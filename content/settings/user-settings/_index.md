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
The User settings contains basic settings that apply to the whole application when viewing different content on different pages. This is where you can specify your favorite date-time format for all the dates you are seeing in the system, you can adjust your current timezone to get the right track of the data, choose the language you are most common with or set your most preferable [Page Size](/glossary#page-size) for viewing data. Also you can set your default value for Event Type, Event State, Event Acknowledge State and Grace period.
{{</lead>}}

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="user_settings" src="/user-settings.png" alt="User Settings">
    <figcaption >Fig 1. User Settings</figcaption>
</figure>

The “Page Size” drop down list enables the [User](/glossary#user) to select the number of values in each table. The “Language” drop down list enables the User to select the general language of the application. The “Time Zone” dropdown list enables the User to select the [Time Zone](/glossary#time-zone) for the whole application. The “Date Time Format” dropdown list enables the user to select the dates format. The “Time Format” drop down list enables the User to set the Time Format. The Event Type drop down list enables the User to select type of events (All, Alarm or other). The Event State drop down list enables the User to select state of event (All, Active or Inactive). The Event Acknowledge State drop down list enables the User to select All, Acknowledged or Unacknowledged value and the Incl. Grace drop down list enables the User to select Default, Enabled or Disabled value.

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