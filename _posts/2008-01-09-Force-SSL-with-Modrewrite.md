---
layout: default
title: "Force SSL with Mod_rewrite"
permalink: /2008/01/09/Force-SSL-with-Modrewrite/
---

<p>To get Apache to force a URL to&nbsp; https try this...</p>
<pre>RewriteEngine on<br />RewriteCond %{HTTPS} !^on$ [NC]<br />RewriteRule . https://%{HTTP_HOST}%{REQUEST_URI} [L]</pre>
<p>The idea came from <a href="http://www.dervishmoose.com/blog/index.cfm/2008/1/7/Force-SSL-with-Modrewrite" target="_blank">Mark W. Breneman</a></p>