---
title: "History"
date: 2020-08-20T15:30:16+02:00
weight: 6
pre: ""
---

<!-- The Modal -->
<div id="myModal" class="modal">
  <span class="close">&times;</span>
  <img class="modal-content" id="img01">
  <div id="caption"></div>
</div>

{{<lead>}}

History view displays a list of all the values from a selected tag.

{{</lead>}}

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="history_view" src="/history_view.png" alt="History view">
    <figcaption >Fig 1. History view</figcaption>
</figure>

By selecting a tag from the "Tag" filter (searchable drop down list), the table is filled with all the information associated with that tag. The table displays the time and value for each line of information. Additionally, in the bottom left corner we have statistical information which displays the number of values, minimum, maximum, average and standard deviation value of the Value column. This table can be refreshed to update its content and downloaded in .xlsx or .csv format. 

By clicking the <img src="/history_filter_button.png" alt="last value logo" class = "logo_resize"> button the user can add or remove filters for the table content. In addition to the default Tag filter, used to select a tag to show its content in the table, there is a “Group By” and “Time” filter. The "Group By" filter is used to group the table content by Hour or Day. This filter is accompanied with a "Function" filter which allows us to select which statistical information to be calculated for our grouped content.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="history_filter_options" src="/history_filter_options.png" alt="History filter options">
    <figcaption >Fig 2. History filter options</figcaption>
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
</script>