---
layout: default
title: "Browser Authenication and CFLOGIN"
permalink: /2003/09/20/Browser-Authenication-and-CFLOGIN/
---

<P>I've been struggling with getting browser authenication working with the new CFLOGIN framework. I can get the username/password challenge up but it never seems to complete even if I do give it the right password! </P>
<P>Then I found <A class="" href="http://webforums.macromedia.com/coldfusion/messageview.cfm?catid=3&amp;threadid=567678" target=_blank>this</A> on the ColdFusion forum. The missing link was just to have "Anonymous access" checked in the directory security under IIS for the domain concerned. </P>
<P>Easy when when you know how! </P>
<P>Thanks to "aki_gunnar" from the ColdFusion forums.</P>