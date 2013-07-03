<a href="/TABLE%20OF%20CONTENTS.md">BACK TO TABLE OF CONTENTS</a>
<BR>
<a href="/API%20FUNCTIONS.md">BACK TO API FUNCTIONS</a>
<BR>
<BR>


<h1>sendSavedMMS()</h1>
<BR>

<p><strong>Synopsis:</strong><br />
This API sends stored content from a specified account using a MMSID to a one or a list of mobile numbers. Recipient 
addresses are specified by a comma delimited list of valid mobile numbers. List up to 100 numbers is supported. FROM 
must be one of shortcodes allowed for your account. In case there are numbers from different countries than FROM 
shortcode is assigned to &#8211; default shortcode for those countries will be used.</p>
<p><strong>Content Transcoding:</strong><br />
Every binary MMS we deliver can be transcoded for the destination handset and every web page we deliver is transcoded 
for the browsing handset. To transcode a binary MMS we must know what type of handset the user has. We are able to 
obtain this handset type information from delivery receipts and store the record in a handset cache for later use. 
We have a database of attributes which we manually match to every new handset in the cache so we can adapt the content 
during MMS delivery.</p>
<p>A Device Discovery Message (DDM) is a short textual MMS message that is sent to the number to discover what handset 
the end user is using. We store this handset information in our system and reuse it, so a DDM is sent only to new 
numbers. If the DDM settings are not included within your API call and the number is not in the handset cache we will 
deliver the MMS with generic settings. If the handset is in the handset cache the DDM will not be sent and the MMS 
message will be transcoded and delivered immediately.</p>
<p>Our API allows you to customize DDM by setting 3 parameters:<br />
DDMTITLE &#8211; this is the DDM title<br />
DDMTEXT &#8211; this is the DDM body<br />
DDMTIMEOUT &#8211; when we send DDM we wait for the Delivery Report which contain the handset profile. In some cases we 
don&#8217;t receive it or it takes very long (handset turned off or out of range). This variable tells the system how 
long should it wait for DDM Delivery Report before sending actual content using Default parameters. Default value of 
this parameter is 5 minutes.</p>
<div><strong>Request:</strong></div>
<pre>&lt;REQUEST&gt;
  &lt;ACTION&gt;sendSavedMMS&lt;/ACTION&gt;
	&lt;API_KEY&gt;API KEY&lt;/API_KEY&gt;
	&lt;MMSID&gt;MMSID&lt;/MMSID&gt;
	&lt;TO&gt;Number&lt;/TO&gt;
	&lt;FROM&gt;Shortcode&lt;/FROM&gt;
	&lt;CAMPAIGNREF&gt;CampaignID&lt;/CAMPAIGNREF&gt;
        &lt;DDMTITLE&gt;DDM Title&lt;/DDMTITLE&gt;
        &lt;DDMTEXT&gt;DDM Body&lt;/DDMTEXT&gt;
        &lt;DDMTIMEOUT&gt;DDM Timeout in minutes&lt;/DDMTIMEOUT&gt;
&lt;/REQUEST&gt;</pre>
<div><strong>Request Parameters:</strong></div>
<pre><strong>Mandatory:</strong> Action, API_KEY, MMSID, To, From
<strong>Optional: </strong>CampaignRef</pre>

<strong>Response Parameters:</strong><br />

	MMSID, Status, To, TrackingID, Errorcode, Errorinfo
	
<strong>Related Errorcodes: </strong><br />

	E110, E111, E241, E620, E621, E623, E626, E628, E629, E713, E714, E715
	
<div><strong>Request Example:</strong></div>
<pre>&lt;REQUEST&gt;
	&lt;ACTION&gt; sendSavedMMS &lt;/ACTION&gt;
	&lt;API_KEY&gt;qTFkykO9JTfahCOqJ0V2Wf5Cg1t8iWlZ&lt;/API_KEY&gt;
	&lt;TO&gt;16501234123,16501234124&lt;/TO&gt;
	&lt;FROM&gt;60856&lt;/FROM&gt;
	&lt;CAMPAIGNREF&gt;12333&lt;/CAMPAIGNREF&gt;
	&lt;MMSID&gt;35674&lt;/MMSID&gt;
        &lt;DDMTITLE&gt;We are detecting your handset&lt;/DDMTITLE&gt;
        &lt;DDMTEXT&gt;This message is free of charge and will allow us to deliver your content nice and smooth&lt;/DDMTEXT&gt;
        &lt;DDMTIMEOUT&gt;10&lt;/DDMTIMEOUT&gt;
