---
title: "Add Widget to Dashboard"
date: 2020-11-27T14:11:09+01:00
weight: 5
---

<!-- The Modal -->
<div id="myModal" class="modal">
  <span class="close">&times;</span>
  <img class="modal-content" id="img01">
  <div id="caption"></div>
</div>

Widgets can easily be added to any open Dashboard. From the Dashboards view, enter the configuration mode and click <img src="/add_widgets.png" alt="add widget button"> to open up the [widget list](/dashboards-and-widgets/widget-types). 
When you select a widget from the list, it is shown on the grid panel. To organize the widgets in the grid panel you can drag and drop them to the desired location. To resize a Widget, use the Widget handle <img src="/widget_handle.png" alt="widget handle"> located in the lower right corner on every Widget or by drag and drop edges and corners. After configuring the Dashboard layout you can click the <img src="/save_button.png" alt="save button"> button to save the Dashboard or the <img src="/cancel_button.png" alt="cancel button"> button if you do not want to save the Dashboard. Afterwards, if you need to add additional Widgets to the Dashboard, you only need to click the "Add widget" button by which you are greeted with the same window as if you were creating a new Dashboard.

All Widgets can be configured by opening the Widget Menu and selecting “Edit Widget”. An edit widget form opens for you to configure it. Every Widget has its own unique configuration parameter.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="widget_menu" src="/widget_menu.png" alt="Widget components" style="width: 35%;">
    <figcaption >Fig 1. Widget components</figcaption>
</figure>

You can save the Widget configuration by clicking the <img src="/edit_widget_save_button.png" alt="close button"> button, or you can close the edit window by clicking the <img src="/edit_widget_close_button.png" alt="close button"> button.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="edit_widget_menu" src="/edit_widget_menu.png" alt="Edit widget mode">
    <figcaption >Fig 2. Edit widget mode</figcaption>
</figure>

When the Widget configuration is complete, the Widget Menu is updated with the new options defined by the Widget.

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