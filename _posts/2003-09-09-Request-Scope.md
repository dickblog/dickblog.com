---
layout: default
title: "Request Scope"
permalink: /2003/09/09/Request-Scope/
---

<P>Well, if you understand that setting a local variable DSN will work, can you think of any situation in which your code may expect to have access to that variable but won't be able to? Think hard. OK, custom tags. Yep, remember, custom tags have their own local variable scope. So a local variable set in the caller (or in the application.cfm) will not be available to the custom tag. </P>
<P>When we were setting the dsn variable to an application scope, then it was indeed available in the custom tag (as are all shared scopes and also form, url, cgi, and other variables passed to the calling template). 
<P>But by changing the application.dsn to simply dsn (or variables.dsn, same thing), while it's available in all templates under control of the application.cfm, it's not available to any custom tags called by those templates. That's why we need to use the request scope instead. 
<P>It's sole purpose, poorly understood though it is, is to create local variables in a program that are indeed available within custom tags (and vice-versa). That's it. Nothing more. 
<P>Many often confuse the request scope with some sort of persistence or shared nature (and the fact that there is a different kind "request" scope in other languages like ASP and JSP only confuses matters further). But it's best to think of it as nothing more than a scope that allows local variables to be seen in a custom tag called by the template setting the request scope variable. And since our request.dsn variable is set in the application.cfm , it trickles down to the template being executed and is therefore also available to any custom tags we call as well. 
<P>So that's why you should use the request scope rather than a local scope. </P>