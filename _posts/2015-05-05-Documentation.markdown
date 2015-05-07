---
layout: post
title:  "What is Reinforcement Learning?"
date:   2015-05-05 04:03:00
categories: jekyll update
---

<!DOCTYPE html PUBLIC "-//W3C//DTD HTML 4.0 Transitional//EN">
<html><head><title>Python: module features</title>
<meta charset="utf-8">
</head><body bgcolor="#f0f0f8">

<table width="100%" cellspacing=0 cellpadding=2 border=0 summary="heading">
<tr bgcolor="#7799ee">
<td valign=bottom>&nbsp;<br>
<font color="#ffffff" face="helvetica, arial">&nbsp;<br><big><big><strong>features</strong></big></big></font></td
><td align=right valign=bottom
><font color="#ffffff" face="helvetica, arial"><a href=".">index</a><br><a href="file:/home/snorthway/semester-8/softdes/PacMan-AI/PacMan1/features.py">/home/snorthway/semester-8/softdes/PacMan-AI/PacMan1/features.py</a></font></td></tr></table>
    <p><tt>@authors:&nbsp;Kelly&nbsp;Brennan,&nbsp;Stephanie&nbsp;Norway&nbsp;and&nbsp;Pinar&nbsp;Demetci<br>
All&nbsp;of&nbsp;the&nbsp;possible&nbsp;features&nbsp;that&nbsp;can&nbsp;be&nbsp;incorporated&nbsp;into&nbsp;Q-learning&nbsp;algorithm</tt></p>
<p>
<table width="100%" cellspacing=0 cellpadding=2 border=0 summary="section">
<tr bgcolor="#aa55cc">
<td colspan=3 valign=bottom>&nbsp;<br>
<font color="#ffffff" face="helvetica, arial"><big><strong>Modules</strong></big></font></td></tr>
    
<tr><td bgcolor="#aa55cc"><tt>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</tt></td><td>&nbsp;</td>
<td width="100%"><table width="100%" summary="list"><tr><td width="25%" valign=top><a href="random.html">random</a><br>
</td><td width="25%" valign=top></td><td width="25%" valign=top></td><td width="25%" valign=top></td></tr></table></td></tr></table><p>
<table width="100%" cellspacing=0 cellpadding=2 border=0 summary="section">
<tr bgcolor="#ee77aa">
<td colspan=3 valign=bottom>&nbsp;<br>
<font color="#ffffff" face="helvetica, arial"><big><strong>Classes</strong></big></font></td></tr>
    
<tr><td bgcolor="#ee77aa"><tt>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</tt></td><td>&nbsp;</td>
<td width="100%"><dl>
<dt><font face="helvetica, arial"><a href="__builtin__.html#object">__builtin__.object</a>
</font></dt><dd>
<dl>
<dt><font face="helvetica, arial"><a href="features.html#Feature">Feature</a>
</font></dt><dd>
<dl>
<dt><font face="helvetica, arial"><a href="features.html#NearestCapsuleFeature">NearestCapsuleFeature</a>
</font></dt><dt><font face="helvetica, arial"><a href="features.html#NearestFoodFeature">NearestFoodFeature</a>
</font></dt><dt><font face="helvetica, arial"><a href="features.html#NearestNormalGhostFeature">NearestNormalGhostFeature</a>
</font></dt><dt><font face="helvetica, arial"><a href="features.html#NearestScaredGhostFeature">NearestScaredGhostFeature</a>
</font></dt><dt><font face="helvetica, arial"><a href="features.html#ScoreFeature">ScoreFeature</a>
</font></dt><dt><font face="helvetica, arial"><a href="features.html#TotalFoodFeature">TotalFoodFeature</a>
</font></dt></dl>
</dd>
</dl>
</dd>
</dl>
 <p>
<table width="100%" cellspacing=0 cellpadding=2 border=0 summary="section">
<tr bgcolor="#ffc8d8">
<td colspan=3 valign=bottom>&nbsp;<br>
<font color="#000000" face="helvetica, arial"><a name="Feature">class <strong>Feature</strong></a>(<a href="__builtin__.html#object">__builtin__.object</a>)</font></td></tr>
    
<tr><td bgcolor="#ffc8d8"><tt>&nbsp;&nbsp;&nbsp;</tt></td><td>&nbsp;</td>
<td width="100%">Methods defined here:<br>
<dl><dt><a name="Feature-__init__"><strong>__init__</strong></a>(self, value<font color="#909090">=0.7078434263686345</font>, weight<font color="#909090">=0.7891369079881876</font>)</dt><dd><tt>Main&nbsp;class&nbsp;for&nbsp;all&nbsp;features.&nbsp;Each&nbsp;feature&nbsp;will&nbsp;inherit&nbsp;from&nbsp;this&nbsp;class.<br>
Follwing&nbsp;the&nbsp;same&nbsp;pattern&nbsp;as&nbsp;Agent;&nbsp;the&nbsp;index&nbsp;is&nbsp;for&nbsp;the<br>
Agent&nbsp;<a href="__builtin__.html#object">object</a>&nbsp;to&nbsp;know&nbsp;which&nbsp;feature&nbsp;it&nbsp;is&nbsp;in&nbsp;the&nbsp;features&nbsp;list.<br>
&nbsp;<br>
Value:&nbsp;attribute&nbsp;to&nbsp;calculate&nbsp;Q-values<br>
weight:&nbsp;each&nbsp;feature&nbsp;has&nbsp;a&nbsp;weight&nbsp;associated&nbsp;with&nbsp;it,&nbsp;which&nbsp;will&nbsp;be&nbsp;updated&nbsp;for&nbsp;agent&nbsp;to&nbsp;learn<br>
&nbsp;&nbsp;&nbsp;&nbsp;which&nbsp;feature&nbsp;to&nbsp;prioritize</tt></dd></dl>

