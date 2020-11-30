---
title: "Create, Rename and Delete Dashboard"
date: 2020-11-27T14:11:30+01:00
weight: 3
---

{{<lead>}}
Qlarm [Dashboards](/glossary#dashboard) are designed to display the custom Dashboards along with various configured [Widget](/glossary#widget). It is highly flexible and enables you to create your own Dashboards and share between other Dashboard viewers. Qlarm comes with a variety of configurable Widgets that you can use to build a specific Dashboard view that meets the different needs of your business. They provide you real-time monitoring of sensor values with configurable states which makes the detection of desired on undesired behaviors much more easier.
{{</lead>}}

<br>
<br>
Dashboards provide easy-to-read, easy access, real-time information about sensor values and process states which makes the detection of both desired and undesired behaviors easier.

When you add a dashboard, you can choose to make it a project dashboard or one specific to a team. Use project dashboards to display information or status about the project or when you want to control who can edit the dashboard. Use team dashboards to focus information specific to a team.


Project dashboards are owned by the person that created the dashboard. The owner can set permissions as to who can edit the dashboard. Team dashboards are owned by team administrators and can be edited by any member of the team. All dashboards can be viewed by members of the project. All widgets available to team dashboards are available for project dashboards. For team-specific widgets, if you aren't able to select a team through the widget, then the team defaults to the default project team.

When a project is first created, a default team and default team dashboard is created. You can customize this default dashboard by adding widgets. Each widget provides access to one or more features or functions. To learn more about each widget, see the [Widget types](/dashboards-and-widgets/widget-types).

### Configure header
Adding a new dashboard starts with entering the dashboard configuration mode in the Dashboard View
The configuration header contains the main functionalities that allow you to configure Dashboards to your needs. In view mode, you can view different Dashboards that are available, and you can change them from the "Dashboards" dropdown list. You can enter edit mode by clicking the <img src="/configure_button.png" alt="Configure Button"> button.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="configure_header_view_mode" src="/configure_header_view_mode.png" alt="Configure header in view mode">
    <figcaption>Fig 2. Configure header in view mode</figcaption>
</figure>

Once you have entered configuration mode, the configuration header will change to present the different functionalities available for managing dashboards. 

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="configure_header_edit_mode" src="/configure_header_edit_mode.png" alt="Configure header in edit mode">
    <figcaption>Fig 3. Configure header in edit mode</figcaption>
</figure>


### Dashboard configuration

The right cluster of buttons contains the main functionalities for configuring the Dashboard you are working on.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="button_cluster" src="/button_cluster.png" alt="Configure functionalities for dashboard" style="width: 45%;">
    <figcaption>Fig 4. Configure functionalities for dashboard</figcaption>
</figure>

### New Dashboard

The "New Dashboard" button <img src="/new_dashboard_button.png" alt="New Dashboard button"> allows you to create a new Dashboard. When you go to New Dashboard, a new window opens to configure your new Dashboard. You can select a name for it under the "Dashboard Name" field and add custom Widgets.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="add_widgets_mode" src="/add_widgets_mode.png" alt="Creating a new dashboard">
    <figcaption >Fig 5. Creating a new dashboard</figcaption>
</figure>




### Save Dashboard

To keep the changes in the Dashboard you can save the configurations by clicking on the <img src="/save_button1.png" alt="save button"> button.

### Discard Dashboard

The <img src="/discard_changes_button.png" alt="discard changes button"> button discards all the applied changes you did in the Dashboard you are configuring.

### Delete Dashboard

The <img src="/delete_dashboard_button.png" alt="delete dashboard button"> button deletes the selected Dashboard that you have configured.

### Copy Dashboard

Whenever you are viewing a Dashboard created by another User, you can copy the existing Dashboard by clicking on the <img src="/copy_button.png" alt="copy button"> button. This will ask you if you want to rename the Dashboard and save the copy as your own after clicking the <img src="/user_save.png" alt="save button"> button.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="save_dashboard_copy" src="/save_dashboard_copy.png" alt="Save copy of dashboard">
    <figcaption >Fig 16. Save copy of dashboard</figcaption>
</figure>

### Exit Dashboard

The <img src="/exit_button.png" alt="exit button"> button allows us to leave the edit mode and get back to the view mode.

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