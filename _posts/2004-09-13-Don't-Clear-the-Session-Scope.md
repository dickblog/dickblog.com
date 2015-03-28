---
layout: default
title: "Don't Clear the Session Scope"
permalink: /2004/09/13/Don't-Clear-the-Session-Scope/
---

<P>I came across this <A class="" href="http://www.macromedia.com/support/coldfusion/ts/documents/tn17479.htm" target=_blank>Macromedia TechNote</A> the other day. It says "don't clear the session scope as you'll kill the system generated CFTOKEN etc."</P>
<P>The best solution from the TechNote is to copy the system sessions into a temp structure and put them back after the STRUCTCLEAR(session)...</P>

<div class="code"><FONT COLOR=GRAY><I>&lt;!--- Copy the important values. ---&gt;</I></FONT><br>
<FONT COLOR=MAROON>&lt;CFLOCK SCOPE=<FONT COLOR=BLUE>"Session"</FONT> TYPE=<FONT COLOR=BLUE>"ReadOnly"</FONT> TIMEOUT=60&gt;</FONT><br>
<FONT COLOR=MAROON>&lt;CFSET Temp = StructNew()&gt;</FONT><br>
<FONT COLOR=MAROON>&lt;CFSET Temp.CFID = Session.CFID&gt;</FONT><br>
<FONT COLOR=MAROON>&lt;CFSET Temp.CFTOKEN = Session.CFTOKEN&gt;</FONT><br>
<FONT COLOR=MAROON>&lt;CFSET Temp.SESSIONID = Session.SESSIONID&gt;</FONT><br>
<FONT COLOR=MAROON>&lt;CFSET Temp.URLTOKEN = Session.URLTOKEN&gt;</FONT><br>
<FONT COLOR=MAROON>&lt;/CFLOCK&gt;</FONT><br>
<FONT COLOR=GRAY><I>&lt;!--- Kill the session ---&gt;</I></FONT><br>
<FONT COLOR=MAROON>&lt;CFLOCK SCOPE=<FONT COLOR=BLUE>"Session"</FONT> TYPE=<FONT COLOR=BLUE>"Exclusive"</FONT> TIMEOUT=60&gt;</FONT><br>
<FONT COLOR=MAROON>&lt;CFSET StructClear(Session)&gt;</FONT><br>
<FONT COLOR=MAROON>&lt;/CFLOCK&gt;</FONT><br>
<FONT COLOR=GRAY><I>&lt;!--- Restore the important values. ---&gt;</I></FONT><br>
<FONT COLOR=MAROON>&lt;CFLOCK SCOPE=<FONT COLOR=BLUE>"Session"</FONT> TYPE=<FONT COLOR=BLUE>"ReadOnly"</FONT> TIMEOUT=60&gt;</FONT><br>
<FONT COLOR=MAROON>&lt;CFSET Session.CFID = Temp.CFID&gt;</FONT><br>
<FONT COLOR=MAROON>&lt;CFSET Session.CFTOKEN = Temp.CFTOKEN&gt;</FONT><br>
<FONT COLOR=MAROON>&lt;CFSET Session.SESSIONID = Temp.SESSIONID&gt;</FONT><br>
<FONT COLOR=MAROON>&lt;CFSET Session.URLTOKEN = Temp.URLTOKEN&gt;</FONT><br>
<FONT COLOR=MAROON>&lt;/CFLOCK&gt;</FONT></div>


<P>Looks good to me!</P>