<dl><dt><a name="Feature-__str__"><strong>__str__</strong></a>(self)</dt><dd><tt>Allows&nbsp;the&nbsp;tracking&nbsp;the&nbsp;values&nbsp;and&nbsp;weights&nbsp;of&nbsp;features&nbsp;after&nbsp;each&nbsp;update<br>
makes&nbsp;it&nbsp;easier&nbsp;to&nbsp;see&nbsp;how&nbsp;PacMan&nbsp;is&nbsp;learning</tt></dd></dl>

<dl><dt><a name="Feature-extractFromState"><strong>extractFromState</strong></a>(self, state, costs<font color="#909090">=None</font>)</dt><dd><tt>Map&nbsp;the&nbsp;state&nbsp;onto&nbsp;the&nbsp;feature&nbsp;space&nbsp;(i.e.&nbsp;a&nbsp;real&nbsp;number).<br>
Gets&nbsp;the&nbsp;value,&nbsp;doesn't&nbsp;update&nbsp;it.<br>
This&nbsp;will&nbsp;be&nbsp;implemented&nbsp;for&nbsp;each&nbsp;feature.<br>
If&nbsp;forgot&nbsp;to&nbsp;implement,&nbsp;raises&nbsp;and&nbsp;error.<br>
&nbsp;<br>
state:&nbsp;GameState&nbsp;<a href="__builtin__.html#object">object</a>,<br>
costs:&nbsp;tile&nbsp;objects&nbsp;of&nbsp;game&nbsp;layout&nbsp;-&nbsp;only&nbsp;necessary&nbsp;for&nbsp;some&nbsp;features</tt></dd></dl>

<dl><dt><a name="Feature-updateValue"><strong>updateValue</strong></a>(self, state, costs)</dt><dd><tt>Updates&nbsp;the&nbsp;value&nbsp;based&nbsp;on&nbsp;the&nbsp;state.<br>
&nbsp;<br>
state:&nbsp;GameState&nbsp;<a href="__builtin__.html#object">object</a><br>
costs:&nbsp;tile&nbsp;objects&nbsp;of&nbsp;game&nbsp;layout</tt></dd></dl>

<hr>
Data descriptors defined here:<br>
<dl><dt><strong>__dict__</strong></dt>
<dd><tt>dictionary&nbsp;for&nbsp;instance&nbsp;variables&nbsp;(if&nbsp;defined)</tt></dd>
</dl>
<dl><dt><strong>__weakref__</strong></dt>
<dd><tt>list&nbsp;of&nbsp;weak&nbsp;references&nbsp;to&nbsp;the&nbsp;object&nbsp;(if&nbsp;defined)</tt></dd>
</dl>
</td></tr></table> <p>
<table width="100%" cellspacing=0 cellpadding=2 border=0 summary="section">
<tr bgcolor="#ffc8d8">
<td colspan=3 valign=bottom>&nbsp;<br>
<font color="#000000" face="helvetica, arial"><a name="NearestCapsuleFeature">class <strong>NearestCapsuleFeature</strong></a>(<a href="features.html#Feature">Feature</a>)</font></td></tr>
    
<tr bgcolor="#ffc8d8"><td rowspan=2><tt>&nbsp;&nbsp;&nbsp;</tt></td>
<td colspan=2><tt>Distance&nbsp;to&nbsp;the&nbsp;nearest&nbsp;capsule.<br>
Inherits&nbsp;from&nbsp;<a href="#Feature">Feature</a>&nbsp;class,&nbsp;like&nbsp;every&nbsp;other&nbsp;feature.<br>
Uses&nbsp;A-star&nbsp;to&nbsp;calculate&nbsp;the&nbsp;distance<br>&nbsp;</tt></td></tr>
<tr><td>&nbsp;</td>
<td width="100%"><dl><dt>Method resolution order:</dt>
<dd><a href="features.html#NearestCapsuleFeature">NearestCapsuleFeature</a></dd>
<dd><a href="features.html#Feature">Feature</a></dd>
<dd><a href="__builtin__.html#object">__builtin__.object</a></dd>
</dl>
<hr>
Methods defined here:<br>
<dl><dt><a name="NearestCapsuleFeature-extractFromState"><strong>extractFromState</strong></a>(self, state, costs)</dt><dd><tt>Implemented&nbsp;to&nbsp;generate&nbsp;the&nbsp;distance&nbsp;to&nbsp;the&nbsp;nearest&nbsp;capsule<br>
&nbsp;<br>
state:&nbsp;GameState&nbsp;<a href="__builtin__.html#object">object</a><br>
costs:&nbsp;tile&nbsp;<a href="__builtin__.html#object">object</a>&nbsp;of&nbsp;game&nbsp;layout<br>
return:&nbsp;(float)&nbsp;if&nbsp;capsules&nbsp;present,&nbsp;return&nbsp;minimum&nbsp;distance&nbsp;to&nbsp;capsule<br>
&nbsp;&nbsp;&nbsp;&nbsp;otherwise&nbsp;return&nbsp;the&nbsp;manhattanDistance&nbsp;of&nbsp;the&nbsp;layout&nbsp;board,&nbsp;making&nbsp;pacman&nbsp;think&nbsp;they&nbsp;are&nbsp;far&nbsp;away</tt></dd></dl>

