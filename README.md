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

To display CSGO levels aswell, use this code:
```
$('strong[ng-bind="::teamMember.nickname"]').each(function(e){
var s=$(this).html();$.getJSON("https://api.faceit.com/api/nicknames/
"+s,function(s){var a=s.payload.country,n="<img style='margin-left: 4px;'
class='flag flag--16' src='https://cdn.faceit.com/frontend/159/assets/
images/flags/"+a.toUpperCase()+".png'>",t="<img style='margin-left: 4px;'
class='skill-icon' src='https://cdn.faceit.com/frontend/159/assets/images/
skill-icons/skill_level_"+s.payload.csgo_skill_level+"_md.png'>";
$('strong[ng-bind="::teamMember.nickname"]').eq(e).append(n+t)})});
```
