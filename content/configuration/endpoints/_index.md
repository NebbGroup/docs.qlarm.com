---
title: "Endpoints"
date: 2020-08-20T15:54:44+02:00
weight: 11
---

{{<lead>}}
The Endpoints configuration contains all of the accessible endpoints and their associated nodes.
{{</lead>}}

<figure class="image_container">
    <img class="center_image" src="/endpoints_configurator.png" alt="configure header in view mode">
    <figcaption>Fig 1. Endpoints configuration</figcaption>
</figure>

Upon opening the Endpoints configuration the user is greeted with a list of the accessible endpoints which can be filtered by entering a keyword in the Search Filter.

Each Endpoint is displayed with basic information: Name, Location, Status; and additional information: Date Time Format, IoT Device Name, Description, Type, Time Zone, Time Format and Number of Tags. The Date Time and Time format shows the format preference for the Date Time and Time for the notifications that that show up in the Notifications View. The Time Zone shows the time zone in which the endpoint operates. Type shows the type of the endpoint. IoT Device Name and Descriptions may contains additional naming information for the specific endpoint. Most of this information can be edited by clicking the <img src="/edit_button.png" alt="New Dashboard button"> by which we are in edit mode for the specific Endpoint. Here the Name, Date Time Format, IoT Device Name, Description, Time Zone and Time Format can be set or changed. Additionally in this mode there is more information about the specific endpoint: Unique Identifier, Keywords, Update frequency, Geographical Coordinates, Geo Location and IP Address. Also here we can set the specific endpoint to be the default endpoint which will enable every information associated with this endpoint appear first in any table content. When a specific endpoint is not se to default the "Set Default" button is blank <img src="/set_default_blank.png" alt="New Dashboard button">, else it is colored <img src="/set_default_primary.png" alt="New Dashboard button">. 

<figure class="image_container">
    <img class="center_image" src="/edit_endpoint.png" alt="configure header in view mode">
    <figcaption>Fig 2. Endpoint edit mode<figcaption>
</figure>

<img src="/log_button.png" alt="New Dashboard button"> contains the logs for any changes associated with the specific Endpoint.

<figure class="image_container">
    <img class="center_image" src="/logs.png" alt="configure header in view mode">
    <figcaption>Fig 3. Endpoint logs<figcaption>
</figure>

The Status Label displays if the Endpoint is <img src="/online_status.png" alt="New Dashboard button"> or <img src="/offline_status.png" alt="New Dashboard button">. 