<hr>
Methods inherited from <a href="features.html#Feature">Feature</a>:<br>
<dl><dt><a name="NearestCapsuleFeature-__init__"><strong>__init__</strong></a>(self, value<font color="#909090">=0.7078434263686345</font>, weight<font color="#909090">=0.7891369079881876</font>)</dt><dd><tt>Main&nbsp;class&nbsp;for&nbsp;all&nbsp;features.&nbsp;Each&nbsp;feature&nbsp;will&nbsp;inherit&nbsp;from&nbsp;this&nbsp;class.<br>
Follwing&nbsp;the&nbsp;same&nbsp;pattern&nbsp;as&nbsp;Agent;&nbsp;the&nbsp;index&nbsp;is&nbsp;for&nbsp;the<br>
Agent&nbsp;<a href="__builtin__.html#object">object</a>&nbsp;to&nbsp;know&nbsp;which&nbsp;feature&nbsp;it&nbsp;is&nbsp;in&nbsp;the&nbsp;features&nbsp;list.<br>
&nbsp;<br>
Value:&nbsp;attribute&nbsp;to&nbsp;calculate&nbsp;Q-values<br>
weight:&nbsp;each&nbsp;feature&nbsp;has&nbsp;a&nbsp;weight&nbsp;associated&nbsp;with&nbsp;it,&nbsp;which&nbsp;will&nbsp;be&nbsp;updated&nbsp;for&nbsp;agent&nbsp;to&nbsp;learn<br>
&nbsp;&nbsp;&nbsp;&nbsp;which&nbsp;feature&nbsp;to&nbsp;prioritize</tt></dd></dl>

<dl><dt><a name="NearestCapsuleFeature-__str__"><strong>__str__</strong></a>(self)</dt><dd><tt>Allows&nbsp;the&nbsp;tracking&nbsp;the&nbsp;values&nbsp;and&nbsp;weights&nbsp;of&nbsp;features&nbsp;after&nbsp;each&nbsp;update<br>
makes&nbsp;it&nbsp;easier&nbsp;to&nbsp;see&nbsp;how&nbsp;PacMan&nbsp;is&nbsp;learning</tt></dd></dl>

<dl><dt><a name="NearestCapsuleFeature-updateValue"><strong>updateValue</strong></a>(self, state, costs)</dt><dd><tt>Updates&nbsp;the&nbsp;value&nbsp;based&nbsp;on&nbsp;the&nbsp;state.<br>
&nbsp;<br>
state:&nbsp;GameState&nbsp;<a href="__builtin__.html#object">object</a><br>
costs:&nbsp;tile&nbsp;objects&nbsp;of&nbsp;game&nbsp;layout</tt></dd></dl>

<hr>
Data descriptors inherited from <a href="features.html#Feature">Feature</a>:<br>
<dl><dt><strong>__dict__</strong></dt>
<dd><tt>dictionary&nbsp;for&nbsp;instance&nbsp;variables&nbsp;(if&nbsp;defined)</tt></dd>
</dl>
<dl><dt><strong>__weakref__</strong></dt>
<dd><tt>list&nbsp;of&nbsp;weak&nbsp;references&nbsp;to&nbsp;the&nbsp;object&nbsp;(if&nbsp;defined)</tt></dd>
</dl>
</td></tr></table> <p>
<table width="100%" cellspacing=0 cellpadding=2 border=0 summary="section">
<tr bgcolor="#ffc8d8">
<td colspan=3 valign=bottom>&nbsp;<br>
<font color="#000000" face="helvetica, arial"><a name="NearestFoodFeature">class <strong>NearestFoodFeature</strong></a>(<a href="features.html#Feature">Feature</a>)</font></td></tr>
    
