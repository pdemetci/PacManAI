---
layout: post
title:  "Documentation"
date:   2015-05-05 05:46:00
categories: jekyll update
---

**Documentation**

The following was generated with pydoc.

<table width="100%" cellspacing=0 cellpadding=2 border=0 summary="heading">
<tr bgcolor="#7799ee">
<td valign=bottom>&nbsp;<br>
<font color="#ffffff" face="helvetica, arial">&nbsp;<br><big><big><strong>pacmanAgents</strong></big></big></font></td
><td align=right valign=bottom
><font color="#ffffff" face="helvetica, arial"><a href=".">index</a><br><a href="file:/home/snorthway/semester-8/softdes/PacMan-AI/PacMan1/pacmanAgents.py">/home/snorthway/semester-8/softdes/PacMan-AI/PacMan1/pacmanAgents.py</a></font></td></tr></table>
    <p><tt>Glue&nbsp;for&nbsp;interfacing&nbsp;with&nbsp;the&nbsp;Berkeley&nbsp;code.<br>
@author&nbsp;Stephanie&nbsp;Northway,&nbsp;Kelly&nbsp;Brennan&nbsp;and&nbsp;Pinar&nbsp;Demetci</tt></p>
<p>
<table width="100%" cellspacing=0 cellpadding=2 border=0 summary="section">
<tr bgcolor="#aa55cc">
<td colspan=3 valign=bottom>&nbsp;<br>
<font color="#ffffff" face="helvetica, arial"><big><strong>Modules</strong></big></font></td></tr>
    
<tr><td bgcolor="#aa55cc"><tt>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</tt></td><td>&nbsp;</td>
<td width="100%"><table width="100%" summary="list"><tr><td width="25%" valign=top><a href="operator.html">operator</a><br>
</td><td width="25%" valign=top><a href="pickle.html">pickle</a><br>
</td><td width="25%" valign=top><a href="random.html">random</a><br>
</td><td width="25%" valign=top></td></tr></table></td></tr></table><p>
<table width="100%" cellspacing=0 cellpadding=2 border=0 summary="section">
<tr bgcolor="#ee77aa">
<td colspan=3 valign=bottom>&nbsp;<br>
<font color="#ffffff" face="helvetica, arial"><big><strong>Classes</strong></big></font></td></tr>
    
<tr><td bgcolor="#ee77aa"><tt>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</tt></td><td>&nbsp;</td>
<td width="100%"><dl>
<dt><font face="helvetica, arial"><a href="game.html#Agent">game.Agent</a>(<a href="__builtin__.html#object">__builtin__.object</a>)
</font></dt><dd>
<dl>
<dt><font face="helvetica, arial"><a href="pacmanAgents.html#SimpleQPacman">SimpleQPacman</a>
</font></dt></dl>
</dd>
</dl>
 <p>
<table width="100%" cellspacing=0 cellpadding=2 border=0 summary="section">
<tr bgcolor="#ffc8d8">
<td colspan=3 valign=bottom>&nbsp;<br>
<font color="#000000" face="helvetica, arial"><a name="SimpleQPacman">class <strong>SimpleQPacman</strong></a>(<a href="game.html#Agent">game.Agent</a>)</font></td></tr>
    
