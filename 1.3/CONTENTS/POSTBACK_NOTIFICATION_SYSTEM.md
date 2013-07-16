<a href="/1.3/README.md">Back to the Table of Contents</a>
<h2>Overview: Postback Notification System</h2>
<p>The Postback system notifies remote servers about different events related to the account. For each event, a notification in XML format is inserted into a Postback queue. The  notifications in the Postback queue are processed as a batch every minute. The notifications for each account are batched together and wrapped with &lt;POSTBACK&gt; XML tag then sent in one HTTP request to the Postback URL. The Postback URL is an address on your server where you would like to receive these notifications and is defined in your API Account settings. If establishing a connection to the Postback URL takes longer than 10 seconds, the connection will time out and fail. if establishing a connection is successful, we expect the remote server to respond with a properly formed HTTP header containing 200 HTTP code. If no HTTP response is provided or the HTTP code is not 200, we consider the Postback Notification a failed request and will retry five minutes later up to five times.</p>
<h1>Postback Groups</h1>
<p>Our servers generate different Postbacks, which we divide into three groups. There are sub-groups within each Postback group. Each postback contain few unified fields:</p>
<p>NOTIFICATION id &#8211; unique ID of each notification</p>
<p>NOTIFICATION created -  timestamp when postback is generated</p>
<p>ORIGIN &#8211; identifies origin of the postback</p>
<p>CODE &#8211; identifies situation when postback is generated</p>
<p>BODY &#8211; postback body, different for each ORIGIN/CODE &#8211; this will be described for each case.</p>
<p><strong>Group #1- SMS</strong></p>
<p><strong>a) Synopsis: </strong>This Postback provides a notification when the SMS is sent out from our server. Inside the postback BODY we have following information:</p>
<p>HISTORYID &#8211; ID in our history. This postback can be matched with history report using this field.</p>
<p>TO &#8211; SMS receiver</p>
<p>TRACKINGID &#8211; ID returned via API &#8211; this postback can be matched with API response using this field.</p>
<p>TIMESTAMP &#8211; timestamp of the SMS was sent</p>
<p><strong>Postback Notification Example:</strong></p>
<p><small><code>&lt;NOTIFICATION id="521395" created="2012-06-07 04:52:07.563447-04"&gt;<br />
&lt;ORIGIN&gt;SMS_MT&lt;/ORIGIN&gt;<br />
&lt;CODE&gt;N201&lt;/CODE&gt;<br />
&lt;BODY&gt;<br />
&lt;HISTORYID&gt;455795&lt;/HISTORYID&gt;<br />
&lt;TO&gt;16501112222&lt;/TO&gt;<br />
&lt;TRACKINGID&gt;SMS_45695&lt;/TRACKINGID&gt;<br />
&lt;TIMESTAMP&gt;2012-06-07 04:52:07.374174-04&lt;/TIMESTAMP&gt;<br />
&lt;/BODY&gt;<br />
&lt;/NOTIFICATION&gt;<br />
</code></small></p>
<p><strong>b) Synopsis:</strong> This Postback provides a notification about the status of an SMS. Inside the postback BODY we have following information:</p>
<p>HISTORYID &#8211; ID in our history. This postback can be matched with history report using this field.</p>
<p>TO &#8211; SMS receiver</p>
<p>TRACKINGID &#8211; ID returned via API &#8211; this postback can be matched with API response using this field.</p>
<p>TIMESTAMP &#8211; timestamp of the SMS was sent</p>
<p>STATUS protocole/status &#8211; this is actual status of the SMS &#8211; to understand that values please reffer to API documentation APPENDIX B part iii.</p>
<p><strong>Postback Notification Example:</strong></p>
<p><code><small>&lt;NOTIFICATION id="521396" created="2012-06-07 04:55:09.985645-04"&gt;<br />
&lt;ORIGIN&gt;SMS_MT&lt;/ORIGIN&gt;<br />
&lt;CODE&gt;N202&lt;/CODE&gt;<br />
&lt;BODY&gt;<br />
&lt;HISTORYID&gt;455801&lt;/HISTORYID&gt;<br />
&lt;TO&gt;16501112222&lt;/TO&gt;<br />
&lt;TRACKINGID&gt;SMS_45697&lt;/TRACKINGID&gt;<br />
&lt;STATUS protocole="3" status="1"/&gt;<br />
&lt;TIMESTAMP&gt;2012-06-07 04:55:09.90765-04&lt;/TIMESTAMP&gt;<br />
&lt;/BODY&gt;<br />
&lt;/NOTIFICATION&gt;<br />
</small></code></p>
<p><strong>c) Synopsis: </strong>This Postback provides a notification when SMS MO is received. Inside the postback BODY we have following information:</p>
<p>FROM &#8211; SMS sender mobile number</p>
<p>TO &#8211; shortcode the SMS was sent to</p>
<p>TEXT &#8211; this is actuall text that was sent by the sender</p>
<p>RECEIVED &#8211; timestamp of the SMS received by our server</p>
<p><strong>Postback Notification Example:</strong></p>
<p><small><code>&lt;NOTIFICATION id="521495" created="2012-04-16 09:05:56.954258-04"&gt;<br />
&lt;ORIGIN&gt;SMS_MO&lt;/ORIGIN&gt;<br />
&lt;CODE&gt;N211&lt;/CODE&gt;<br />
&lt;BODY&gt;<br />
&lt;FROM&gt;16311112222&lt;/FROM&gt;<br />
&lt;TO&gt;60856&lt;/TO&gt;<br />
&lt;TEXT&gt;MYKEYCODE&lt;/TEXT&gt;<br />
&lt;RECEIVED&gt;2012-04-16 09:05:56.153785-04&lt;/RECEIVED&gt;<br />
&lt;/BODY&gt;<br />
&lt;/NOTIFICATION&gt;<br />
</code></small></p>
<p><strong>Group #2-MMS</strong></p>
<p>For MMS, we have two methods for delivering content. In addition, we send different Postbacks depending on which method is used.</p>
<p><strong>a) The Binary Method</strong></p>
<p>In binary sending, we deliver a Postback notification called &#8220;N101&#8243; immediately after we begin to process the MMS. Upon receiving Delivery Report (DLR), the system generates Postback notification &#8220;N102&#8243; with the handset name. N101 and N102 notifications are linked by both an ID in our history table (HISTORYID) and a sending que ID (TRACKINGID). Inside BODY element those postbacks contain following fields:</p>
<p>HISTORYID &#8211; ID in our history. This postback can be matched with history report using this field.</p>
<p>MMSID &#8211; ID of the MMS</p>
<p>TO &#8211; MMS receiver</p>
<p>SPID &#8211; carrier ID &#8211; please check API documentation Appendinx E</p>
<p>TRACKINGID &#8211; ID returned via API &#8211; this postback can be matched with API response using this field.</p>
<p>TIMESTAMP &#8211; timestamp of the MMS was sent (N101) or when MMS was delivered (N102)</p>
<p>HANDSET &#8211; handset profile returned inside Delivery Receipt.</p>
<p>STATUS &#8211; delivery status received in Delivery Receipt.</p>
<p><strong> N101 Example:</strong></p>
<p><small><code>&lt;NOTIFICATION id="521495" created="2012-06-07 07:27:29.954258-04"&gt;<br />
&lt;ORIGIN&gt;MMS_MT&lt;/ORIGIN&gt;<br />
&lt;CODE&gt;N101&lt;/CODE&gt;<br />
&lt;BODY&gt;<br />
&lt;HISTORYID&gt;455811&lt;/HISTORYID&gt;<br />
&lt;MMSID&gt;39597&lt;/MMSID&gt;<br />
&lt;TO&gt;16501112222&lt;/TO&gt;<br />
&lt;TRACKINGID&gt;MMS_389076&lt;/TRACKINGID&gt;<br />
&lt;SPID&gt;000157&lt;/SPID&gt;<br />
&lt;TIMESTAMP&gt;2012-06-07 07:27:29&lt;/TIMESTAMP&gt;<br />
&lt;/BODY&gt;<br />
&lt;/NOTIFICATION&gt;<br />
</code></small></p>
<p><strong>N102 Example:</strong></p>
<p><small><code>&lt;NOTIFICATION id="521495" created="2012-06-07 07:27:34.398593-04"&gt;<br />
&lt;ORIGIN&gt;MMS_MT&lt;/ORIGIN&gt;<br />
&lt;CODE&gt;N102&lt;/CODE&gt;<br />
&lt;BODY&gt;<br />
&lt;HISTORYID&gt;455811&lt;/HISTORYID&gt;<br />
&lt;MMSID&gt;39597&lt;/MMSID&gt;<br />
&lt;TO&gt;16501112222&lt;/TO&gt;<br />
&lt;TRACKINGID&gt;MMS_389076&lt;/TRACKINGID&gt;<br />
&lt;SPID&gt;000157&lt;/SPID&gt;<br />
&lt;HANDSET&gt;motol7c&lt;/HANDSET&gt;<br />
&lt;STATUS celly="20" provider="1000" text="Retrieved" description="" /&gt;<br />
&lt;TIMESTAMP&gt;2012-06-07 07:27:34-04&lt;/TIMESTAMP&gt;<br />
&lt;/BODY&gt;<br />
&lt;/NOTIFICATION&gt;<br />
</code></small></p>
<p><strong>b) The XHTML Method</strong></p>
<p>For XHTML, we send one Postback N101 notifying that we started to process the message. N102 is generated once the SMS with a link to the content is sent out. When we receive Delivery Report(DLR) for SMS, we generate Postback notification N202. N101, N102 and N202 are described above.</p>
<p><strong>PLEASE NOTE:</strong></p>
<p>Notification N101 is linked to N102 via TRACKINGID and HISTORYID</p>
<p>Notification N102 contain additional field SMSID and is linked to N202 via SMSID in N102 and TRACKINGID in N202</p>
<p><strong>N101 Example:</strong><br />
<small><code> &lt;NOTIFICATION id="521536" created="2012-06-07 07:27:34.398593-04"&gt;<br />
&lt;ORIGIN&gt;MMS_MT&lt;/ORIGIN&gt;<br />
&lt;CODE&gt;N101&lt;/CODE&gt;<br />
&lt;BODY&gt;<br />
&lt;HISTORYID&gt;455800&lt;/HISTORYID&gt;<br />
&lt;MMSID&gt;39755&lt;/MMSID&gt;<br />
&lt;TO&gt;16502424956&lt;/TO&gt;<br />
&lt;TRACKINGID&gt;MMS_389068&lt;/TRACKINGID&gt;<br />
&lt;SPID&gt;000114&lt;/SPID&gt;<br />
&lt;TIMESTAMP&gt;2012-06-07 07:27:34&lt;/TIMESTAMP&gt;<br />
&lt;/BODY&gt;<br />
&lt;/NOTIFICATION&gt;<br />
</code></small></p>
<p><strong><strong>N102 Example:</strong></strong></p>
<p><small><code>&lt;NOTIFICATION id="521537" created="2012-06-07 07:28:01.138593-04"&gt;<br />
&lt;ORIGIN&gt;MMS_MT&lt;/ORIGIN&gt;<br />
&lt;CODE&gt;N102&lt;/CODE&gt;<br />
&lt;BODY&gt;<br />
&lt;HISTORYID&gt;455800&lt;/HISTORYID&gt;<br />
&lt;MMSID&gt;39755&lt;/MMSID&gt;<br />
&lt;TO&gt;16502424956&lt;/TO&gt;<br />
&lt;TRACKINGID&gt;MMS_389068&lt;/TRACKINGID&gt;<br />
&lt;SMSID&gt;SMS_45697&lt;/SMSID&gt;<br />
&lt;STATUS celly="10" provider="1000" /&gt;<br />
&lt;TIMESTAMP&gt;2012-06-07 07:28:01.030338-04&lt;/TIMESTAMP&gt;<br />
&lt;/BODY&gt;<br />
&lt;/NOTIFICATION&gt;<br />
</code></small></p>
<p><strong><strong>N202 Example:</strong></strong></p>
<p><small><code>&lt;NOTIFICATION id="521538" created="2012-06-07 07:28:09.398593-04"&gt;<br />
&lt;ORIGIN&gt;SMS_MT&lt;/ORIGIN&gt;<br />
&lt;CODE&gt;N202&lt;/CODE&gt;<br />
&lt;BODY&gt;<br />
&lt;HISTORYID&gt;455801&lt;/HISTORYID&gt;<br />
&lt;TO&gt;16502424956&lt;/TO&gt;<br />
&lt;TRACKINGID&gt;SMS_45697&lt;/TRACKINGID&gt;<br />
&lt;STATUS protocole="3" status="1"/&gt;<br />
&lt;TIMESTAMP&gt;2012-06-07 07:28:09.90765-04&lt;/TIMESTAMP&gt;<br />
&lt;/BODY&gt;<br />
&lt;/NOTIFICATION&gt;<br />
</code></small></p>
<h5><strong>c)  Save MMS</strong></h5>
<p>When MMS is saved (using API or our MMS Composer) we generate postback notification. When saving was successful we generate N003:</p>
<p><small><code>&lt;NOTIFICATION CREATED="2011-01-01 20:09:12.975911-04"ID="325"&gt;<br />
&lt;ORIGIN&gt;MMS_MT&lt;/ORIGIN&gt;<br />
&lt;CODE&gt;N003&lt;/CODE&gt;<br />
&lt;BODY&gt;<br />
&lt;MMSID&gt;35674&lt;/MMSID&gt;<br />
&lt;/BODY&gt;<br />
&lt;/NOTIFICATION&gt;</code></small></p>
<p>If encoding of the Content failed we generate postback E002 containgin MMSID and AUDIONAME/VIDEONAME pointing ti the content that failed to encode proerly. Below is example of E002:</p>
<p><small><code>&lt;NOTIFICATION ID="325" CREATED="2011-01-01 20:09:12.975911-04"&gt;<br />
&lt;ORIGIN&gt;MMS_MT&lt;/ORIGIN&gt;<br />
&lt;CODE&gt;E002&lt;/CODE&gt;<br />
&lt;BODY&gt;<br />
&lt;MMSID&gt;35674&lt;/MMSID&gt;<br />
&lt;AUDIONAME&gt;sample.mp3&lt;/AUDIONAME&gt;<br />
&lt;/BODY&gt;<br />
&lt;/NOTIFICATION&gt;</code></small></p>
<p><strong>Group #3- Subscribe/Unsubscribe for Phone/Email</strong></p>
<p><strong>a) Synopsis:</strong> This Postback notification subscribes a phone number to a specific campaign. Inside BODY element those postbacks contain following fields:</p>
<p>MOBILE &#8211; subscriber&#8217;s mobile</p>
<p>CAMPAIGNID &#8211; ID of the campaign</p>
<p>SUBID &#8211; subscription ID</p>
<p><strong>Postback Notification Example:</strong></p>
<p><small><code>&lt;NOTIFICATION id="532168" created="2012-04-16 09:05:56.954258-04"&gt;<br />
&lt;ORIGIN&gt;SUB&lt;/ORIGIN&gt;<br />
&lt;CODE&gt;N301&lt;/CODE&gt;<br />
&lt;BODY&gt;<br />
&lt;MOBILE&gt;16501112222&lt;/MOBILE&gt;<br />
&lt;CAMPAIGNID&gt;1478&lt;/CAMPAIGNID&gt;<br />
&lt;SUBID&gt;656655&lt;/SUBID&gt;<br />
&lt;/BODY&gt;<br />
&lt;/NOTIFICATION&gt;<br />
</code></small></p>
<p><strong>b) Synopsis:</strong> This Postback notification unsubscribes a phone number from a specific campaign. Inside BODY element those postbacks contain following fields:</p>
<p>MOBILE &#8211; subscriber&#8217;s mobile</p>
<p>CAMPAIGNID &#8211; ID of the campaign</p>
<p>SUBID &#8211; subscription ID</p>
<p><strong>Postback Notification Example:</strong></p>
<p><small><code>&lt;NOTIFICATION id="532169" created="2012-04-16 09:15:56.784653-04"&gt;<br />
&lt;ORIGIN&gt;SUB&lt;/ORIGIN&gt;<br />
&lt;CODE&gt;N302&lt;/CODE&gt;<br />
&lt;BODY&gt;<br />
&lt;MOBILE&gt;16502424956&lt;/MOBILE&gt;<br />
&lt;CAMPAIGNID&gt;1478&lt;/CAMPAIGNID&gt;<br />
&lt;SUBID&gt;656655&lt;/SUBID&gt;<br />
&lt;/BODY&gt;<br />
&lt;/NOTIFICATION&gt;<br />
</code></small></p>
<p><strong>c) Synopsis:</strong> This Postback notification subscribes an email to a specific campaign. Inside BODY element those postbacks contain following fields:</p>
<p>EMAIL &#8211; subscriber&#8217;s email</p>
<p>CAMPAIGNID &#8211; ID of the campaign</p>
<p>SUBID &#8211; subscription ID</p>
<p><strong>Postback Notification Example:</strong></p>
<p><small><code>&lt;NOTIFICATION id="521354" created="2012-04-16 19:15:56.954258-04"&gt;<br />
&lt;ORIGIN&gt;EMAIL_SUB&lt;/ORIGIN&gt;<br />
&lt;CODE&gt;N303&lt;/CODE&gt;<br />
&lt;BODY&gt;<br />
&lt;EMAIL&gt;jacek@skycore.com&lt;/EMAIL&gt;<br />
&lt;CAMPAIGNID&gt;89&lt;/CAMPAIGNID&gt;<br />
&lt;SUBID&gt;12913&lt;/SUBID&gt;<br />
&lt;/BODY&gt;<br />
&lt;/NOTIFICATION&gt;<br />
</code></small></p>
<p><strong>d) Synopsis:</strong> This Postback notification unsubscribes an email from a specific campaign. Inside BODY element those postbacks contain following fields:</p>
<p>EMAIL &#8211; subscriber&#8217;s email</p>
<p>CAMPAIGNID &#8211; ID of the campaign</p>
<p>SUBID &#8211; subscription ID</p>
<p><strong>Postback Notification Example:</strong></p>
<p><small><code>&lt;NOTIFICATION id="521355" created="2012-04-16 19:15:47.598472-04"&gt;<br />
&lt;ORIGIN&gt;EMAIL_SUB&lt;/ORIGIN&gt;<br />
&lt;CODE&gt;N304&lt;/CODE&gt;<br />
&lt;BODY&gt;<br />
&lt;EMAIL&gt;jacek@skycore.com&lt;/EMAIL&gt;<br />
&lt;CAMPAIGNID&gt;89&lt;/CAMPAIGNID&gt;<br />
&lt;SUBID&gt;12913&lt;/SUBID&gt;<br />
&lt;/BODY&gt;<br />
&lt;/NOTIFICATION&gt;<br />
</code></small></p>
