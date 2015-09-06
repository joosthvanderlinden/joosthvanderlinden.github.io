---
layout: page
title: About me
tags: [joost, machine learning, scientific computing, netherlands]
modified: 
comments: false
share: false
image:
  feature: 
  credit: 
  creditlink: 
---

Click the header to read more about my experience, or 
<span style="cursor:hand; cursor:pointer" onClick="openAll()">
  <b> show all </b>
</span> 
/
<span style="cursor:hand; cursor:pointer" onClick="closeAll()">
  <b> close all </b>
</span>
. 
<br /><br />

<div onClick="openClose('a1')" style="cursor:hand; cursor:pointer"><b>Job 1</b></div>
 <div id="a1" class="texter">
   This is the hidden text that was revealed when the header was clicked. Such hidden text is generally
   related to the main header which opens them. You can add any number of collapsible headers. Clicking on
   the header when the text is seen hides the text. Additionally if a header is clicked it will automatically
   close any open text related to any other header while opening its own hidden text.<br /><br />
 </div>

<div onClick="openClose('a2')" style="cursor:hand; cursor:pointer"><b>Skill 1</b></div>
 <div id="a2" class="texter">
   This script works with all the newer versions of browsers like IE5+, NS6, Opera and Firefox.<br />
   This script does not work with older browsers like NSv4.x but degrades very well.<br /><br />
 </div>
 


<div onClick="openClose('a3')" style="cursor:hand; cursor:pointer"><b>Experience 1</b></div>
 <div id="a3" class="texter">
   This is one of the most compact scripts of this nature that you can find in any JavaScript archives.<br /><br />
 </div>

<!-- 'PT Serif', serif; 
Each collapsible header has 2 DIV tags, one is the main header that opens or closes the
     collapsible text and the other is for the collapsible text or content. In the first DIV
     tag the text (onClick="openClose('a1')") should not be changed and in the second DIV tag
     the text (id="a1" class="texter") is required. As you add more collapsible headers the
     identifier 'a1' should be incremented for all new headers in both DIV tags, for example
     a2 for header 2, a3 for header 3 etc. Everything else can be modified as per your
     requirements. Lastly, you can get rid of these comments in your documents. -->
