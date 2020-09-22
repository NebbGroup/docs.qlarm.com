---
title: "Users"
date: 2020-08-20T16:07:05+02:00
weight: 15
---

{{<lead>}}
The Users page lists all the users in the system. <br />
{{</lead>}}
<figure class="image_container">
    <img class="center_image" src="/users.png" alt="Users">
    <figcaption>Fig 1. Users</figcaption>
</figure>

User can be added, edited or deleted. 
You can search users by name and filter them by role.
<figure class="image_container">
    <img class="center_image" src="/filter_users_role_filter.png" alt="Search and filter users">
    <figcaption>Fig 2. Search and filter users</figcaption>
</figure>

## Add user
If you click the "Add user" button <img src="/add_user_button.png"> a popup opens. All the fields in the popup are required to save the user. You need to fill out information for first and last name and a phone number. Select a role in the organization, use one of the organization’s email domains and password with the required complexity. The email and password combination will be the new account credentials for the user to login with in the system. <br />
Scopes you added for the user (see Fig 3.) determine the data that will be visible to the user. For instance,  selecting one endpoint for a user makes all the data related to that endpoint such as tags, events, notifications, dashboards, etc. visible for the user.<br/> 
After filling out the required data, click the "Save" button <img src="/user_save.png"> to save the user.

<figure class="image_container">
    <img class="center_image" src="/user_scopes.png" alt="Scopes">
    <figcaption>Fig 3. Scopes</figcaption>
</figure>

<figure class="image_container">
    <img class="center_image" src="/add_user_popup.png" alt="Add user">
    <figcaption>Fig 4. Add user</figcaption>
</figure>

## Edit user
To edit the user, click the <img src="/row_edit_button.png"> button on the user row. Scopes for the user can be edited. Name, email and mobile cannot be edited when the user is synchronized with the external active directory. Roles can be edited if the user account email domain belongs to the organization domains.

<figure class="image_container">
    <img class="center_image" src="/edit_user.png" alt="Edit user">
    <figcaption>Fig 5. Edit user</figcaption>
</figure>

## Delete user
If the user account email domain belongs to the organization domains, then the <img src="/row_delete_button.png"> is provided. If clicked a confirmation popup will appear. If confirmed, the user will be deleted.
<figure class="image_container">
    <img class="center_image" src="/user_delete_popup.png" alt="Delete user">
    <figcaption>Fig 6. Delete user</figcaption>
</figure>


