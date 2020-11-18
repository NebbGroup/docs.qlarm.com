---
title: "Trend"
date: 2020-08-20T15:30:11+02:00
weight: 5
pre: ""
---

<!-- The Modal -->
<div id="myModal" class="modal">
  <span class="close">&times;</span>
  <img class="modal-content" id="img01">
  <div id="caption"></div>
</div>

{{<lead>}}
The [Trend View](/glossary#view) page is where you can get your [Tags](/glossary#tag) values-data visualized as [Trend](/glossary#trend). It show a chart display of the data for selected Tag(s) for a specific period of time. You can add Tags and change period while viewing a [Report](/glossary#report). Also you can get display of [Event](/glossary#event) raised and event thresholds from the Tags' [Conditions](/glossary#condition). You can customize the chart and have a Reports saved. You can download the Reports as an images and export the chart data in files.
{{</lead>}}
<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="trend_screen" src="/trend_screen.png" alt="Trend">
    <figcaption>Fig 1. Trend</figcaption>
</figure>

## Add tag(s) to chart
In order for Tags data to be displayed Tags needs to be added in chart. This is done by selecting an [Endpoint](/glossary#endpoint) first from the select list "ENDPOINT" then selecting one or more Tags (max 5) from the multiselect "TAGS" list.
<figure class="image_container">
    <img class="center_image myImg figure_resize1" onClick="reply_click(this)"  id="trend_tag_list" src="/trend_tag_list.png" alt="Adding tags">
    <figcaption>Fig 2. Adding tags</figcaption>
</figure>

## Time period
Tags data can be displayed in the chart for the selected period. You can choose the period from the dropdown “TIME PERIOD” list for specified periods or choose a “Custom” period (“Last Day” is the initial preselected period).
<figure class="image_container">
    <img class="center_image myImg figure_resize1" onClick="reply_click(this)"  id="time_period" src="/time_period.png" alt="Time filter">
    <figcaption>Fig 3. Time filter</figcaption>
</figure>

When you choose a Custom for a time period, or click <img src="/custom_time_period_button.png">, a popup is shown for start and end date and time to be selected. Click “Apply” to apply the time settings in the chart.
<figure class="image_container">
    <img class="center_image myImg figure_resize2" onClick="reply_click(this)"  id="custom_filter_screen" src="/custom_filter_screen.png" alt="Custom time period">
    <figcaption>Fig 4. Custom time period</figcaption>
</figure>

## Configuration
Chart displays can be customized in “Configuration” tab. Click <img src="/trend_config.png"> to set parameters for various chart displays. <br/>
<figure class="image_container">
    <img class="center_image myImg figure_resize1" onClick="reply_click(this)"  id="trend_config_popup" src="/trend_config_popup.png" alt="Configuration">
    <figcaption>Fig 5. Configuration</figcaption>
</figure>

If "Show chart symbols" is applied: <br/>
<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="show_chart_symbols" src="/show_chart_symbols.png" alt="Show chart symbols enabled">
    <figcaption>Fig 6. "Show chart symbols" enabled</figcaption>
</figure>

If "Show chart thresholds" is applied: <br/>
<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="show_chart_tresholds" src="/show_chart_tresholds.png" alt="Show chart thresholds enabled">
    <figcaption>Fig 7. "Show chart thresholds" enabled</figcaption>
</figure>

If "Show events" is applied: <br/>
<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="show_events" src="/show_events.png" alt="Show events enabled">
    <figcaption>Fig 8. "Show events" enabled</figcaption>
</figure>

If "Value Axis Position" is applied: <br/>
<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="value_axis_position" src="/value_axis_position.png" alt="Value axis position enabled">
    <figcaption>Fig 9. "Value axis position" enabled</figcaption>
</figure>

If "Single Time Axis" is not applied (value axis by Tag displayed): <br/>
<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="no_single_time_axis" src="/no_single_time_axis.png" alt="Single time axis disabled">
    <figcaption>Fig 10. "Single time axis" disabled</figcaption>
</figure>


## Edit tag settings
The "Color", "Thickness" and "Symbol" of the chart tag line can be customized. Go to "Edit tag settings" with click on the edit button in the Chart Tag.
<figure class="image_container">
    <img class="center_image myImg figure_resize1" onClick="reply_click(this)"  id="edit_trend_tag_button" src="/edit_trend_tag_button.png" alt="Edit chart tag">
    <figcaption>Fig 11. Edit chart tag</figcaption>
</figure>
The change of the "Symbol" ("Round", "Square" or "TriangleUp") can be visible only if the "Show chart symbols" is enabled in "Configuration".
<figure class="image_container">
    <img class="center_image myImg figure_resize2" onClick="reply_click(this)"  id="edit_tag_settings" src="/edit_tag_settings.png" alt="Edit chart settings">
    <figcaption>Fig 12. Edit tag settings</figcaption>
</figure>

## Delete tags
Delete Tags from the chart by clicking the delete button in the chart tag.
<figure class="image_container">
    <img class="center_image myImg figure_resize1" onClick="reply_click(this)"  id="tag_delete_button" src="/tag_delete_button.png" alt="Delete chart tag">
    <figcaption>Fig 13. Delete chart tag</figcaption>
</figure>

## Reset chart
Reset chart by clicking the reset button <img src="/chart_reset_button.png">.

## Save Report
Chart with all the Tags added can be saved as a Report by clicking the Save button <img src="/save_report_button.png">. Insert name and choose to save it in the actual period.
<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="save_new_report" src="/save_new_report.png" alt="Save report">
    <figcaption>Fig 14. Save report</figcaption>
</figure>

## Load Report
Saved Reports can be loaded by clicking the "Open" button <img src="/load_report_button.png">. Then you get the "Load Report" popup where you can select the Report you want to load from the list and click "Load".
<figure class="image_container">
    <img class="center_image myImg figure_resize2" onClick="reply_click(this)"  id="load_report_popup" src="/load_report_popup.png" alt="Load report">
    <figcaption>Fig 15. Load Report</figcaption>
</figure>

## Edit Report
If you edit a loaded Report and if you want to save it, you will get the "Overwrite" option in the popup from Fig 11. to choose if you like to overwrite the existing one.
<figure class="image_container">
    <img class="center_image myImg figure_resize1" onClick="reply_click(this)"  id="overwrite_report" src="/overwrite_report.png" alt="Overwrite report">
    <figcaption>Fig 16. Overwrite Report</figcaption>
</figure> 
 To save the Report as a new Report, select "Save as New" option and the loaded Report will remain unchanged.
<figure class="image_container">
    <img class="center_image myImg figure_resize1" onClick="reply_click(this)"  id="save_as_new_report" src="/save_as_new_report.png" alt="Save report as new">
    <figcaption>Fig 17. Save Report as new</figcaption>
</figure> 

## Chart menu
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