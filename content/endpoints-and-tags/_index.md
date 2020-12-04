---
title: "Endpoints and Tags"
date: 2020-11-30T14:24:50+01:00
weight: 7
---

{{<lead>}}
Endpoints are the portals through which the data from your system enter the Qlarm system. Tags are the individual representations of your data, e.g. a temperature sensor reading or a valve position. 
{{</lead>}}

Learn how to 
* [Configure your endpoints.](/endpoints-and-tags/configure-endpoints/)
* [View all the tags in your system.](/endpoints-and-tags/view-tags/)

## Endpoints
An endpoint is a logical representation of a communications server. In the context of the Qlarm environment, the endpoint provides necessary data to manage an OPC server. Endpoints are the starting point of the main functional and messaging flow into the system. All properties of an Endpoint should be configured to respond to the necessity of the flow. Starting from configuration of the Endpoint (its OPC server with [Tags](/glossary#tag) associated) via [Event Definitions](/glossary#event-definition) to [Events](/glossary#event) raised and [Notifications](/glossary#notification) send to [Recipients](/glossary#recipient), Endpoints are the main trade for all of these entities. Monitoring pages like Live, Events, Notifications can all be filtered by Endpoint.
