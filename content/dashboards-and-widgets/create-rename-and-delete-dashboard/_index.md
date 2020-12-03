---
title: "Create, Rename and Delete Dashboard"
date: 2020-11-27T14:11:30+01:00
weight: 4
---

<!-- The Modal -->
<div id="myModal" class="modal">
  <span class="close">&times;</span>
  <img class="modal-content" id="img01">
  <div id="caption"></div>
</div>

When you log in to Qlarm for the first time, a default dashboard is created. You can customize this default dashboard by adding widgets, or create a new one. Each widget provides access to one or more features or functions. To learn more about each widget, see the [Widget types](/dashboards-and-widgets/widget-types).

### Configure header
Adding a new dashboard starts with entering the dashboard configuration mode in the Dashboard View.
The configuration header contains the main functionalities that allow you to configure Dashboards to your needs. In view mode, you can view different Dashboards that are available, and you can change them from the "Dashboards" dropdown list. You can enter edit mode by clicking the <img src="/configure_button.png" alt="Configure Button"> button.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="configure_header_view_mode" src="/configure_header_view_mode.png" alt="Configure header in view mode">
    <figcaption>Fig 1. Configure header in view mode</figcaption>
</figure>

Once you have entered configuration mode, the configuration header will change to present the different functionalities available for managing dashboards. 

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="configure_header_edit_mode" src="/configure_header_edit_mode.png" alt="Configure header in edit mode">
    <figcaption>Fig 2. Configure header in edit mode</figcaption>
</figure>


### Dashboard configuration

The right cluster of buttons contains the main functionalities for configuring the Dashboard you are working on.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="button_cluster" src="/button_cluster.png" alt="Configure functionalities for dashboard" style="width: 45%;">
    <figcaption>Fig 3. Configure functionalities for dashboard</figcaption>
</figure>

### New Dashboard

The "New Dashboard" button <img src="/new_dashboard_button.png" alt="New Dashboard button"> allows you to create a new Dashboard. When you go to New Dashboard, a new window opens to configure your new Dashboard. You can select a name for it under the "Dashboard Name" field and add custom Widgets.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="add_widgets_mode" src="/add_widgets_mode.png" alt="Creating a new dashboard">
    <figcaption >Fig 4. Creating a new dashboard</figcaption>
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
    <figcaption >Fig 5. Save copy of dashboard</figcaption>
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