---
layout: default
title: "Resetting your Identity Column (SQL Server)"
permalink: /2004/08/26/Resetting-your-Identity-Column-SQL-Server-/
---

<DIV class=body>Just a handy little bit of SQL for when you need to reset an Identity column back to it's initial starting value. 
<P>
<DIV class=code>DBCC CHECKIDENT ('tablename',RESEED,<FONT color=blue>0</FONT>)</DIV>
<P>Useful for when you want to re-initialise your identity columns after testing.</P></DIV>