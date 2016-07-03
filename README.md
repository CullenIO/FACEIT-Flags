# FaceIT Flags
Adds flags to FaceIT's match lobbies

To use, simply add this code to a bookmark as the url:
```
javascript:$('strong[ng-bind="::teamMember.nickname"]').each(function(a){
var n=$(this).html();$.getJSON("https://api.faceit.com/api/nicknames/"+n,
function(n){var e=n.payload.country,t="<img style='margin-left: 4px;'class='
flag flag--16' src='https://cdn.faceit.com/frontend/159/assets/images/flags/"+e
.toUpperCase()+".png'>";$('strong[ng-bind="::teamMember.nickname&q
uot;]').eq(a).append(t)})});
```
