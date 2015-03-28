---
layout: default
title: "Precomplie CF Folder"
permalink: /2003/08/09/Precomplie-CF-Folder/
---

<P>Try this from Charlie Arehart's Blog</P><PRE>set MX_INSTALL=c:\CFusionMX<BR>set PATH=%MX_INSTALL%\runtime\bin;%MX_INSTALL%\runtime\jre\bin;%PATH%<BR>java -classpath %MX_INSTALL%\lib\cfusion.jar coldfusion.tools.Compiler<BR>	-webroot %1 -webinf %MX_INSTALL%\wwwroot\WEB-INF %1<BR></PRE>
<P><A href="http://www.cfmxplus.blogspot.com/2002_12_08_cfmxplus_archive.html" target=_blank>http://www.cfmxplus.blogspot.com/2002_12_08_cfmxplus_archive.html</A></P>