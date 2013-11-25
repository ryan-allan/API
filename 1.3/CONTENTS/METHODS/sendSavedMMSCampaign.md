<a href="/1.3/README.md">Back to the Table of Contents</a>&nbsp;&nbsp;|&nbsp;&nbsp;<a href="API_METHODS.md">Back to API Methods</a>
<h2>sendSavedMMSCampaign</h2>
<div><strong>*Postback Notifications for this action are the same as for SendSavedMMS*</strong></div>
<p><strong>Synopsis:</strong><br />
This API function sends stored MMS from a specified account using a MMSID to a list of mobile numbers that are currently subscribed to a campaign. Recipient addresses are not specified, only the CampaignID is specified. Content will be sent from campaign default shortcode.
<div><strong>Request:</strong></div>
<pre>&lt;REQUEST&gt;
  &lt;ACTION&gt;sendSavedMMSCampaign&lt;/ACTION&gt;
	&lt;API_KEY&gt;API KEY&lt;/API_KEY&gt;
	&lt;MMSID&gt;MMSID&lt;/MMSID&gt;
	&lt;TOCAMPAIGN&gt;CampaignID&lt;/TOCAMPAIGN&gt;
&lt;/REQUEST&gt;</pre>
<div><strong>Request Parameters:</strong></div>
<pre><strong>Mandatory:</strong> Action, API_KEY, MMSID, ToCampaign
<strong>Optional:</strong> N/A</pre>
<strong>Response Parameters:</strong><br />
MMSID, Status, To, ScheduledID, Errorcode, Errorinfo
<strong>Related Errorcodes: </strong><br />
E241, E620, E624, E626, E629, E714

<div><strong>Request Examples</strong></div>
XML:
<pre>&lt;REQUEST&gt;
    &lt;ACTION&gt; sendSavedMMSCampaign&lt;/ACTION&gt;
    &lt;API_KEY&gt;qTFkykO9JTfahCOqJ0V2Wf5Cg1t8iWlZ&lt;/API_KEY&gt;
    &lt;TOCAMPAIGN&gt;332&lt;/TOCAMPAIGN&gt;
    &lt;MMSID&gt;35674&lt;/MMSID&gt;
&lt;/REQUEST&gt;</pre>
GET:
<pre>https://secure.skycore.com/API/wxml/1.3/index.php?action=sendsavedmmscampaign&api_key=qTFkykO9JTfahCOqJ0V2Wf5Cg1t8iWlZ
&campaignid=332&mmsid=35674</pre>
<div><strong>Response Example: Success</strong></div>
<pre>&lt;RESPONSE&gt;
    &lt;STATUS&gt;Success&lt;/STATUS&gt;
    &lt;MMSID&gt;35674&lt;/MMSID&gt;
    &lt;SCHEDULEDID&gt;12346&lt;/SCHEDULEDID&gt;
&lt;/RESPONSE&gt;</pre>
<div><strong>Response Example: Failure</strong></div>
<pre>&lt;RESPONSE&gt;
    &lt;STATUS&gt;Failure&lt;/STATUS&gt;
    &lt;ERRORCODE&gt;E714&lt;/ERRORCODE&gt;
    &lt;ERRORINFO&gt;Missing/Invalid CampaignID&lt;/ERRORINFO&gt;
&lt;/RESPONSE&gt;</pre>
<div><strong>Postback Notifications For SendSavedMMS, SendSavedMMSCampaign</strong></div>
<p>When the MMS delivery is processed successfully the system will generate a Postback notification.
For more details please visit <a href="https://github.com/SkycoreMobile/API/blob/master/1.3/CONTENTS/POSTBACK_NOTIFICATION_SYSTEM.md">postback doc</a></p>
<pre>&lt;?xml version='1.0'?&gt;
&lt;POSTBACK xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
xsi:noNamespaceSchemaLocation ="http://www.skycore.com/schema/postback.xsd"&gt;
&lt;ORIGIN&gt;MMS_MT&lt;/ORIGIN&gt;
&lt;CODE&gt;N101&lt;/CODE&gt;
&lt;SENTAS&gt;MMS&lt;/SENTAS&gt;
&lt;STATUS&gt;Message Sent&lt;/STATUS&gt;
&lt;MMSID&gt;35674&lt;/MMSID&gt;
&lt;TO&gt;16501234123&lt;/TO&gt;
&lt;TRACKINGID&gt;TU1TXzEyMzQ2&lt;/TRACKINGID&gt;
&lt;SPID&gt;0001890&lt;/SPID&gt;
&lt;TIMESTAMP&gt;2011-08-02T07:20:44-04:00&lt;/TIMESTAMP&gt;
&lt;/POSTBACK&gt;</pre>
<p>When an MMS delivery report is received the system will generate a Postback notification. Not all carriers provide MMS delivery receipts.</p>
<pre>&lt;?xml version='1.0'?&gt;
&lt;POSTBACK xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
xsi:noNamespaceSchemaLocation ="http://www.skycore.com/schema/postback.xsd"&gt;
&lt;ORIGIN&gt;MMS_MT&lt;/ORIGIN&gt;
&lt;CODE&gt;N102&lt;/CODE&gt;
&lt;SENTAS&gt;MMS&lt;/SENTAS&gt;
&lt;STATUS&gt;Message Sent/Delivered&lt;/STATUS&gt;
&lt;MMSID&gt;35674&lt;/MMSID&gt;
&lt;TO&gt;16501234123&lt;/TO&gt;
&lt;TRACKINGID&gt;TU1TXzEyMzQ2&lt;/TRACKINGID&gt;
&lt;SPID&gt;0001890&lt;/SPID&gt;
&lt;TIMESTAMP&gt;2011-08-02T07:20:49-04:00&lt;/TIMESTAMP&gt;
&lt;HANDSET&gt;motol7c&lt;/HANDSET&gt;
&lt;AGGREGATORID&gt;11529-64807-97508-73852-97658&lt;/AGGREGATORID&gt;
&lt;/POSTBACK&gt;</pre>
