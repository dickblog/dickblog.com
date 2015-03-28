---
layout: default
title: "Did that SQL DELETE Really Work?"
permalink: /2004/05/11/Did-that-SQL-DELETE-Really-Work?/
---

<P>Here's a neat trick. Say you issue an SQL DELETE via CFQUERY. How many rows did it <STRONG>actually</STRONG> get rid of? Take a look at <A class="" href="http://cephas.net/blog/2004/05/10/coldfusion_mx_and_javasql.html" target=_blank>Aaron Johnson's</A> blog idea.</P>
<P>If the site dies, here's the raw code:</P>


<div class="code"><FONT COLOR=MAROON>&lt;cfscript&gt;</FONT><br>
clazz = CreateObject(<FONT COLOR=BLUE>"java"</FONT>, <FONT COLOR=BLUE>"java.lang.Class"</FONT>);<br><FONT COLOR=GRAY><I>
// replace the package/class name of your db driver</I></FONT><br>
clazz.forName(<FONT COLOR=BLUE>"org.gjt.mm.mysql.Driver"</FONT>);<br>
driverManager = CreateObject(<FONT COLOR=BLUE>"java"</FONT>, <FONT COLOR=BLUE>"java.sql.DriverManager"</FONT>);<br><FONT COLOR=GRAY><I>
// replace w/ your server, database name, username & password</I></FONT><br>
conurl = <FONT COLOR=BLUE>"jdbc:<A TARGET="_blank" HREF="mysql://server/db?user=u&password=p">mysql://server/db?user=u&password=p</A>"</FONT>;<br>
connection = driverManager.getConnection(conurl);<br>
query = <FONT COLOR=BLUE>"DELETE from category where id = 3045"</FONT>;<br>
preparedStatement = connection.prepareStatement(query);<br>
result = preparedStatement.executeUpdate();<br>
WriteOutput(<FONT COLOR=BLUE>"result = "</FONT> & result); <br>
connection.close();<br>
<FONT COLOR=MAROON>&lt;/cfscript&gt;</FONT></div>

<P>Tested by...</P>

<div class="code">if (result == <FONT COLOR=BLUE>"0"</FONT>) {<br>
     WriteOutput(<FONT COLOR=BLUE>"No records were deleted."</FONT>);<br>
} else if (result == <FONT COLOR=BLUE>"1"</FONT>) {<br>
     WriteOutput(<FONT COLOR=BLUE>"One record was deleted."</FONT>);<br>
} else {<br>
     WriteOutput(result & <FONT COLOR=BLUE>" records were deleted."</FONT>);<br>
}</div>