<a href="/1.3/README.md">Back to the Table of Contents</a>&nbsp;&nbsp;|&nbsp;&nbsp;<a href="API_METHODS.md">Back to API Methods</a>
<h2>subscribeEmail + unsubscribeEmail</h2>
<p><strong>Synopsis:</strong><br/>
This API will subscribe or unsubscribe EMAIL addresses to a particular campaign. Once an EMAIL address is subscribed to a campaign they will receive all auto responders and scheduled messages for that campaign until they are unsubscribed through the API or UI. You can unsubscribe ALL subscribers from campaign by using &#8216;ALL&#8217; as an EMAIL address.</p>
<div><strong>Request: subscribeEmail</strong></div>
<pre>&lt;REQUEST&gt;
  &lt;ACTION&gt;subscribeEmail&lt;/ACTION&gt;
	&lt;API_KEY&gt;API KEY&lt;/API_KEY&gt;
	&lt;CAMPAIGNID&gt;Campaign ID&lt;/CAMPAIGNID&gt;
	&lt;EMAIL&gt;Email address to subscribe&lt;/EMAIL&gt;
	&lt;DATA&gt;
		&lt;FIRST_NAME&gt;First Name&lt;/FIRST_NAME&gt;
		&lt;LAST_NAME&gt;Last Name&lt;/LAST_NAME&gt;
		&lt;GENDER&gt;Gender&lt;/GENDER&gt;
		...
	&lt;/DATA&gt;	
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
<strong>Optional:</strong> Data, Notify</pre>
<strong>Response Parameters:</strong><br />

    CAMPAIGNID, Errorcode, Errorinfo, Email, Status

<strong>Related Errorcodes: </strong><br />

    E911, E912, E913, E914

<div><strong>Request Examples</strong></div>
XML:
<pre>&lt;REQUEST&gt;
	&lt;ACTION&gt;subscribeEmail&lt;/ACTION&gt;
	&lt;API_KEY&gt;qTFkykO9JTfahCOqJ0V2Wf5Cg1t8iWlZ&lt;/API_KEY&gt;
	&lt;CAMPAIGNID&gt;1116&lt;/CAMPAIGNID&gt;
	&lt;EMAIL&gt;john@email.com&lt;/EMAIL&gt;
	&lt;DATA&gt;
		&lt;FIRST_NAME&gt;John&lt;/FIRST_NAME&gt;
		&lt;LAST_NAME&gt;Smith&lt;/LAST_NAME&gt;
		&lt;AGE&gt;30&lt;/AGE&gt;
		&lt;PET&gt;Dog&lt;/PET&gt;
	&lt;/DATA&gt;	
	&lt;NOTIFY&gt;yes&lt;/NOTIFY&gt;
&lt;/REQUEST&gt;</pre>
GET:
<pre>https://secure.skycore.com/API/wxml/1.3/index.php?action=subscribeemail&api_key=qTFkykO9JTfahCOqJ0V2Wf5Cg1t8iWlZ
&email=john@email.com&campaignid=1116&notify=yes&data_first_name=John&data_last_name=Smith&data_age=30&data_pet=Dog</pre>
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
