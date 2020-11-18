---
title: "Recipients"
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
In the "Recipients" configuration page, you can list, create, edit and delete [Recipients](/glossary#recipient). You can categorize Recipients as individual <img src="/individual_recipient_icon.png" alt="individual recipient icon" class = "logo_resize"> and groups <img src="/recipients_groups_icon.png" alt="recipient groups icon" class = "logo_resize"> of recipients. You can use groups in applying rules and notifying many recipients at once. Recipient you create should contains required contact details and availability in order to receive [Notifications](/glossary#notification) in many forms. Recipients are organization specific.
{{</lead>}}

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="recipients_configuration" src="/recipients_configuration.png" alt="Recipients configuration">
    <figcaption>Fig 1. Recipients configuration</figcaption>
</figure>

## Recipients

There are four types of Notifications that Recipients can receive:

- SMS Text Message on a mobile phone <img src="/phone_call_and_sms_recipient.png" alt="phone call and sms recipient icon" class = "logo_resize">
- Voice Calls <img src="/phone_call_and_sms_recipient.png" alt="phone call and sms recipient icon" class = "logo_resize">
- E-mail <img src="/email_recipient.png" alt="email icon" class = "logo_resize">
- Push Notifications <img src="/push_notification_recipient.png" alt="push notification icon" class = "logo_resize">

The "Recipients" configuration page lists its Recipients in a table, which shows their name, selected Notification Types, number of Recipients for the [Recipients Group](/glossary#recipient-group). An individual Recipient represents a single person that can receive Notifications. To add a Recipient click the <img src="/add_recipient_button.png" alt="add recipient button" > button by which a form appears:

<figure class="image_container">
    <img class="center_image myImg figure_resize2" onClick="reply_click(this)"  id="add_recipient_form" src="/add_recipient_form.png" alt="Individual recipient configuration">
    <figcaption>Fig 2. Individual recipient configuration</figcaption>
</figure>

The individual Recipient form requires basic contact information about the Recipient. To choose a type of Notification that the individual Recipient will receive, you need to fill a specific contact field and enable it by toggling the switch <img src="/recipient_toggle_switch.png" alt="add recipient button" >. After you are done configuring the individual Recipient save the configuration by clicking the <img src="/add_recipient_form_button.png" alt="add recipient button" > button or <img src="/cancel_recipient_button.png" alt="add recipient button" > to discard the configuration. 

A Recipients Group represents a collection of Recipients that can be the receiver of Notifications. To add a Recipients Group click the <img src="/add_recipient_groups_button.png" alt="add recipient button" > button and a form appears:

<figure class="image_container">
    <img class="center_image myImg figure_resize2" onClick="reply_click(this)"  id="add_recipient_groups_form" src="/add_recipient_groups_form.png" alt="Recipients group configuration">
    <figcaption>Fig 3. Recipients group configuration</figcaption>
</figure>

The form requires that you select a name for the Recipients Group, select Recipients from the dropdown list and a Template or schedule for when this group is reachable. After you are done configuring the Recipients Group save the configuration by clicking the <img src="/add_recipient_form_button.png" alt="add recipient button" > button or <img src="/cancel_recipient_button.png" alt="add recipient button" > to discard the configuration. 

After filling the table with Recipients and Recipients Groups, you can easily search them by using the search text field and filter them by using the filter select list.

<figure class="image_container">
    <img class="center_image myImg figure_resize2" onClick="reply_click(this)"  id="search_and_filter recipients" src="/search_and_filter recipients.png" alt="Search and filter recipients">
    <figcaption>Fig 4. Search and filter recipients</figcaption>
</figure>

## Editing a recipient and recipients groups

You can edit an individual Recipient or a Recipients Group by clicking the <img src="/edit_recipient_button.png" alt="add recipient button" > button after which a filled form will appear in which you can make the changes. To remove a Recipient or a Recipients Group click the <img src="/delete_recipient_button.png" alt="add recipient button" > button.

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