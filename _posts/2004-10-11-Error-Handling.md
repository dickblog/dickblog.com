---
layout: default
title: "Error Handling"
permalink: /2004/10/11/Error-Handling/
---

<P>I'm forever forgetting how ColdFusion handles error, so I thought I'd better capture here my thoughts.</P>
<P>This will be a work, constantly, in progress as a add bit from time to time as I remember issues/solutions.</P>
<H3>Order of Precedence</H3>
<OL>
<LI><FONT size=2>CFTRY/CFCATCH<BR><BR></FONT></LI>
<LI><FONT size=2>CFERROR TYPE="Exception"<BR><BR></FONT></LI>
<LI><FONT size=2>Site-Wide Error Handler<BR><BR></FONT></LI>
<LI><FONT size=2>CFERROR TYPE="Request"</LI></OL></FONT>
<H3>CFTRY/CFCATCH</H3>
<P>Always bracket any potentially dodgy code with a CFTRY/CFCATCH. This includes any file interaction (CFFILE, CFFTP etc) and maybe database calls which may fail for any known reason. So bracket the code with a CFTRY and then CFCATCH all the possible exception types.</P>
<P>Within the CFCATCH you can try and handle the error in the most appropriate way. This could be a simple step-over or a manual generation of data which allows the application to proceed. You can, of course, have different CFCATCH blocks to handle the different types of errors your application could throw.</P>
<H3>CFERROR: General Notes</H3>
<P>The best place for your CFERROR tag is in your Application.cfm script. There can be script by script exceptions to this, but this will be determined my your application.</P>
<H3>CFERROR TYPE="Exception"</H3>
<P>Creating a CFERROR TYPE="Exception" in your Application.cfm will override the Site-Wide error handler as specified in the ColdFusion Administrator.</P>
<H3>ColdFusion Administrator: Site-Wide Error Handler.</H3>
<P>This one is a little m<FONT size=2>isnomer</FONT>. It's not site-wide it's server-wide. All sites hosted on your server will be governed by this setting.</P>
<P>All servers should/must have a Site-Wide error handler. It's the really the last back-stop to ensure that the default ColdFusion page, which is ugly and full of detailed information,&nbsp;is hidden from your visitors and hackers!</P>
<H3>Other References Sources</H3>
<UL>
<LI><A class="" href="http://www.sys-con.com/coldfusion/article.cfm?id=412" target=_blank>Ben Forta, of course</A></LI>
<LI><A class="" href="http://www.houseoffusion.com/error.ppt" target=_blank>House of Fusion</A></LI></UL>