<tr bgcolor="#ffc8d8"><td rowspan=2><tt>&nbsp;&nbsp;&nbsp;</tt></td>
<td colspan=2><tt>Represents&nbsp;the&nbsp;pacman&nbsp;agent&nbsp;that&nbsp;implements&nbsp;the&nbsp;continuous&nbsp;state&nbsp;Q-learning<br>
algorithm&nbsp;to&nbsp;learn&nbsp;from&nbsp;it's&nbsp;previous&nbsp;exerience.&nbsp;The&nbsp;agent&nbsp;inherits&nbsp;the<br>
attritbutes&nbsp;and&nbsp;methods&nbsp;from&nbsp;the&nbsp;Berkeley&nbsp;<a href="game.html#Agent">Agent</a>&nbsp;Class.<br>
&nbsp;<br>
features:&nbsp;a&nbsp;list&nbsp;of&nbsp;Features&nbsp;the&nbsp;agent&nbsp;will&nbsp;use<br>
tiles:&nbsp;dictionary&nbsp;to&nbsp;hold&nbsp;all&nbsp;of&nbsp;the&nbsp;tiles&nbsp;on&nbsp;the&nbsp;game&nbsp;layout<br>
learningRate:&nbsp;how&nbsp;much&nbsp;you&nbsp;adjust&nbsp;the&nbsp;weight&nbsp;relative&nbsp;to&nbsp;the&nbsp;Q-value<br>
discountFactor:&nbsp;Weight&nbsp;to&nbsp;balance&nbsp;instant&nbsp;reward&nbsp;with&nbsp;future&nbsp;long&nbsp;term&nbsp;awards<br>
exploraitonRate:&nbsp;probability&nbsp;that&nbsp;pacman&nbsp;will&nbsp;explore,&nbsp;instead&nbsp;of&nbsp;using&nbsp;optimal&nbsp;action<br>&nbsp;</tt></td></tr>
<tr><td>&nbsp;</td>
<td width="100%"><dl><dt>Method resolution order:</dt>
<dd><a href="pacmanAgents.html#SimpleQPacman">SimpleQPacman</a></dd>
<dd><a href="game.html#Agent">game.Agent</a></dd>
<dd><a href="__builtin__.html#object">__builtin__.object</a></dd>
</dl>
<hr>
Methods defined here:<br>
<dl><dt><a name="SimpleQPacman-__init__"><strong>__init__</strong></a>(self, fromPickle<font color="#909090">=True</font>)</dt><dd><tt>Pickling&nbsp;the&nbsp;feature&nbsp;weights&nbsp;for&nbsp;agent&nbsp;to&nbsp;learn&nbsp;from&nbsp;its&nbsp;actions&nbsp;in&nbsp;previous&nbsp;GameState</tt></dd></dl>

<dl><dt><a name="SimpleQPacman-getAction"><strong>getAction</strong></a>(self, state)</dt><dd><tt>getAction&nbsp;runs&nbsp;pacman&nbsp;agent's&nbsp;show&nbsp;by&nbsp;determing&nbsp;what&nbsp;action&nbsp;the<br>
agent&nbsp;will&nbsp;take,&nbsp;based&nbsp;on&nbsp;it's&nbsp;current&nbsp;state&nbsp;and&nbsp;Q-learning&nbsp;values<br>
&nbsp;<br>
Initialize&nbsp;the&nbsp;game&nbsp;layout&nbsp;tiles&nbsp;when&nbsp;pacman&nbsp;is&nbsp;in&nbsp;start&nbsp;configuration<br>
Updates&nbsp;the&nbsp;pacman's&nbsp;feature&nbsp;values<br>
Determines&nbsp;the&nbsp;agent's&nbsp;optimal&nbsp;action,&nbsp;given&nbsp;its&nbsp;specific&nbsp;configuration<br>
based&nbsp;on&nbsp;the&nbsp;maximum&nbsp;Q&nbsp;value&nbsp;or&nbsp;implements&nbsp;a&nbsp;random&nbsp;action<br>
Updates&nbsp;feature&nbsp;weights&nbsp;based&nbsp;on&nbsp;it's&nbsp;final&nbsp;action<br>
&nbsp;<br>
state:&nbsp;GameState&nbsp;object<br>
returns:&nbsp;random&nbsp;action,&nbsp;if&nbsp;exploring,&nbsp;and&nbsp;optimal&nbsp;action,&nbsp;if&nbsp;not&nbsp;exploring</tt></dd></dl>

<dl><dt><a name="SimpleQPacman-getApproximateQValue"><strong>getApproximateQValue</strong></a>(self, state)</dt><dd><tt>Calculate&nbsp;the&nbsp;linear&nbsp;combination&nbsp;of&nbsp;the&nbsp;feature&nbsp;values&nbsp;and&nbsp;their<br>
respective&nbsp;weights&nbsp;to&nbsp;approximate&nbsp;Q-value.<br>
&nbsp;<br>
state:&nbsp;GameState&nbsp;object<br>
return:&nbsp;Approximate&nbsp;Q&nbsp;value&nbsp;based&nbsp;on&nbsp;the&nbsp;feature&nbsp;weights,&nbsp;#</tt></dd></dl>

