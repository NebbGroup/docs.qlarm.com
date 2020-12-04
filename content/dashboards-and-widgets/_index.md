---
title: "Dashboards and Widgets"
date: 2020-11-27T14:13:47+01:00
weight: 2
---
<!-- The Modal -->
<div id="myModal" class="modal">
  <span class="close">&times;</span>
  <img class="modal-content" id="img01">
  <div id="caption"></div>
</div>

{{<lead>}}
Dashboards provide easy-to-read, easy access, real-time information about sensor values and process states which make the detection of both desired and undesired behaviors easier.
When you add a dashboard, you can choose to make it a project dashboard or one specific to a team. Use dashboards to display information or status about the project or when you want to control who can edit the dashboard. Use team dashboards to focus information specific to a team.

Qlarm Dashboards are designed to display custom Dashboards along with various configured widgets. It is highly flexible and enables you to create your own dashboards and share between other dashboard viewers. Qlarm comes with a variety of configurable Widgets that you can use to build a specific Dashboard view that meets the different needs of your business. They provide you real-time monitoring of sensor values with configurable states which makes the detection of desired on undesired behaviors much more easier.
{{</lead>}}

Access the dashboards by clicking "Dashboards" in the left-hand menu.

<figure class="image_container">
    <img class="center_image figure_resize1" onClick="reply_click(this)"  id="dashboard_menu" src="/dashboard_menu.png" alt="Dashboard left-hand menu option">
    <figcaption>Fig 1. Dashboard left-hand menu option</figcaption>
</figure>

Get started quickly by learning how to 

* [View and share dashboards](/dashboards-and-widgets/view-and-share-dashboard)
* [Create your first dashboard](/dashboards-and-widgets/create-rename-and-delete-dashboard)
* [Add widgets to your dashboards](/dashboards-and-widgets/add-widget-to-dashboard).

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