<tr bgcolor="#ffc8d8"><td rowspan=2><tt>&nbsp;&nbsp;&nbsp;</tt></td>
<td colspan=2><tt>Distance&nbsp;to&nbsp;nearest&nbsp;food<br>
Inherits&nbsp;from&nbsp;<a href="#Feature">Feature</a><br>&nbsp;</tt></td></tr>
<tr><td>&nbsp;</td>
<td width="100%"><dl><dt>Method resolution order:</dt>
<dd><a href="features.html#NearestFoodFeature">NearestFoodFeature</a></dd>
<dd><a href="features.html#Feature">Feature</a></dd>
<dd><a href="__builtin__.html#object">__builtin__.object</a></dd>
</dl>
<hr>
Methods defined here:<br>
<dl><dt><a name="NearestFoodFeature-extractFromState"><strong>extractFromState</strong></a>(self, state, costs)</dt><dd><tt>Uses&nbsp;manhattanDistance&nbsp;instead&nbsp;of&nbsp;A-star&nbsp;to&nbsp;speed&nbsp;up&nbsp;the&nbsp;process.<br>
&nbsp;<br>
state:&nbsp;GameState&nbsp;<a href="__builtin__.html#object">object</a><br>
costs:&nbsp;tile&nbsp;<a href="__builtin__.html#object">object</a>&nbsp;of&nbsp;game&nbsp;layout&nbsp;-&nbsp;not&nbsp;used&nbsp;here<br>
return:&nbsp;(float)&nbsp;if&nbsp;food&nbsp;exists,&nbsp;manhattanDistance&nbsp;to&nbsp;nearest&nbsp;food&nbsp;pellet<br>
&nbsp;&nbsp;&nbsp;&nbsp;otherwise,&nbsp;return&nbsp;0&nbsp;(Game&nbsp;has&nbsp;been&nbsp;won)</tt></dd></dl>

<hr>
Methods inherited from <a href="features.html#Feature">Feature</a>:<br>
<dl><dt><a name="NearestFoodFeature-__init__"><strong>__init__</strong></a>(self, value<font color="#909090">=0.7078434263686345</font>, weight<font color="#909090">=0.7891369079881876</font>)</dt><dd><tt>Main&nbsp;class&nbsp;for&nbsp;all&nbsp;features.&nbsp;Each&nbsp;feature&nbsp;will&nbsp;inherit&nbsp;from&nbsp;this&nbsp;class.<br>
Follwing&nbsp;the&nbsp;same&nbsp;pattern&nbsp;as&nbsp;Agent;&nbsp;the&nbsp;index&nbsp;is&nbsp;for&nbsp;the<br>
Agent&nbsp;<a href="__builtin__.html#object">object</a>&nbsp;to&nbsp;know&nbsp;which&nbsp;feature&nbsp;it&nbsp;is&nbsp;in&nbsp;the&nbsp;features&nbsp;list.<br>
&nbsp;<br>
Value:&nbsp;attribute&nbsp;to&nbsp;calculate&nbsp;Q-values<br>
weight:&nbsp;each&nbsp;feature&nbsp;has&nbsp;a&nbsp;weight&nbsp;associated&nbsp;with&nbsp;it,&nbsp;which&nbsp;will&nbsp;be&nbsp;updated&nbsp;for&nbsp;agent&nbsp;to&nbsp;learn<br>
&nbsp;&nbsp;&nbsp;&nbsp;which&nbsp;feature&nbsp;to&nbsp;prioritize</tt></dd></dl>

<dl><dt><a name="NearestFoodFeature-__str__"><strong>__str__</strong></a>(self)</dt><dd><tt>Allows&nbsp;the&nbsp;tracking&nbsp;the&nbsp;values&nbsp;and&nbsp;weights&nbsp;of&nbsp;features&nbsp;after&nbsp;each&nbsp;update<br>
makes&nbsp;it&nbsp;easier&nbsp;to&nbsp;see&nbsp;how&nbsp;PacMan&nbsp;is&nbsp;learning</tt></dd></dl>

<dl><dt><a name="NearestFoodFeature-updateValue"><strong>updateValue</strong></a>(self, state, costs)</dt><dd><tt>Updates&nbsp;the&nbsp;value&nbsp;based&nbsp;on&nbsp;the&nbsp;state.<br>
&nbsp;<br>
state:&nbsp;GameState&nbsp;<a href="__builtin__.html#object">object</a><br>
costs:&nbsp;tile&nbsp;objects&nbsp;of&nbsp;game&nbsp;layout</tt></dd></dl>

<hr>
Data descriptors inherited from <a href="features.html#Feature">Feature</a>:<br>
<dl><dt><strong>__dict__</strong></dt>
<dd><tt>dictionary&nbsp;for&nbsp;instance&nbsp;variables&nbsp;(if&nbsp;defined)</tt></dd>
</dl>
<dl><dt><strong>__weakref__</strong></dt>
<dd><tt>list&nbsp;of&nbsp;weak&nbsp;references&nbsp;to&nbsp;the&nbsp;object&nbsp;(if&nbsp;defined)</tt></dd>
</dl>
</td></tr></table> <p>
<table width="100%" cellspacing=0 cellpadding=2 border=0 summary="section">
<tr bgcolor="#ffc8d8">
<td colspan=3 valign=bottom>&nbsp;<br>
<font color="#000000" face="helvetica, arial"><a name="NearestNormalGhostFeature">class <strong>NearestNormalGhostFeature</strong></a>(<a href="features.html#Feature">Feature</a>)</font></td></tr>
    
