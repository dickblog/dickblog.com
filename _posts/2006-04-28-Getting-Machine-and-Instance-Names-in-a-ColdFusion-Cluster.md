---
layout: default
title: "Getting Machine and Instance Names in a ColdFusion Cluster"
permalink: /2006/04/28/Getting-Machine-and-Instance-Names-in-a-ColdFusion-Cluster/
---

From <a href="http://willychang.coldfusionjournal.com/how_to_find_an_instance_name_or_machine_name_in_a_cfmx_clust.htm" target="_blank">Will.Chang</a>

<code>
<cfscript>
machineName = createObject("java", "java.net.InetAddress").localhost.getHostName();
// get this instance name
instanceName   = createObject("java", "jrunx.kernel.JRun").getServerName();
</cfscript>
<cfoutput>
Machine: #machineName#<br>
Instance: #instanceName#
</cfoutput>
</code>