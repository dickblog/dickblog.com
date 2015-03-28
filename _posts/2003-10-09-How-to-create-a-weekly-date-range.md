---
layout: default
title: "How to create a weekly date range"
permalink: /2003/10/09/How-to-create-a-weekly-date-range/
---

<P>This is great for creating weekly reports. For example, your boss wants you to create a tool to track project information, time worked, etc. He/she wants to be able to view a week at a time.</P><PRE>&lt;!--- Initialize a default date value, if none is provided ---&gt;<BR>&lt;CFPARAM NAME="TheDate" DEFAULT="#NOW()#"&gt;</PRE><PRE>&lt;!--- Get the start and end date of the date value passed ---&gt;<BR>&lt;CFSET WeekStart=DateAdd("d",-(DayOfWeek(TheDate)-1),TheDate)&gt;<BR>&lt;CFSET WeekEnd=DateAdd("d",6,WeekStart)&gt;</PRE><PRE>&lt;!--- Get the values using 'BETWEEN' ---&gt;<BR>&lt;CFQUERY DATASOURCE="myDSN" NAME="getItemsByDate"&gt;<BR>	SELECT fields<BR>	FROM table<BR>	WHERE dateField BETWEEN #WeekStart# AND #WeekEnd#<BR>	ORDER BY dateField DESC<BR>&lt;/CFQUERY&gt;</PRE>