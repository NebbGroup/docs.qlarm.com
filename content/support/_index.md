---
title: "Support"
date: 2020-09-18T15:15:08+02:00
weight: 23
---

<!-- The Modal -->
<div id="myModal" class="modal">
  <span class="close">&times;</span>
  <img class="modal-content" id="img01">
  <div id="caption"></div>
</div>

{{<lead>}}
Support section is where you can ask for an information about Qlarm. This is where you can find the User Manual and Submit Ticket Form. The Chat option is also provided for this purpose.
{{</lead>}}

You can open the chat by clicking the chat button in the bottom-left corner.<img src="/chat_button.png">
<figure class="image_container">
    <img class="center_image myImg figure_resize1" onClick="reply_click(this)"  id="support_popup" src="/support_popup.png" alt="Chat">
    <figcaption>Fig 1. Chat</figcaption>
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