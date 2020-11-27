---
title: "Widget Types"
date: 2020-11-27T14:14:11+01:00
weight: 5
---

The Widget List contains eight different types of Widgets that can be added to your dashboard.

### Latest Value  <img src="/last_value_widget_logo.png" alt="last value logo" class = "logo_resize"> 
This widget shows the latest value of a selected sensor. In the “Subjects” tab you can select an [Endpoint](/glossary#endpoint) and [Tags](/glossary#tag) available from that Endpoint for which you want to see the latest value. You can also give the Widget an alias name to differ from the other Latest Value Widgets. In the “Ranges” tab you can adjust custom ranges to view the latest value in a certain colour, if it falls in that range. The “Labels” tab contains additional settings for Widget configuration.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="last_value_widget_menu" src="/last_value_widget_menu.png" alt="Last value widget menu">
    <figcaption >Fig 8. Last value widget menu</figcaption>
</figure>

### Latest Value Gauge  <img src="/last_value_gauge_widget_logo.png" alt="last value logo" class = "logo_resize"> 
This widget shows the latest value of a selected sensor using a gauge with custom range values and colours. In the “Subjects” tab you can select an Endpoint and Tags available from that Endpoint for which you want to see the latest value. You can also give the Widget an alias name to differ from the other Latest Value Gauge Widgets. In the “Ranges” tab you can adjust the appearance of the gauge. First you need to set the minimum and maximum value and the base colour of the scale. Then you can add custom ranges on the scale to view the latest value in a certain colour, if it falls in that range. The “Labels” tab contains additional settings for Widget configuration.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="latest_value_gauge_widget_menu" src="/latest_value_gauge_widget_menu.png" alt="Last value gauge widget menu">
    <figcaption >Fig 9. Last value gauge widget menu</figcaption>
</figure>

### Tag State  <img src="/tag_state_widget_logo.png" alt="last value logo" class = "logo_resize"> 
This widget shows the state of a selected sensor by setting custom range values and different colours. In the “Subjects” tab you can select an Endpoint and Tags available from that Endpoint for which you want to see the Tag State. You can also give the Widget an alias name to differ from the other Latest Value Widgets. In the “States” tab you can adjust custom ranges to view the Tag State in a certain colour, if it falls in that range. The “Labels” tab contains additional settings for Widget configuration.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="tag_state_widget_menu" src="/tag_state_widget_menu.png" alt="Tag state widget menu">
    <figcaption >Fig 10. Tag State widget menu</figcaption>
</figure>

### Tag Chart  <img src="/tag_chart_widget_logo.png" alt="last value logo" class = "logo_resize"> 
This widget displays Tag Chart values for a selected period. In the “Subjects” tab you can select an Endpoint and Tags available from that Endpoint for which you want to see the Tag Chart. You can also give the Widget an alias name to differ from the other Latest Value Widgets. In the “Interval” tab you can adjust the unit of time, number and colour of time units. The “Labels” tab contains additional settings for Widget configuration.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="tag_chart_widget_menu" src="/tag_chart_widget_menu.png" alt="Tag chart widget menu">
    <figcaption >Fig 11. Tag Chart widget menu</figcaption>
</figure>

### Elapsed time for Endpoint 
<img src="/elapsed_time_for_endpoint_widget_logo.png" alt="last value logo" class = "logo_resize"> - displays latest log [Events](/glossary#event) from the Endpoint. In the “Subjects” tab you can select an Endpoint to see the elapsed time. In the “Data” and “Event” tabs you can add intervals with different ranges and colours that represent the “Last Data” and “Last Event”. The “Labels” tab contains additional settings for Widget configuration.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="elapsed_time_for_endpoint_widget_menu" src="/elapsed_time_for_endpoint_widget_menu.png" alt="Elapsed time for endpoint widget menu">
    <figcaption >Fig 12. Elapsed time for endpoint widget menu</figcaption>
</figure>

### Elapsed time for system 
<img src="/elapsed_time_for_system_widget_logo.png" alt="last value logo" class = "logo_resize"> - displays latest log Events in the system. Go to “Subjects” tab and select an Endpoint to see the elapsed time. In the “Data” and “Event” tabs you can add intervals with different ranges and colours to represent the “Last Data” and “Last Event”. The “Labels” tab contains additional settings for Widget configuration.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="elapsed_time_for_system_widget_menu" src="/elapsed_time_for_system_widget_menu.png" alt="Elapsed time for system widget menu">
    <figcaption >Fig 13. Elapsed time for system widget menu</figcaption>
</figure>

### Endpoint state 
<img src="/endpoint_state_widget_logo.png" alt="last value logo" class = "logo_resize"> - shows the current connection state of an Endpoint. In the “Subject” tab you can select an Endpoint to monitor its state. In the "States" tab you can add colours for the "ONLINE" and "OFFLINE" status. The "Labels" tab contains additional settings for configuring the Widget.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="endpoint_state_widget_menu" src="/endpoint_state_widget_menu.png" alt="Endpoint state widget menu">
    <figcaption >Fig 14. Endpoint state widget menu</figcaption>
</figure>

### System status 
<img src="/system_status_widget_logo.png" alt="last value logo" class = "logo_resize"> - shows the system cumulative health status for all endpoints states. Go to “Statuses” tab to add colours for the “OK”, “BROKEN” and “SYSTEM SHUTDOWN” status. The “Labels” tab contains additional settings for Widget configuration.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="system_status_widget_menu" src="/system_status_widget_menu.png" alt="System status widget menu">
    <figcaption >Fig 15. System status widget menu</figcaption>
</figure>
