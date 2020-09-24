---
title: "Users"
date: 2020-08-20T16:07:05+02:00
weight: 15
---

<!-- The Modal -->
<div id="myModal" class="modal">
  <span class="close">&times;</span>
  <img class="modal-content" id="img01">
  <div id="caption"></div>
</div>

{{<lead>}}
The Users tab lists all the users in the system. <br />
{{</lead>}}
<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="users" src="/users.png" alt="Users">
    <figcaption>Fig 1. Users</figcaption>
</figure>

A user can be added, edited or deleted. You can search users by name and filter them by role.
<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="filter_users_role_filter" src="/filter_users_role_filter.png" alt="Search and filter users">
    <figcaption>Fig 2. Search and filter users</figcaption>
</figure>

## Add user

If we click the <img src="/add_user_button.png"> button a popup appears. All the fields in the popup are required to save the user. You need to insert first and last name, phone number, select a role that is available for the organization, also insert an email with a domain that is available for the organization and password with a required complexity. The email and password combination will be the new account credentials for the user to login with in the system. <br />
Scopes we add to the user (see Fig 3.) determine the data that will be visible to the user. E.g. endpoints are listed and selecting one for a user makes all the data related to that endpoint such as tags, events, notifications, dashboards e.t.c. will be visible for the user.<br/> 
After we fill the data we click "Save" button <img src="/user_save.png"> to save the user.

<figure class="image_container">
    <img class="center_image myImg figure_resize2" onClick="reply_click(this)"  id="user_scopes" src="/user_scopes.png" alt="Scopes">
    <figcaption>Fig 3. Scopes</figcaption>
</figure>

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="add_user_popup" src="/add_user_popup.png" alt="Add user">
    <figcaption>Fig 4. Add user</figcaption>
</figure>

## Edit user
To edit the user, click the <img src="/row_edit_button.png"> button on the user row. Scopes for the user can be edited. Name, email and mobile cannot be edited when the user is synchronized with the external active directory. Roles can be edited if the user account email domain belongs to the organization domains.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="edit_user" src="/edit_user.png" alt="Edit user">
    <figcaption>Fig 5. Edit user</figcaption>
</figure>

## Delete user
If the user account email domain belongs to the organization domains, then the <img src="/row_delete_button.png"> is provided. If clicked a confirmation popup will appear. If confirmed, the user will be deleted.
<figure class="image_container">
    <img class="center_image myImg figure_resize1" onClick="reply_click(this)"  id="user_delete_popup" src="/user_delete_popup.png" alt="Delete user">
    <figcaption>Fig 6. Delete user</figcaption>
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