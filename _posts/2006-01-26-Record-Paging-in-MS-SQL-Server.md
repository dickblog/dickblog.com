---
layout: default
title: "Record Paging in MS SQL Server"
permalink: /2006/01/26/Record-Paging-in-MS-SQL-Server/
---

MySQL has always had a great clause in the SELECT function called LIMIT which allows you to get to a subset of records in the db. MS SQL Server doesn't have that. <br/><br/>I found <a href="http://josephlindsay.com/archives/2005/05/27/paging-results-in-ms-sql-server/" target="_blank">this blog entry</a> which also directed me to <a href="http://msdn.microsoft.com/library/default.asp?url=/library/en-us/dnpag/html/scalenethowto05.asp" target="_blank">this MS TechNote</a> which seems to offer a soluction.<br/><br/>Here's the code:<br/><br/><pre class="code">SELECT TOP &lt;pageSize&gt; CustomerID,CompanyName,ContactName,ContactTitle<br/>  FROM<br/>  (SELECT TOP &lt;currentPageNumber * pageSize&gt; <br/>          CustomerID,CompanyName,ContactName,ContactTitle <br/>   FROM <br/>     Customers AS T1 ORDER BY ContactName ASC)<br/>  AS T2 ORDER BY ContactName DESC</pre><br/>