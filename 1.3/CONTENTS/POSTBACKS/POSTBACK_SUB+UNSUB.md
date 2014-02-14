<a href="/1.3/README.md">Back to the Table of Contents</a>&nbsp;&nbsp;|&nbsp;&nbsp;<a href="/1.3/CONTENTS/POSTBACKS/POSTBACK_SYSTEM_OVERVIEW.md">Postback System Overview</a>

<h2>Subscribe and Unsubscribe Postbacks</h2>
<div id="page-content"><strong>Brief Overview:</strong>
This document will provide a technical description of the Subscribe and Unsubscribe postbacks API for phone and email. Briefly, this API allows those with subscribe and unsubscribe postbacks enabled to generate and forward postbacks to their server when an individual subscribes or unsubscribes from a mobile or email campaign.

<strong>Mobile Subscribe</strong>
<p><strong>Synopsis:</strong> This postback notification subscribes a phone number to a specific campaign.</p>
<strong><p>This postback will contain the following nodes:</p></strong>
CODE, ORIGIN<BR/>
MOBILE &#8211; subscriber&#8217;s mobile<BR/>
CAMPAIGNID &#8211; ID of the campaign<BR/>
SUBID &#8211; subscription ID<BR/>

<p><strong>This postback has the following anatomy:</strong></p>
<pre>
&lt;?xml version='1.0'?&gt;
&lt;POSTBACK&gt;
  &lt;ORIGIN&gt;SUB&lt;/ORIGIN&gt;
  &lt;CODE&gt;N301&lt;/CODE&gt;
  &lt;MOBILE&gt;16501112222&lt;/MOBILE&gt;
  &lt;CAMPAIGNID&gt;1478&lt;/CAMPAIGNID&gt;
  &lt;SUBID&gt;656655&lt;/SUBID&gt;
&lt;/POSTBACK&gt;
</pre>

<strong>Mobile Unsubscribe</strong>
<p><strong>Synopsis:</strong> This postback notification unsubscribes a phone number from a specific campaign.</p>
<strong><p>This postback will contain the following nodes:</p></strong>
CODE, ORIGIN<BR/>
MOBILE &#8211; subscriber&#8217;s mobile<BR/>
CAMPAIGNID &#8211; ID of the campaign<BR/>
SUBID &#8211; subscription ID<BR/>

<p><strong>This postback has the following anatomy:</strong></p>
<pre>
&lt;?xml version='1.0'?&gt;
&lt;POSTBACK&gt;
  &lt;ORIGIN&gt;SUB&lt;/ORIGIN&gt;
  &lt;CODE&gt;N302&lt;/CODE&gt;
  &lt;MOBILE&gt;16502424956&lt;/MOBILE&gt;
  &lt;CAMPAIGNID&gt;1478&lt;/CAMPAIGNID&gt;
  &lt;SUBID&gt;656655&lt;/SUBID&gt;
&lt;/POSTBACK&gt;
</pre>

<strong>Email Subscribe</strong>
<p><strong>Synopsis:</strong> This postback notification subscribes an email to a specific campaign.</p>
<strong><p>This postback will contain the following nodes:</p></strong>
CODE, ORIGIN<BR/>
EMAIL &#8211; subscriber&#8217;s email<BR/>
CAMPAIGNID &#8211; ID of the campaign<BR/>
SUBID &#8211; subscription ID<BR/>

<p><strong>This postback has the following anatomy:</strong></p>
<pre>
&lt;?xml version='1.0'?&gt;
&lt;POSTBACK&gt;
  &lt;ORIGIN&gt;EMAIL_SUB&lt;/ORIGIN&gt;
  &lt;CODE&gt;N303&lt;/CODE&gt;
  &lt;EMAIL&gt;jacek@skycore.com&lt;/EMAIL&gt;
  &lt;CAMPAIGNID&gt;89&lt;/CAMPAIGNID&gt;
  &lt;SUBID&gt;12913&lt;/SUBID&gt;
&lt;/POSTBACK&gt;
</pre>

<strong>Email Unsubscribe</strong>
<p><strong>Synopsis:</strong> This postback notification unsubscribes an email from a specific campaign.</p>
<strong><p>This postback will contain the following nodes:</p></strong>
CODE, ORIGIN<BR/>
EMAIL &#8211; subscriber&#8217;s email<BR/>
CAMPAIGNID &#8211; ID of the campaign<BR/>
SUBID &#8211; subscription ID<BR/>

<p><strong>This postback has the following anatomy:</strong></p>
<pre>
&lt;?xml version='1.0'?&gt;
&lt;POSTBACK&gt;
  &lt;ORIGIN&gt;EMAIL_SUB&lt;/ORIGIN&gt;
  &lt;CODE&gt;N304&lt;/CODE&gt;
  &lt;EMAIL&gt;jacek@skycore.com&lt;/EMAIL&gt;
  &lt;CAMPAIGNID&gt;89&lt;/CAMPAIGNID&gt;
  &lt;SUBID&gt;12913&lt;/SUBID&gt;
&lt;/POSTBACK&gt;
</pre>
