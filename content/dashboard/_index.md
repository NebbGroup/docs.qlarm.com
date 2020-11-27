---
title: "Dashboard"
date: 2020-08-20T15:28:26+02:00
weight: 6
pre: ""
---

{{<lead>}}
Qlarm [Dashboards](/glossary#dashboard) are designed to display the custom Dashboards along with various configured [Widget](/glossary#widget). It is highly flexible and enables you to create your own Dashboards and share between other Dashboard viewers. Qlarm comes with a variety of configurable Widgets that you can use to build a specific Dashboard view that meets the different needs of your business. They provide you real-time monitoring of sensor values with configurable states which makes the detection of desired on undesired behaviors much more easier.
{{</lead>}}

## Overview
The Dashboard [View](/glossary#view) contains two main components, configuration header and display grid. The configuration header contains essential functionalities for Dashboard configuration which can be accessed by clicking the <img src="/configure_button.png" alt="Configure Button"> button. The display grid displays the available Dashboards that can be selected from the Dashboards list, and there you can configure the presentation and layout of the Widgets within the selected Dashboard.


<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="dashboard" src="/dashboard.png" alt="Dashboard configuration">
    <figcaption>Fig 1. Dashboard configuration</figcaption>
</figure>

<!-- The Modal -->
<div id="myModal" class="modal">
  <span class="close">&times;</span>
  <img class="modal-content" id="img01">
  <div id="caption"></div>
</div>

## Working with Dashboards

In the following sections, the two main functionalities of Qlarm Dashboards are explained:

- Viewing Dashboards
- Managing Dashboards

## Viewing Dashboards

### Default Dashboard

Upon logging into Qlarm a [Default Dashboard](/glossary#default-dashboard) is displayed. The Default Dashboard at first login is the "System Dashboard", but any other Dashboard that is available can be selected to be the new Default Dashboard by checking the "Default" checkbox <img src="/default_checkbox.png" alt="default checkbox">.


### Dashboard list
The "Dashboards" dropdown list allows you to select the Dashboard you want to view. All the available Dashboards are listed here, including the default "System Dashboard" and other Dashboards that are shared by other [Users](/glossary#user). You can always filter the list to view the custom Dashboards that are predefined in the system by checking "Mine" checkbox <img src="/mine_checkbox.png" alt="mine checkbox">. 


### Dashboard themes
The "Theme" dropdown list is used to select and change the visual colour of the Dashboard you are choosing to configure. By default, the light theme is selected, other themes, include the blue, dark and extra dark theme.


### Sharing a Dashboard
By checking the "Share" checkbox <img src="/share_checkbox.png" alt="share checkbox">, you can enable a selected Dashboard that you configured and share it with the other Users.


## Managing Dashboards

### Configure header
The configuration header contains the main functionalities that allow you to configure Dashboards to your needs. In view mode, you can view different Dashboards that are available, and you can change them from the "Dashboards" dropdown list. You can enter edit mode by clicking the <img src="/configure_button.png" alt="Configure Button"> button.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="configure_header_view_mode" src="/configure_header_view_mode.png" alt="Configure header in view mode">
    <figcaption>Fig 2. Configure header in view mode</figcaption>
</figure>

In edit mode the configuration header is changed by adding new functionalities so you can configure Dashboards. 

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

### New Dashboard and Add Widgets

The "New Dashboard" button <img src="/new_dashboard_button.png" alt="New Dashboard button"> allows you to create a new Dashboard. When you go to New Dashboard, a new window opens to configure your new Dashboard. You can select a name for it under the "Dashboard Name" field and add custom Widgets.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="add_widgets_mode" src="/add_widgets_mode.png" alt="Creating a new dashboard">
    <figcaption >Fig 5. Creating a new dashboard</figcaption>
</figure>

When you select a Widget from the list, it is shown on the grid panel. To organize the widgets in the grip panel you can drag and drop them to the desired location and order. To resize a Widget, use the Widget handle <img src="/widget_handle.png" alt="widget handle"> located in the lower right corner on every Widget or by drag and drop edges and corners. After configuring the Dashboard layout you can click the <img src="/save_button.png" alt="save button"> button to save the Dashboard or the <img src="/cancel_button.png" alt="cancel button"> button if you do not want to save the Dashboard. Afterwards, if you need to add additional Widgets to the Dashboard, you only need to click the <img src="/add_widgets.png" alt="add widget button"> button by which you are greeted with the same window as if you were creating a new Dashboard.

All Widgets can be configured by opening the Widget Menu and selecting “Edit Widget”. An edit widget form opens for you to configure it. Every Widget has its own unique configuration parameter (more on this in the Widgets subsection).

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="widget_menu" src="/widget_menu.png" alt="Widget components" style="width: 35%;">
    <figcaption >Fig 6. Widget components</figcaption>
</figure>

You can save the Widget configuration by clicking the <img src="/edit_widget_save_button.png" alt="close button"> button, or you can close the edit window by clicking the <img src="/edit_widget_close_button.png" alt="close button"> button.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="edit_widget_menu" src="/edit_widget_menu.png" alt="Edit widget mode">
    <figcaption >Fig 7. Edit widget mode</figcaption>
</figure>

When the Widget configuration is complete, the Widget Menu is updated with the new options defined by the Widget.


### Widgets
The Widget List contains eight different types of Widgets that can be added one by one from the list.

- Latest Value Widget <img src="/last_value_widget_logo.png" alt="last value logo" class = "logo_resize"> - shows the latest value of a selected sensor. In the “Subjects” tab you can select an [Endpoint](/glossary#endpoint) and [Tags](/glossary#tag) available from that Endpoint for which you want to see the latest value. You can also give the Widget an alias name to differ from the other Latest Value Widgets. In the “Ranges” tab you can adjust custom ranges to view the latest value in a certain colour, if it falls in that range. The “Labels” tab contains additional settings for Widget configuration.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="last_value_widget_menu" src="/last_value_widget_menu.png" alt="Last value widget menu">
    <figcaption >Fig 8. Last value widget menu</figcaption>
</figure>

- Latest Value Gauge <img src="/last_value_gauge_widget_logo.png" alt="last value logo" class = "logo_resize"> - shows the latest value of a selected sensor using a gauge with custom range values and colours. In the “Subjects” tab you can select an Endpoint and Tags available from that Endpoint for which you want to see the latest value. You can also give the Widget an alias name to differ from the other Latest Value Gauge Widgets. In the “Ranges” tab you can adjust the appearance of the gauge. First you need to set the minimum and maximum value and the base colour of the scale. Then you can add custom ranges on the scale to view the latest value in a certain colour, if it falls in that range. The “Labels” tab contains additional settings for Widget configuration.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="latest_value_gauge_widget_menu" src="/latest_value_gauge_widget_menu.png" alt="Last value gauge widget menu">
    <figcaption >Fig 9. Last value gauge widget menu</figcaption>
</figure>

- Tag State <img src="/tag_state_widget_logo.png" alt="last value logo" class = "logo_resize"> - shows the state of a selected sensor by setting custom range values and different colours. In the “Subjects” tab you can select an Endpoint and Tags available from that Endpoint for which you want to see the Tag State. You can also give the Widget an alias name to differ from the other Latest Value Widgets. In the “States” tab you can adjust custom ranges to view the Tag State in a certain colour, if it falls in that range. The “Labels” tab contains additional settings for Widget configuration.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="tag_state_widget_menu" src="/tag_state_widget_menu.png" alt="Tag state widget menu">
    <figcaption >Fig 10. Tag State widget menu</figcaption>
</figure>

- Tag Chart <img src="/tag_chart_widget_logo.png" alt="last value logo" class = "logo_resize"> - displays Tag Chart values for a selected period. In the “Subjects” tab you can select an Endpoint and Tags available from that Endpoint for which you want to see the Tag Chart. You can also give the Widget an alias name to differ from the other Latest Value Widgets. In the “Interval” tab you can adjust the unit of time, number and colour of time units. The “Labels” tab contains additional settings for Widget configuration.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="tag_chart_widget_menu" src="/tag_chart_widget_menu.png" alt="Tag chart widget menu">
    <figcaption >Fig 11. Tag Chart widget menu</figcaption>
</figure>

- Elapsed time for Endpoint <img src="/elapsed_time_for_endpoint_widget_logo.png" alt="last value logo" class = "logo_resize"> - displays latest log [Events](/glossary#event) from the Endpoint. In the “Subjects” tab you can select an Endpoint to see the elapsed time. In the “Data” and “Event” tabs you can add intervals with different ranges and colours that represent the “Last Data” and “Last Event”. The “Labels” tab contains additional settings for Widget configuration.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="elapsed_time_for_endpoint_widget_menu" src="/elapsed_time_for_endpoint_widget_menu.png" alt="Elapsed time for endpoint widget menu">
    <figcaption >Fig 12. Elapsed time for endpoint widget menu</figcaption>
</figure>

- Elapsed time for system <img src="/elapsed_time_for_system_widget_logo.png" alt="last value logo" class = "logo_resize"> - displays latest log Events in the system. Go to “Subjects” tab and select an Endpoint to see the elapsed time. In the “Data” and “Event” tabs you can add intervals with different ranges and colours to represent the “Last Data” and “Last Event”. The “Labels” tab contains additional settings for Widget configuration.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="elapsed_time_for_system_widget_menu" src="/elapsed_time_for_system_widget_menu.png" alt="Elapsed time for system widget menu">
    <figcaption >Fig 13. Elapsed time for system widget menu</figcaption>
</figure>

- Endpoint state <img src="/endpoint_state_widget_logo.png" alt="last value logo" class = "logo_resize"> - shows the current connection state of an Endpoint. In the “Subject” tab you can select an Endpoint to monitor its state. In the "States" tab you can add colours for the "ONLINE" and "OFFLINE" status. The "Labels" tab contains additional settings for configuring the Widget.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="endpoint_state_widget_menu" src="/endpoint_state_widget_menu.png" alt="Endpoint state widget menu">
    <figcaption >Fig 14. Endpoint state widget menu</figcaption>
</figure>

- System status <img src="/system_status_widget_logo.png" alt="last value logo" class = "logo_resize"> - shows the system cumulative health status for all endpoints states. Go to “Statuses” tab to add colours for the “OK”, “BROKEN” and “SYSTEM SHUTDOWN” status. The “Labels” tab contains additional settings for Widget configuration.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="system_status_widget_menu" src="/system_status_widget_menu.png" alt="System status widget menu">
    <figcaption >Fig 15. System status widget menu</figcaption>
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