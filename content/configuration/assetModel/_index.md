---
title: "Asset Model"
date: 2020-08-20T15:54:44+02:00
weight: 13
---

<!-- The Modal -->
<div id="myModal" class="modal">
  <span class="close">&times;</span>
  <img class="modal-content" id="img01">
  <div id="caption"></div>
</div>

{{<lead>}}
Asset Model is a platform that enables the creation of twin graphs based on digital models of entire environments, which could be markets, buildings, factories, farms, energy networks, railways, stadiums, and more—even entire cities. These digital models can be used to gain insights that drive better products, optimized operations, reduced costs, and breakthrough customer experiences.
{{</lead>}}

## Overview

Asset Model can be used to design a digital twin architecture that represents actual IoT devices, and which connects to IoT Hub device twins to send and receive live data.
Take advantage of your domain expertise on top of Asset Model to build customized, connected solutions that:

- You can model your environment and bring asset twins to life in a scalable and secure manner
- You can Connect assets such as IoT devices
- With uses of Asset Model, you can connect your business logic and data processing

A sample architecture of a complete solution using Asset Model may contain the following components:
- This service stores your twin models and your twin graph with its state.
- With Asset Model instance you can configure models, create topology, and extract insights from the twin graph.
- One or more external compute resources to process events generated by Asset Model or connected data sources such as devices.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="dashboard" src="/assetModel.png" alt="Asset model">
    <figcaption>Fig 1. Asset Model</figcaption>
</figure>

## Functionalities

The Assets Page provides a flexible and organized asset model for visualizing your graphs. Every node’s data can be displayed in the JSON editor, where users can see all the properties and their values. Also, users can preview the models, add new Assets, export the graph, manipulate with the graph and add new custom properties.

### Model

Models menu by default is hidden. In order to view Models, click this button <img src="/hideModelsMenu.png" alt="Hide Models Menu"> in the top left corner. In order to hide the Models click again on the same button.

### Download Models

User can download all models provided (Asset and Tag models), in JSON file, by clicking <img src="/downloadAllModels.png" alt="Download All Models"> Download models button.

### Create asset

User can create new asset by clicking <img src="/createNewAsset.png" alt="Create New Asset"> Create an asset button. After click, a popup form appears. ‘Name’ is a required field. After clicking Add, the newly created Asset will be displayed in the graph. Name of the new asset should be unique.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="button_cluster" src="/createNewAssetPopUp.png" alt="Create New Asset Pop Up" style="width: 25%;">
    <figcaption>Fig 2. Create New Asset Pop Up</figcaption>
</figure>

### Upload model image

By clicking the Upload model image button <img src="/uploadModelImage.png" alt="Upload Model Image">, user can upload an image for Asset or Tag and the main node will be replaced with the uploaded image. Uploaded images can be replaced or deleted.

### View Model

User can preview model in JSON format by clicking View Model button <img src="/previewModel.png" alt="Preview Model">.

### Asset Graph

In the Asset Graph are displayed all Assets and Tags with their relations. Assets and Tags nodes are displayed with different colors, to be distinct. Relations are also displayed with two colors, because there are two different types of relations, contains asset and contains tag. 

### Options for the whole graph

User can Zoom in, Zoom out, Zoom to Fit, Center and Filter the graph, by clicking these buttons placed in the bottom left corner of the Assets page. 

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="button_cluster" src="/graphOptions.png" alt="Graph Options" style="width: 6%;">
    <figcaption>Fig 3. Graph Options</figcaption>
</figure>

Users can export the graph in JSON file by clicking the Export Graph button <img src="/exportGraph.png" alt="Export Graph"> placed on the top of the page. 
Users can view the whole graph, if some of the nodes or relations are hidden previously, by clicking the View All button <img src="/viewAllRelationships.png" alt="View All Relationships"> placed on the top of the page. In order to see the hidden relations from the graph you should click on the Show All Relationships button <img src="/showAllRelationships.png" alt="Show All Relationships">. 

### Layouts

Layouts provide a mechanism for automatically positioning nodes in a graph. Default layouts include Cola, Dagre, fCoSE and Klay. User can choose preferred layout from the drop-down menu.

### Context menu

In the graph there are context menus around nodes, which can be displayed by selecting some node and right click on the node or just right click on the node, after that the context menu with filters and actions is displayed.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="button_cluster" src="/assetContextMenu.png" alt="Asset Context Menu" style="width: 20%;">
    <figcaption>Fig 4. Asset Context Menu</figcaption>
</figure>


In the asset context menu, there are several options for Filters and Actions.

## Filters

