---
layout: default
title: "Validating Variables For Queries"
permalink: /2003/09/23/Validating-Variables-For-Queries/
---

<P><A name=validatingvars></A>Running dynamic queries by using variables passed in a form or URL string is common enough, but what happens when a malicious user modifies those values? If userID is passed on the URL string, it could be anything, including something like "?userID=14%3BDROP%20TABLE%20users" Which would be outputted as "SELECT * FROM users WHERE userID=14;DROP TABLE users" In SQL Server this SQL statement would drop the users table, which would erase all the data stored inside. How do you get around that? By using the val() function or using &lt;cfqueryparam&gt;. <BR>


<div class="code"><FONT COLOR=MAROON>&lt;cfquery name=<FONT COLOR=BLUE>"userDetail"</FONT> datasource=<FONT COLOR=BLUE>"#request.DSN#"</FONT>&gt;</FONT><br>
SELECT * FROM users WHERE productID=#val(attributes.productID)#<br>
<FONT COLOR=MAROON>&lt;/cfquery&gt;</FONT></div>

or

<div class="code"><FONT COLOR=MAROON>&lt;cfquery name=<FONT COLOR=BLUE>"userDetail"</FONT> datasource=<FONT COLOR=BLUE>"#request.DSN#"</FONT>&gt;</FONT><br>
SELECT * FROM users WHERE productID= <FONT COLOR=MAROON>&lt;cfqueryparam value=<FONT COLOR=BLUE>"#attributes.userID#"</FONT> cfsqltype=<FONT COLOR=BLUE>"CF_SQL_INTEGER"</FONT>&gt;</FONT><br>
<FONT COLOR=MAROON>&lt;/cfquery&gt;</FONT></div>