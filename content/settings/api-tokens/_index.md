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
{{</lead>}}


## Usage of API Tokens

You can use API Tokens in API requests from code or by tool for API requests.
In order to get the tags available by the token, a GET request should be made to URL <b>https://api.qlarm.com/api/apiTokenAccess/getTagsByToken</b> with two request headers: <br/><b>header name: "Tenant", header value: (e.g.)"Tenant_name"</b> and <br/><b>header name: "ApiToken", header value: (e.g. see Fig 1)"7c9fc2bf-f94a-b554-6b75-9d4ff6b5025d"</b>.

ApiToken header value can be copied from Qlarm API Tokens page. API Token will appear on this page if the logged in user has all the scopes included in the API token. Using this getTagsByToken API request, the user will be able to get scoped tags in the response.

<figure class="image_container">
    <img class="center_image myImg" onClick="reply_click(this)"  id="copy_api_token_guid" src="/copy_api_token_guid.png" alt="Copy API token">
<figcaption>Fig 1. Copy API Token for request header</figcaption>
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