<dl><dt><a name="SimpleQPacman-getExpectedNextReward"><strong>getExpectedNextReward</strong></a>(self, state, action)</dt><dd><tt>More&nbsp;reward&nbsp;is&nbsp;given&nbsp;when&nbsp;pacman&nbsp;agent&nbsp;increases&nbsp;the&nbsp;score&nbsp;with&nbsp;it's&nbsp;action<br>
Calculate&nbsp;the&nbsp;expected&nbsp;reward&nbsp;of&nbsp;a&nbsp;given&nbsp;state&nbsp;and&nbsp;action&nbsp;based&nbsp;on&nbsp;score&nbsp;change<br>
r_t+1&nbsp;=&nbsp;R(s_t,&nbsp;a_t,&nbsp;s_t+1)<br>
&nbsp;<br>
state:&nbsp;GameState&nbsp;object<br>
Action:&nbsp;direction&nbsp;(string)<br>
return:&nbsp;change&nbsp;in&nbsp;score&nbsp;based&nbsp;on&nbsp;action</tt></dd></dl>

<dl><dt><a name="SimpleQPacman-getMaxQ"><strong>getMaxQ</strong></a>(self, state)</dt><dd><tt>Calculate&nbsp;the&nbsp;Q-values&nbsp;of&nbsp;all&nbsp;the&nbsp;legal&nbsp;actions&nbsp;and&nbsp;determine&nbsp;max&nbsp;Q-value<br>
to&nbsp;determine&nbsp;the&nbsp;optimal&nbsp;action<br>
&nbsp;<br>
state:&nbsp;GameState&nbsp;object<br>
return:&nbsp;action,&nbsp;maximum&nbsp;Q-value&nbsp;(tuple:&nbsp;string,&nbsp;float)</tt></dd></dl>

<dl><dt><a name="SimpleQPacman-getMaxQAction"><strong>getMaxQAction</strong></a>(self, state)</dt><dd><tt>return&nbsp;action&nbsp;with&nbsp;max&nbsp;Q-value&nbsp;of&nbsp;given&nbsp;agent&nbsp;state<br>
&nbsp;<br>
state:&nbsp;GameState&nbsp;object<br>
return:&nbsp;action&nbsp;with&nbsp;the&nbsp;maximum&nbsp;Q-value&nbsp;(string)</tt></dd></dl>

<dl><dt><a name="SimpleQPacman-getMaxQValue"><strong>getMaxQValue</strong></a>(self, state)</dt><dd><tt>return&nbsp;max&nbsp;Q-value&nbsp;of&nbsp;given&nbsp;agent&nbsp;state<br>
&nbsp;<br>
state:&nbsp;GameState&nbsp;object<br>
return:&nbsp;maximum&nbsp;Q-Value&nbsp;(float)</tt></dd></dl>

<dl><dt><a name="SimpleQPacman-getQValue"><strong>getQValue</strong></a>(self, state, action)</dt><dd><tt>Calculate&nbsp;the&nbsp;Q-Value&nbsp;based&nbsp;on&nbsp;algorithm<br>
Q'&nbsp;=&nbsp;(1-learningRate)&nbsp;*&nbsp;(Q&nbsp;+&nbsp;learningRate)&nbsp;*&nbsp;(R&nbsp;+&nbsp;R')<br>
&nbsp;<br>
state:&nbsp;GameState&nbsp;object<br>
action:&nbsp;direction&nbsp;(string)<br>
return:&nbsp;Q-value&nbsp;(float)</tt></dd></dl>

<dl><dt><a name="SimpleQPacman-isExploring"><strong>isExploring</strong></a>(self)</dt><dd><tt>Uses&nbsp;explorationRate&nbsp;to&nbsp;decide&nbsp;if&nbsp;pacman&nbsp;agent&nbsp;explores&nbsp;or&nbsp;uses&nbsp;Q-learning<br>
&nbsp;<br>
returns:&nbsp;True&nbsp;or&nbsp;False</tt></dd></dl>

