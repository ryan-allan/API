<a href="/1.3/README.md">Back to the Table of Contents</a>&nbsp;&nbsp;|&nbsp;&nbsp;<a href="API_METHODS.md">Back to API Methods</a>
<h2>sendMMSBarcode</h2>
<p><strong>Synopsis:</strong><br />
This API sends stored MMS containing a barcode image template from a specified account using a MMSID to a one number. The barcodeID along with the phone number is added to Database. The BarcodeID is encoded into a barcode image which is inserted into the MMS and is delivered to the number.
<br>
NOTE: BarcodeID passed in API call will always be used even for Databases with 'Always generate new IDs' switch set to 'Yes'</p>
<div><strong>Request:</strong></div>
<pre>&lt;REQUEST&gt;
  &lt;ACTION&gt;sendMMSBarcode&lt;/ACTION&gt;
	&lt;API_KEY&gt;API KEY&lt;/API_KEY&gt;
	&lt;MMSID&gt;MMSID&lt;/MMSID&gt;
	&lt;TO&gt;Number&lt;/TO&gt;
        &lt;FROM&gt;Shortcode&lt;/FROM&gt;
        &lt;BARCODEID&gt;BarcodeID&lt;/BARCODEID&gt;
        &lt;CAMPAIGNREF&gt;CampaignID&lt;/CAMPAIGNREF&gt;
&lt;/REQUEST&gt;</pre>
<div><strong>Request Parameters:</strong></div>
<pre><strong>Mandatory:</strong> Action, API_KEY, MMSID, To, BarcodeID, From
<strong>Optional: </strong>CampaignRef</pre>
<strong>Response Parameters:</strong><br />
MMSID, Status, To, TrackingID, Errorcode, Errorinfo
<strong>Related Errorcodes: </strong><br />
E110, E111, E241, E620, E621, E623, E626, E628, E629, E630, E631, E632, E633, E713, E714, E715
  
<div><strong>Request Examples</strong></div>
XML:
<pre>&lt;REQUEST&gt;
	&lt;ACTION&gt; sendMMSBarcode &lt;/ACTION&gt;
	&lt;API_KEY&gt;qTFkykO9JTfahCOqJ0V2Wf5Cg1t8iWlZ&lt;/API_KEY&gt;
	&lt;TO&gt;16501234123&lt;/TO&gt;
        &lt;FROM&gt;60856&lt;/FROM&gt;
        &lt;BARCODEID&gt;Ticket_12345&lt;/BARCODEID&gt;
        &lt;CAMPAIGNREF&gt;12333&lt;/CAMPAIGNREF&gt;
	&lt;MMSID&gt;35674&lt;/MMSID&gt;
&lt;/REQUEST&gt;</pre>
GET:
<pre>https://secure.skycore.com/API/wxml/1.3/index.php?action=sendmmsbarcode&api_key=qTFkykO9JTfahCOqJ0V2Wf5Cg1t8iWlZ
&to=16501234123&from=60856&barcodeid=Ticket_12345&campaignref=12333&mmsid=35674</pre>
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
