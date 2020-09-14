---
title: "Dashboard Configuration"
date: 2020-08-20T15:28:26+02:00
weight: 2
pre: "<b>1. </b>"
---

{{<lead>}}
One of the most important features of QLARM is creating custom dashboards where you can display different custom configured widgets. Every configured dashboard can be named, configured, saved, reloaded when needed, set as default and shared with other participants.
{{</lead>}}

## Overview

<div align="justify">
    At a glance, in the Dashboard View we are greeted with two components, the configuration header and display grid. The configuration header contains the important functionalities for configuring the dashboard. The display grid as it name suggest it displays the available dashboards that we selected from the configuration div and here we can configure the presentation and layout of the widgets in the dashboard. By default we are greeted with a default System Dashboard.
</div>

<figure class="image_container">
    <img class="center_image" src="/dashboard.png" alt="configure header in view mode">
    <figcaption>Fig 1. Dashboard configuration</figcaption>
</figure>

## Configure header

<div align="justify">
    The configuration header contains the main functionalities that lets us configure dashboards to our needs. In view mode we can view different dashboards that are available to us by changing them in the dashboard dropdown list. We can enter edit mode by clicking on the "Configure" button <img src="/configure_button.png" alt="Configure Button">.
</div>

<figure class="image_container">
    <img class="center_image" src="/configure_header_view_mode.png" alt="configure header in view mode">
    <figcaption>Fig 2. Configure header in view mode</figcaption>
</figure>

In edit mode the configuration header is changed by adding new functionalities so we can configure dashboards. 

<figure class="image_container">
    <img class="center_image" src="/configure_header_edit_mode.png" alt="configure header in edit mode">
    <figcaption>Fig 3. Configure header in edit mode</figcaption>
</figure>

### Dashboard list

<div align="justify">
    The Dashboard drop down list lets us select the dashboard we need to view. Here are listed all the available dashboards to view, including the default System Dashboard and other users’ dashboards that are made available for sharing. We can always filter the list to view our custom dashboards by selecting the "Mine" checkbox <img src="/mine_checkbox.png" alt="Mine checkbox">. 
</div>

### Dashboard themes

<div align="justify">
    The theme dropdown list is used to select and change the visual color of the dashboard view we are configuring. By default, the light theme is selected, but there are other themes, including the blue, dark and extra dark theme.
</div>

### Default Dashboard

<div align="justify">
Upon opening QLARM a default dashboard is always displayed. By default, a System Dashboard is set to be the default dashboard but any other dashboard that is available can be set to be the new default dashboard by selecting the "Default" checkbox <img src="/default_checkbox.png" alt="Mine checkbox">.

### Sharing a Dashboard

<div align="justify">
By checking the "Share" checkbox <img src="/share_checkbox.png" alt="Mine checkbox">, we are enabling a selected dashboard that is configured by us to be shared to the other participants in the system.
</div>

### Dashboard configuring

<div align="justify">
The right cluster of buttons contains the main functionalities for configuring the dashboard we are working on.
</div>

<figure class="image_container">
    <img class="center_image" src="/button_cluster.png" alt="configure header in edit mode" style="width: 45%;">
    <figcaption>Fig 4. Configure functionalities for dashboard</figcaption>
</figure>

### New Dashboard

<div align="justify">
The "New Dashboard" button <img src="/new_dashboard_button.png" alt="New Dashboard button"> allows us to create a new dashboard. Upon clicking it, a new window is open to configure our new dashboard by naming it in the "Dashboard Name" field and adding custom widgets. 
</div>

<figure class="image_container">
    <img class="center_image" src="/add_widgets_mode.png" alt="configure header in edit mode">
    <figcaption >Fig 5. Configure functionalities for dashboard</figcaption>
</figure>

When a widget is clicked from the list it is shown on the grid panel, here we can rearrange them by dragging and dropping the widgets at the desired location on the grid and resize them by using the widget handle <img src="/widget_handle.png" alt="widget handle"> located in the lower right angle on every widget or by dragging and dropping the edges and corners. After configuring the dashboard layout we can click the "Save" button <img src="/save_button.png" alt="save button"> to save the dashboard or the "Cancel" button <img src="/cancel_button.png" alt="cancel button"> if we do not wish to save the dashboard.

Every widget can we configured by opening the widget menu and selecting “Edit Widget”. Here a new edit widget view is opened to configure the widget. Each widget has its own unique parameter for configuration (more on this in the Widgets subsection).

<figure class="image_container">
    <img class="center_image" src="/widget_menu.png" alt="Widget details" style="width: 35%;">
    <figcaption >Fig 6. Widget components</figcaption>
</figure>

 We can saved the widget configuration by clicking the “Save” button <img src="/edit_widget_save_button.png" alt="close button">, otherwise we can close this edit window by clicking the “Close” button <img src="/edit_widget_close_button.png" alt="close button">.

<figure class="image_container">
    <img class="center_image" src="/edit_widget_menu.png" alt="Widget menu">
    <figcaption >Fig 7. Edit widget mode</figcaption>
</figure>

After configuring the widget, the Widget menu is updated with few more options, “Show Trend” and “Show Events” which are available to interact with depending on the circumstances.

<figure class="image_container">
    <img class="center_image" src="/updated_edit_widget_menu.png" alt="Widget menu" style="width: 15%;">
    <figcaption >Fig 8. Updated edit widget mode</figcaption>
</figure>

##### Widgets

The widget list contains eight different types of widgets that can be add by clicking on any of them. 

- Latest Value widget <img src="/last_value_widget_logo.png" alt="last value logo"> - shows the latest value of a desired sensor. In the "Subjects" tab we select an endpoint and tags available from that endpoint for which we wish to see the latest value. Here we can also give the widget an alias name to differ from the other Latest Value widgets. In the "Ranges" tab we adjust custom ranges with whom we will view the latest value in a certain color if it falls in that range. The "Labels" tab contains additional settings for configuring the widget.

<figure class="image_container">
    <img class="center_image" src="/last_value_widget_menu.png" alt="Widget menu">
    <figcaption >Fig 8. Last value widget menu</figcaption>
</figure>

- Latest Value Gauge - shows the latest value of a desired sensor using a gauge with custom range values and colors,
- Tag state - shows the state of a desired sensor by setting custom range values and different colors,
- Tag chart - displays tag values for a desired period with a chart,
- Elapsed time for endpoint -  displays the time since last event/data for an endpoint,
- Elapsed time for system - displays the time since last event/data for the system,
- Endpoint state - shows the current connection state of an endpoint,
- System status - shows the system cumulative health status of all endpoints states.

### Save Dashboard

When we have made all the desired configurations in the dashboard we can save it buy clicking on the "Save" button <img src="/save_button1.png" alt="save button">.

### Add Widget

The "Add Widget" button <img src="/add_widgets.png" alt="add widget button"> allows us to add additional widgets to our dashboard. By clicking the button we are greeted with the same window as if we were creating a new dashboard.

### Discard Dashboard

The  "Discard" button <img src="/discard_changes_button.png" alt="discard changes button"> discards all of the applied changes we did in the dashboard we are configuring.

### Delete Dashboard

The "Delete" button <img src="/delete_dashboard_button.png" alt="delete dashboard button">  deletes the selected dashboard that we have configured.

### Exit Dashboard

The "Exit" button <img src="/exit_button.png" alt="exit button"> allows us to leave the edit mode and get back to the view mode.

## Grid panel

The grid panel displays the configured dashboards by laying out the saved configured widgets. It is here where we can rearrange and resize each widget.







