---
layout: default
title: "Date Bind Variable CFSQLTYPE for CFQUERYPARAM"
permalink: /2004/03/25/Date-Bind-Variable-CFSQLTYPE-for-CFQUERYPARAM/
---

<P>I've recently been caught out by this one. When you have a database column of DateTime and you need to refer to it with CFQUERYPARAM for either a stored procedure or to counteract URL hacking/SQL injection you'd think you'd use the CFSQLType of "DATETIME". Nope, you should use "TIMESTAMP".</P>