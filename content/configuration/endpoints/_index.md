---
title: "Endpoints"
date: 2020-08-20T15:54:44+02:00
weight: 12
---

{{<lead>}}
The Endpoints configuration contains all of the accessible endpoints and their associated nodes.
{{</lead>}}

<figure class="image_container">
    <img class="center_image" src="/endpoints_configurator.png" alt="configure header in view mode">
    <figcaption>Fig 1. Endpoints configuration</figcaption>
</figure>

Upon opening the Endpoints configuration the user is greeted with a list of the accessible endpoints which can be filtered by entering a keyword in the Search Filter.

Each Endpoint is displayed with basic information: Name, Location, Status; and additional information: Date Time Format, IoT Device Name, Description, Type, Time Zone, Time Format and Number of Tags. The Date Time and Time format shows the format preference for the Date Time and Time for the notifications that show up in the Notifications View. The Time Zone shows the time zone in which the Endpoint operates. Type shows the type of the Endpoint. IoT Device Name and Descriptions may contain additional naming information for the specific Endpoint. Most of this information can be edited by clicking the <img src="/edit_button.png" alt="New Dashboard button"> button, separately for each Endpoint. You can edit Name, Date Time Format, IoT Device Name, Description, Time Zone and Time Format. Additionally, in this mode there is more information about a specific endpoint: Unique Identifier, Keywords, Update frequency, Geographical Coordinates, Geo Location and IP Address. You can also set the specific Endpoint to be the default endpoint which will enable every information associated with it to appear first in any table content. When a specific endpoint is not set as default the "Set Default" button is blank <img src="/set_default_blank.png" alt="New Dashboard button">, otherwise it is coloured <img src="/set_default_primary.png" alt="New Dashboard button">. 

<figure class="image_container">
    <img class="center_image" src="/edit_endpoint.png" alt="configure header in view mode">
    <figcaption>Fig 2. Endpoint edit mode<figcaption>
</figure>

<img src="/log_button.png" alt="New Dashboard button"> contains the logs for any changes associated with the specific Endpoint.

<figure class="image_container">
    <img class="center_image" src="/logs.png" alt="configure header in view mode">
    <figcaption>Fig 3. Endpoint logs<figcaption>
</figure>

The Status Label displays if the Endpoint is <img src="/online_status.png" alt="online status"> or <img src="/offline_status.png" alt="offline status">. 

By clicking the <img src="/tag_button.png" alt="New Dashboard button"> button the user the view the table of associated tags for that endpoint. For each known tag the table displays its Name, Description, OPC UA URL, Value Type, Precision, Deadband, Unit, Live Data View, Log View, Enable status. 

<figure class="image_container">
    <img class="center_image" src="/tags.png" alt="tags">
    <figcaption>Fig 4. Endpoint tags<figcaption>
</figure>

By clicking clicking on the <img src="/edit_recipient_button.png" alt="online status"> button we can change the actions for the specific tag listed in the table, upon witch a edit tag form appears. Also by selecting multiple tags and clicking on the <img src="/change_button.png" alt="New Dashboard button"> button we can apply changes to all of the selected tags.

<figure class="image_container">
    <img class="center_image" src="/edit_tag.png" alt="tags">
    <figcaption>Fig 5. Edit tag<figcaption>
</figure>

<figure class="image_container">
    <img class="center_image" src="/edit_tags.png" alt="tags">
    <figcaption>Fig 6. Edit selected tags<figcaption>
</figure>

The user can add a new tag by clicking on the <img src="/add_tag_button.png" alt="online status"> button, upon which an add tag form appears which requires information to be provided.

<figure class="image_container">
    <img class="center_image" src="/add_tag.png" alt="tags">
    <figcaption>Fig 7. Add tag form<figcaption>
</figure>