<dl><dt><a name="SimpleQPacman-lose"><strong>lose</strong></a>(self, state)</dt><dd><tt>Stores&nbsp;feature&nbsp;weight&nbsp;values&nbsp;when&nbsp;game&nbsp;ends&nbsp;so&nbsp;pacman&nbsp;agent&nbsp;can&nbsp;learn&nbsp;from&nbsp;experience<br>
over&nbsp;multiple&nbsp;games<br>
Update&nbsp;the&nbsp;feature&nbsp;weights&nbsp;and&nbsp;store&nbsp;by&nbsp;pickling&nbsp;when&nbsp;pacman&nbsp;agent&nbsp;loses<br>
&nbsp;<br>
input:&nbsp;GameState&nbsp;object<br>
output:&nbsp;feature&nbsp;weights&nbsp;in&nbsp;pickle&nbsp;file</tt></dd></dl>

<dl><dt><a name="SimpleQPacman-updateFeatures"><strong>updateFeatures</strong></a>(self, state)</dt><dd><tt>Update&nbsp;the&nbsp;feature&nbsp;values<br>
&nbsp;<br>
state:&nbsp;GameState&nbsp;object<br>
returns:&nbsp;None</tt></dd></dl>

<dl><dt><a name="SimpleQPacman-updateWeights"><strong>updateWeights</strong></a>(self, state, action)</dt><dd><tt>Essential&nbsp;for&nbsp;pacman&nbsp;learning&nbsp;what&nbsp;features&nbsp;are&nbsp;most&nbsp;important&nbsp;for&nbsp;earning&nbsp;rewards<br>
negative&nbsp;weight&nbsp;values&nbsp;-&nbsp;pacman&nbsp;attracted&nbsp;toward&nbsp;feature&nbsp;to&nbsp;increase&nbsp;reward<br>
&nbsp;&nbsp;&nbsp;&nbsp;ex.&nbsp;agent&nbsp;going&nbsp;towards&nbsp;food<br>
positive&nbsp;weight&nbsp;values&nbsp;-&nbsp;pacman&nbsp;repelled&nbsp;by&nbsp;feature&nbsp;to&nbsp;increase&nbsp;reward<br>
&nbsp;&nbsp;&nbsp;&nbsp;ex.&nbsp;agent&nbsp;going&nbsp;away&nbsp;from&nbsp;ghosts<br>
&nbsp;<br>
update&nbsp;weight&nbsp;values&nbsp;of&nbsp;each&nbsp;feature&nbsp;based&nbsp;on&nbsp;the&nbsp;change&nbsp;in&nbsp;that<br>
feature&nbsp;from&nbsp;the&nbsp;last&nbsp;state.<br>
w_t+1&nbsp;=&nbsp;w_t&nbsp;+&nbsp;alpha(r_t+1&nbsp;+&nbsp;gamma*&nbsp;max(a)Q(s',&nbsp;a)&nbsp;-&nbsp;Q(s,&nbsp;a))*phi_t<br>
&nbsp;<br>
state:&nbsp;GameState&nbsp;object,<br>
action:&nbsp;direction&nbsp;(string)<br>
return:&nbsp;None</tt></dd></dl>

<dl><dt><a name="SimpleQPacman-win"><strong>win</strong></a>(self, state)</dt><dd><tt>Stores&nbsp;feature&nbsp;weight&nbsp;values&nbsp;when&nbsp;game&nbsp;ends&nbsp;so&nbsp;pacman&nbsp;agent&nbsp;can&nbsp;learn&nbsp;from&nbsp;experience<br>
over&nbsp;multiple&nbsp;games<br>
Update&nbsp;the&nbsp;feature&nbsp;weights&nbsp;and&nbsp;store&nbsp;by&nbsp;pickling&nbsp;when&nbsp;pacman&nbsp;agent&nbsp;wins<br>
&nbsp;<br>
input:&nbsp;GameState&nbsp;object<br>
output:&nbsp;feature&nbsp;weights&nbsp;in&nbsp;pickle&nbsp;file</tt></dd></dl>

<hr>
Data descriptors inherited from <a href="game.html#Agent">game.Agent</a>:<br>
<dl><dt><strong>__dict__</strong></dt>
<dd><tt>dictionary&nbsp;for&nbsp;instance&nbsp;variables&nbsp;(if&nbsp;defined)</tt></dd>
</dl>
<dl><dt><strong>__weakref__</strong></dt>
<dd><tt>list&nbsp;of&nbsp;weak&nbsp;references&nbsp;to&nbsp;the&nbsp;object&nbsp;(if&nbsp;defined)</tt></dd>
</dl>
</td></tr></table></td></tr></table>

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

<body bgcolor="#f0f0f8">

<table width="100%" cellspacing=0 cellpadding=2 border=0 summary="heading">
<tr bgcolor="#7799ee">
<td valign=bottom>&nbsp;<br>
<font color="#ffffff" face="helvetica, arial">&nbsp;<br><big><big><strong>util2</strong></big></big></font></td
><td align=right valign=bottom
><font color="#ffffff" face="helvetica, arial"><a href=".">index</a><br><a href="file:/home/snorthway/semester-8/softdes/PacMan-AI/PacMan1/util2.py">/home/snorthway/semester-8/softdes/PacMan-AI/PacMan1/util2.py</a></font></td></tr></table>
    <p><tt>@author:&nbsp;Kelly&nbsp;Brennan,&nbsp;Stephanie&nbsp;Norway&nbsp;and&nbsp;Pinar&nbsp;Demetci<br>
Our&nbsp;own&nbsp;utility&nbsp;functions&nbsp;and&nbsp;classes.</tt></p>
<p>
<table width="100%" cellspacing=0 cellpadding=2 border=0 summary="section">
<tr bgcolor="#ee77aa">
<td colspan=3 valign=bottom>&nbsp;<br>
<font color="#ffffff" face="helvetica, arial"><big><strong>Classes</strong></big></font></td></tr>
    
<tr><td bgcolor="#ee77aa"><tt>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</tt></td><td>&nbsp;</td>
<td width="100%"><dl>
<dt><font face="helvetica, arial"><a href="__builtin__.html#object">__builtin__.object</a>
</font></dt><dd>
<dl>
<dt><font face="helvetica, arial"><a href="util2.html#Tile">Tile</a>
</font></dt></dl>
</dd>
</dl>
 <p>
<table width="100%" cellspacing=0 cellpadding=2 border=0 summary="section">
<tr bgcolor="#ffc8d8">
<td colspan=3 valign=bottom>&nbsp;<br>
<font color="#000000" face="helvetica, arial"><a name="Tile">class <strong>Tile</strong></a>(<a href="__builtin__.html#object">__builtin__.object</a>)</font></td></tr>
    
<tr bgcolor="#ffc8d8"><td rowspan=2><tt>&nbsp;&nbsp;&nbsp;</tt></td>
<td colspan=2><tt>Represents&nbsp;a&nbsp;position&nbsp;on&nbsp;the&nbsp;board&nbsp;in&nbsp;terms&nbsp;of&nbsp;what&nbsp;it&nbsp;will&nbsp;cost&nbsp;Pacman&nbsp;to&nbsp;get&nbsp;there.<br>
For&nbsp;example&nbsp;layout,&nbsp;food&nbsp;is&nbsp;in&nbsp;[(18,&nbsp;1),&nbsp;(1,9)].&nbsp;Bottom&nbsp;left-hand&nbsp;corner&nbsp;=&nbsp;(1,1).<br>
&nbsp;<br>
coordinates:&nbsp;the&nbsp;coordinates&nbsp;of&nbsp;this&nbsp;tile<br>
g_cost:&nbsp;total&nbsp;cost&nbsp;of&nbsp;moving&nbsp;the&nbsp;agent&nbsp;from&nbsp;a&nbsp;start&nbsp;position&nbsp;to&nbsp;a&nbsp;given&nbsp;square<br>
h_cost:&nbsp;number&nbsp;of&nbsp;total&nbsp;moves&nbsp;(as&nbsp;the&nbsp;crow&nbsp;flies)&nbsp;to&nbsp;goal<br>
f_cost:&nbsp;the&nbsp;score&nbsp;for&nbsp;this&nbsp;<a href="#Tile">Tile</a><br>&nbsp;</tt></td></tr>
<tr><td>&nbsp;</td>
<td width="100%">Methods defined here:<br>
<dl><dt><a name="Tile-__init__"><strong>__init__</strong></a>(self, coordinates, g_cost<font color="#909090">=None</font>, h_cost<font color="#909090">=None</font>, f_cost<font color="#909090">=None</font>)</dt></dl>

<dl><dt><a name="Tile-__repr__"><strong>__repr__</strong></a>(self)</dt></dl>

<dl><dt><a name="Tile-__str__"><strong>__str__</strong></a>(self)</dt></dl>

<hr>
Data descriptors defined here:<br>
<dl><dt><strong>__dict__</strong></dt>
<dd><tt>dictionary&nbsp;for&nbsp;instance&nbsp;variables&nbsp;(if&nbsp;defined)</tt></dd>
</dl>
<dl><dt><strong>__weakref__</strong></dt>
<dd><tt>list&nbsp;of&nbsp;weak&nbsp;references&nbsp;to&nbsp;the&nbsp;object&nbsp;(if&nbsp;defined)</tt></dd>
</dl>
</td></tr></table></td></tr></table><p>
<table width="100%" cellspacing=0 cellpadding=2 border=0 summary="section">
<tr bgcolor="#eeaa77">
<td colspan=3 valign=bottom>&nbsp;<br>
<font color="#ffffff" face="helvetica, arial"><big><strong>Functions</strong></big></font></td></tr>
    
<tr><td bgcolor="#eeaa77"><tt>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</tt></td><td>&nbsp;</td>
<td width="100%"><dl><dt><a name="-Astar"><strong>Astar</strong></a>(state, start, goal, layout, costs)</dt><dd><tt>Astar&nbsp;function&nbsp;that&nbsp;runs&nbsp;the&nbsp;show<br>
Determines&nbsp;the&nbsp;distance&nbsp;between&nbsp;a&nbsp;position&nbsp;and&nbsp;a&nbsp;goal&nbsp;with&nbsp;obstacles,&nbsp;such&nbsp;as&nbsp;walls&nbsp;present<br>
&nbsp;<br>
start:&nbsp;initial&nbsp;position&nbsp;of&nbsp;search&nbsp;(tuple)<br>
goal:&nbsp;end&nbsp;position&nbsp;of&nbsp;search&nbsp;(tuple)<br>
layout:&nbsp;Layout&nbsp;<a href="__builtin__.html#object">object</a>&nbsp;for&nbsp;game<br>
costs:&nbsp;dictionary&nbsp;of&nbsp;tile&nbsp;objects&nbsp;that&nbsp;can&nbsp;be&nbsp;accessed&nbsp;with&nbsp;coordinate&nbsp;keys<br>
returns:&nbsp;distance&nbsp;between&nbsp;start&nbsp;and&nbsp;goal,&nbsp;if&nbsp;goal&nbsp;exists<br>
&nbsp;&nbsp;&nbsp;&nbsp;manhattanDistance&nbsp;of&nbsp;the&nbsp;layout&nbsp;board,&nbsp;if&nbsp;goal&nbsp;does&nbsp;not&nbsp;exist</tt></dd></dl>
 <dl><dt><a name="-DepthFirstSearch"><strong>DepthFirstSearch</strong></a>(state, start, costs, closed_list<font color="#909090">=[]</font>)</dt><dd><tt>Depth-first&nbsp;search&nbsp;algorithm&nbsp;to&nbsp;find&nbsp;close&nbsp;food&nbsp;pellets&nbsp;with&nbsp;greater&nbsp;computational&nbsp;efficiency&nbsp;than&nbsp;running<br>
Astar&nbsp;on&nbsp;every&nbsp;position&nbsp;with&nbsp;food.<br>
Recursive&nbsp;function,&nbsp;until&nbsp;it&nbsp;finds&nbsp;a&nbsp;food&nbsp;pellet<br>
First,&nbsp;finds&nbsp;a&nbsp;list&nbsp;of&nbsp;open&nbsp;adjacent&nbsp;coordinates.&nbsp;If&nbsp;food&nbsp;at&nbsp;coordinate,&nbsp;return&nbsp;distance&nbsp;from&nbsp;Pacman<br>
&nbsp;&nbsp;&nbsp;&nbsp;Otherwise,&nbsp;run&nbsp;function&nbsp;with&nbsp;new&nbsp;coordinate&nbsp;input<br>
&nbsp;<br>
state:&nbsp;the&nbsp;GameState&nbsp;<a href="__builtin__.html#object">object</a><br>
start:&nbsp;(x,&nbsp;y)&nbsp;coordinates&nbsp;from&nbsp;which&nbsp;to&nbsp;start&nbsp;the&nbsp;search<br>
costs:&nbsp;{(x,&nbsp;y):&nbsp;<a href="#Tile">Tile</a>((x,&nbsp;y))}<br>
closed_list:&nbsp;list&nbsp;of&nbsp;coordinates&nbsp;no&nbsp;longer&nbsp;being&nbsp;considered<br>
returns:&nbsp;Astar&nbsp;distance&nbsp;to&nbsp;the&nbsp;closest&nbsp;food&nbsp;pellet</tt></dd></dl>
 <dl><dt><a name="-get_h_cost"><strong>get_h_cost</strong></a>(coord_a, coord_b)</dt><dd><tt>Calculate&nbsp;h_cost&nbsp;of&nbsp;given&nbsp;position&nbsp;and&nbsp;goal<br>
&nbsp;<br>
coord_a:&nbsp;starting&nbsp;coordinate<br>
coord_b:&nbsp;goal&nbsp;coordinate<br>
Returns:&nbsp;the&nbsp;h&nbsp;score,&nbsp;the&nbsp;manhattan&nbsp;distance&nbsp;between&nbsp;coord_a&nbsp;and&nbsp;the&nbsp;cood_b</tt></dd></dl>
 <dl><dt><a name="-get_lowest_cost_open_coord"><strong>get_lowest_cost_open_coord</strong></a>(open_list)</dt><dd><tt>Find&nbsp;the&nbsp;tile&nbsp;with&nbsp;the&nbsp;lowest&nbsp;cost.<br>
&nbsp;<br>
open_list:&nbsp;list&nbsp;of&nbsp;<a href="#Tile">Tile</a>&nbsp;objects&nbsp;to&nbsp;sort<br>
returns:&nbsp;open_list&nbsp;sorted&nbsp;by&nbsp;f_cost</tt></dd></dl>
 <dl><dt><a name="-get_open_adj_coords"><strong>get_open_adj_coords</strong></a>(state, coords, layout)</dt><dd><tt>Finds&nbsp;the&nbsp;coordinates&nbsp;of&nbsp;the&nbsp;up&nbsp;to&nbsp;four&nbsp;open&nbsp;adjacent&nbsp;positions&nbsp;to&nbsp;coords.<br>
&nbsp;<br>
coords:&nbsp;the&nbsp;center&nbsp;coordinate&nbsp;pair<br>
layout:&nbsp;the&nbsp;Layout&nbsp;<a href="__builtin__.html#object">object</a>&nbsp;for&nbsp;the&nbsp;game<br>
returns:&nbsp;(list&nbsp;of&nbsp;open&nbsp;adjacent&nbsp;coordinates,&nbsp;ones(same&nbsp;length))</tt></dd></dl>
 <dl><dt><a name="-get_open_adj_coords_DFS"><strong>get_open_adj_coords_DFS</strong></a>(state, coords, layout)</dt><dd><tt>Get&nbsp;open&nbsp;adjacent&nbsp;coordinates&nbsp;for&nbsp;the&nbsp;DepthFirstSearch&nbsp;function.<br>
&nbsp;<br>
coords:&nbsp;the&nbsp;center&nbsp;coordinate&nbsp;pair<br>
layout:&nbsp;the&nbsp;Layout&nbsp;<a href="__builtin__.html#object">object</a>&nbsp;for&nbsp;the&nbsp;game<br>
returns:&nbsp;list&nbsp;of&nbsp;open&nbsp;adjacent&nbsp;coordinate&nbsp;pairs</tt></dd></dl>
 <dl><dt><a name="-initializeTiles"><strong>initializeTiles</strong></a>(layout)</dt><dd><tt>Initializes&nbsp;the&nbsp;open&nbsp;positions&nbsp;on&nbsp;the&nbsp;board&nbsp;as&nbsp;<a href="#Tile">Tile</a>&nbsp;objects.&nbsp;This<br>
gets&nbsp;called&nbsp;once&nbsp;at&nbsp;the&nbsp;beginning&nbsp;of&nbsp;a&nbsp;game.<br>
&nbsp;<br>
layout:&nbsp;the&nbsp;Layout&nbsp;<a href="__builtin__.html#object">object</a>&nbsp;for&nbsp;the&nbsp;game<br>
returns:&nbsp;a&nbsp;dictionary&nbsp;like&nbsp;{(x,&nbsp;y):&nbsp;<a href="#Tile">Tile</a>((x,&nbsp;y))}</tt></dd></dl>
</td></tr></table>