<tr bgcolor="#ffc8d8"><td rowspan=2><tt>&nbsp;&nbsp;&nbsp;</tt></td>
<td colspan=2><tt>Distance&nbsp;to&nbsp;the&nbsp;nearest&nbsp;non-scared&nbsp;(normal)&nbsp;ghost.<br>
Implements&nbsp;Astar&nbsp;search&nbsp;algorithm<br>&nbsp;</tt></td></tr>
<tr><td>&nbsp;</td>
<td width="100%"><dl><dt>Method resolution order:</dt>
<dd><a href="features.html#NearestNormalGhostFeature">NearestNormalGhostFeature</a></dd>
<dd><a href="features.html#Feature">Feature</a></dd>
<dd><a href="__builtin__.html#object">__builtin__.object</a></dd>
</dl>
<hr>
Methods defined here:<br>
<dl><dt><a name="NearestNormalGhostFeature-extractFromState"><strong>extractFromState</strong></a>(self, state, costs)</dt><dd><tt>determine&nbsp;distance&nbsp;between&nbsp;pacman&nbsp;and&nbsp;a&nbsp;normal&nbsp;ghost<br>
&nbsp;<br>
state:&nbsp;GameState&nbsp;<a href="__builtin__.html#object">object</a><br>
costs:&nbsp;tile&nbsp;<a href="__builtin__.html#object">object</a>&nbsp;of&nbsp;game&nbsp;layout<br>
return:&nbsp;(float)&nbsp;if&nbsp;normal&nbsp;ghosts&nbsp;present,&nbsp;return&nbsp;minimum&nbsp;distance&nbsp;to&nbsp;normal&nbsp;ghost<br>
&nbsp;&nbsp;&nbsp;&nbsp;otherwise&nbsp;return&nbsp;the&nbsp;manhattanDistance&nbsp;of&nbsp;the&nbsp;layout&nbsp;board,&nbsp;making&nbsp;pacman&nbsp;think&nbsp;they&nbsp;are&nbsp;far&nbsp;away</tt></dd></dl>

<hr>
Methods inherited from <a href="features.html#Feature">Feature</a>:<br>
<dl><dt><a name="NearestNormalGhostFeature-__init__"><strong>__init__</strong></a>(self, value<font color="#909090">=0.7078434263686345</font>, weight<font color="#909090">=0.7891369079881876</font>)</dt><dd><tt>Main&nbsp;class&nbsp;for&nbsp;all&nbsp;features.&nbsp;Each&nbsp;feature&nbsp;will&nbsp;inherit&nbsp;from&nbsp;this&nbsp;class.<br>
Follwing&nbsp;the&nbsp;same&nbsp;pattern&nbsp;as&nbsp;Agent;&nbsp;the&nbsp;index&nbsp;is&nbsp;for&nbsp;the<br>
Agent&nbsp;<a href="__builtin__.html#object">object</a>&nbsp;to&nbsp;know&nbsp;which&nbsp;feature&nbsp;it&nbsp;is&nbsp;in&nbsp;the&nbsp;features&nbsp;list.<br>
&nbsp;<br>
Value:&nbsp;attribute&nbsp;to&nbsp;calculate&nbsp;Q-values<br>
weight:&nbsp;each&nbsp;feature&nbsp;has&nbsp;a&nbsp;weight&nbsp;associated&nbsp;with&nbsp;it,&nbsp;which&nbsp;will&nbsp;be&nbsp;updated&nbsp;for&nbsp;agent&nbsp;to&nbsp;learn<br>
&nbsp;&nbsp;&nbsp;&nbsp;which&nbsp;feature&nbsp;to&nbsp;prioritize</tt></dd></dl>

<dl><dt><a name="NearestNormalGhostFeature-__str__"><strong>__str__</strong></a>(self)</dt><dd><tt>Allows&nbsp;the&nbsp;tracking&nbsp;the&nbsp;values&nbsp;and&nbsp;weights&nbsp;of&nbsp;features&nbsp;after&nbsp;each&nbsp;update<br>
makes&nbsp;it&nbsp;easier&nbsp;to&nbsp;see&nbsp;how&nbsp;PacMan&nbsp;is&nbsp;learning</tt></dd></dl>

<dl><dt><a name="NearestNormalGhostFeature-updateValue"><strong>updateValue</strong></a>(self, state, costs)</dt><dd><tt>Updates&nbsp;the&nbsp;value&nbsp;based&nbsp;on&nbsp;the&nbsp;state.<br>
&nbsp;<br>
state:&nbsp;GameState&nbsp;<a href="__builtin__.html#object">object</a><br>
costs:&nbsp;tile&nbsp;objects&nbsp;of&nbsp;game&nbsp;layout</tt></dd></dl>

<hr>
Data descriptors inherited from <a href="features.html#Feature">Feature</a>:<br>
<dl><dt><strong>__dict__</strong></dt>
<dd><tt>dictionary&nbsp;for&nbsp;instance&nbsp;variables&nbsp;(if&nbsp;defined)</tt></dd>
</dl>
<dl><dt><strong>__weakref__</strong></dt>
<dd><tt>list&nbsp;of&nbsp;weak&nbsp;references&nbsp;to&nbsp;the&nbsp;object&nbsp;(if&nbsp;defined)</tt></dd>
</dl>
</td></tr></table> <p>
<table width="100%" cellspacing=0 cellpadding=2 border=0 summary="section">
<tr bgcolor="#ffc8d8">
<td colspan=3 valign=bottom>&nbsp;<br>
<font color="#000000" face="helvetica, arial"><a name="NearestScaredGhostFeature">class <strong>NearestScaredGhostFeature</strong></a>(<a href="features.html#Feature">Feature</a>)</font></td></tr>
    
