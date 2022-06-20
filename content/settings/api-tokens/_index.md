---
title: "API Tokens"
date: 2020-08-20T16:07:13+02:00
weight: 16
---

<!-- The Modal -->
<div id="myModal" class="modal">
  <span class="close">&times;</span>
  <img class="modal-content" id="img01">
  <div id="caption"></div>
</div>

{{<lead>}}
In the API Tokens page you can list, create, edit, delete and revoke API Tokens.
{{</lead>}}

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="apiTokensView" src="/apiTokensView.png" alt="API Tokens View">
    <figcaption>Fig 1. APi Tokens View</figcaption>
</figure>

The table lists all the API Tokens for selected Scopes that are available for the current User. The table shows the name, GUID, Active from date, Expiration date, and Token status information (Is active column). You can filter the content in the table by activating the Search by name, Search by GUID, Scope and Token status filters. 

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="apiTokensFiltersOptions" src="/apiTokensFiltersOptions.png" alt="API Tokens Filters">
    <figcaption>Fig 2. APi Tokens Filters</figcaption>
</figure>

In the Search by Name filter you can search by one or more keywords and filter your Tokens by name. In the Search by GUID filter you can search tokens by GUID. You can easily copy Token’s GUID by clicking the <img src="/apiTokensCopy.png"> button, right next to the GUID value in the GUID column. In the [Scopes](/glossary#scope) filter, the user can filter the Tokens by the scopes that are assigned to the current User. In the Token status filter the user can filter the Tokens by their status (Active or Inactive). 
You can sort the table content by Name and by Is active columns.

## Create token

If you click the <img src="/apiTokensCreateButton.png"> button a popup form appears

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="apiTokensCreateTokensPopUp" src="/apiTokensCreateTokensPopUp.png" alt="Create API Token">
    <figcaption>Fig 3. Create APi Token</figcaption>
</figure>

Name and [Scopes](/glossary#scope) fields are required. GUID field is automatically populated and disabled, it cannot be edited. In order to copy the GUID value click on the <img src="/apiTokensCopy1.png"> button. If you want to regenerate a new GUID value, click on the <img src="/apiTokensRegenerate.png"> button. Description, Valid from and Valid to fields are optional. If you create a token without Valid from and Valid to values, the token is active from the moment of creation and will be active forever. Past dates in the calendar menu are disabled.


<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="apiTokensCalendar" src="/apiTokensCalendar.png" alt="apiTokensCalendar"  style="width: 35%;">
<figcaption>Fig 4. Calendar</figcaption>
</figure>

<img src="/apiTokensSave.png"> button will be disabled if you haven’t populated the required fields, or you have entered invalid dates in the Valid from and Valid to fields. 
After you are done configuring the token save the token by clicking the <img src="/apiTokensSaveEnabled.png"> button or <img src="/apiTokensCancel.png"> to discard the configuration.

## Edit token

To edit a token, click the <img src="/apiTokensEdit.png"> button after which a filled form will appear in which you can make the changes.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="apiTokensEditPopUp" src="/apiTokensEditPopUp.png" alt="Edit Token" >
<figcaption>Fig 5. Edit Token</figcaption>
</figure>

## Delete token

To remove a token, click the <img src="/apiTokensDelete.png" style="width: 2rem;">  button after which a confirmation popup window will appear. If confirmed, the Token will be deleted.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="apiTokensDeletePopUp" src="/apiTokensDeletePopUp.png" alt="Delete Token" style="width: 35%;">
<figcaption>Fig 6. Delete Token</figcaption>
</figure>

## Revoke token

To revoke a token, click the <img src="/apiTokensRevoke.png"> button after which a confirmation popup window will appear. If confirmed, the Token will be revoked. When you revoke a token, it goes to inactive state and sets the Valid to value to current date and time. When token is inactive, Revoke button is disabled (<img src="/apiTokensRevokeDisabled.png">). 

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="apiTokensRevokePopUp" src="/apiTokensRevokePopUp.png" alt="Revoke Token" style="width: 35%;">
<figcaption>Fig 7. Revoke Token</figcaption>
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