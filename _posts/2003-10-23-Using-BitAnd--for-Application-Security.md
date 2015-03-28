---
layout: default
title: "Using BitAnd() for Application Security"
permalink: /2003/10/23/Using-BitAnd--for-Application-Security/
---

<P>Using the BitAnd function within ColdFusion is a great way to manage the security of parts of your website.</P>
<P>First agree a list of secure features and assign them a number in the range 2 to the power X, ie 0, 1, 2, 4, 8, 16, 32, ...</P>
<BLOCKQUOTE dir=ltr style="MARGIN-RIGHT: 0px"><PRE>0 = No access<BR>1 = Login access<BR>2 = Add entry<BR>4 = Edit entry<BR>8 = Delete entry<BR>...</PRE></BLOCKQUOTE>
<P>Next assign each user a security clearance value which is the sum of the features you wish them to have access to. </P>
<P>For example.&nbsp;</P>
<UL>
<LI>A user with just login rights would have a security value of 1 (login = 1). <BR></LI>
<LI>An author would have a value of 3 (login + add = 1 + 2). <BR></LI>
<LI>An editor would have a value of 7 (login + add + edit = 1 + 2 +4).<BR></LI>
<LI>An administrator would have a value of 15 (login + add + edit + delete = 1 + 2 + 4 +8).<BR></LI>
<LI>The Helpdesk could have a value of 9 (login + delete = 1 + 8).</LI></UL>
<P>Finally bracket your code with with a CFIF which uses BitAnd to test the security clearance of the logged in user. </P><PRE>&lt;cfif BitAnd(intUserPermissionLevel, intRequiredPermissionLevel)&gt;<BR><BR>    &lt;p&gt;You are cleared to edit this entry&lt;/p&gt;<BR>    ...<BR>    ...<BR>&lt;cfelse&gt;<BR>    &lt;p&gt;Sorry, but you don't have the permission <BR>       to edit an entry.&lt;/p&gt;<BR>&lt;/cfif&gt;</PRE>
<P>Where intUserPermissionLevel =&nbsp;9 and intRequiredPermissionLevel = 4. Therefore BitAnd(9, 4) = 0 which is false. Visually, in binary,&nbsp;it looks like this.</P>
<BLOCKQUOTE dir=ltr style="MARGIN-RIGHT: 0px"><PRE>2 ^ X  = 1 2 4 8<BR>         -------<BR>     9 = 1 0 0 1<BR>     4 = 0 0 1 0<BR>         -------<BR>BitAnd = 0 0 0 0</PRE></BLOCKQUOTE>
<P>For further discussion, take a look at <A class="" href="http://www.halhelms.com/index.cfm?fuseaction=newsletters.jul2000" target=_blank>Hal Helms' article</A> on the subject.</P>