---
title: "Schedules"
date: 2020-08-20T15:54:27+02:00
weight: 10
---
<!-- The Modal -->
<div id="myModal" class="modal">
  <span class="close">&times;</span>
  <img class="modal-content" id="img01">
  <div id="caption"></div>
</div>

{{<lead>}}
In the Schedules configuration page, you can add, edit, and delete Schedules. It allows users to manage schedules for sending notifications to recipient groups. Schedules are used to specify the time periods during which notifications should be sent to the selected recipient groups.
{{<lead>}}

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)" id="schedule_view" src="/schedulesView.png" alt="Schedules view">
    <figcaption>Fig 1. Schedule table</figcaption>
</figure>

## Add schedule

If you click the “Add schedule” button <img src="/addScheduleBtn.png" alt="add schedule button">, “Add schedule” popup is opened.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)" id="schedule_configuration" src="/scheduleConfiguration.png" alt="Schedule configuration">
    <figcaption>Fig 2. Schedule configuration</figcaption>
</figure>

To create a new schedule, you must fill in the following information: “NAME”, “START DAY”, “START HOUR”, “END DAY” and “END HOUR”. Once you have those fields populated, click on “Add period” button <img src="/addPeriodBtn.png" alt="add period button"> and your period table will be displayed. Under “Actions” from the period table, you can edit and delete the period. 
</br>
In the top right corner of the popup window, there is a toggle button <img src="/toggleBtn.png" alt="enable/disable button"> which indicates whether the schedule is enabled or disabled. If the toggle button is on, the schedule will be enabled, and the notifications will only be sent to the recipient group according to the period configuration. If the toggle button is off, the schedule will be disabled, and the notifications will be sent to the recipient group regardless of the period configuration.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)" id="configured_schedule" src="/configuredSchedule.png" alt="Configured schedule">
    <figcaption>Fig 3. Configured schedule</figcaption>
</figure>

After you are done configuring the schedule, click on “Save” button <img src="/saveSchedule.png" alt="save schedule button"> to create the schedule, or “Cancel” button <img src="/cancelSchedule.png" alt="cancel schedule button"> to discard the configuration.

The created schedules can be used when creating a recipient group. In the “Add recipient group” popup window, click on “SELECT SCHEDULE” drop-down menu to select a schedule.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)" id="use_configured_schedule" src="/createRecipientGroupFromSchedules.png" alt="use created schedule">
    <figcaption>Fig 4. Configure recipient group with added schedule</figcaption>
</figure>

## Edit schedule

You can edit a schedule by clicking the “Edit” button <img src="/edit-button.png" alt="edit schedule button"> after which a filled form will appear in which you can make the changes.

## Delete schedule

To delete a schedule, simply click on the “Delete” button <img src="/delete-icon.png" alt="delete schedule button"> and click on the “Yes” button from the confirmation window.
