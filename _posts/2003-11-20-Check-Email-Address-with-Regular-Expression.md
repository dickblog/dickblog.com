---
layout: default
title: "Check Email Address with Regular Expression"
permalink: /2003/11/20/Check-Email-Address-with-Regular-Expression/
---

<div class="code"><FONT COLOR=MAROON>&lt;cfset strEmailPattern=<FONT COLOR=BLUE>"^['_A-Za-z0-9-]+(\.['_A-Za-z0-9-]+)*@[A-Za-z0-9-]+(\.[A-Za-z0-9-]+)*\.(([A-Za-z]{2,<FONT COLOR=BLUE>3</FONT>})|(aero|coop|info|museum|name))$"</FONT>&gt;</FONT><br>
...<br>
<FONT COLOR=MAROON>&lt;cfinput name=<FONT COLOR=BLUE>"strWorkEmailAddress"</FONT> <br>
    type=<FONT COLOR=BLUE>"text"</FONT> id=<FONT COLOR=BLUE>"strWorkEmailAddress"</FONT> <br>
   required=<FONT COLOR=BLUE>"yes"</FONT> validate=<FONT COLOR=BLUE>"regular_expression"</FONT> <br>
   pattern=<FONT COLOR=BLUE>"#strEmailPattern#"</FONT> maxlength=<FONT COLOR=BLUE>"50"</FONT> <br>
     message=<FONT COLOR=BLUE>"A valid work email address in the right format is required"</FONT>&gt;</FONT></div>