&lt;/REQUEST&gt;</pre>
<div><strong>Response Example: Success</strong></div>
<pre>&lt;RESPONSE&gt;
    &lt;STATUS&gt;Success&lt;/STATUS&gt;
    &lt;MMSID&gt;35674&lt;/MMSID&gt;
    &lt;SENDING&gt;
        &lt;TRACKINGID&gt;MMS_12346&lt;/TRACKINGID&gt;
        &lt;TO&gt;16501234123&lt;/TO&gt;
    &lt;/SENDING&gt;
    &lt;SENDING&gt;
        &lt;ERRORCODE&gt;E715&lt;/ERRORCODE&gt;
        &lt;TO&gt;16501234124&lt;/TO&gt;
        &lt;ERRORINFO&gt;Number is not subscribed in this campaign&lt;/ERRORINFO&gt;
    &lt;/SENDING&gt;
&lt;/RESPONSE&gt;</pre>
<div><strong>Response Example: Failure</strong></div>
<pre>&lt;RESPONSE&gt;
	 &lt;STATUS&gt;Failure&lt;/STATUS&gt;
	 &lt;ERRORCODE&gt;E713&lt;/ERRORCODE&gt;
	 &lt;TO&gt;16501234123,16501234124&lt;/TO&gt;
	 &lt;ERRORINFO&gt;There is billing problem on your account&lt;/ERRORINFO&gt;
&lt;/RESPONSE&gt;</pre>
<div><strong>Postback Notifications For SendSavedMMS</strong></div>
<p>When the MMS delivery is processed successfully the system will generate a Postback notification.</p>
<pre>&lt;NOTIFICATION   ID="325" CREATED="2011-08-02 07:20:45.870623-04"&gt;
	&lt;ORIGIN&gt;MMS_MT&lt;/ORIGIN&gt;
	&lt;CODE&gt;N101&lt;/CODE&gt;
	&lt;BODY&gt;
        &lt;HISTORYID&gt;249687&lt;/HISTORYID&gt;
        &lt;MMSID&gt;35674&lt;/MMSID&gt;
        &lt;TO&gt;16501234123&lt;/TO&gt;
        &lt;TRACKINGID&gt;MMS_12346&lt;/TRACKINGID&gt;
        &lt;SPID&gt;000189&lt;/SPID&gt;
        &lt;TIMESTAMP&gt;2011-08-02 07:20:44-04&lt;/TIMESTAMP&gt;
	&lt;/BODY&gt;
&lt;/NOTIFICATION&gt;</pre>
<p>When an MMS delivery report is received the system will generate a Postback notification. Not all carriers provide 
MMS delivery receipts.</p>
<p>&lt;NOTIFICATION ID=&#8221;326&#8243; CREATED=&#8221;2011-08-02 07:20:52.332193-04&#8243;&gt; &lt;ORIGIN&gt;
MMS_MT&lt;/ORIGIN&gt; &lt;CODE&gt;N102&lt;/CODE&gt; &lt;BODY&gt; &lt;HISTORYID&gt;249687&lt;/HISTORYID&gt; &lt;MMSID&gt;
35674&lt;/MMSID&gt; &lt;TO&gt;16501234123&lt;/TO&gt; &lt;TRACKINGID&gt;MMS_12346&lt;/TRACKINGID&gt; &lt;SPID&gt;000189
&lt;/SPID&gt; &lt;HANDSET&gt;motol7c&lt;/HANDSET&gt; &lt;STATUS CELLY=&#8221;20&#8243; PROVIDER=&#8221;1000&#8243; 
TEXT=&#8221;Retrieved&#8221; DESCRIPTION=&#8221;" /&gt; &lt;TIMESTAMP&gt;2011-08-02 07:20:49-04&lt;/TIMESTAMP&gt; &lt;
/BODY&gt; &lt;
/NOTIFICATION&gt;</p>
<div><strong><a id="sendmmsbarcode"></a>sendMMSBarcode()</strong></div>
<p><strong>Synopsis:</strong><br />
This API sends stored content containing a barcode from a specified account using a MMSID to a one number. The barcodeid
along with the number is added to database and then MMS is delivered with barcode containing passed barcodeid.</p>
<div><strong>Request:</strong></div>
<pre>&lt;REQUEST&gt;
	&lt;ACTION&gt;sendMMSBarcode&lt;/ACTION&gt;
	&lt;API_KEY&gt;API KEY&lt;/API_KEY&gt;
	&lt;MMSID&gt;MMSID&lt;/MMSID&gt;
	&lt;TO&gt;Number&lt;/TO&gt;
        &lt;FROM&gt;Shortcode&lt;/FROM&gt;
        &lt;DATABASEID&gt;DatabaseID&lt;/DATABASEID&gt;
        &lt;BARCODEID&gt;BarcodeID&lt;/BARCODEID&gt;
        &lt;CAMPAIGNREF&gt;CampaignID&lt;/CAMPAIGNREF&gt;
