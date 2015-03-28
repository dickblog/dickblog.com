---
layout: default
title: "Multiple IIS Sites on XP Pro"
permalink: /2005/09/18/Multiple-IIS-Sites-on-XP-Pro/
---

Windows XP Professional is only able to run one website at a time. If you&rsquo;re developing in a multisite environment it is practically impossible when one site depends on another. Using <a href="http://www.hairy-spider.com/multisite.aspx" target="_blank">Multisite</a> you can extend IIS to run as many websites as you need.<br/><br/>Multisite is an ISAPI filter that intercepts requests then looks at the host header and redirects the request to the appropriate place on your on your filesystem. Oh, and the filter is FREE!