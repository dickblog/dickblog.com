---
layout: default
title: "This is Scary!"
permalink: /2004/04/08/This-is-Scary/
---

<P>Now it seems like phisher can replace your address bar with a custom JavaScript replacement to maintain the deception!</P>
<P>The issue, reported by the <A class="" href="http://www.antiphishing.org/news/03-31-04_Alert-FakeAddressBar.html" target=_blank>Anti-Phishing Working Group</A>, was first reported by <A class="" href="http://www.tumbleweed.com/company/press_releases/2004/2004-03-18b.html" target=_blank>Tumbleweed Communications</A>&nbsp;and mentioned by the <A class="" href="http://news.bbc.co.uk/1/hi/technology/3608943.stm" target=_blank>BBC</A>.</P>
<P>"A consumer receives a forged email that pretends to be from a bank. The email claims that the recipient must verify their email address, and includes a web link. When clicked, the user's browser is opened, and they are taken to a Web page with an email verification form. The web link is HTML and the displayed text appears to link to the real bank's site. </P>
<P>However, the URL does not take the user to the bank's website. Instead, it takes him to a fraudster's site. The fraudulent site instantly detects the user's browser, and runs custom JavaScript code that removes the real address bar and replaces it with a fake address bar at the top of the browser window. The copy is exact. It has the "Address" field, it displays a URL web address that appears to be a secure link to the real bank (e.g. "https://"), and it has the "Go" button on the right hand side.</P>
<P>In almost all respects, the web address and web page appear to be real. You can even type in the bank's web address directly into the fake Address bar. This is a live piece of JavaScript code, not a static fake Address bar image.</P>
<P>Even more dangerous, if you right click the page in order to view the HTML source code, the source code of the phishing Java applet is not displayed. The real source code to the phishing Address bar can only be seen by using the top menu of your browser to view the source code.</P>
<P>There are only one or two clues that the web page is not valid:</P>
<UL>
<LI>Despite the fact that the address bar shows HTTPS in the Address bar, there is no SSL padlock present in the lower corner of the browser 
<LI>When the user types a different URL into this address bar, the browser title does not change from the fake 'Welcome' message."</LI></UL>