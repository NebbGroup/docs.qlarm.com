---
title: "Dashboard"
date: 2020-08-20T15:28:26+02:00
weight: 2
pre: ""
---

{{<lead>}}
QLARM dashboards are designed to display the custom dashboards along with various configured widgets. It is highly flexible and enables you to create your own dashboards and share between other dashboard viewers. QLARM comes with a variety of premade configurable dashboard widgets that you can use to build a specific dashboard view that meets the different needs of your business.
{{</lead>}}


## Overview

<div align="justify">
    The Dashboard View contains two main components, configuration header and display grid. The configuration header contains essential functionalities for dashboard configuration which can be accessed by clicking the <img src="/configure_button.png" alt="Configure Button"> button. The display grid displays the available dashboards that can be selected from the dashboards list, and there you can configure the presentation and layout of the widgets within the selected dashboard.
</div>

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

In the following sections we will explain the two main functionalities of QLARM dashboards:

- Viewing Dashboards
- Managing Dashboards

## Viewing Dashboards

### Default Dashboard

<div align="justify">
Upon logging into QLARM a default dashboard is displayed. a System Dashboard is present to be the default dashboard nevertheless, any other dashboard that is available can be selected to be the new default dashboard by checking the "Default" checkbox <img src="/default_checkbox.png" alt="default checkbox">.
</div>

### Dashboard list

<div align="justify">
    The Dashboard drop down list allows you to select the dashboard you want to view. All the available dashboards are listed here, including the default System Dashboard and other dashboards that are shared by other users. You can always filter the list to view the custom dashboards that are predefined in the system by checking "Mine" checkbox <img src="/mine_checkbox.png" alt="mine checkbox">. 
</div>

### Dashboard themes

<div align="justify">
    The theme dropdown list is used to select and change the visual colour of the dashboard view you are choosing to configure. By default, the light theme is selected, other themes, include the blue, dark and extra dark theme.
</div>

### Sharing a Dashboard

<div align="justify">
By checking the "Share" checkbox <img src="/share_checkbox.png" alt="share checkbox">, you can enable a selected dashboard that you configured and share it with the other users.
</div>

## Managing Dashboards

### Configure header

<div align="justify">
    The configuration header contains the main functionalities that allow us to configure dashboards to our needs. In view mode, you can view different dashboards that are available, and you can change them from the dashboard dropdown list. You can enter edit mode by clicking the <img src="/configure_button.png" alt="Configure Button"> button.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="configure_header_view_mode" src="/configure_header_view_mode.png" alt="Configure header in view mode">
    <figcaption>Fig 2. Configure header in view mode</figcaption>
</figure>

In edit mode the configuration header is changed by adding new functionalities so we can configure dashboards. 

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="configure_header_edit_mode" src="/configure_header_edit_mode.png" alt="Configure header in edit mode">
    <figcaption>Fig 3. Configure header in edit mode</figcaption>
</figure>

</div>

### Dashboard configuring

<div align="justify">
The right cluster of buttons contains the main functionalities for configuring the dashboard you are working on.
</div>

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="button_cluster" src="/button_cluster.png" alt="Configure functionalities for dashboard" style="width: 45%;">
    <figcaption>Fig 4. Configure functionalities for dashboard</figcaption>
</figure>

### New Dashboard and Add Widgets

<div align="justify">
The "New Dashboard" button <img src="/new_dashboard_button.png" alt="New Dashboard button"> allows you to create a new dashboard. When you go to New Dashboard, a new window opens to configure your new dashboard. You can select a name for it  under the "Dashboard Name" field and add custom widgets.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="add_widgets_mode" src="/add_widgets_mode.png" alt="Creating a new dashboard">
    <figcaption >Fig 5. Creating a new dashboard</figcaption>
</figure>

When you select a widget from the list, it is shown on the grid panel. Drag and drop to rearrange widgets to the desired location on the grid and resize them by using the widget handle <img src="/widget_handle.png" alt="widget handle"> located in the lower right angle on every widget or by drag and drop edges and corners. After configuring the dashboard layout you can click the <img src="/save_button.png" alt="save button"> button to save the dashboard or the <img src="/cancel_button.png" alt="cancel button"> button if you do not want to save the dashboard. Afterwards, if we need to add additional widgets to the dashboard we only need to click the <img src="/add_widgets.png" alt="add widget button"> button by which we are greeted with the same window as if we were creating a new dashboard.

All widget can be configured by opening the widget menu and selecting “Edit Widget”. A new edit widget view opens which allows you to configure it. Every widget has its own unique configuration parameter (more on this in the Widgets subsection).

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="widget_menu" src="/widget_menu.png" alt="Widget components" style="width: 35%;">
    <figcaption >Fig 6. Widget components</figcaption>
</figure>

You can save the widget configuration by clicking the <img src="/edit_widget_save_button.png" alt="close button"> button, or you can close the edit window by clicking the <img src="/edit_widget_close_button.png" alt="close button"> button.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="edit_widget_menu" src="/edit_widget_menu.png" alt="Edit widget mode">
    <figcaption >Fig 7. Edit widget mode</figcaption>
</figure>

When the widget configuration is complete, the Widget menu is updated with the new options defined by the widget.

</div>

### Widgets
<div align="justify">
The widget list contains eight different types of widgets that can be added one by one from the list.

- Latest Value widget <img src="/last_value_widget_logo.png" alt="last value logo" class = "logo_resize"> - shows the latest value of a selected sensor. In the “Subjects” tab you can select an endpoint and tags available from that endpoint for which we want to see the latest value. You can also give the widget an alias name to differ from the other Latest Value widgets. In the “Ranges” tab you can adjust custom ranges to view the latest value in a certain colour, if it falls in that range. The “Labels” tab contains additional settings for widget configuration.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="last_value_widget_menu" src="/last_value_widget_menu.png" alt="Last value widget menu">
    <figcaption >Fig 8. Last value widget menu</figcaption>
