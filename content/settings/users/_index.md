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
In the Users page you can list all the [Users](/glossary#user) in the system. Users are created or registered in Qlarm and they can login and use the system with authorizations. Users can belong to different organizations. Every organization provides the User specific authorizations. User can be present in the system with a corresponding [Recipient](/glossary#recipient).
{{</lead>}}
<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="users" src="/users.png" alt="Users">
    <figcaption>Fig 1. Users</figcaption>
</figure>

A User can be added, edited or deleted. You can search Users by name and filter them by [Role](/glossary#role).
<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="filter_users_role_filter" src="/filter_users_role_filter.png" alt="Search and filter users" style="width:50%">
    <figcaption>Fig 2. Search and filter users</figcaption>
</figure>

## Add user

A new user can be added to Qlarm from the Settings -> Users menu, by clicking on the Add User button. This opens a popup window where information about the new user can be entered:

- First name.
- Last name.
- Phone number.
- [Role](/glossary#role).
- [Scopes](/glossary#scope).
- Asset scopes.
- Email (email account that will be used by the new user to log in to Qlarm).
- Radio button if the user should be listed as a recipient as well.


<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="user_scopes" src="/addUser.png" alt="Add New User">
    <figcaption>Fig 3. Add New User</figcaption>
</figure>

After entering the data and clicking the Save button, the new user will receive an email on the entered email address. The email informs that he/she was added as a user to Qlarm and contains a link to the Qlarm’s Log In screen where he/she will need to enter few more information to complete the registration and to be able to log in to Qlarm.

If the email used for the new user is used for his/hers Azure Active Directory (Azure AD) authentication, then the user will be able to log in to Qlarm using Azure AD authentication as well just by clicking on Enterprise Log In button on the Qlarm’s Log In screen.

## Edit user
To edit the User, click the <img src="/row_edit_button.png"> button on the User's row. Scopes for the User can be edited. Name, email and mobile cannot be edited when the User is synchronized with the external active directory. Roles can be edited if the User Account email domain belongs to the organization domains.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="edit_user" src="/editUser.png" alt="Edit user">
    <figcaption>Fig 5. Edit user</figcaption>
</figure>

## Delete user
If the User Account email domain belongs to the organization domains, then the <img src="/row_delete_button.png"> is provided. If clicked a confirmation popup will appear. If confirmed, the User will be deleted.
<figure class="image_container">
    <img class="center_image myImg figure_resize1" onClick="reply_click(this)"  id="user_delete_popup" src="/removeUser.png" alt="Delete user">
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