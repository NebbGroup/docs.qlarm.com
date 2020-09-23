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
The General settings allows you to change the logo of the application that appears in the right corner of every page, so that the organization can have a more personal experience.
{{</lead>}}

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="general_settings" src="/general_settings.png" alt="General settings">
    <figcaption >Fig 1. General settings</figcaption>
</figure>

Click the button to upload  the company logo to personalize QLARM. The QLARM logo is used by default.

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