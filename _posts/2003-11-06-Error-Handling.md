---
layout: default
title: "Error Handling"
permalink: /2003/11/06/Error-Handling/
---

<P>There may well be an error in your CFMAIL code or settings. When an error <BR>is generated inside of a CFERROR error handler, an error is thrown that <BR>cannot be caught with TYPE="Exception." It can only be caught by <BR>TYPE="Request" which does not allow the use of CFML. So you should do two <BR>things: <BR><BR>1. Change your Application.cfm to look like: <BR>&lt;CFERROR TYPE="Exception" TEMPLATE="error.cfm" MAILTO="admin@mydomain.com"&gt; <BR>&lt;CFERROR TYPE="Request" TEMPLATE="fatalError.cfm"&gt; <BR><BR>2. Debug your CFMAIL code/settings based on the gray-box CF error that is <BR>currently being shown. </P>
<HR>

<P>Or use this method...</P>
<P><A href="http://tutorial108.easycfm.com/" target=_blank>http://tutorial108.easycfm.com/</A></P>
<P>Trap Request type errors by pointing CFERROR to an intermediate page that gathers the error scope variables into hidden fields in a form and then submits them to a fully featured error handling page like this...</P>


<div class="code"><FONT COLOR=NAVY>&lt;html&gt;</FONT><br>
<FONT COLOR=NAVY>&lt;head&gt;</FONT><br>
<FONT COLOR=NAVY>&lt;meta http-equiv=<FONT COLOR=BLUE>"Content-Type"</FONT> content=<FONT COLOR=BLUE>"text/html; charset=iso-8859-1"</FONT>&gt;</FONT><br>
<FONT COLOR=NAVY>&lt;/head&gt;</FONT><br>
<FONT COLOR=NAVY>&lt;body onLoad=<FONT COLOR=BLUE>"document.forms[0].submit();"</FONT>&gt;</FONT><br>
<FONT COLOR=NAVY><FONT COLOR=FF8000>&lt;form name=<FONT COLOR=BLUE>"forError"</FONT> id=<FONT COLOR=BLUE>"forError"</FONT> action=<FONT COLOR=BLUE>"error/error.cfm"</FONT> method=<FONT COLOR=BLUE>"post"</FONT>&gt;</FONT></FONT><br>
  <FONT COLOR=NAVY><FONT COLOR=FF8000>&lt;input type=<FONT COLOR=BLUE>"hidden"</FONT> name=<FONT COLOR=BLUE>"browser"</FONT> value=<FONT COLOR=BLUE>"#error.Browser#"</FONT>&gt;</FONT></FONT><br>
    <FONT COLOR=NAVY><FONT COLOR=FF8000>&lt;input type=<FONT COLOR=BLUE>"hidden"</FONT> name=<FONT COLOR=BLUE>"datetime"</FONT> value=<FONT COLOR=BLUE>"#error.DateTime#"</FONT>&gt;</FONT></FONT><br>
  <FONT COLOR=NAVY><FONT COLOR=FF8000>&lt;input type=<FONT COLOR=BLUE>"hidden"</FONT> name=<FONT COLOR=BLUE>"diagnostics"</FONT> value=<FONT COLOR=BLUE>"#error.Diagnostics#"</FONT>&gt;</FONT></FONT><br>
    <FONT COLOR=NAVY><FONT COLOR=FF8000>&lt;input type=<FONT COLOR=BLUE>"hidden"</FONT> name=<FONT COLOR=BLUE>"httpreferer"</FONT> value=<FONT COLOR=BLUE>"#error.HTTPReferer#"</FONT>&gt;</FONT></FONT><br>
    <FONT COLOR=NAVY><FONT COLOR=FF8000>&lt;input type=<FONT COLOR=BLUE>"hidden"</FONT> name=<FONT COLOR=BLUE>"mailto"</FONT> value=<FONT COLOR=BLUE>"#error.MailTo#"</FONT>&gt;</FONT></FONT><br>
      <FONT COLOR=NAVY><FONT COLOR=FF8000>&lt;input type=<FONT COLOR=BLUE>"hidden"</FONT> name=<FONT COLOR=BLUE>"querystring"</FONT> value=<FONT COLOR=BLUE>"#error.QueryString#"</FONT>&gt;</FONT></FONT><br>
    <FONT COLOR=NAVY><FONT COLOR=FF8000>&lt;input type=<FONT COLOR=BLUE>"hidden"</FONT> name=<FONT COLOR=BLUE>"remoteaddress"</FONT> value=<FONT COLOR=BLUE>"#error.RemoteAddress#"</FONT>&gt;</FONT></FONT><br>
        <FONT COLOR=NAVY><FONT COLOR=FF8000>&lt;input type=<FONT COLOR=BLUE>"hidden"</FONT> name=<FONT COLOR=BLUE>"template"</FONT> value=<FONT COLOR=BLUE>"#error.Template#"</FONT>&gt;</FONT></FONT><br>
<FONT COLOR=NAVY><FONT COLOR=FF8000>&lt;/form&gt;</FONT></FONT><br>
<FONT COLOR=NAVY>&lt;/body&gt;</FONT><br>
<FONT COLOR=NAVY>&lt;/html&gt;</FONT></div>



<P>
<HR>

<P></P>
<P></P>
<P>Order the CFERROR tags in the Application.cfm like this...</P>

<div class="code"><FONT COLOR=MAROON>&lt;cferror type=<FONT COLOR=BLUE>"exception"</FONT> template=<FONT COLOR=BLUE>"error/dspException.cfm"</FONT> exception=<FONT COLOR=BLUE>"any"</FONT> mailto=<A HREF="mailto:spam@spaminc.com">spam@spaminc.com</A>&gt;</FONT><br>
<FONT COLOR=MAROON>&lt;cferror type=<FONT COLOR=BLUE>"request"</FONT>   template=<FONT COLOR=BLUE>"error/actCatchRequestError.cfm"</FONT> mailto=<FONT COLOR=BLUE>"<A HREF="mailto:spam@spaminc.com">spam@spaminc.com</A>"</FONT>&gt;</FONT></div>

<P>The first CFERROR traps any exception type errors and the second CFERROR acts as a backstop for any other type of error.</P>