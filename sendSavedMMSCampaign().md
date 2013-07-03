<a href="/TABLE%20OF%20CONTENTS.md">BACK TO TABLE OF CONTENTS</a>
<BR>
<a href="/API%20FUNCTIONS.md">BACK TO API FUNCTIONS</a>
<BR>
<BR>


<h1>sendSavedMMSCampaign()</h1>
<BR>

<div><strong>Postback Notifications for this action are the same as for SendSavedMMS</strong></div>
<div></div>
<div><strong><a id="sendsavedcontentcampaign"></a>sendSavedMMSCampaign()</strong></div>
<p><strong>Synopsis:</strong><br />
This API sends stored content from a specified account using a MMSID to a list of mobile numbers that are subscribed to a campaign. Recipient addresses are not specified, only the CampaignID is specified. Content will be sent from campaign default shortcode.</p>
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
    
<div><strong>Request Example:</strong></div>
<pre>&lt;REQUEST&gt;
    &lt;ACTION&gt; sendSavedMMSCampaign&lt;/ACTION&gt;
    &lt;API_KEY&gt;qTFkykO9JTfahCOqJ0V2Wf5Cg1t8iWlZ&lt;/API_KEY&gt;
    &lt;TOCAMPAIGN&gt;332&lt;/TOCAMPAIGN&gt;
    &lt;MMSID&gt;35674&lt;/MMSID&gt;
&lt;/REQUEST&gt;</pre>
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
<p>When the MMS delivery is processed successfully the system will generate a Postback notification.</p>
<pre>&lt;NOTIFICATION ID="325" CREATED="2011-08-02 07:20:45.870623-04"&gt;
    &lt;ORIGIN&gt;MMS_MT&lt;/ORIGIN&gt;
    &lt;CODE&gt;N101&lt;/CODE&gt;
    &lt;BODY&gt;
        &lt;HISTORYID&gt;249687&lt;/HISTORYID&gt;
        &lt;MMSID&gt;35674&lt;/MMSID&gt;
        &lt;TO&gt;16501234123&lt;/TO&gt;
        &lt;TRACKINGID&gt;MMS_12346&lt;/TRACKINGID&gt;
        &lt;SCHEDULEDID&gt;12346&lt;/SCHEDULEDID&gt;
        &lt;SPID&gt;000189&lt;/SPID&gt;
        &lt;TIMESTAMP&gt;2011-08-02 07:20:44-04&lt;/TIMESTAMP&gt;
    &lt;/BODY&gt;
&lt;/NOTIFICATION&gt;</pre>
<p>When an MMS delivery report is received the system will generate a Postback notification. Not all carriers provide MMS delivery receipts.</p>
<pre>&lt;NOTIFICATION  ID="326" CREATED="2011-08-02 07:20:52.332193-04"&gt;
    &lt;ORIGIN&gt;MMS_MT&lt;/ORIGIN&gt;
    &lt;CODE&gt;N102&lt;/CODE&gt;
    &lt;BODY&gt;
        &lt;HISTORYID&gt;249687&lt;/HISTORYID&gt;
        &lt;MMSID&gt;35674&lt;/MMSID&gt;
        &lt;TO&gt;16501234123&lt;/TO&gt;
        &lt;TRACKINGID&gt;MMS_12346&lt;/TRACKINGID&gt;
        &lt;SCHEDULEDID&gt;12346&lt;/SCHEDULEDID&gt;
        &lt;SPID&gt;000189&lt;/SPID&gt;
        &lt;HANDSET&gt;motol7c&lt;/HANDSET&gt;
        &lt;STATUS CELLY="20" PROVIDER="1000" TEXT="Retrieved" DESCRIPTION="" /&gt;
        &lt;TIMESTAMP&gt;2011-08-02 07:20:49-04&lt;/TIMESTAMP&gt;
    &lt;/BODY&gt;
&lt;/NOTIFICATION&gt;</pre>