<tr bgcolor="#ffc8d8"><td rowspan=2><tt>&nbsp;&nbsp;&nbsp;</tt></td>
<td colspan=2><tt>Distance&nbsp;to&nbsp;the&nbsp;nearest&nbsp;scared&nbsp;ghost&nbsp;after&nbsp;PacMan&nbsp;eats&nbsp;a&nbsp;capsule.<br>
Implements&nbsp;Astar&nbsp;search&nbsp;algorithm<br>&nbsp;</tt></td></tr>
<tr><td>&nbsp;</td>
<td width="100%"><dl><dt>Method resolution order:</dt>
<dd><a href="features.html#NearestScaredGhostFeature">NearestScaredGhostFeature</a></dd>
<dd><a href="features.html#Feature">Feature</a></dd>
<dd><a href="__builtin__.html#object">__builtin__.object</a></dd>
</dl>
<hr>
Methods defined here:<br>
<dl><dt><a name="NearestScaredGhostFeature-extractFromState"><strong>extractFromState</strong></a>(self, state, costs)</dt><dd><tt>determine&nbsp;distance&nbsp;between&nbsp;pacman&nbsp;and&nbsp;a&nbsp;scared&nbsp;ghost<br>
&nbsp;<br>
state:&nbsp;GameState&nbsp;<a href="__builtin__.html#object">object</a><br>
costs:&nbsp;tile&nbsp;<a href="__builtin__.html#object">object</a>&nbsp;of&nbsp;game&nbsp;layout<br>
return:&nbsp;(float)&nbsp;if&nbsp;scared&nbsp;ghosts&nbsp;present,&nbsp;return&nbsp;minimum&nbsp;distance&nbsp;to&nbsp;scared&nbsp;ghost<br>
&nbsp;&nbsp;&nbsp;&nbsp;otherwise&nbsp;return&nbsp;the&nbsp;manhattanDistance&nbsp;of&nbsp;the&nbsp;layout&nbsp;board,&nbsp;making&nbsp;pacman&nbsp;think&nbsp;they&nbsp;are&nbsp;far&nbsp;away</tt></dd></dl>

<hr>
Methods inherited from <a href="features.html#Feature">Feature</a>:<br>
<dl><dt><a name="NearestScaredGhostFeature-__init__"><strong>__init__</strong></a>(self, value<font color="#909090">=0.7078434263686345</font>, weight<font color="#909090">=0.7891369079881876</font>)</dt><dd><tt>Main&nbsp;class&nbsp;for&nbsp;all&nbsp;features.&nbsp;Each&nbsp;feature&nbsp;will&nbsp;inherit&nbsp;from&nbsp;this&nbsp;class.<br>
Follwing&nbsp;the&nbsp;same&nbsp;pattern&nbsp;as&nbsp;Agent;&nbsp;the&nbsp;index&nbsp;is&nbsp;for&nbsp;the<br>
Agent&nbsp;<a href="__builtin__.html#object">object</a>&nbsp;to&nbsp;know&nbsp;which&nbsp;feature&nbsp;it&nbsp;is&nbsp;in&nbsp;the&nbsp;features&nbsp;list.<br>
&nbsp;<br>
Value:&nbsp;attribute&nbsp;to&nbsp;calculate&nbsp;Q-values<br>
weight:&nbsp;each&nbsp;feature&nbsp;has&nbsp;a&nbsp;weight&nbsp;associated&nbsp;with&nbsp;it,&nbsp;which&nbsp;will&nbsp;be&nbsp;updated&nbsp;for&nbsp;agent&nbsp;to&nbsp;learn<br>
&nbsp;&nbsp;&nbsp;&nbsp;which&nbsp;feature&nbsp;to&nbsp;prioritize</tt></dd></dl>

<dl><dt><a name="NearestScaredGhostFeature-__str__"><strong>__str__</strong></a>(self)</dt><dd><tt>Allows&nbsp;the&nbsp;tracking&nbsp;the&nbsp;values&nbsp;and&nbsp;weights&nbsp;of&nbsp;features&nbsp;after&nbsp;each&nbsp;update<br>
makes&nbsp;it&nbsp;easier&nbsp;to&nbsp;see&nbsp;how&nbsp;PacMan&nbsp;is&nbsp;learning</tt></dd></dl>

<dl><dt><a name="NearestScaredGhostFeature-updateValue"><strong>updateValue</strong></a>(self, state, costs)</dt><dd><tt>Updates&nbsp;the&nbsp;value&nbsp;based&nbsp;on&nbsp;the&nbsp;state.<br>
&nbsp;<br>
state:&nbsp;GameState&nbsp;<a href="__builtin__.html#object">object</a><br>
costs:&nbsp;tile&nbsp;objects&nbsp;of&nbsp;game&nbsp;layout</tt></dd></dl>

<hr>
Data descriptors inherited from <a href="features.html#Feature">Feature</a>:<br>
<dl><dt><strong>__dict__</strong></dt>
<dd><tt>dictionary&nbsp;for&nbsp;instance&nbsp;variables&nbsp;(if&nbsp;defined)</tt></dd>
</dl>
<dl><dt><strong>__weakref__</strong></dt>
<dd><tt>list&nbsp;of&nbsp;weak&nbsp;references&nbsp;to&nbsp;the&nbsp;object&nbsp;(if&nbsp;defined)</tt></dd>
</dl>
</td></tr></table> <p>
<table width="100%" cellspacing=0 cellpadding=2 border=0 summary="section">
<tr bgcolor="#ffc8d8">
<td colspan=3 valign=bottom>&nbsp;<br>
<font color="#000000" face="helvetica, arial"><a name="ScoreFeature">class <strong>ScoreFeature</strong></a>(<a href="features.html#Feature">Feature</a>)</font></td></tr>
    
