---
layout: default
title: "Using Identity Keys in SQL Server"
permalink: /2003/08/12/Using-Identity-Keys-in-SQL-Server/
---

<p>Most applications rely on primary keys in database tables. Many of those same applications use the auto-increment capabilities of some DBMSes like MSSQL Server. When inserting a record in a table that uses auto-increment primary keys, you do not have to insert the value of the primary key yourself - the DB does it for you. But what if you want to know the value of the row's primary key that you just inserted? Commonly, developers will run two queries in a row, wrapped in &lt;cftransaction&gt;. The first one inserts the record and the second one selects the newest record. But using this syntax, SQL server can insert the record as well as return the value of the new primary key all in one query.<br/></p><p><a href="http://mkruger.cfwebtools.com/index.cfm?mode=alias&amp;alias=identity%203" target="_blank">READ THIS FIRST!</a><br type="_moz"/>
</p><div class="code"><font color="MAROON">&lt;cfquery name=<font color="BLUE">&quot;insert&quot;</font> datasource=<font color="BLUE">&quot;DSN&quot;</font>&gt;</font><br/>
set nocount on     insert into customer (firstName, lastName)     values     ('#attributes.firstName#', '#attributes.LastName#')     select @@identity as newID     set nocount off<br/>
<font color="MAROON">&lt;/cfquery&gt;</font>    <br/>
<br/>
I am the new primary key value:<br/><font color="MAROON">&lt;cfoutput&gt;</font>#insert.newID#<font color="MAROON">&lt;/cfoutput&gt;</font></div>