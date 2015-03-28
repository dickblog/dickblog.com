---
layout: default
title: "Re-running the Setup Wizard in CFMX"
permalink: /2004/06/11/Re-running-the-Setup-Wizard-in-CFMX/
---

<P>Macromedia just published a new Tech Note that shows <A href="http://www.macromedia.com/support/coldfusion/ts/documents/rerun_install_wizards.htm" target=_blank>how to re-run the setup wizard</A> by editing one of the XML configuration files. This can be useful to re-install the ODBC services or migrate settings from another installation.</P>
<P>Also found this from MM about <A class="" href="http://www.macromedia.com/support/coldfusion/ts/documents/cfmx_sequelink.htm#drive" target=_blank>reinstalling CFMX</A>.</P>
<P>Seem like where the ODBC Server and ODBC Agent services, used by ColdFusion to allow connections to ODBC datasources would not start.</P>
<P>This issue is when ColdFusion isinstalled on the D drive of this machine. Apparently, when you install/upgrade CFMX on a drive other than C (Windows), the .ini files used by the two services in question get incorrect drive/directory references. </P>
<P>The solution for the problem is to do a search and replace all instances of: 
<P>C:\Program Files\Merant\ 
<P>with 
<P>D:\CFusionMX 
<P>in the directory D:\CFusionMX\db\slserver52 and all of its subdirectories. This assumes your install is on the D drive.</P>