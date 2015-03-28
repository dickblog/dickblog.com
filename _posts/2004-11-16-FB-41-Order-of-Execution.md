---
layout: default
title: "FB 4.1: Order of Execution"
permalink: /2004/11/16/FB-41-Order-of-Execution/
---

<P>Hey, <A class="" href="http://www.corfield.org/blog/index.cfm?do=blog.entry&amp;entry=3DB6B0F8-DEFA-9C14-AD423A1261191FB8" target=_blank>this was me</A>!</P>
<P>"The exact order of execution of various phases and plugins in Fusebox 4.1".
<OL>
<LI>fusebox.init.cfm - note that this cannot output anything! 
<LI>preProcess plugin phase - for the entire request 
<LI>preFuseaction plugin phase - for global preprocess fuseaction 
<LI>globalPreprocess - the actual fuse for a global preprocess fuseaction 
<LI>postFuseaction plugin phase - for global preprocess fuseaction 
<LI>preFuseaction plugin phase - for the main fuseaction 
<LI>mainFuse - the fuse invoked by the requested fuseaction 
<LI>postFuseaction plugin phase - for the main fuseaction 
<LI>preFuseaction plugin phase - for global postprocess fuseaction 
<LI>globalPostprocess - the actual fuse for a global postprocess fuseaction 
<LI>postFuseaction plugin phase - for global postprocess fuseaction 
<LI>postProcess plugin phase - for the entire request </LI></OL>