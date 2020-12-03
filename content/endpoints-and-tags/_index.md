---
title: "Endpoints and Tags"
date: 2020-11-30T14:24:50+01:00
weight: 7
---

{{<lead>}}
PLACEHOLDER TEXT
{{</lead>}}


## Endpoints
An Endpoint is a logical representation of [OPC server](/glossary#opc-server) in the context of Qlarm environment, providing necessary data to manage an OPC server. Endpoints are the starting point of the main functional flow in the system, the messaging flow. All properties of an Endpoint should be configured to respond to the necessity of the flow. Starting from configuration of the Endpoint (its OPC server with [Tags](/glossary#tag) associated) via [Event Definitions](/glossary#event-definition) to [Events](/glossary#event) raised and [Notifications](/glossary#notification) send to [Recipients](/glossary#recipient), Endpoints are the main trade for all of these entities. Monitoring pages like Live, Events, Notifications can all be filtered by Endpoint.
