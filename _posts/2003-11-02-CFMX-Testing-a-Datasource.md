---
layout: default
title: "CFMX: Testing a Datasource"
permalink: /2003/11/02/CFMX-Testing-a-Datasource/
---

<P>Need to test a datasource? Try this...</P>

<div class="code"><FONT COLOR=MAROON>&lt;cftry&gt;</FONT><br>
<FONT COLOR=MAROON>&lt;cfset result=<FONT COLOR=BLUE>"true"</FONT>&gt;</FONT><br>
<FONT COLOR=MAROON>&lt;cfset resuly=ds.verifyDatasource(<FONT COLOR=BLUE>"dsn"</FONT>)&gt;</FONT><br>
<FONT COLOR=MAROON>&lt;cfcatch type=<FONT COLOR=BLUE>"any"</FONT>&gt;</FONT><br>
<FONT COLOR=MAROON>&lt;cfset result=<FONT COLOR=BLUE>"false"</FONT>&gt;</FONT><br>
<FONT COLOR=MAROON>&lt;/cfcatch&gt;</FONT><br>
<FONT COLOR=MAROON>&lt;cftry&gt;</FONT></div>