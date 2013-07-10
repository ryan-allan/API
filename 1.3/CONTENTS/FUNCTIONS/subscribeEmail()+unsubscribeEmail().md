<a href="/1.3/README.md">BACK TO TABLE OF CONTENTS</a>
<BR>
<a href="API_FUNCTIONS.md">BACK TO API FUNCTIONS</a>
<BR>
<BR>

<h1>subscribeEmail()+unsubscribeEmail()</h1>
<BR>

<p><strong>Synopsis:</strong><br />
This API will subscribe or unsubscribe EMAIL addresses to a particular campaign. Once an EMAIL address is subscribed to a campaign they will receive all auto responders and scheduled messages for that campaign until they are unsubscribed through the API or UI. You can unsubscribe ALL subscribers from campaign by using &#8216;ALL&#8217; as an EMAIL address.</p>
<div><strong>Request: subscribeEmail</strong></div>
<pre>&lt;REQUEST&gt;
  &lt;ACTION&gt;subscribeEmail&lt;/ACTION&gt;
	&lt;API_KEY&gt;API KEY&lt;/API_KEY&gt;
	&lt;CAMPAIGNID&gt;Campaign ID&lt;/CAMPAIGNID&gt;
	&lt;EMAIL&gt;Email address to subscribe&lt;/EMAIL&gt;
	&lt;NOTIFY&gt;'yes/no' on whether to notify user on successful opt in&lt;/NOTIFY&gt;
&lt;/REQUEST&gt;</pre>
<div><strong>Request: unsubscribeEmail</strong></div>
<pre>&lt;REQUEST&gt;
    &lt;ACTION&gt;unsubscribeEmail&lt;/ACTION&gt;
    &lt;API_KEY&gt;API KEY&lt;/API_KEY&gt;
    &lt;CAMPAIGNID&gt;Campaign ID&lt;/CAMPAIGNID&gt;
    &lt;EMAIL&gt;Email address to subscribe&lt;/EMAIL&gt;
&lt;/REQUEST&gt;</pre>
<div><strong>Request Parameters:</strong></div>
<pre><strong>Mandatory:</strong> Action, API_KEY, CAMPAIGNID, Email
<strong>Optional:</strong> Notify</pre>
<strong>Response Parameters:</strong><br />

    CAMPAIGNID, Errorcode, Errorinfo, Email, Status

<strong>Related Errorcodes: </strong><br />

    E911, E912, E913, E914

<div><strong>Request Example:</strong></div>
<pre>&lt;REQUEST&gt;
	&lt;ACTION&gt;subscribeEmail&lt;/ACTION&gt;
	&lt;API_KEY&gt;qTFkykO9JTfahCOqJ0V2Wf5Cg1t8iWlZ&lt;/API_KEY&gt;
	&lt;CAMPAIGNID&gt;1116&lt;/CAMPAIGNID&gt;
	&lt;EMAIL&gt;john@email.com&lt;/EMAIL&gt;
	&lt;NOTIFY&gt;yes&lt;/NOTIFY&gt;
&lt;/REQUEST&gt;</pre>
<div><strong>Response Example: Success</strong></div>
<pre>&lt;RESPONSE&gt;
    &lt;STATUS&gt;Success&lt;/STATUS&gt;
    &lt;CAMPAIGNID&gt;1116&lt;/CAMPAIGNID&gt;
    &lt;EMAIL&gt;john@email.com&lt;/EMAIL&gt;
&lt;/RESPONSE&gt;</pre>
<div><strong>Response Example: Failure</strong></div>
<pre>&lt;RESPONSE&gt;
    &lt;STATUS&gt;Failure&lt;/STATUS&gt;
    &lt;ERRORCODE&gt;E912&lt;/ERRORCODE&gt;
    &lt;ERRORINFO&gt; Invalid CAMPAIGNID &lt;/ERRORINFO&gt;
&lt;/RESPONSE&gt;</pre>
