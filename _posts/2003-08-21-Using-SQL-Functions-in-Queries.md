---
layout: default
title: "Using SQL Functions in Queries"
permalink: /2003/08/21/Using-SQL-Functions-in-Queries/
---

<P>We came across a curious error that seems tied to the use of a SQL columname in a SQL function. </P>
<P>The following syntax:<BR>
<UL>select *, {fn mid(postingdatetime,6,10)} as xdate </UL>
<P>It got the error: </P>
<UL>Undefined function 'mid' in expression. </UL>
<P>After some research, we tried the following modification, in which the columnname "postingdatetime" was enclosed within a pair of brackets, as </P>
<UL>select *, {fn mid([postingdatetime],6,10)} as xdate </UL>
<P>This solved the problem. Apparently, the columnname was causing an interaction with the ODBC driver, perhaps even an interaction with CF's processing of the query. Anyway, the brackets solved the problem. </P>
<P>This happened to be in Access, but while the error arose in one server's Access 97 driver, it did not occur in anothers. There was a slight difference in versions of the driver, but the solution works in both, so let this be a warning for folks. </P>