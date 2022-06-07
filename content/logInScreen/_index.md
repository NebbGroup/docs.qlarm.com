---
title: "Log In Screen"
date: 2020-08-20T15:28:26+02:00
weight: 1
pre: ""
---

<div id="myModal" class="modal">
  <span class="close">&times;</span>
  <img class="modal-content" id="img01">
  <div id="caption"></div>
</div>

{{<lead>}}
The log in screen allows the users to accomplish the following three actions:
1.	Log In with their email account by filling in their email and password and clicking the Log In button.
2.	Log In using their Azure AD authentication by clicking on the Enterprise Log In button.
3.	Sign Up for a trial of Qlarm on a specific Trial environment by creating a new trial account.
{{</lead>}}

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="users" src="/LogInScreen.png" alt="Log In Screen">
    <figcaption>Fig 1. Log In Screen</figcaption>
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
