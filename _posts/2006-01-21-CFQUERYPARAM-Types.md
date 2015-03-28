---
layout: default
title: "CFQUERYPARAM Types"
permalink: /2006/01/21/CFQUERYPARAM-Types/
---

<table cellspacing="0" cellpadding="5" border="1">
	<tbody>
		<tr>
			<th valign="top"> ColdFusion </th>
			<th valign="top"> JDBC </th>
			<th valign="top"> DB2 </th>
			<th valign="top"> Informix </th>
			<th valign="top"> Oracle </th>
			<th valign="top">MS Access </th>
			<th valign="top"> MSSQL </th>
		</tr>
		<tr>
			<td valign="top"><p>CF_SQL_ARRAY</p></td>
			<td valign="top"><p>ARRAY</p></td>
			<td valign="top"><p>&nbsp;</p></td>
			<td valign="top"><p>&nbsp;</p></td>
			<td valign="top"><p>&nbsp;</p></td>
			<td valign="top">&nbsp;</td>
			<td valign="top"><p>&nbsp;</p></td>
		</tr>
		<tr>
			<td valign="top"><p>CF_SQL_BIGINT</p></td>
			<td valign="top"><p>BIGINT</p></td>
			<td valign="top"><p>Bigint</p></td>
			<td valign="top"><p>int8, serial8</p></td>
			<td valign="top"><p>&nbsp;</p></td>
			<td valign="top">Yes/No</td>
			<td valign="top"><p>&nbsp;</p></td>
		</tr>
		<tr>
			<td valign="top"><p>CF_SQL_BINARY</p></td>
			<td valign="top"><p>BINARY</p></td>
			<td valign="top"><p>Char for Bit Data</p></td>
			<td valign="top"><p>&nbsp;</p></td>
			<td valign="top"><p>&nbsp;</p></td>
			<td valign="top">&nbsp;</td>
			<td valign="top"><p>binary</p>
					<p>timestamp</p></td>
		</tr>
		<tr>
			<td valign="top"><p>CF_SQL_BIT</p></td>
			<td valign="top"><p>BIT</p></td>
			<td valign="top"><p>&nbsp;</p></td>
			<td valign="top"><p>boolean</p></td>
			<td valign="top"><p>&nbsp;</p></td>
			<td valign="top">&nbsp;</td>
			<td valign="top"><p>bit</p></td>
		</tr>
		<tr>
			<td valign="top"><p>CF_SQL_BLOB</p></td>
			<td valign="top"><p>BLOB</p></td>
			<td valign="top"><p>Blob</p></td>
			<td valign="top"><p>blob</p></td>
			<td valign="top"><p>blob, bfile</p></td>
			<td valign="top">&nbsp;</td>
			<td valign="top"><p>&nbsp;</p></td>
		</tr>
		<tr>
			<td valign="top"><p>CF_SQL_CHAR</p></td>
			<td valign="top"><p>CHAR</p></td>
			<td valign="top"><p>Char</p></td>
			<td valign="top"><p>char, </p>
					<p>nchar</p></td>
			<td valign="top"><p>char,</p>
					<p>nchar</p></td>
			<td valign="top">&nbsp;</td>
			<td valign="top"><p>char, nchar,</p>
					<p>unique<br/>
						identifier</p></td>
		</tr>
		<tr>
			<td valign="top"><p>CF_SQL_CLOB</p></td>
			<td valign="top"><p>CLOB</p></td>
			<td valign="top"><p>Clob</p></td>
			<td valign="top"><p>clob</p></td>
			<td valign="top"><p>clob,nclob</p></td>
			<td valign="top">&nbsp;</td>
			<td valign="top"><p>&nbsp;</p></td>
		</tr>
		<tr>
			<td valign="top"><p>CF_SQL_DATE</p></td>
			<td valign="top"><p>DATE</p></td>
			<td valign="top"><p>Date</p></td>
			<td valign="top"><p>date, datetime, year to day</p></td>
			<td valign="top"><p>&nbsp;</p></td>
			<td valign="top">&nbsp;</td>
			<td valign="top"><p>&nbsp;</p></td>
		</tr>
		<tr>
			<td valign="top"><p>CF_SQL_DECIMAL</p></td>
			<td valign="top"><p>DECIMAL</p></td>
			<td valign="top"><p>Decimal</p></td>
			<td valign="top"><p>decimal, money</p></td>
			<td valign="top"><p>number</p></td>
			<td valign="top">&nbsp;</td>
			<td valign="top"><p>decimal, money, small<br/>
				money</p></td>
		</tr>
		<tr>
			<td valign="top"><p>CF_SQL_DISTINCT</p></td>
			<td valign="top"><p>DISTINCT</p></td>
			<td valign="top"><p>&nbsp;</p></td>
			<td valign="top"><p>&nbsp;</p></td>
			<td valign="top"><p>&nbsp;</p></td>
			<td valign="top">&nbsp;</td>
			<td valign="top"><p>&nbsp;</p></td>
		</tr>
		<tr>
			<td valign="top"><p>CF_SQL_DOUBLE</p></td>
			<td valign="top"><p>DOUBLE</p></td>
			<td valign="top"><p>Double</p></td>
			<td valign="top"><p>&nbsp;</p></td>
			<td valign="top"><p>&nbsp;</p></td>
			<td valign="top">&nbsp;</td>
			<td valign="top"><p>&nbsp;</p></td>
		</tr>
		<tr>
			<td valign="top"><p>CF_SQL_FLOAT</p></td>
			<td valign="top"><p>FLOAT</p></td>
			<td valign="top"><p>Float</p></td>
			<td valign="top"><p>float</p></td>
			<td valign="top"><p>number</p></td>
			<td valign="top">&nbsp;</td>
			<td valign="top"><p>float</p></td>
		</tr>
		<tr>
			<td valign="top"><p>CF_SQL_IDSTAMP</p></td>
			<td valign="top"><p>CHAR</p></td>
			<td valign="top"><p>Char</p></td>
			<td valign="top"><p>char, nchar</p></td>
			<td valign="top"><p>char, nchar</p></td>
			<td valign="top">&nbsp;</td>
			<td valign="top"><p>char, nchar, unique<br/>
				identifier</p></td>
		</tr>
		<tr>
			<td valign="top"><p>CF_SQL_INTEGER</p></td>
			<td valign="top"><p>INTEGER</p></td>
			<td valign="top"><p>Integer</p></td>
			<td valign="top"><p>integer, serial</p></td>
			<td valign="top"><p>&nbsp;</p></td>
			<td valign="top">AutoNumber</td>
			<td valign="top"><p>int</p></td>
		</tr>
		<tr>
			<td valign="top"><p>CF_SQL_LONGVARBINARY</p></td>
			<td valign="top"><p>LONGVARBINARY</p></td>
			<td valign="top"><p>Long Varchar for Bit Data</p></td>
			<td valign="top"><p>byte</p></td>
			<td valign="top"><p>long raw</p></td>
			<td valign="top">&nbsp;</td>
			<td valign="top"><p>image</p></td>
		</tr>
		<tr>
			<td valign="top"><p>CF_SQL_LONGVARCHAR</p></td>
			<td valign="top"><p>LONGVARCHAR</p></td>
			<td valign="top"><p>Long Varchar</p></td>
			<td valign="top"><p>text</p></td>
			<td valign="top"><p>long</p></td>
			<td valign="top">Memo</td>
			<td valign="top"><p>text, ntext</p></td>
		</tr>
		<tr>
			<td valign="top"><p>CF_SQL_MONEY</p></td>
			<td valign="top"><p>DOUBLE</p></td>
			<td valign="top"><p>Double</p></td>
			<td valign="top"><p>&nbsp;</p></td>
			<td valign="top"><p>&nbsp;</p></td>
			<td valign="top">Currency</td>
			<td valign="top"><p>&nbsp;</p></td>
		</tr>
		<tr>
			<td valign="top"><p>CF_SQL_MONEY4</p></td>
			<td valign="top"><p>DOUBLE</p></td>
			<td valign="top"><p>Double</p></td>
			<td valign="top"><p>&nbsp;</p></td>
			<td valign="top"><p>&nbsp;</p></td>
			<td valign="top">&nbsp;</td>
			<td valign="top"><p>&nbsp;</p></td>
		</tr>
		<tr>
			<td valign="top"><p>CF_SQL_NULL</p></td>
			<td valign="top"><p>NULL</p></td>
			<td valign="top"><p>&nbsp;</p></td>
			<td valign="top"><p>&nbsp;</p></td>
			<td valign="top"><p>&nbsp;</p></td>
			<td valign="top">&nbsp;</td>
			<td valign="top"><p>&nbsp;</p></td>
		</tr>
		<tr>
			<td valign="top"><p>CF_SQL_NUMERIC</p></td>
			<td valign="top"><p>NUMERIC</p></td>
			<td valign="top"><p>Numeric</p></td>
			<td valign="top"><p>&nbsp;</p></td>
			<td valign="top"><p>&nbsp;</p></td>
			<td valign="top">Number</td>
			<td valign="top"><p>numeric</p></td>
		</tr>
		<tr>
			<td valign="top"><p>CF_SQL_OTHER</p></td>
			<td valign="top"><p>OTHER</p></td>
			<td valign="top"><p>&nbsp;</p></td>
			<td valign="top"><p>&nbsp;</p></td>
			<td valign="top"><p>&nbsp;</p></td>
			<td valign="top">&nbsp;</td>
			<td valign="top"><p>&nbsp;</p></td>
		</tr>
		<tr>
			<td valign="top"><p>CF_SQL_REAL</p></td>
			<td valign="top"><p>REAL</p></td>
			<td valign="top"><p>Real</p></td>
			<td valign="top"><p>smallfloat</p></td>
			<td valign="top"><p>&nbsp;</p></td>
			<td valign="top">&nbsp;</td>
			<td valign="top"><p>real</p></td>
		</tr>
		<tr>
			<td valign="top"><p>CF_SQL_REFCURSOR</p></td>
			<td valign="top"><p>REF</p></td>
			<td valign="top"><p>&nbsp;</p></td>
			<td valign="top"><p>&nbsp;</p></td>
			<td valign="top"><p>&nbsp;</p></td>
			<td valign="top">&nbsp;</td>
			<td valign="top"><p>&nbsp;</p></td>
		</tr>
		<tr>
			<td valign="top"><p>CF_SQL_SMALLINT</p></td>
			<td valign="top"><p>SMALLINT</p></td>
			<td valign="top"><p>Smallint</p></td>
			<td valign="top"><p>smallint</p></td>
			<td valign="top"><p>&nbsp;</p></td>
			<td valign="top">&nbsp;</td>
			<td valign="top"><p>smallint</p></td>
		</tr>
		<tr>
			<td valign="top"><p>CF_SQL_STRUCT</p></td>
			<td valign="top"><p>STRUCT</p></td>
			<td valign="top"><p>&nbsp;</p></td>
			<td valign="top"><p>&nbsp;</p></td>
			<td valign="top"><p>&nbsp;</p></td>
			<td valign="top">&nbsp;</td>
			<td valign="top"><p>&nbsp;</p></td>
		</tr>
		<tr>
			<td valign="top"><p>CF_SQL_TIME</p></td>
			<td valign="top"><p>TIME</p></td>
			<td valign="top"><p>Time</p></td>
			<td valign="top"><p>datetime hour to second</p></td>
			<td valign="top"><p>&nbsp;</p></td>
			<td valign="top">&nbsp;</td>
			<td valign="top"><p>&nbsp;</p></td>
		</tr>
		<tr>
			<td valign="top"><p>CF_SQL_TIMESTAMP</p></td>
			<td valign="top"><p>TIMESTAMP</p></td>
			<td valign="top"><p>Timestamp</p></td>
			<td valign="top"><p>datetime year to fraction(5), datetime year to second</p></td>
			<td valign="top"><p>date</p></td>
			<td valign="top">Date/Time</td>
			<td valign="top"><p>datetime, smalldate<br/>
				time</p></td>
		</tr>
		<tr>
			<td valign="top"><p>CF_SQL_TINYINT</p></td>
			<td valign="top"><p>TINYINT</p></td>
			<td valign="top"><p>&nbsp;</p></td>
			<td valign="top"><p>&nbsp;</p></td>
			<td valign="top"><p>&nbsp;</p></td>
			<td valign="top">&nbsp;</td>
			<td valign="top"><p>tinyint</p></td>
		</tr>
		<tr>
			<td valign="top"><p>CF_SQL_VARBINARY</p></td>
			<td valign="top"><p>VARBINARY</p></td>
			<td valign="top"><p>Rowid</p></td>
			<td valign="top"><p>&nbsp;</p></td>
			<td valign="top"><p>raw</p></td>
			<td valign="top">&nbsp;</td>
			<td valign="top"><p>varbinary</p></td>
		</tr>
		<tr>
			<td valign="top"><p>CF_SQL_VARCHAR</p></td>
			<td valign="top"><p>VARCHAR</p></td>
			<td valign="top"><p>Varchar</p></td>
			<td valign="top"><p>varchar, nvarchar, lvarchar</p></td>
			<td valign="top"><p>varchar2, nvarchar2</p></td>
			<td valign="top">Text</td>
			<td valign="top"><p>varchar, nvarchar, sysname</p></td>
		</tr>
	</tbody>
</table>