<tr bgcolor="#ffc8d8"><td rowspan=2><tt>&nbsp;&nbsp;&nbsp;</tt></td>
<td colspan=2><tt>game&nbsp;score<br>&nbsp;</tt></td></tr>
<tr><td>&nbsp;</td>
<td width="100%"><dl><dt>Method resolution order:</dt>
<dd><a href="features.html#ScoreFeature">ScoreFeature</a></dd>
<dd><a href="features.html#Feature">Feature</a></dd>
<dd><a href="__builtin__.html#object">__builtin__.object</a></dd>
</dl>
<hr>
Methods defined here:<br>
<dl><dt><a name="ScoreFeature-extractFromState"><strong>extractFromState</strong></a>(self, state, costs)</dt><dd><tt>Calculate&nbsp;the&nbsp;game&nbsp;score<br>
&nbsp;<br>
state:&nbsp;GameState&nbsp;<a href="__builtin__.html#object">object</a><br>
costs:&nbsp;tile&nbsp;<a href="__builtin__.html#object">object</a>&nbsp;of&nbsp;game&nbsp;layout&nbsp;-&nbsp;not&nbsp;used&nbsp;here<br>
return:&nbsp;weighted&nbsp;score&nbsp;(float)</tt></dd></dl>

<hr>
Methods inherited from <a href="features.html#Feature">Feature</a>:<br>
<dl><dt><a name="ScoreFeature-__init__"><strong>__init__</strong></a>(self, value<font color="#909090">=0.7078434263686345</font>, weight<font color="#909090">=0.7891369079881876</font>)</dt><dd><tt>Main&nbsp;class&nbsp;for&nbsp;all&nbsp;features.&nbsp;Each&nbsp;feature&nbsp;will&nbsp;inherit&nbsp;from&nbsp;this&nbsp;class.<br>
Follwing&nbsp;the&nbsp;same&nbsp;pattern&nbsp;as&nbsp;Agent;&nbsp;the&nbsp;index&nbsp;is&nbsp;for&nbsp;the<br>
Agent&nbsp;<a href="__builtin__.html#object">object</a>&nbsp;to&nbsp;know&nbsp;which&nbsp;feature&nbsp;it&nbsp;is&nbsp;in&nbsp;the&nbsp;features&nbsp;list.<br>
&nbsp;<br>
Value:&nbsp;attribute&nbsp;to&nbsp;calculate&nbsp;Q-values<br>
weight:&nbsp;each&nbsp;feature&nbsp;has&nbsp;a&nbsp;weight&nbsp;associated&nbsp;with&nbsp;it,&nbsp;which&nbsp;will&nbsp;be&nbsp;updated&nbsp;for&nbsp;agent&nbsp;to&nbsp;learn<br>
&nbsp;&nbsp;&nbsp;&nbsp;which&nbsp;feature&nbsp;to&nbsp;prioritize</tt></dd></dl>

<dl><dt><a name="ScoreFeature-__str__"><strong>__str__</strong></a>(self)</dt><dd><tt>Allows&nbsp;the&nbsp;tracking&nbsp;the&nbsp;values&nbsp;and&nbsp;weights&nbsp;of&nbsp;features&nbsp;after&nbsp;each&nbsp;update<br>
makes&nbsp;it&nbsp;easier&nbsp;to&nbsp;see&nbsp;how&nbsp;PacMan&nbsp;is&nbsp;learning</tt></dd></dl>

<dl><dt><a name="ScoreFeature-updateValue"><strong>updateValue</strong></a>(self, state, costs)</dt><dd><tt>Updates&nbsp;the&nbsp;value&nbsp;based&nbsp;on&nbsp;the&nbsp;state.<br>
&nbsp;<br>
state:&nbsp;GameState&nbsp;<a href="__builtin__.html#object">object</a><br>
costs:&nbsp;tile&nbsp;objects&nbsp;of&nbsp;game&nbsp;layout</tt></dd></dl>

<hr>
Data descriptors inherited from <a href="features.html#Feature">Feature</a>:<br>
<dl><dt><strong>__dict__</strong></dt>
<dd><tt>dictionary&nbsp;for&nbsp;instance&nbsp;variables&nbsp;(if&nbsp;defined)</tt></dd>
</dl>
<dl><dt><strong>__weakref__</strong></dt>
<dd><tt>list&nbsp;of&nbsp;weak&nbsp;references&nbsp;to&nbsp;the&nbsp;object&nbsp;(if&nbsp;defined)</tt></dd>
</dl>
</td></tr></table> <p>
<table width="100%" cellspacing=0 cellpadding=2 border=0 summary="section">
<tr bgcolor="#ffc8d8">
<td colspan=3 valign=bottom>&nbsp;<br>
<font color="#000000" face="helvetica, arial"><a name="TotalFoodFeature">class <strong>TotalFoodFeature</strong></a>(<a href="features.html#Feature">Feature</a>)</font></td></tr>
    