&lt;/REQUEST&gt;</pre>
<div><strong>Request Parameters:</strong></div>
<pre><strong>Mandatory:</strong> Action, API_KEY, MMSID, To, DatabaseID, BarcodeID, From
<strong>Optional: </strong>CampaignRef</pre>
<p><strong>Response Parameters:</strong><br />
MMSID, Status, To, TrackingID, Errorcode, Errorinfo</p>
<p><strong>Related Errorcodes: </strong><br />
E110, E111, E241, E620, E621, E623, E626, E628, E629, E630, E631, E632, E713, E714, E715</p>
<div><strong>Request Example:</strong></div>
<pre>&lt;REQUEST&gt;
	&lt;ACTION&gt; sendMMSBarcode &lt;/ACTION&gt;
	&lt;API_KEY&gt;qTFkykO9JTfahCOqJ0V2Wf5Cg1t8iWlZ&lt;/API_KEY&gt;
	&lt;TO&gt;16501234123&lt;/TO&gt;
        &lt;FROM&gt;60856&lt;/FROM&gt;
        &lt;DATABASEID&gt;17856&lt;/DATABASEID&gt;
        &lt;BARCODEID&gt;Ticket_12345&lt;/BARCODEID&gt;
        &lt;CAMPAIGNREF&gt;12333&lt;/CAMPAIGNREF&gt;
	&lt;MMSID&gt;35674&lt;/MMSID&gt;
&lt;/REQUEST&gt;</pre>
<div><strong>Response Example: Success</strong></div>
<pre>&lt;RESPONSE&gt;
    &lt;STATUS&gt;Success&lt;/STATUS&gt;
    &lt;MMSID&gt;35674&lt;/MMSID&gt;
    &lt;TRACKINGID&gt;MMS_12346&lt;/TRACKINGID&gt;
    &lt;TO&gt;16501234123&lt;/TO&gt;
&lt;/RESPONSE&gt;</pre>
<div><strong>Response Example: Failure</strong></div>
<pre>&lt;RESPONSE&gt;
    &lt;STATUS&gt;Failure&lt;/STATUS&gt;
    &lt;ERRORCODE&gt;E713&lt;/ERRORCODE&gt;
    &lt;TO&gt;16501234123&lt;/TO&gt;
    &lt;ERRORINFO&gt;There is billing problem on your account&lt;/ERRORINFO&gt;
&lt;/RESPONSE&gt;</pre>
<div><strong>Postback Notifications for this action are the same as for SendSavedMMS</strong></div>
<div></div>
<div><strong><a id="sendsavedcontentcampaign"></a>sendSavedMMSCampaign()</strong></div>
<p><strong>Synopsis:</strong><br />
This API sends stored content from a specified account using a MMSID to a list of mobile numbers that are subscribed to 
a campaign. Recipient addresses are not specified, only the CampaignID is specified. Content will be sent from campaign
default shortcode.</p>
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
<p><strong>Response Parameters:</strong><br />
MMSID, Status, To, ScheduledID, Errorcode, Errorinfo</p>
<p><strong>Related Errorcodes: </strong><br />
E241, E620, E624, E626, E629, E714</p>
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
<p>When an MMS delivery report is received the system will generate a Postback notification. Not all carriers provide 
MMS delivery receipts.</p>
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
