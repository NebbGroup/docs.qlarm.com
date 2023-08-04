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
    <img class="center_image myImg" onClick="reply_click(this)"  id="apiTokensView" src="/apiTokens-table.png" alt="API Tokens View">
    <figcaption>Fig 1. API Tokens View</figcaption>
</figure>

The table lists all the API Tokens for selected Scopes that are available for the current User. The table shows the name, GUID, Active from date, Expiration date, and Token status information (Is active column). You can filter the content in the table by name, Token, Asset(s) and Token status filters. 

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="apiTokensFiltersOptions" src="/APITokensFilters.png" alt="API Tokens Filters">
    <figcaption>Fig 2. API Tokens Filters</figcaption>
</figure>

In the Name search filter you can search by one or more keywords and filter your Tokens by name. In the Token search filter you can search tokens by Token. You can easily copy Token’s token GUID by clicking the <img src="/apiTokensCopy.png"> button, right next to the Token value in the Token column. In the [Assets](/glossary#assetScope) filter, the user can filter the Tokens by the asset scopes that are assigned to the current User. In the Token status filter the user can filter the Tokens by their status (Active or Inactive). 
You can sort the table content by Name and by Is active columns.

## Create token

If you click the <img src="/apiTokensCreateButton.png"> button a popup form appears

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="apiTokensCreateTokensPopUp" src="/CreateAPIToken.png" alt="Create API Token">
    <figcaption>Fig 3. Create API Token</figcaption>
</figure>

Name and [Assets](/glossary#assetScope) fields are required. Token field is automatically populated and disabled, it cannot be edited. In order to copy the Token GUID value click on the <img src="/apiTokensCopy1.png"> button. If you want to regenerate a new Token GUID value, click on the <img src="/apiTokensRegenerate.png"> button. Description, Valid from and Valid to fields are optional. If you create a token without Valid from and Valid to values, the token is active from the moment of creation and will be active forever. Past dates in the calendar menu are disabled.


<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="apiTokensCalendar" src="/apiTokensCalendar.png" alt="apiTokensCalendar"  style="width: 35%;">
<figcaption>Fig 4. Calendar</figcaption>
</figure>

<img src="/apiTokensSave.png"> button will be disabled if you haven’t populated the required fields, or you have entered invalid dates in the Valid from and Valid to fields. 
After you are done configuring the token save the token by clicking the <img src="/apiTokensSaveEnabled.png"> button or <img src="/apiTokensCancel.png"> to discard the configuration.

## Edit token

To edit a token, click the <img src="/edit-button.png"> button after which a filled form will appear in which you can make the changes.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="apiTokensEditPopUp" src="/EditAPIToken.png" alt="Edit Token" >
<figcaption>Fig 5. Edit Token</figcaption>
</figure>

## Delete token

To remove a token, click the <img src="/delete-icon.png" style="width: 2rem;">  button after which a confirmation popup window will appear. If confirmed, the Token will be deleted.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="apiTokensDeletePopUp" src="/apiTokensDeletePopUp.png" alt="Delete Token" style="width: 35%;">
<figcaption>Fig 6. Delete Token</figcaption>
</figure>

## Revoke token

To revoke a token, click the <img src="/revoke-button.png"> button after which a confirmation pop-up window will appear. If confirmed, the Token will be revoked. When you revoke a token, it goes to inactive state and sets the Valid to value to current date and time. When token is inactive, Revoke button is disabled (<img src="/apiTokensRevokeDisabled.png">). 

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="apiTokensRevokePopUp" src="/apiTokensRevokePopUp.png" alt="Revoke Token" style="width: 35%;">
<figcaption>Fig 7. Revoke Token</figcaption>
</figure>

## Usage of API Tokens
<br>

#### Latest Values of Tags
You can use API Tokens in API requests by tool for API requests. In order to get the latest values for selected tags in the token, 
a GET request should be made to URL https://api.qlarm.com/api/apiTokenAccess/getTagsByToken with two request headers: <br>

header name: "Tenant", header value: (e.g.)"Tenant_name" and <br />
header name: "ApiToken", header value: (e.g. see Fig 1)"7c9fc2bf-f94a-b554-6b75-9d4ff6b5025d".

ApiToken header value can be copied from Qlarm API Tokens page. Using this getTagsByToken API request, the user will be able to get the latest values for token's selected tags, in the response.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="copyTokenForHeader" src="/CopyToken.png" alt="Copy API Token for request header" style="width: 35%;">
<figcaption>Fig 8. Copy API Token for request header </figcaption>
</figure>


#### Historical Values of Tags
You can use API Tokens in API requests by tool for API requests. There are two steps to getting historical values for a tag in the token.

First, a GET request should be made to the URL https://api.qlarm.com/odata/tags with two request headers: <br>

header name: "Tenant", header value: (e.g.)"Tenant_name" and <br />
header name: "ApiToken", header value: (e.g.) "e137764a-585c-4614-a34d-2d3cac0f062b".

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="copyTokenForHeader" src="/odata_tags.png" alt="Copy API Token for request header" style="width: 55%;">
<figcaption>Fig 9. GET for Tag Id </figcaption>
</figure>

Second, get the id from the tag you would like to see historical values. Then a GET request should be made to the URL https://api.qlarm.com/odata/data(TagId='tagId',TimeFrom='startTime',TimeTo='endTime') with the following parameters: <br>

parameter tagId: should be the id from the tag, (e.g.) 0d302e53-c505-4792-a89e-46b5138d9dd3 <br />
parameter startTime: should be the starting date, formatted 2023-06-30 00:00:00 <br />
parameter endTime: should be the ending date, formatted 2023-07-31 00:00:00

Historical value is limited to show results from the last year. Ensure the dates that are entered are within the past 365 days.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="copyTokenForHeader" src="/odata_data.png" alt="Copy API Token for request header" style="width: 80%;">
<figcaption>Fig 10. GET for Historical Values of the Tag</figcaption>
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