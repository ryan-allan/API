<a href="/1.3/README.md">Back to the Table of Contents</a>&nbsp;&nbsp;|&nbsp;&nbsp;<a href="API_METHODS.md">Back to API Methods</a>
<h2>sendSavedEmail</h2>
<p><strong>Synopsis:</strong><br />
'sendSavedEmail' API sends a stored email template to an email address. Also, it requires a reference email campaign to which this email address will be subscribed to.
If any case, the subscription fails then the email address is added to the email campaign's audience manager as 'unsubscribed'. Subscription to the campaign may fail if: <br/>
<ol>
<li>The <i>email address</i> has already opted-out of a campaign in your account.</li>
<li>The <i>email address</i> has unsubscribed from any campaign associated with the SMTP server you are using.</li>
<li>The <i>email address</i> has filed a spam complaint.</li>
<li>The <i>email address</i> bounced during a previous delivery.</li>
</ol><br/>
The email address is referenced by 'EMAIL', email template is referenced by 'EMAILTEMPLATEID' and the email campaign is referenced by CAMPAIGNID in the API.
</p>
<p><strong>Request:</strong></p>
<pre>&lt;REQUEST&gt;
  &lt;ACTION&gt;sendSavedEmail&lt;/ACTION&gt;
	&lt;API_KEY&gt;apiKey&lt;/API_KEY&gt;
	&lt;EMAILTEMPLATEID&gt;emailTemplateId&lt;/EMAILTEMPLATEID&gt;
	&lt;EMAIL&gt;email&lt;/EMAIL&gt;
	&lt;CAMPAIGNID&gt;emailCampaignId&lt;/CAMPAIGNID&gt;
	&lt;DATA&gt;
		&lt;FIRST_NAME&gt;First Name&lt;/FIRST_NAME&gt;
		&lt;LAST_NAME&gt;Last Name&lt;/LAST_NAME&gt;
		&lt;GENDER&gt;Gender&lt;/GENDER&gt;
		...
	&lt;/DATA&gt;	
&lt;/REQUEST&gt;</pre>
<div><strong>Request Parameters:</strong></div>
<pre><strong>Mandatory:</strong> ACTION, API_KEY, EMAILTEMPLATEID, EMAIL, CAMPAIGNID
<strong>Optional:</strong> N/A</pre>
<strong>Response Parameters:</strong>
EMAILTEMPLATEID, CAMPAIGNID, EMAIL, STATUS, TRACKINGID, ERRORCODE, ERRORINFO<br>
<strong>Related Errorcodes: </strong><br />
E401, E402, E403, E713, E915, E916, E917
<div><strong>Request Examples</strong></div>
XML:
<pre>&lt;REQUEST&gt;
	&lt;ACTION&gt;sendSavedEmail&lt;/ACTION&gt;
	&lt;API_KEY&gt;qTFkykO9JTfahCOqJ0V2Wf5Cg1t8iWlZ&lt;/API_KEY&gt;
	&lt;EMAIL&gt;john@email.com&lt;/EMAIL&gt;
	&lt;EMAILTEMPLATEID&gt;1234&lt;/EMAILTEMPLATEID&gt;
	&lt;CAMPAIGNID&gt;5678&lt;/CAMPAIGNID&gt;
	&lt;DATA&gt;
		&lt;FIRST_NAME&gt;John&lt;/FIRST_NAME&gt;
		&lt;LAST_NAME&gt;Smith&lt;/LAST_NAME&gt;
		&lt;AGE&gt;29&lt;/AGE&gt;
		&lt;PET&gt;Dog&lt;/PET&gt;
	&lt;/DATA&gt;	
&lt;/REQUEST&gt;</pre>
GET:
<pre>https://secure.skycore.com/API/wxml/1.3/index.php?action=sendsavedemail&api_key=qTFkykO9JTfahCOqJ0V2Wf5Cg1t8iWlZ
&email=john@email.com&emailtemplateid=1234&campaignid=5678&data_first_name=John&data_last_name=Smith&data_age=29
&data_pet=Dog</pre>
<div><strong>Response Example: Success</strong></div>
<pre>&lt;RESPONSE&gt;
    &lt;STATUS&gt;Success&lt;/STATUS&gt;
    &lt;EMAILTEMPLATEID&gt;1234&lt;/EMAILTEMPLATEID&gt;
    &lt;TRACKINGID&gt;EMAIL_12346&lt;/TRACKINGID&gt;
    &lt;EMAIL&gt;john@email.com&lt;/EMAIL&gt;
    &lt;CAMPAIGNID&gt;5678&lt;/CAMPAIGNID&gt;
&lt;/RESPONSE&gt;</pre>
<div><strong>Response Example: Failure</strong></div>
<pre>&lt;RESPONSE&gt;
	 &lt;STATUS&gt;Failure&lt;/STATUS&gt;
	 &lt;ERRORCODE&gt;E713&lt;/ERRORCODE&gt;
         &lt;EMAIL&gt;john@email.com&lt;/EMAIL&gt;
         &lt;EMAILTEMPLATEID&gt;1234&lt;/EMAILTEMPLATEID&gt;
         &lt;CAMPAIGNID&gt;5678&lt;/CAMPAIGNID&gt;
	 &lt;ERRORINFO&gt;There is billing problem on your account&lt;/ERRORINFO&gt;
&lt;/RESPONSE&gt;</pre>
