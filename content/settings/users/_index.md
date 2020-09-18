---
title: "Users"
date: 2020-08-20T16:07:05+02:00
weight: 16
---

{{<lead>}}
Users lists all users in the system. <br />
{{</lead>}}
<figure class="image_container">
    <img class="center_image" src="/users.png" alt="Users">
    <figcaption>Fig 1. Users</figcaption>
</figure>

User can be added, edited or deleted. 
We can search users by name and filter them by role.
<figure class="image_container">
    <img class="center_image" src="/filter_users_role_filter.png" alt="Search and filter users">
    <figcaption>Fig 2. Search and filter users</figcaption>
</figure>

## Add user
If we click on "Add user" button <img src="/add_user_button.png"> a popup will appear. All the fields in the popup are required for the user to be saved. We insert first and last name, phone, select a role that is available for the organization, also insert an email with a domain that is available for the organization and password with a required complexity. The email and pasword combination will be the new account credentials for the user to login with in the system. <br />
Scopes we add to the user (see Fig 3.) determine the data that will be visible to the user. E.g. endpoints are listed and selecting one for a user makes all the data related to that endpoint such as tags, events, notifications, dashboards e.t.c. will be visible for the user.<br/> 
After we fill the data we click "Save" button <img src="/user_save.png"> to save the user.

<figure class="image_container">
    <img class="center_image" src="/user_scopes.png" alt="Scopes">
    <figcaption>Fig 3. Scopes</figcaption>
</figure>

<figure class="image_container">
    <img class="center_image" src="/add_user_popup.png" alt="Add user">
    <figcaption>Fig 4. Add user</figcaption>
</figure>

## Edit user
User can be edited by clicking on this row button <img src="/row_edit_button.png">.
Scopes for the user can always be edited. Name, email and mobile are not editable in case of a user that is synced from external active directory. Role can be edited if the user account email domain belongs to the organization domains.

<figure class="image_container">
    <img class="center_image" src="/edit_user.png" alt="Edit user">
    <figcaption>Fig 5. Edit user</figcaption>
</figure>

## Delete user
If the user account email domain belongs to the organization domains, then the button is provided <img src="/row_delete_button.png"> and if clicked a confirmation popup will appear. If we confirm the user will be deleted.
<figure class="image_container">
    <img class="center_image" src="/user_delete_popup.png" alt="Delete user">
    <figcaption>Fig 6. Delete user</figcaption>
</figure>


