---
layout: default
title: "Check Email Address"
permalink: /2003/09/23/Check-Email-Address/
---

<div class="code">function checkEmail(formName) {    if (formName.strPreferredEmailType[1].checked) {<br>
   if (isEmail(formName.strAlternativeEmailAddress.value) == false) {      return false;     } else {      formName.strPreferredEmailAddress.value = formName.strAlternativeEmailAddress.value;      return true;     }    } else {     formName.strPreferredEmailAddress.value = formName.strWorkEmailAddress.value;<br>
   return true ;<br>
  }<br>
 }<br>
 function isEmail(string) {<br>
  if (string.search(/^\w+((-\w+)|(\.\w+))*\@[A-Za-z0-9]+((\.|-)[A-Za-z0-9]+)*\.(([A-Za-z]{2,<FONT COLOR=BLUE>3</FONT>})|(aero|coop|info|museum|name))$/) != -1) {<br>
   return true;<br>
  } else {<br>
   return false;<br>
  }<br>
 }</div>