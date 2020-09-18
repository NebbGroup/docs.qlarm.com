---
title: "Trend"
date: 2020-08-20T15:30:11+02:00
weight: 5
pre: ""
---

{{<lead>}}
Trend view is where we can get chart display of the data for selected tag(s) for a chosen period of time with an options to display events and event conditions tresholds. Charts look can be customized and reports can be saved.
{{</lead>}}
<figure class="image_container">
    <img class="center_image" src="/trend_screen.png" alt="Trend">
    <figcaption>Fig 1. Trend</figcaption>
</figure>

## Add tag(s) to chart
In order for tag(s) data to be displayed tags needs to be added in chart. This is done by selecting an endpoint first from the select list "ENDPOINT" then selecting one or many tags (max 5) from the multiselect list "TAGS".
<figure class="image_container">
    <img class="center_image" src="/trend_tag_list.png" alt="Adding tags">
    <figcaption>Fig 2. Adding tags</figcaption>
</figure>

## Time period
Tag(s) data can be displayed in the chart for the period selected. We can select the period from the dropdown list "TIME PERIOD" of defined periods or choose a "Custom" period ("Last Day" is the initial preselected period). 
<figure class="image_container">
    <img class="center_image" src="/time_period.png" alt="Time filter">
    <figcaption>Fig 3. Time filter</figcaption>
</figure>

When we choose a Custom for a time period, or click to <img src="/custom_time_period_button.png">, popup is displayed for start and end date and time to be inserted. This period is applied to the chart after click on "Apply" button.
<figure class="image_container">
    <img class="center_image" src="/custom_filter_screen.png" alt="Custom time period">
    <figcaption>Fig 4. Custom time period</figcaption>
</figure>

## Configuration
We can configure what and how to be displayed on the chart via the "Configuration" which can be opened with click on <img src="/trend_config.png">. <br/>
<figure class="image_container">
    <img class="center_image" src="/trend_config_popup.png" alt="Configuration">
    <figcaption>Fig 5. Configuration</figcaption>
</figure>

If "Show chart symbols" is applied: <br/>
<figure class="image_container">
    <img class="center_image" src="/show_chart_symbols.png" alt="Show chart symbols enabled">
    <figcaption>Fig 6. "Show chart symbols" enabled</figcaption>
</figure>

If "Show chart tresholds" is applied: <br/>
<figure class="image_container">
    <img class="center_image" src="/show_chart_tresholds.png" alt="Show chart tresholds enabled">
    <figcaption>Fig 7. "Show chart tresholds" enabled</figcaption>
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
The "Color", "Thickness" and "Symbol" of the chart tag line can be customized. This can be done via the "Edit tag settings" which is displayed with click on the edit button in the chart tag.
<figure class="image_container">
    <img class="center_image" src="/edit_trend_tag_button.png" alt="Edit chart tag">
    <figcaption>Fig 11. Edit chart tag</figcaption>
</figure>
The change of the "Symbol" ("Round", "Square" or "TriangleUp") can be visible only if the "Show chart symbols" is enabled in "Configuration" part.
<figure class="image_container">
    <img class="center_image" src="/edit_tag_settings.png" alt="Edit tag settings">
    <figcaption>Fig 12. Edit tag settings</figcaption>
</figure>

## Delete tags
Tag can be removed from the chart by clicking the delete button in the chart tag.
<figure class="image_container">
    <img class="center_image" src="/tag_delete_button.png" alt="Delete chart tag">
    <figcaption>Fig 13. Delete chart tag</figcaption>
</figure>

## Reset chart
Chart can be reset by clicking the reset button <img src="/chart_reset_button.png">.

## Save Report
Chart with all the tags added can be saved as a Report by clicking the Save button <img src="/save_report_button.png">, insert name and choose to save it in the actual period or not.
<figure class="image_container">
    <img class="center_image" src="/save_new_report.png" alt="Save report">
    <figcaption>Fig 14. Save report</figcaption>
</figure>

## Load Report
Saved reports can be loaded by clicking on "Open" button <img src="/load_report_button.png">. Then we get the "Load report" popup where we choose the report we want to load from the list and then click "Load".
<figure class="image_container">
    <img class="center_image" src="/load_report_popup.png" alt="Load report">
    <figcaption>Fig 15. Load report</figcaption>
</figure>

## Edit Report
If we edit an already loaded report and if we like to save it, we will get the "Overwrite" option in the popup from Fig 11. to choose if we like to overwrite the existing one.
<figure class="image_container">
    <img class="center_image" src="/overwrite_report.png" alt="Overwrite report">
    <figcaption>Fig 16. Overwrite report</figcaption>
</figure> 
 If we like to save the report as a new one then we choose the "Save as New" option. Previously loaded one will stay unchanged.
<figure class="image_container">
    <img class="center_image" src="/save_as_new_report.png" alt="Save report as new">
    <figcaption>Fig 17. Save report as new</figcaption>
</figure> 

## Chart menu
Chart data can be exported as JSON, CSV, XLSX, HTML, PDF. 
<figure class="image_container">
    <img class="center_image" src="/chart_data_menu.png" alt="Chart data menu">
    <figcaption>Fig 18. Chart data menu</figcaption>
</figure> 
Chart can be saved as image, printed and anotated. Images could be saved as PNG, JPG, SVG or PDF.
<figure class="image_container">
    <img class="center_image" src="/chart_image_menu.png" alt="Chart image menu">
    <figcaption>Fig 19. Chart image menu</figcaption>
</figure>  







 