---
title: "General Settings"
date: 2020-08-20T16:07:34+02:00
weight: 17
---

<!-- The Modal -->
<div id="myModal" class="modal">
  <span class="close">&times;</span>
  <img class="modal-content" id="img01">
  <div id="caption"></div>
</div>

{{<lead>}}
The General settings allows you to change the logo of the application that appears in the right corner of every page, so that the organization can have a more personal experience. Click the button to upload the company logo to personalize Qlarm. The Qlarm logo is used by default.
{{</lead>}}

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="general_settings" src="/general_settings.png" alt="General settings">
    <figcaption >Fig 1. General settings</figcaption>
</figure>

The “Time Zone” dropdown list enables the User to select the [Time Zone](/glossary#time-zone) for the whole application. The “Date Time Format” dropdown list enables the user to select the dates format. The “Time Format” drop down list lest the User set the Time Format. The Event Type drop down is list enables the User to select type of events (All, Alarm or other). The Event State drop down is list enables the User to select state of event (All, Active or Inactive). The Event Acknowledge State drop down is list enables the User to select All, Acknowledged or Unacknowledged value and the checkbox to include grace period.

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