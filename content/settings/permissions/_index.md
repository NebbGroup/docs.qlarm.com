---
title: "Permissions"
date: 2020-08-20T16:07:13+02:00
weight: 16
---

<!-- The Modal -->
<div id="myModal" class="modal">
  <span class="close">&times;</span>
  <img class="modal-content" id="img01">
  <div id="caption"></div>
</div>

{{<lead>}}
The "Permissions" page is used to set [Permissions](/glossary#permission) for a [Role](/glossary#role). Permissions are organization specific. This is a comfortable way to manage and control [User](/glossary#user)'s actions in the system. You can simply apply a Permission to a Role of a User and be certain that your content is secured.
{{</lead>}}

[Roles](/glossary#role) are predefined and listed in the "CHOOSE ROLE" list.
<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="choose_role_list" src="/choose_role_list.png" alt="Choose role">
    <figcaption>Fig 1. Choose Role</figcaption>
</figure>

Permissions names mainly correspond to the application [Site Menu Items](/glossary#site-menu-items), and they refer to these pages and their functionalities. But sections or functionalities other than pages can be also set under permission like [Scopes](/glossary#scope), or Acknowledge of Event. After (de)selecting Permissions for a chosen Role, the Role can be saved by clicking the "Save changes" button <img src="/save_changes_button.png" >

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="permissions" src="/permissions.png" alt="Permissions">
    <figcaption>Fig 2. Permissions</figcaption>
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