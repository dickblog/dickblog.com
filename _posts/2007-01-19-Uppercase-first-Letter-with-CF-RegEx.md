---
layout: default
title: "Uppercase first Letter with CF RegEx"
permalink: /2007/01/19/Uppercase-first-Letter-with-CF-RegEx/
---

I needed to uppercase the first letter of a word before displaying it. Here is neat RegEx (CF specific but will probably work in Perl) that will do just that.

<code>
<cfset variable = rereplace(variable , '^(\w)(.*)', '\u\1\2') />
</code>

You can use the above when you need it done on the server. Here is the more elegant client side solution with CSS:

<code>
<span style="text-transform: capitalize;">boyan</span>
</code>


While I'm at it here is nice CF RegEx tester: http://www.cftopper.com/contentfiles/tools/regularExpTester.cfm