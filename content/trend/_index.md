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
The Trend page provides a flexible chart for visualizing your data. Data from multiple [Tags](/glossary#tag) can be displayed on the chart, and the time period from which the data are collected can be adjusted. The resulting trend view can be saved as a Report which can be retrieved later or saved to file.
{{</lead>}}
<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="trend_screen" src="/trend-view.png" alt="Trend">
    <figcaption>Fig 1. Trend</figcaption>
</figure>

## Getting started
The trend window is by default blank when entering the Trend page. In order to start viewing your data, you can either add individual tags or [load a previously saved Report](/trend#reports).

### Adding tags to the chart
Multiple Tags can be added to the chart in order to view their data. This is done by selecting one or more Tags (max 5) from the multiselect "TAGS" tree view dropdown list.
<figure class="image_container">
    <img class="center_image myImg figure_resize1" onClick="reply_click(this)"  id="trend_tag_list" src="/tag-list.png" alt="Adding tags">
    <figcaption>Fig 2. Adding tags</figcaption>
</figure>

### Change time period
Tag data can be displayed in the chart for the selected period. You can choose the period from the dropdown “TIME” list for specified periods or choose a “Custom” period (“Today” is the initial preselected period).
<figure class="image_container">
    <img class="center_image myImg figure_resize1" onClick="reply_click(this)"  id="time_period" src="/time-filter-trend.png" alt="Time filter">
    <figcaption>Fig 3. Time filter</figcaption>
</figure>

When you choose a Custom time period, or click <img src="/custom_time_period_button.png">, a popup is shown for start and end date and time to be selected. Click “Apply” to apply the time settings in the chart.
<figure class="image_container">
    <img class="center_image myImg figure_resize2" onClick="reply_click(this)"  id="custom_filter_screen" src="/custom_filter_screen.png" alt="Custom time period">
    <figcaption>Fig 4. Custom time period</figcaption>
</figure>

## Customize the chart
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


### Configure trend line
Each trend line's "Color", "Thickness" and "Symbol" is customizable via configuration in the "Edit tag settings".
<figure class="image_container">
    <img class="center_image myImg figure_resize1" onClick="reply_click(this)"  id="edit_trend_tag_button" src="/edit_trend_tag_button.png" alt="Edit chart tag">
    <figcaption>Fig 11. Edit chart tag</figcaption>
</figure>
The trend line Color can be customized by entering Hex Color Codes or by choosing a color from the color pallet. Trend line data points Symbols, that take "Round", "Square" or "TriangleUp" form, can be visible only if the "Show chart symbols" setting is enabled in the Chart Configuration. The thickness of the trend line is customizable by choosing an integer value in the range of 1 to 10.</br></br>
The Moving Average feature is a calculation used to analyze data points by creating a series of averages of different subsets of the full trend data. The size of the subsets is determined by selecting a number of data points to be included for the calculation. Currently Qlarm supports 5, 10, 25 and 50 data points for each calculating subset.</br></br>
To visualize data points for long time periods, the data in each trend line is compressed (downsampled) by keeping high precision average data for only a limited time frame, which is calculated depending of the length of the selected time period. The Maximum and Minimum series feature affiliates the downsampled data to give more insight, by calculating the maximum and minimum for the limited time frame.
<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="edit_tag_settings" src="/edit_tag_settings.png" alt="Edit chart settings">
    <figcaption>Fig 12. Edit tag settings</figcaption>
</figure>

### Delete tags
Delete individual Tags from the chart by clicking the delete button in the chart tag.
<figure class="image_container">
    <img class="center_image myImg figure_resize1" onClick="reply_click(this)"  id="tag_delete_button" src="/tag_delete_button.png" alt="Delete chart tag">
    <figcaption>Fig 13. Delete chart tag</figcaption>
</figure>

### Reset chart
Clear the chart of all tags and trends by clicking the reset button <img src="/chart_reset_button.png">.

## Reports 
Reports are collections of Tags which can be saved with their associated time period for later retrieval.
### Save Report
The Save button stores all the currently selected Tags in a Report. <img src="/save_report_button.png">.<br> 
Choose a unique name for your Report, and enable "Save Time Period" to save your choice of Time Period other than "Last Day".
<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="save_new_report" src="/new-trend-report.png" alt="Save report">
    <figcaption>Fig 14. Save report</figcaption>
</figure>

### Load Report
Saved Reports can be loaded by clicking the "Open" button <img src="/load_report_button.png">. The "Load Report" popup lets you select the Report you want to load from a list of saved reports. Click "Load" to retrieve the selected Report. Click "Delete" to delete chosen report.
<figure class="image_container">
    <img class="center_image myImg figure_resize2" onClick="reply_click(this)"  id="load_report_popup" src="/load-trend-report.png" alt="Load report">
    <figcaption>Fig 15. Load Report</figcaption>
</figure>

### Edit Report
If you edit a loaded Report and if you want to save it, you will get access to the "Overwrite" option in the popup from Fig 14. This overwrites the currently selected Report.
<figure class="image_container">
    <img class="center_image myImg figure_resize1" onClick="reply_click(this)"  id="overwrite_report" src="/overwrite-option.png" alt="Overwrite report">
    <figcaption>Fig 16. Overwrite Report</figcaption>
</figure> 
 To save the Report as a new Report, select "Save as New" option and the loaded Report will remain unchanged.
<figure class="image_container">
    <img class="center_image myImg figure_resize1" onClick="reply_click(this)"  id="save_as_new_report" src="/save-as-new-report.png" alt="Save report as new">
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