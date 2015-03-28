---
layout: default
title: "Multi-Case Switch in CFSCRIPT"
permalink: /2003/08/09/Multi-Case-Switch-in-CFSCRIPT/
---

<PRE>&lt;cfscript&gt;<BR>switch (#fusebox.fuseaction#) {<BR>&nbsp;case "peoplelineGeneral": case "peoplelineLegal": <BR>&nbsp;case "peoplelineHome": case "peoplelineWork": <BR> case "peoplelineCounsel": {<BR>&nbsp;&nbsp;subSection="health";<BR>&nbsp;&nbsp;subSectionTitle="Health &amp; Wellbeing";<BR>&nbsp;&nbsp;level4CrumbTrailTitle="PeopleLine";<BR>&nbsp;&nbsp;break;<BR>&nbsp;}</PRE><PRE>&nbsp;case "sickPayPolicy": {<BR>&nbsp;&nbsp;subSection="health";<BR>&nbsp;&nbsp;subSectionTitle="Health &amp; Wellbeing";<BR>&nbsp;&nbsp;level4CrumbTrailTitle="Absence, Sick Pay and Long Term Disability";<BR>&nbsp;&nbsp;break;<BR>&nbsp;}</PRE><PRE>&nbsp;case "maternityPolicy": {<BR>&nbsp;&nbsp;subSection="timeoff";<BR>&nbsp;&nbsp;subSectionTitle="Time Off";<BR>&nbsp;&nbsp;level4CrumbTrailTitle="Maternity and Paternity Leave Policy";<BR>&nbsp;&nbsp;break;<BR>&nbsp;}<BR>}<BR>&lt;/cfscript&gt;</PRE>