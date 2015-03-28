---
layout: default
title: "Insert Autonumbers Without Autonumber Data Type"
permalink: /2003/09/09/Insert-Autonumbers-Without-Autonumber-Data-Type/
---

<p><a name="isNull pkeys"></a>Most people use their DB's auto-incremental integer data type to create new primary keys. In MS Access, it's an &quot;autonumber&quot; data type. In MS SQL Server, it's an integer data type with the &quot;Identity&quot; attribute set to &quot;1&quot;. </p>
<p>If you've ever had to migrate data from one database to another, you've probably noticed how those primary keys can get in the way sometimes. The trouble is that autonumbers can't be reused, even if the row is permanently deleted. </p>
<p>To combat this problem, you can do a lookup of the current highest number, along the lines of Steve Nelson's &lt;cf_maxID&gt; tag, or wrap a &quot;select max(ID)&quot; query with your insert query with &lt;cftransaction&gt;. </p>
<p>But we think those ways are a little hokey. Instead, use this syntax to let the DB create a new incremental primary key while inserting the new data - all in one query. <br/></p><p><a href="http://mkruger.cfwebtools.com/index.cfm?mode=alias&amp;alias=identity%203" target="_blank">READ THIS FIRST!</a><br/></p>
<div class="code"><font color="MAROON">&lt;cfquery name=<font color="BLUE">&quot;insert&quot;</font> datasource=<font color="BLUE">&quot;DSN&quot;</font>&gt;</font><br/>
INSERT INTO myTable        (autoID,         field1)<br/>
SELECT         IsNull(MAX(autoID),<font color="BLUE">0</font>)+1 AS autoID,         #attributes.field1# AS field1      FROM myTable<br/><font color="MAROON">&lt;/cfquery&gt;<br type="_moz"/></font></div>