In the Filtering options if user clicks on <b>Show of type</b>, it will filter all nodes with the same type as the selected one. By clicking <b>Show of model</b>, it will filter all nodes with the same model as the selected one. 
By clicking <b>Show selected</b> it will show only the selected node and hide all other nodes. By clicking <b>Show selected + Children</b> it will filter only the selected node(s) and nodes below selected node(s). By clicking <b>Hide selected</b> it will hide the selected node(s) and its relationship(s) (if it has one). By clicking <b>Hide selected + Children</b> it will hide the selected nodes(s), all the nodes below them and their relationships.

## Actions

### Edit Asset

By clicking Edit asset action opens the editor on the right side of the screen.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="button_cluster" src="/editAssetActions.png" alt="Edit Asset Actions" style="width: 35%;">
    <figcaption>Fig 5. Edit Asset Actions</figcaption>
</figure>


In the editor, for the selected asset or tag, are displayed all properties and their latest values.
User can edit only the displayName, name, description and type properties of the selected tag or asset. In order to save the changes, user should click Save Asset button <img src="/saveAssetButton.png" alt="Save Asset Button">.


### Delete Asset(s)

By clicking Delete asset(s), confirmation pop-up is displayed, after clicking Yes selected Asset(s) and its relationships will be deleted and the graph will be updated. 
Note: Delete asset(s) action is only available for Asset nodes.

### Get Relationships

In order to see information about incoming and outgoing relationships for selected node, you should click Get relationships from the Context menu. 

## Relationship context menu

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="button_cluster" src="/relationshipContextMenu.png" alt="Relationship Context Menu" style="width: 35%;">
    <figcaption>Fig 6. Relationship Context Menu</figcaption>
</figure>

### Filters

By clicking Hide relationship it will hide the selected relationship. By clicking Hide relationships of type it will hide all the relationships of the same type as the selected one.

### Delete Relationship(s)

In order to delete relationship(s) you should click on the Delete relationship(s) option from the context menu. In order to delete multiple relationships at once you should select them by pressing Ctrl + Left click and select all the desired relationships. After deleting relationship(s) the graph will be updated. 

### Add Relationships

In order to add relationship between nodes, at first you should select the parent node, than press Ctrl, than select the child node and then Right click on the child node. After that the context menu will be displayed with Add relationships option. After clicking the option, a modal is displayed:

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="button_cluster" src="/createRelationship.png" alt="Create Relationship" style="width: 25%;">
    <figcaption>Fig 7. Create Relationship</figcaption>
</figure>

In the Create relationship modal there is information about the Source ID (parent node ID) and Target ID (child node ID). In the Relationship dropdown you can choose the relationship type. If you are adding relationship between Assets, you can choose relationship of type ‘contains asset’. If you are adding relationship between Asset and Tag, you can choose relationship of type ‘contains tag’. After clicking Save the graph will be updated.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="button_cluster" src="/containsAsset.png" alt="Contains Asset" style="width: 20%;">
    <figcaption>Fig 8. Contains Asset</figcaption>
</figure>

Note: Add relationships action is only available when user wants to add relationship between Asset -> Tag and Asset -> Asset.

## Editor

Editor by default is hidden. In order to open it you should select some node and click Edit asset. In order to close it, you should click this button <img src="/hideEditor.png" alt="Hide Editor">.

## Add properties

In order to add some custom property to some Asset or Tag, you should click Add properties <img src="/addProperties.png" alt="Add Properties">. 

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="button_cluster" src="/assetCustomProperties.png" alt="Asset Custom Properties" style="width: 20%;">
    <figcaption>Fig 9. Asset Custom Properties</figcaption>
</figure>

In the pop-up modal you should enter the name of the new property and then click Add. Newly added properties are displayed above the field, and they can also be removed. After clicking Save, the newly created properties will be displayed in the editor and then you should click <img src="/saveAssetProperties.png" alt="Save Asset Properties"> in order to save the Asset or Tag with the new properties.

## Filter/Highlight the graph

The first option for filtering the graph is explained in the Context menu part. 
The second option for filtering the graph is by clicking Filter/Highlight button  <img src="/filterButton.png" alt="Filter Button">. 
In the Filter and Highlight sub-menus there is a field in which users can add terms to filter/highlight the graph. Terms can be removed or disabled by clicking the toggle button. Filtering will display only those nodes where there is a matching term and highlighting will highlight the matching nodes. The option Add Outgoing Relationships is selected by default, in order to deselect it you should click on the   and the pop-up will be displayed.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="button_cluster" src="/filterPopup.png" alt=" Filter Popup" style="width: 35%;">
    <figcaption>Fig 10. Filter Popup</figcaption>
</figure>

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