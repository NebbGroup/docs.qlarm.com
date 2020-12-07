---
title: "Submit Ticket"
date: 2020-09-18T15:16:37+02:00
weight: 21
---

<!-- The Modal -->
<div id="myModal" class="modal">
  <span class="close">&times;</span>
  <img class="modal-content" id="img01">
  <div id="caption"></div>
</div>

{{<lead>}}
Whenever you have an issue about Qlarm to be explained or solved, any request or info needed you can submit a [Ticket](/glossary#ticket) via Support ticket page. The "Submit Ticket" page leads you to a ticket form you need to fill in and submit and we will respond to your Ticket as soon as possible. <br />
{{</lead>}}
<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="submit_issue" src="/submit_issue.png" alt="Submit ticket">
    <figcaption>Fig 1. Submit ticket</figcaption>
</figure> 

Enter your first and last name, the email you want to get the response to and a brief subject of the issue. Describing details is optional.

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