---
layout: default
title: "Install Pre-Requisites"
permalink: /2004/11/16/Install-Pre-Requisites/
---

<P>Had this prob on a recent install on a clean W2K machine...</P>
<P>"...msvcp60.dll&nbsp; not found..."</P>
<P>Had me stumpted for a long time. Eventually found a copy of the DLL and added it to the system path.</P>
<P>But then today I read this in the <A class="" href="http://livedocs.macromedia.com/coldfusion/6.1/htmldocs/intro5.htm" target=_blank>install system requirments doc's</A>...</P>
<P>"To install ColdFusion MX in Windows NT 4.0, or Windows 2000, Windows XP, or Windows 2003, you must already have the following components installed: MDAC 2.6 SP2 (<A href="http://www.microsoft.com/data/download.htm" target=_blank>www.microsoft.com/data/download.htm</A>) and the Microsoft Visual C++ 6.0 runtime <A href="http://support.microsoft.com/default.aspx?scid=kb;en-us;259403" target=_blank>http://support.microsoft.com/default.aspx?scid=kb;en-us;259403</A>)."</P>
<P>The additional livedocs comment...</P>
<P>"After you install the Visual C++ 6.0 runtime components, you must manually copy msvcp60.dll from the install directory to the system32 Directory.</P>
<P>...</P>
<P>From the MSVC runtime, you also need msvcrt.dll.<BR><BR>Runtime modules should be in the windows\system32 directory (this might also be named WINNT\system32). "</P>