</figure>

- Latest Value Gauge <img src="/last_value_gauge_widget_logo.png" alt="last value logo" class = "logo_resize"> - shows the latest value of a selected sensor using a gauge with custom range values and colours. In the “Subjects” tab you can select an endpoint and tags available from that endpoint for which we want to see the latest value. You can also give the widget an alias name to differ from the other Latest Value Gauge widgets. In the “Ranges” tab you can adjust the appearance of the gauge. First you need to set the minimum and maximum value and the base colour of the scale. Then you can add custom ranges on the scale to view the latest value in a certain colour, if it falls in that range. The “Labels” tab contains additional settings for widget configuration.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="latest_value_gauge_widget_menu" src="/latest_value_gauge_widget_menu.png" alt="Last value gauge widget menu">
    <figcaption >Fig 9. Last value gauge widget menu</figcaption>
</figure>

- Tag state <img src="/tag_state_widget_logo.png" alt="last value logo" class = "logo_resize"> - shows the state of a selected sensor by setting custom range values and different colours. In the “Subjects” tab we select an endpoint and tags available from that endpoint for which we want to see the tag state. You can also give the widget an alias name to differ from the other Latest Value widgets. In the “States” tab you can adjust custom ranges to view the tag state in a certain colour, if it falls in that range. The “Labels” tab contains additional settings for widget configuration.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="tag_state_widget_menu" src="/tag_state_widget_menu.png" alt="Tag state widget menu">
    <figcaption >Fig 10. Tag state widget menu</figcaption>
</figure>

- Tag chart <img src="/tag_chart_widget_logo.png" alt="last value logo" class = "logo_resize"> - displays tag chart values for a selected period In the “Subjects” tab you can select an endpoint and tags available from that endpoint which you want to see the tag chart. You can also give the widget an alias name to differ from the other Latest Value widgets. In the “Interval” tab you can adjust the unit of time, number and colour of time units. The “Labels” tab contains additional settings for widget configuration.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="tag_chart_widget_menu" src="/tag_chart_widget_menu.png" alt="Tag chart widget menu">
    <figcaption >Fig 11. Tag chart widget menu</figcaption>
</figure>

- Elapsed time for endpoint <img src="/elapsed_time_for_endpoint_widget_logo.png" alt="last value logo" class = "logo_resize"> - displays latest log events from the endpoint. In the “Subjects” tab you can select an endpoint to see the elapsed time. In the “Data” and “Event” tabs you can add intervals with different ranges and colours that represent the “Last Data” and “Last Event”. The “Labels” tab contains additional settings for widget configuration.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="elapsed_time_for_endpoint_widget_menu" src="/elapsed_time_for_endpoint_widget_menu.png" alt="Elapsed time for endpoint widget menu">
    <figcaption >Fig 12. Elapsed time for endpoint widget menu</figcaption>
</figure>

- Elapsed time for system <img src="/elapsed_time_for_system_widget_logo.png" alt="last value logo" class = "logo_resize"> - displays latest log events in the system. Go to “Subjects” tab and select an endpoint to see the elapsed time. In the “Data” and “Event” tabs you can add intervals with different ranges and colours to represent the “Last Data” and “Last Event”. The “Labels” tab contains additional settings for widget configuration.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="elapsed_time_for_system_widget_menu" src="/elapsed_time_for_system_widget_menu.png" alt="Elapsed time for system widget menu">
    <figcaption >Fig 13. Elapsed time for system widget menu</figcaption>
</figure>

- Endpoint state <img src="/endpoint_state_widget_logo.png" alt="last value logo" class = "logo_resize"> - shows the current connection state of an endpoint. In the “Subject” tab you can select an endpoint to monitor its state. In the "States" tab we add colors for the "ONLINE" and "OFFLINE" status. The "Labels" tab contains additional settings for configuring the widget.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="endpoint_state_widget_menu" src="/endpoint_state_widget_menu.png" alt="Endpoint state widget menu">
    <figcaption >Fig 14. Endpoint state widget menu</figcaption>
</figure>

- System status <img src="/system_status_widget_logo.png" alt="last value logo" class = "logo_resize"> - shows the system cumulative health status for all endpoints states. Go to “Statuses” tab to add colours for the “OK”, “BROKEN” and “SYSTEM SHUTDOWN” status. The “Labels” tab contains additional settings for widget configuration.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="system_status_widget_menu" src="/system_status_widget_menu.png" alt="System status widget menu">
    <figcaption >Fig 15. System status widget menu</figcaption>
</figure>
</div>

### Save Dashboard

To keep the changes in the dashboard we can save the configurations by clicking on the <img src="/save_button1.png" alt="save button"> button.

### Discard Dashboard

The <img src="/discard_changes_button.png" alt="discard changes button"> button discards all of the applied changes we did in the dashboard we are configuring.

### Delete Dashboard

The <img src="/delete_dashboard_button.png" alt="delete dashboard button"> button deletes the selected dashboard that we have configured.

### Copy Dashboard

<div align="justify">
Whenever you are viewing a dashboard created by another user, you can copy the existing dashboard by clicking on the <img src="/copy_button.png" alt="copy button"> button. This will ask you if you want to rename the dashboard and save the copy as your own after clicking the <img src="/user_save.png" alt="save button"> button.
</div>

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


// Get the <span> element that closes the modal
var span = document.getElementsByClassName("close")[0];

// When the user clicks on <span> (x), close the modal
span.onclick = function() { 
  modal.style.display = "none";
}
</script>