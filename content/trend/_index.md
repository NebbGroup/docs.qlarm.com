---
title: "Trend"
date: 2020-08-20T15:30:11+02:00
weight: 5
pre: ""
---

{{<lead>}}
Trend view shows a chart display of the data for selected tag(s) for a specific period of time with options to display events and event conditions thresholds. Charts can be customized and reports can be saved.
{{</lead>}}
<figure class="image_container">
    <img class="center_image" src="/trend_screen.png" alt="Trend">
    <figcaption>Fig 1. Trend</figcaption>
</figure>

## Add tag(s) to chart
In order for tag(s) data to be displayed tags needs to be added in chart. This is done by selecting an endpoint first from the select list "ENDPOINT" then selecting one or more tags (max 5) from the multiselect "TAGS" list.
<figure class="image_container">
    <img class="center_image figure_resize1" src="/trend_tag_list.png" alt="Adding tags">
    <figcaption>Fig 2. Adding tags</figcaption>
</figure>

## Time period
Tag(s) data can be displayed in the chart for the selected period. You can choose the period from the dropdown “TIME PERIOD” list for specified periods or choose a “Custom” period (“Last Day” is the initial preselected period).
<figure class="image_container">
    <img class="center_image figure_resize1" src="/time_period.png" alt="Time filter">
    <figcaption>Fig 3. Time filter</figcaption>
</figure>

When you choose a Custom for a time period, or click <img src="/custom_time_period_button.png">, a popup is shown for start and end date and time to be selected. Click “Apply” to apply the time settings in the chart.
<figure class="image_container">
    <img class="center_image figure_resize2" src="/custom_filter_screen.png" alt="Custom time period">
    <figcaption>Fig 4. Custom time period</figcaption>
</figure>

## Configuration
Chart displays can be customized in “Configuration” tab. Click <img src="/trend_config.png"> to set parameters for various chart displays. <br/>
<figure class="image_container">
    <img class="center_image figure_resize1" src="/trend_config_popup.png" alt="Configuration">
    <figcaption>Fig 5. Configuration</figcaption>
</figure>

If "Show chart symbols" is applied: <br/>
<figure class="image_container">
    <img class="center_image" src="/show_chart_symbols.png" alt="Show chart symbols enabled">
    <figcaption>Fig 6. "Show chart symbols" enabled</figcaption>
</figure>

If "Show chart thresholds" is applied: <br/>
<figure class="image_container">
    <img class="center_image" src="/show_chart_tresholds.png" alt="Show chart tresholds enabled">
    <figcaption>Fig 7. "Show chart thresholds" enabled</figcaption>
</figure>

If "Show events" is applied: <br/>
<figure class="image_container">
    <img class="center_image" src="/show_events.png" alt="Show events enabled">
    <figcaption>Fig 8. "Show events" enabled</figcaption>
</figure>

If "Value Axis Position" is applied: <br/>
<figure class="image_container">
    <img class="center_image" src="/value_axis_position.png" alt="Value axis position enabled">
    <figcaption>Fig 9. "Value axis position" enabled</figcaption>
</figure>

If "Single Time Axis" is not applied (value axis by tag displayed): <br/>
<figure class="image_container">
    <img class="center_image" src="/no_single_time_axis.png" alt="Single time axis disabled">
    <figcaption>Fig 10. "Single time axis" disabled</figcaption>
</figure>


## Edit tag settings
The "Color", "Thickness" and "Symbol" of the chart tag line can be customized. Go to "Edit tag settings" with click on the edit button in the chart tag.
<figure class="image_container">
    <img class="center_image figure_resize1" src="/edit_trend_tag_button.png" alt="Edit chart tag">
    <figcaption>Fig 11. Edit chart tag</figcaption>
</figure>
The change of the "Symbol" ("Round", "Square" or "TriangleUp") can be visible only if the "Show chart symbols" is enabled in "Configuration".
<figure class="image_container">
    <img class="center_image figure_resize2" src="/edit_tag_settings.png" alt="Edit tag settings">
    <figcaption>Fig 12. Edit tag settings</figcaption>
</figure>

## Delete tags
Delete tags from the chart by clicking the delete button in the chart tag.
<figure class="image_container">
    <img class="center_image figure_resize1" src="/tag_delete_button.png" alt="Delete chart tag">
    <figcaption>Fig 13. Delete chart tag</figcaption>
</figure>

## Reset chart
Reset chart by clicking the reset button <img src="/chart_reset_button.png">.

## Save Report
Chart with all the tags added can be saved as a Report by clicking the Save button <img src="/save_report_button.png">. Insert name and choose to save it in the actual period.
<figure class="image_container">
    <img class="center_image" src="/save_new_report.png" alt="Save report">
    <figcaption>Fig 14. Save report</figcaption>
</figure>

## Load Report
Saved reports can be loaded by clicking the "Open" button <img src="/load_report_button.png">. Then you get the "Load report" popup where you can select the report you want to load from the list and click "Load".
<figure class="image_container">
    <img class="center_image figure_resize2" src="/load_report_popup.png" alt="Load report">
    <figcaption>Fig 15. Load report</figcaption>
</figure>

## Edit Report
If you edit a loaded report and if you want to save it, you will get the "Overwrite" option in the popup from Fig 11. to choose if you like to overwrite the existing one.
<figure class="image_container">
    <img class="center_image figure_resize1" src="/overwrite_report.png" alt="Overwrite report">
    <figcaption>Fig 16. Overwrite report</figcaption>
</figure> 
 To save the report as a new report, select "Save as New" option and the loaded report will remain unchanged.
<figure class="image_container">
    <img class="center_image figure_resize1" src="/save_as_new_report.png" alt="Save report as new">
    <figcaption>Fig 17. Save report as new</figcaption>
</figure> 

## Chart menu
Chart data can be exported as JSON, CSV, XLSX, HTML, PDF. 
<figure class="image_container">
    <img class="center_image figure_resize1" src="/chart_data_menu.png" alt="Chart data menu">
    <figcaption>Fig 18. Chart data menu</figcaption>
</figure> 
Charts can be saved as images, printed and annotated. Images can be saved as PNG, JPG, SVG or PDF.
<figure class="image_container">
    <img class="center_image figure_resize1" src="/chart_image_menu.png" alt="Chart image menu">
    <figcaption>Fig 19. Chart image menu</figcaption>
</figure>  







 