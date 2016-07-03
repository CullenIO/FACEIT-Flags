# FaceIT Flags
Adds flags to FaceIT's match lobbies

![Faceit Flags Example Screenshot](http://image.prntscr.com/image/751c8f5c41a8418aabcca741bda98522.png)

To use, simply add this code to a bookmark (best in the bookmark bar) as the url:
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
javascript:$('strong[ng-bind="::teamMember.nickname"]').each(function(e){
var s=$(this).html();$.getJSON("https://api.faceit.com/api/nicknames/"+s,
function(s){var a=s.payload.country,
n="<img style='margin-left: 4px;' class='flag flag--16' src='https://cdn.faceit.com/frontend/159/assets/images/flags/"+
a.toUpperCase()+".png'>",t="<img style='margin-left: 4px;' class='skill-icon' src='https://cdn.faceit.com/frontend/159/assets/images/skill-icons/skill_level_"+
s.payload.csgo_skill_level+"_md.png'>";$('strong[ng-bind="::teamMember.nickname"]').eq(e).append(n+t)})});
```

##How to use

Right click on the bookmark bar, click add page/new bookmark.
In the url box, paste the code.
When on the FaceIT match page, click the bookmark and it will activate.

Chrome: https://support.google.com/chrome/answer/95745?hl=en-GB

Firefox: https://support.mozilla.org/en-US/kb/bookmarks-toolbar-display-favorite-websites
