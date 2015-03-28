---
layout: default
title: "Password Regular Expression"
permalink: /2003/08/17/Password-Regular-Expression/
---

<P>This allows alphanumberic passwords which must contain a numeral with a minimum and maximum number of characters.</P>

<div class="code"><FONT COLOR=MAROON>&lt;cfinput name=<FONT COLOR=BLUE>"strPassword"</FONT> <br>
    type=<FONT COLOR=BLUE>"password"</FONT> id=<FONT COLOR=BLUE>"strPassword"</FONT> <br>
       required=<FONT COLOR=BLUE>"yes"</FONT> maxlength=<FONT COLOR=BLUE>"#intMaxPasswordLength#"</FONT> <br>
      onvalidate=<FONT COLOR=BLUE>"validatePassword"</FONT> <br>
  message=<FONT COLOR=BLUE>"You must provide a valid password"</FONT>&gt;</FONT><br>
<br>
function validatePassword(formObject,fieldObject,fieldValue) {<br>
  var strRegExpression = /^\w*(?=\w*\d)(?=\w*[A-Za-z])\w*$/<br>
       var intMinPasswordLength = <FONT COLOR=MAROON>&lt;cfoutput&gt;</FONT>#intMinPasswordLength#<FONT COLOR=MAROON>&lt;/cfoutput&gt;</FONT>;<br>
 var intMaxPasswordLength = <FONT COLOR=MAROON>&lt;cfoutput&gt;</FONT>#intMaxPasswordLength#<FONT COLOR=MAROON>&lt;/cfoutput&gt;</FONT>;<br>
 return (fieldValue.length &gt;= intMinPasswordLength && fieldValue.length &lt;= intMaxPasswordLength && strRegExpression.test(fieldValue))<br>
}</div>