<tr bgcolor="#ffc8d8"><td rowspan=2><tt>&nbsp;&nbsp;&nbsp;</tt></td>
<td colspan=2><tt><a href="#Feature">Feature</a>&nbsp;Total&nbsp;number&nbsp;of&nbsp;food&nbsp;remaining&nbsp;on&nbsp;the&nbsp;board.<br>
This&nbsp;feature&nbsp;exists&nbsp;so&nbsp;that&nbsp;PacMan&nbsp;will&nbsp;care&nbsp;about&nbsp;eating&nbsp;all&nbsp;the&nbsp;food.<br>&nbsp;</tt></td></tr>
<tr><td>&nbsp;</td>
<td width="100%"><dl><dt>Method resolution order:</dt>
<dd><a href="features.html#TotalFoodFeature">TotalFoodFeature</a></dd>
<dd><a href="features.html#Feature">Feature</a></dd>
<dd><a href="__builtin__.html#object">__builtin__.object</a></dd>
</dl>
<hr>
Methods defined here:<br>
<dl><dt><a name="TotalFoodFeature-extractFromState"><strong>extractFromState</strong></a>(self, state, costs)</dt><dd><tt>Returns&nbsp;the&nbsp;total&nbsp;number&nbsp;of&nbsp;food.<br>
&nbsp;<br>
state:&nbsp;GameState&nbsp;<a href="__builtin__.html#object">object</a><br>
costs:&nbsp;tile&nbsp;<a href="__builtin__.html#object">object</a>&nbsp;of&nbsp;game&nbsp;layout&nbsp;-&nbsp;not&nbsp;used&nbsp;here<br>
return:&nbsp;number&nbsp;of&nbsp;total&nbsp;food&nbsp;on&nbsp;the&nbsp;board&nbsp;(float)</tt></dd></dl>

<hr>
Methods inherited from <a href="features.html#Feature">Feature</a>:<br>
<dl><dt><a name="TotalFoodFeature-__init__"><strong>__init__</strong></a>(self, value<font color="#909090">=0.7078434263686345</font>, weight<font color="#909090">=0.7891369079881876</font>)</dt><dd><tt>Main&nbsp;class&nbsp;for&nbsp;all&nbsp;features.&nbsp;Each&nbsp;feature&nbsp;will&nbsp;inherit&nbsp;from&nbsp;this&nbsp;class.<br>
Follwing&nbsp;the&nbsp;same&nbsp;pattern&nbsp;as&nbsp;Agent;&nbsp;the&nbsp;index&nbsp;is&nbsp;for&nbsp;the<br>
Agent&nbsp;<a href="__builtin__.html#object">object</a>&nbsp;to&nbsp;know&nbsp;which&nbsp;feature&nbsp;it&nbsp;is&nbsp;in&nbsp;the&nbsp;features&nbsp;list.<br>
&nbsp;<br>
Value:&nbsp;attribute&nbsp;to&nbsp;calculate&nbsp;Q-values<br>
weight:&nbsp;each&nbsp;feature&nbsp;has&nbsp;a&nbsp;weight&nbsp;associated&nbsp;with&nbsp;it,&nbsp;which&nbsp;will&nbsp;be&nbsp;updated&nbsp;for&nbsp;agent&nbsp;to&nbsp;learn<br>
&nbsp;&nbsp;&nbsp;&nbsp;which&nbsp;feature&nbsp;to&nbsp;prioritize</tt></dd></dl>

<dl><dt><a name="TotalFoodFeature-__str__"><strong>__str__</strong></a>(self)</dt><dd><tt>Allows&nbsp;the&nbsp;tracking&nbsp;the&nbsp;values&nbsp;and&nbsp;weights&nbsp;of&nbsp;features&nbsp;after&nbsp;each&nbsp;update<br>
makes&nbsp;it&nbsp;easier&nbsp;to&nbsp;see&nbsp;how&nbsp;PacMan&nbsp;is&nbsp;learning</tt></dd></dl>

<dl><dt><a name="TotalFoodFeature-updateValue"><strong>updateValue</strong></a>(self, state, costs)</dt><dd><tt>Updates&nbsp;the&nbsp;value&nbsp;based&nbsp;on&nbsp;the&nbsp;state.<br>
&nbsp;<br>
state:&nbsp;GameState&nbsp;<a href="__builtin__.html#object">object</a><br>
costs:&nbsp;tile&nbsp;objects&nbsp;of&nbsp;game&nbsp;layout</tt></dd></dl>

<hr>
Data descriptors inherited from <a href="features.html#Feature">Feature</a>:<br>
<dl><dt><strong>__dict__</strong></dt>
<dd><tt>dictionary&nbsp;for&nbsp;instance&nbsp;variables&nbsp;(if&nbsp;defined)</tt></dd>
</dl>
<dl><dt><strong>__weakref__</strong></dt>
<dd><tt>list&nbsp;of&nbsp;weak&nbsp;references&nbsp;to&nbsp;the&nbsp;object&nbsp;(if&nbsp;defined)</tt></dd>
</dl>
</td></tr></table></td></tr></table>
</body></html>
