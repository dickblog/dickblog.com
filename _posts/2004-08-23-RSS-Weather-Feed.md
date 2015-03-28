---
layout: default
title: "RSS Weather Feed"
permalink: /2004/08/23/RSS-Weather-Feed/
---

<p>I found this code on <a class="" href="http://www.andyjarrett.co.uk/andy/blog/index.cfm?mode=entry&amp;entry=7B6BE137-3048-28EB-0E9F41A44B9CB5A1" target="_blank">Andy Jarrett's blog</a>&nbsp;which feeds off of a <a class="" href="http://www.rssweather.com/dir/Europe/United%20Kingdom/" target="_blank">RSSWeather</a> feed...</p>
<div class="code"><font color="MAROON">&lt;cfcomponent hint=<font color="BLUE">&quot;Return the weather&quot;</font>&gt;</font><br/>
&nbsp;&nbsp;&nbsp;&lt;!---<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Author: &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Andy Jarrett - <a href="mailto:mail@andyjarrett.co.uk">mail@andyjarrett.co.uk</a><br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Created:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;20/08/04<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Desciption: Returns the weather for you area from a RSS feed<br/>
&nbsp;&nbsp;&nbsp;---&gt;<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<br/>
&nbsp;&nbsp;&nbsp;<font color="MAROON">&lt;cffunction name=<font color="BLUE">&quot;myWeather&quot;</font> returntype=<font color="BLUE">&quot;struct&quot;</font> hint=<font color="BLUE">&quot;Returns the weather from <a target="_blank" href="http://www.rssweather.com">http://www.rssweather.com</a>&quot;</font> &gt;</font><br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<font color="GRAY"><i>&lt;!--- Basic vars needed ---&gt;</i></font><br/>
<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<font color="MAROON">&lt;cfset var weatherRss = <font color="BLUE">&quot;<a target="_blank" href="http://www.rssweather.com/rss.php?config=&amp;forecast=zandh&amp;icao=EGHI&amp;alt=rss20a">http://www.rssweather.com/rss.php?config=&amp;forecast=zandh&amp;icao=EGHI&amp;alt=rss20a</a>&quot;</font>&gt;</font><br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<font color="MAROON">&lt;cfset var weatherXML = <font color="BLUE">&quot;&quot;</font>&gt;</font><br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<font color="MAROON">&lt;cfset var weatherToday = structNew()&gt;</font><br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<font color="MAROON">&lt;cfif NOT isDefined(<font color="BLUE">&quot;application.weatherXML.lastParsed&quot;</font>) OR NOW() GT dateAdd(<font color="BLUE">&quot;H&quot;</font>,<font color="BLUE"> 3</font>, application.weatherXML.lastParsed)&gt;</font><br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<font color="GRAY"><i>&lt;!--- Get feed ---&gt;</i></font><br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<font color="MAROON">&lt;cfhttp url=<font color="BLUE">&quot;#weatherRss#&quot;</font> method=<font color="BLUE">&quot;GET&quot;</font>&gt;</font><font color="MAROON">&lt;/cfhttp&gt;</font><br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<font color="GRAY"><i>&lt;!--- You need to know the reason it was last parsed because you will get<br/>banned if you hit several times within the hour. ---&gt;</i></font><br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<font color="MAROON">&lt;cfset application.weatherXml.lastParsed = NOW()&gt;</font><br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<font color="MAROON">&lt;cfset application.weatherXml.parsed = xmlParse(cfhttp.filecontent)&gt;</font><br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<font color="MAROON">&lt;/cfif&gt;</font><br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<font color="MAROON">&lt;cfscript&gt;</font><br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;weatherXML = application.weatherXml.parsed;<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;weatherToday.text = weatherXML.rss.channel.item.description.xmlText;<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;weatherToday.link = weatherXML.rss.channel.item.link.xmlText;<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<font color="MAROON">&lt;/cfscript&gt;</font><br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<font color="MAROON">&lt;cfreturn weatherToday&gt;</font><br/>
&nbsp;&nbsp;&nbsp;<font color="MAROON">&lt;/cffunction&gt;</font>&nbsp;&nbsp;&nbsp;<br/>
<font color="MAROON">&lt;/cfcomponent&gt;</font></div>