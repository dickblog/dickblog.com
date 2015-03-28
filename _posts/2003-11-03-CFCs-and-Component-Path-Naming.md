---
layout: default
title: "CFCs and Component Path Naming"
permalink: /2003/11/03/CFCs-and-Component-Path-Naming/
---

<P>I've been having prob's getting the path naming of components right for CFCs recently.</P>
<P>The issue has been around the concept of the web root for my multi-homed server. The location "/" isn't at the root of the current domain, it's at the root of the webserver as controlled by the mapping of "/" in the CF Administrator. </P>
<P>So remember, when you're building up the dot notation path from the&nbsp;web root to the location of the CFC you want to instantiate, it's not from the domain root but from the CF mapping of the root.</P>
<P>One other thing to note is that if you have a dot in the path you can use the "/" as a separator.</P>
<P>Also you can store ColdFusion components in a variety of places in your application. <SPAN class=caps>CFMX</SPAN> looks through these addresses in a particular order to find the <SPAN class=caps>CFC.</SPAN></P>
<UL>
<LI>Local Folder; the same folder as the template attempting to instantiate the <SPAN class=caps>CFC<BR></SPAN></LI>
<LI><SPAN class=caps></SPAN>CFMAPPING; ColdFusion mappings (which are not the same as web server virtuals) are set up and configured the ColdFusion administrator<BR></LI>
<LI>Web Root of your application<BR></LI>
<LI>Custom Tag Paths; also set up in the <SPAN class=caps>CF</SPAN> administrator</LI></UL>