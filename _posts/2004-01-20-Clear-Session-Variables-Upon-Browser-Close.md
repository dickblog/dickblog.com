---
layout: default
title: "Clear Session Variables Upon Browser Close"
permalink: /2004/01/20/Clear-Session-Variables-Upon-Browser-Close/
---

<P>The following will clear all the session variables when the <STRONG>browser</STRONG> is closed. Beware, a browser can have several <STRONG>windows</STRONG>, so a window isn't always a <STRONG>browser</STRONG>.</p>

<div class="code"><FONT COLOR=MAROON>&lt;cfif IsDefined(<FONT COLOR=BLUE>"cookie.cfid"</FONT>) AND IsDefined(<FONT COLOR=BLUE>"cookie.cftoken"</FONT>)&gt;</FONT><br>
<FONT COLOR=MAROON>&lt;cfcookie name=<FONT COLOR=BLUE>"cfid"</FONT> value=<FONT COLOR=BLUE>"#cookie.cfid#"</FONT>&gt;</FONT><br>
<FONT COLOR=MAROON>&lt;cfcookie name=<FONT COLOR=BLUE>"cftoken"</FONT> value=<FONT COLOR=BLUE>"#cookie.cftoken#"</FONT>&gt;</FONT><br>
<FONT COLOR=MAROON>&lt;/cfif&gt;</FONT></div>

ColdFusion uses two cookies set on the user's computer, CFID and CFTOKEN, to tie them to a set of session variables. By default, these two cookies are set to never expire. By re-saving the cookies with the same name and value, any existing session variables will be maintained but the browser will set the cookies to automatically delete when the browser closes. If the user opens their browser back up and goes back to your page, the Cold Fusion server detects that there is no CFID/CFTOKEN cookies set and will generate a new combination - thus a new session.</P>
<P>It's worth checking out this <A class="" href="http://www.macromedia.com/support/coldfusion/ts/documents/tn17915.htm" target=_blank>Macromedia TechNote</A> for a detailed explanation of this and the new <A class="" href="http://www.macromedia.com/support/coldfusion/ts/documents/tn18232.htm" target=_blank>J2EE session management</A>&nbsp;in CFMX.</P>