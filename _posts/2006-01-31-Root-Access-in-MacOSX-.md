---
layout: default
title: "Root Access in MacOSX:"
permalink: /2006/01/31/Root-Access-in-MacOSX-/
---

Here's how to do it...<br/><br/><div align="left">
													<p><font size="2" face="Verdana"><b>Method #1 - Sudo</b><br/>
Sudo is a command to give admin users temporary, per-command root
access to the the system using individual admin passwords. It is used
in front of a command that requires root access. The admin user is then
asked to verify his or her password to ensure they have the capabillity
to issue root commands. After verification, the command will be
executed and the user is returned to a normal access state.</font></p>
													<p><font size="2" face="Verdana">open terminal window<br/>
															<br/>
															type:<br/>
														</font><font size="2" face="Verdana">sudo passwd root<br/>
															<br/>
At the prompt, enter your admin password. Enter a new password for
root. Now you can issue the command &quot;su&quot;. After password verification,
the user will become root. </font></p>
												</div>
												<table cellspacing="0" cellpadding="0" border="0" style="width: 721px; height: 184px;">
													<tbody><tr>
														<td width="120" valign="top">
															<p><font size="2" face="Verdana"><b>Method #2 - NetInfo Manager<br/>
																	</b>Open the </font><font size="2" face="Verdana">Net Info Manager from the Utilities folder.<br/>
																	Go to Domain -&gt;&nbsp;Security -&gt;&nbsp;Authenticate<br/>
																</font></p>
														</td>
														<td><br/></td>
													</tr>
												</tbody></table>
												
												<p><font size="2" face="Verdana">Go back to Domain -&gt;&nbsp;Security -&gt;&nbsp;and select Enable Root.<br/>
														You will be promted for a password, as none is set.<br/>
														Enter and confirm your password and you've got root!</font></p>
												<div align="left">
													<p><font size="2" face="Verdana,Arial"><b>Metod #3 - Installation CD</b></font></p>
													<p><font size="2" face="Verdana">Boot from the MacOSX install CD.<br/>
															When the installer starts, go to the &quot;Installer&quot; menu.<br/>
															Select &quot;Change password...&quot; from the menu.<br/>
															Select the volume containing your OSX system.<br/>
															Enter a new password for root.<br/>
															Click save.<br/>
															Restart.</font></p>
												</div><br/>