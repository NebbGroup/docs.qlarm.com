---
title: "Creating Reports"
date: 2020-11-30T14:36:01+01:00
weight: 17

---
<!-- The Modal -->
<div id="myModal" class="modal">
  <span class="close">&times;</span>
  <img class="modal-content" id="img01">
  <div id="caption"></div>
</div>

## Reports 
Reports are collections of Tags which can be saved with their associated time period for later retrieval.
### Save Report
The Save button stores all the currently selected Tags in a Report. <img src="/save_report_button.png">.<br> 
Choose a unique name for your Report, and enable "Save Time Period" to save your choice of Time Period other than "Last Day".
<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="save_new_report" src="/save_new_report.png" alt="Save report">
    <figcaption>Fig 14. Save report</figcaption>
</figure>

### Load Report
Saved Reports can be loaded by clicking the "Open" button <img src="/load_report_button.png">. The "Load Report" popup lets you select the Report you want to load from a list of saved reports. Click "Load" to retrieve the selected Report.
<figure class="image_container">
    <img class="center_image myImg figure_resize2" onClick="reply_click(this)"  id="load_report_popup" src="/load_report_popup.png" alt="Load report">
    <figcaption>Fig 15. Load Report</figcaption>
</figure>

### Edit Report
If you edit a loaded Report and if you want to save it, you will get access to the "Overwrite" option in the popup from Fig 14. This overwrites the currently selected Report.
<figure class="image_container">
    <img class="center_image myImg figure_resize1" onClick="reply_click(this)"  id="overwrite_report" src="/overwrite_report.png" alt="Overwrite report">
    <figcaption>Fig 16. Overwrite Report</figcaption>
</figure> 
 To save the Report as a new Report, select "Save as New" option and the loaded Report will remain unchanged.
<figure class="image_container">
    <img class="center_image myImg figure_resize1" onClick="reply_click(this)"  id="save_as_new_report" src="/save_as_new_report.png" alt="Save report as new">
    <figcaption>Fig 17. Save Report as new</figcaption>
</figure> 

## Export chart data
Chart data can be exported as JSON, CSV, XLSX, HTML, PDF. 
<figure class="image_container">
    <img class="center_image myImg figure_resize1" onClick="reply_click(this)"  id="chart_data_menu" src="/chart_data_menu.png" alt="Chart data menu">
    <figcaption>Fig 18. Chart data menu</figcaption>
</figure> 
Charts can be saved as images, printed and annotated. Images can be saved as PNG, JPG, SVG or PDF.
<figure class="image_container">
    <img class="center_image myImg figure_resize1" onClick="reply_click(this)"  id="chart_image_menu" src="/chart_image_menu.png" alt="Chart image menu">
    <figcaption>Fig 19. Chart image menu</figcaption>
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