<a href="/1.3/README.md">Back to the Table of Contents</a>&nbsp;&nbsp;|&nbsp;&nbsp;<a href="/1.3/CONTENTS/POSTBACKS/New%20Postback%20Files/POSTBACK_SYSTEM_OVERVIEW.md">Postback System Overview</a>

<p><strong>Group #3- Subscribe/Unsubscribe for Phone/Email</strong></p>
<p><strong>a) Synopsis:</strong> This Postback notification subscribes a phone number to a specific campaign. Postback contain following nodes:</p>
<p>CODE, ORIGIN</p>
<p>MOBILE &#8211; subscriber&#8217;s mobile</p>
<p>CAMPAIGNID &#8211; ID of the campaign</p>
<p>SUBID &#8211; subscription ID</p>
<p><strong>Postback Notification Example:</strong></p>
<p><small><code>&lt;?xml version='1.0'?&gt;<br>
&lt;POSTBACK&gt;<br>
&lt;ORIGIN&gt;SUB&lt;/ORIGIN&gt;<br />
&lt;CODE&gt;N301&lt;/CODE&gt;<br />
&lt;MOBILE&gt;16501112222&lt;/MOBILE&gt;<br />
&lt;CAMPAIGNID&gt;1478&lt;/CAMPAIGNID&gt;<br />
&lt;SUBID&gt;656655&lt;/SUBID&gt;<br />
&lt;/POSTBACK&gt;<br />
</code></small></p>
<p><strong>b) Synopsis:</strong> This Postback notification unsubscribes a phone number from a specific campaign. Postback contain following nodes:</p>
<p>MOBILE &#8211; subscriber&#8217;s mobile</p>
<p>CAMPAIGNID &#8211; ID of the campaign</p>
<p>SUBID &#8211; subscription ID</p>
<p><strong>Postback Notification Example:</strong></p>
<p><small><code>&lt;?xml version='1.0'?&gt;<br>
&lt;POSTBACK&gt;<br>
&lt;ORIGIN&gt;SUB&lt;/ORIGIN&gt;<br />
&lt;CODE&gt;N302&lt;/CODE&gt;<br />
&lt;MOBILE&gt;16502424956&lt;/MOBILE&gt;<br />
&lt;CAMPAIGNID&gt;1478&lt;/CAMPAIGNID&gt;<br />
&lt;SUBID&gt;656655&lt;/SUBID&gt;<br />
&lt;/POSTBACK&gt;<br />
</code></small></p>
<p><strong>c) Synopsis:</strong> This Postback notification subscribes an email to a specific campaign. Postback contain following nodes:</p>
<p>CODE, ORIGIN</p>
<p>EMAIL &#8211; subscriber&#8217;s email</p>
<p>CAMPAIGNID &#8211; ID of the campaign</p>
<p>SUBID &#8211; subscription ID</p>
<p><strong>Postback Notification Example:</strong></p>
<p><small><code>&lt;?xml version='1.0'?&gt;<br>
&lt;POSTBACK&gt;<br>
&lt;ORIGIN&gt;EMAIL_SUB&lt;/ORIGIN&gt;<br />
&lt;CODE&gt;N303&lt;/CODE&gt;<br />
&lt;EMAIL&gt;jacek@skycore.com&lt;/EMAIL&gt;<br />
&lt;CAMPAIGNID&gt;89&lt;/CAMPAIGNID&gt;<br />
&lt;SUBID&gt;12913&lt;/SUBID&gt;<br />
&lt;/POSTBACK&gt;<br />
</code></small></p>
<p><strong>d) Synopsis:</strong> This Postback notification unsubscribes an email from a specific campaign. Postback contain following nodes:</p>
<p>CODE, ORIGIN</p>
<p>EMAIL &#8211; subscriber&#8217;s email</p>
<p>CAMPAIGNID &#8211; ID of the campaign</p>
<p>SUBID &#8211; subscription ID</p>
<p><strong>Postback Notification Example:</strong></p>
<p><small><code>&lt;?xml version='1.0'?&gt;<br>
&lt;POSTBACK&gt;<br>
&lt;ORIGIN&gt;EMAIL_SUB&lt;/ORIGIN&gt;<br />
&lt;CODE&gt;N304&lt;/CODE&gt;<br />
&lt;EMAIL&gt;jacek@skycore.com&lt;/EMAIL&gt;<br />
&lt;CAMPAIGNID&gt;89&lt;/CAMPAIGNID&gt;<br />
&lt;SUBID&gt;12913&lt;/SUBID&gt;<br />
&lt;/POSTBACK&gt;<br />
</code></small></p>
