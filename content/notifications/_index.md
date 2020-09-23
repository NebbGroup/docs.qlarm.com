---
title: "Notifications"
date: 2020-08-20T15:30:25+02:00
weight: 7
pre: ""
---

<!-- The Modal -->
<div id="myModal" class="modal">
  <span class="close">&times;</span>
  <img class="modal-content" id="img01">
  <div id="caption"></div>
</div>

{{<lead>}}
Notifications view lets us view and filter all of the generated notifications.
{{</lead>}}

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="notifications_view" src="/notifications_view.png" alt="Notifications">
    <figcaption >Fig 1. Notifications</figcaption>
</figure>

The table lists all of the notifications sent to the recipients with their name, type, status, date and recipient information. Using the "Notification Type" drop down list we can filter the notifications by their type (SMS, call, email, push notification). The "Time Filter" drop down list lets us filter the table by the time of the notification. By pressing the <img src="/options_button.png" alt="last value logo" class = "logo_resize"> button we can further input detail for the time filter.

<figure class="image_container">
    <img class="center_image myImg figure_resize2" onClick="reply_click(this)"  id="time_filer_options" src="/time_filer_options.png" alt="Time period filter">
    <figcaption >Fig 2. Time period filter</figcaption>
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


// Get the <span> element that closes the modal
var span = document.getElementsByClassName("close")[0];

// When the user clicks on <span> (x), close the modal
span.onclick = function() { 
  modal.style.display = "none";
}
</script>