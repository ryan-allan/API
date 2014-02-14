<a href="/1.3/README.md">Back to the Table of Contents</a>
<h2>Overview: Postback Notification System</h2>

<strong>What is a postback?</strong>
<ul>
<li>A postback in a notification sent via a single HTTP request in XML format to a user-specified URL containing information regarding SMS/MMS MO's (Mobile Originated), SMS/MMS MT's(Mobile Terminated), and Passes relative to the user's account.</li>
</ul>

<strong>How do postbacks work?</strong>
<ul>
<li>Each event triggers a postback and places it in a queue.</li>
<li>Postbacks in the queue are then processed and sent out every second to the user-specified URL.</li>
<li>Upon your server's reception of the Postback we expect the server to respond with a properly formatted HTTP header containing a 200 HTTP code.</li>
</ul>

<strong>Important Notes</strong>
<ul>
<li>A separate Postback URL specifically for SMS/MMS MO's(Mobile Originated) maybe be set via the API Settings tab of your account.  If it is not set, all postbacks will be sent to the Postback URL that is set.</li>
<li>If establishing a connection to the user-specified Postback URL takes longer than 10 seconds, the connection will time out and fail.  After that, we will attempt to resend the postback every 5 minutes up to a total of 5 times.</li>
<li>If the HTTP response from your server is not provided or the HTTP code is not 200, we consider the postback a failed request and we will attempt to resend the postback every 5 minutes up to a total of 5 times.</li>
</ul>

<h1>Postback Groups</h1>
<p>Our servers generate different Postbacks, which we divide into few groups. 
There are sub-groups within each Postback group. Each postback contain few unified fields:</p>
<p>ORIGIN &#8211; identifies origin of the postback</p>
<p>CODE &#8211; identifies situation when postback is generated</p>
<p><strong>Group #1- SMS</strong></p>
<p><strong>a) Synopsis: </strong>This Postback provides a notification when the SMS is sent out from our server. Postback will contain following nodes:</p>
<p>CODE, ORIGIN</p>
<p>STATUS &#8211; Indicate if the SMS was sent out successfully - allowed values are "Message Sent" or "Message Failed"</p>
<p>TO &#8211; SMS receiver</p>
<p>TRACKINGID &#8211; ID returned via API &#8211; this postback can be matched with API response using this field.</p>
<p>SPID &#8211; Carrier Identification - please reffer to APPENDIX E for more details</p>
<p>TIMESTAMP &#8211; timestamp of the SMS sending</p>
<p><strong>Postback Notification Example:</strong></p>
<p><small><code>&lt;?xml version='1.0'?&gt;<br>
&lt;POSTBACK xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" <br>
xsi:noNamespaceSchemaLocation ="http://www.skycore.com/schema/postback.xsd"&gt;<br>
&lt;ORIGIN&gt;SMS_MT&lt;/ORIGIN&gt;<br>
&lt;CODE&gt;N201&lt;/CODE&gt;<br>
&lt;STATUS&gt;Message Sent&lt;/STATUS&gt;<br>
&lt;TO&gt;16503333058&lt;/TO&gt;<br>
&lt;TRACKINGID&gt;U01TXzgwNjc4&lt;/TRACKINGID&gt;<br>
&lt;SPID&gt;0001470&lt;/SPID&gt;<br>
&lt;TIMESTAMP&gt;2013-11-05T05:41:08-05:00&lt;/TIMESTAMP&gt;<br>
&lt;/POSTBACK&gt;<br>
</code></small></p>
<p><strong>b) Synopsis:</strong> This Postback provides a notification about the status of an SMS. Postback will contain following nodes:</p>
<p>CODE, ORIGIN</p>
<p>STATUS &#8211; Indicate if the SMS was sent out successfully - allowed values are "Message Sent/Delivered" or "Message Sent/Failed"</p>
<p>TO &#8211; SMS receiver</p>
<p>TRACKINGID &#8211; ID returned via API &#8211; this postback can be matched with API response using this field.</p>
<p>SPID &#8211; Carrier Identification - please reffer to APPENDIX E for more details</p>
<p>TIMESTAMP &#8211; timestamp of the SMS Delivery Receipt</p>
<p>AGGREGATOR &#8211; SMS aggregator ID</p>
<p><strong>Postback Notification Example:</strong></p>
<p><code><small>&lt;?xml version='1.0'?&gt;<br>
&lt;POSTBACK xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" <br>
xsi:noNamespaceSchemaLocation ="http://www.skycore.com/schema/postback.xsd"&gt;<br>
&lt;ORIGIN&gt;SMS_MT&lt;/ORIGIN&gt;<br>
&lt;CODE&gt;N202&lt;/CODE&gt;<br>
&lt;STATUS&gt;Message Sent/Delivered&lt;/STATUS&gt;<br>
&lt;TO&gt;16503333058&lt;/TO&gt;<br>
&lt;TRACKINGID&gt;U01TXzgwNjc4&lt;/TRACKINGID&gt;<br>
&lt;SPID&gt;0001470&lt;/SPID&gt;<br>
&lt;TIMESTAMP&gt;2013-11-05T05:41:15-05:00&lt;/TIMESTAMP&gt;<br>
&lt;AGGREGATORID&gt;11529-64807-97508-73852-97658&lt;/AGGREGATORID&gt;
&lt;/POSTBACK&gt;<br>
</small></code></p>
<p><strong>c) Synopsis: </strong>This Postback provides a notification when SMS MO is received. Postback will contain following nodes:</p>
<p>CODE, ORIGIN</p>
<p>FROM &#8211; SMS sender mobile number</p>
<p>TO &#8211; shortcode the SMS was sent to</p>
<p>TEXT &#8211; this is actuall text that was sent by the sender</p>
<p>RECEIVED &#8211; timestamp of the SMS received by our server</p>
<p><strong>Postback Notification Example:</strong></p>
<p><small><code>&lt;?xml version='1.0'?&gt;<br>
&lt;POSTBACK xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" <br>
xsi:noNamespaceSchemaLocation ="http://www.skycore.com/schema/postback.xsd"&gt;<br>
&lt;ORIGIN&gt;SMS_MO&lt;/ORIGIN&gt;<br />
&lt;CODE&gt;N211&lt;/CODE&gt;<br />
&lt;FROM&gt;16311112222&lt;/FROM&gt;<br />
&lt;TO&gt;60856&lt;/TO&gt;<br />
&lt;TEXT&gt;MYKEYCODE&lt;/TEXT&gt;<br />
&lt;RECEIVED&gt;2012-04-16T09:05:56-04:00&lt;/RECEIVED&gt;<br />
&lt;/POSTBACK&gt;<br />
</code></small></p>



<p><strong>Group #2-MMS</strong></p>
<p>For MMS, we have two methods for delivering content binary and xHTML. We send different Postbacks depending on which method is used.</p>
<p><strong>a) The Binary Method</strong></p>
<p>In binary sending, we deliver a Postback notification called &#8220;N101&#8243; immediately after we begin to process the MMS. Upon receiving Delivery Report (DLR), the system generates Postback notification &#8220;N102&#8243; with the handset name. 
N101 and N102 notifications are linked by TRACKINGID. Postback contain following nodes:</p>
<p>CODE, ORIGIN</p>
<p>SENTAS &#8211; this node indicate if MMS was delivered as MMS (binary delivery) or SMS (xHTML). For binary delivery it will always be MMS</p>
<p>MMSID &#8211; ID of the MMS</p>
<p>TO &#8211; MMS receiver</p>
<p>SPID &#8211; carrier ID &#8211; please check API documentation Appendinx E</p>
<p>TRACKINGID &#8211; ID returned via API &#8211; this postback can be matched with API response using this field.</p>
<p>TIMESTAMP &#8211; timestamp of the MMS was sent (N101) or when MMS was delivered (N102)</p>
<p>HANDSET &#8211; handset profile returned inside Delivery Receipt. This is present only in N102 notification</p>
<p>STATUS &#8211; For N101 notification status can be "Message Sent". For N102 notification status can be "Message Sent/Delivered", "Message Sent/Expired" or "Message Sent/Rejected"</p>
<p>STATUSDETAILS &#8211; For N101 notification when status is "Message Failed" postback will contain this node with error details.
<p>AGGREGATORID &#8211; Only in N102 notification, contain Aggregator ID of the sending. 
<p><strong> N101 Example:</strong></p>
<p><small><code>&lt;?xml version='1.0'?&gt;<br>
&lt;POSTBACK xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" <br>
xsi:noNamespaceSchemaLocation ="http://www.skycore.com/schema/postback.xsd"&gt;<br>
&lt;ORIGIN&gt;MMS_MT&lt;/ORIGIN&gt;<br />
&lt;CODE&gt;N101&lt;/CODE&gt;<br />
&lt;SENTAS&gt;MMS&lt;/SENTAS&gt;<br />
&lt;STATUS&gt;Message Sent&lt;/STATUS&gt;<br />
&lt;MMSID&gt;39597&lt;/MMSID&gt;<br />
&lt;TO&gt;16501112222&lt;/TO&gt;<br />
&lt;TRACKINGID&gt;TU1TXzU5Nzg3OQ==&lt;/TRACKINGID&gt;<br />
&lt;SPID&gt;0001570&lt;/SPID&gt;<br />
&lt;TIMESTAMP&gt;2012-06-07T07:27:29-05:00&lt;/TIMESTAMP&gt;<br />
&lt;/POSTBACK&gt;<br />
</code></small></p>
<p><strong>N102 Example:</strong></p>
<p><small><code>&lt;?xml version='1.0'?&gt;<br>
&lt;POSTBACK xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" <br>
xsi:noNamespaceSchemaLocation ="http://www.skycore.com/schema/postback.xsd"&gt;<br>
&lt;ORIGIN&gt;MMS_MT&lt;/ORIGIN&gt;<br />
&lt;CODE&gt;N102&lt;/CODE&gt;<br />
&lt;SENTAS&gt;MMS&lt;/SENTAS&gt;<br />
&lt;STATUS&gt;Message Sent/Delivered&lt;/STATUS&gt;<br />
&lt;MMSID&gt;39597&lt;/MMSID&gt;<br />
&lt;TO&gt;16501112222&lt;/TO&gt;<br />
&lt;TRACKINGID&gt;TU1TXzU5Nzg3OQ==&lt;/TRACKINGID&gt;<br />
&lt;SPID&gt;0001570&lt;/SPID&gt;<br />
&lt;TIMESTAMP&gt;2012-06-07T07:27:34-05:00&lt;/TIMESTAMP&gt;<br />
&lt;HANDSET&gt;motol7c&lt;/HANDSET&gt;<br />
&lt;AGGREGATORID&gt;11529-64807-97508-73852-97658&lt;/AGGREGATORID&gt;<br />
&lt;/POSTBACK&gt;<br />
</code></small></p>

<p><strong>b) The XHTML Method</strong></p>
<p>In this method we deliver MMS as SMS link to the content, we send one Postback N101 notifying that we started to process the message. 
When we receive Delivery Report(DLR) for SMS, we generate Postback notification N202. Postbacks will contain following nodes:</p>
<p>CODE, ORIGIN</p>
<p>SENTAS &#8211; this node indicate if MMS was delivered as MMS (binary delivery) or SMS (xHTML). For xHTML delivery it will always be SMS</p>
<p>MMSID &#8211; ID of the MMS</p>
<p>TO &#8211; MMS receiver</p>
<p>SPID &#8211; carrier ID &#8211; please check API documentation Appendinx E</p>
<p>TRACKINGID &#8211; ID returned via API &#8211; this postback can be matched with API response using this field.</p>
<p>TIMESTAMP &#8211; timestamp of the MMS was sent (N101) or when SMS was delivered (N202)</p>
<p>STATUS &#8211; For N101 notification status can be "Message Sent". For N202 notification status can be "Message Sent/Delivered" or "Message Sent/Failed"</p>
<p>AGGREGATORID &#8211; Only in N202 notification, contain Aggregator ID of the sending. 

<p><strong>N101 Example:</strong><br />
<small><code>&lt;?xml version='1.0'?&gt;<br>
&lt;POSTBACK xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" <br>
xsi:noNamespaceSchemaLocation ="http://www.skycore.com/schema/postback.xsd"&gt;<br>
&lt;ORIGIN&gt;MMS_MT&lt;/ORIGIN&gt;<br />
&lt;CODE&gt;N101&lt;/CODE&gt;<br />
&lt;SENTAS&gt;SMS&lt;/SENTAS&gt;<br />
&lt;STATUS&gt;Message Sent&lt;/STATUS&gt;<br />
&lt;MMSID&gt;39755&lt;/MMSID&gt;<br />
&lt;TO&gt;16502424956&lt;/TO&gt;<br />
&lt;TRACKINGID&gt;TU1TXzU5Nzg3Nw==&lt;/TRACKINGID&gt;<br />
&lt;SPID&gt;0001140&lt;/SPID&gt;<br />
&lt;TIMESTAMP&gt;2012-06-07T07:27:34-05:00&lt;/TIMESTAMP&gt;<br />
&lt;/POSTBACK&gt;<br />
</code></small></p>
<p><strong><strong>N202 Example:</strong></strong></p>
<p><small><code>&lt;?xml version='1.0'?&gt;<br>
&lt;POSTBACK xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" <br>
xsi:noNamespaceSchemaLocation ="http://www.skycore.com/schema/postback.xsd"&gt;<br>
&lt;ORIGIN&gt;MMS_MT&lt;/ORIGIN&gt;<br />
&lt;CODE&gt;N202&lt;/CODE&gt;<br />
&lt;SENTAS&gt;SMS&lt;/SENTAS&gt;<br />
&lt;STATUS&gt;Message Sent/Delivered&lt;/STATUS&gt;<br />
&lt;TO&gt;16502424956&lt;/TO&gt;<br />
&lt;TRACKINGID&gt;TU1TXzU5Nzg3Nw==&lt;/TRACKINGID&gt;<br />
&lt;SPID&gt;0001140&lt;/SPID&gt;<br />
&lt;TIMESTAMP&gt;2012-06-07T07:28:09-05:00&lt;/TIMESTAMP&gt;<br />
&lt;AGGREGATORID&gt;11529-64807-97508-73852-97658&lt;/AGGREGATORID&gt;<br />
&lt;/POSTBACK&gt;<br />
</code></small></p>

<p><strong>c) Binary MMS degraded to xHTML and delivered as SMS link.</strong></p>
<p>In some rare cases we degrade the binary MMS and deliver it as SMS link, it may be due to MMS being too big to deliver as binary.
We send one Postback N101 notifying that we started to process the message - in this case the postback will contain additional STATUSDETAILS node describing why it is being delivered as xHTML (This is the only difference VS xHTML delivery). 
When we receive Delivery Report(DLR) for SMS, we generate Postback notification N202. Postbacks will contain following nodes:</p>
<p>CODE, ORIGIN</p>
<p>SENTAS &#8211; this node indicate if MMS was delivered as MMS (binary delivery) or SMS (xHTML). For xHTML delivery it will always be SMS</p>
<p>MMSID &#8211; ID of the MMS</p>
<p>TO &#8211; MMS receiver</p>
<p>SPID &#8211; carrier ID &#8211; please check API documentation Appendinx E</p>
<p>TRACKINGID &#8211; ID returned via API &#8211; this postback can be matched with API response using this field.</p>
<p>TIMESTAMP &#8211; timestamp of the MMS was sent (N101) or when SMS was delivered (N202)</p>
<p>STATUS &#8211; For N101 notification status can be "Message Sent". For N202 notification status can be "Message Sent/Delivered" or "Message Sent/Failed"</p>
<p>STATUSDETAILS &#8211; For N101 notification this node will contain details why the MMS is being delivered as xHTML.</p>
<p>AGGREGATORID &#8211; Only in N202 notification, contain Aggregator ID of the sending. </p>

<p><strong>N101 Example:</strong><br />
<small><code>&lt;?xml version='1.0'?&gt;<br>
&lt;POSTBACK xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" <br>
xsi:noNamespaceSchemaLocation ="http://www.skycore.com/schema/postback.xsd"&gt;<br>
&lt;ORIGIN&gt;MMS_MT&lt;/ORIGIN&gt;<br />
&lt;CODE&gt;N101&lt;/CODE&gt;<br />
&lt;SENTAS&gt;SMS&lt;/SENTAS&gt;<br />
&lt;STATUS&gt;Message Sent&lt;/STATUS&gt;<br />
&lt;MMSID&gt;39755&lt;/MMSID&gt;<br />
&lt;TO&gt;16502424956&lt;/TO&gt;<br />
&lt;TRACKINGID&gt;TU1TXzU5Nzg3Nw==&lt;/TRACKINGID&gt;<br />
&lt;SPID&gt;0001140&lt;/SPID&gt;<br />
&lt;TIMESTAMP&gt;2012-06-07T07:27:34-05:00&lt;/TIMESTAMP&gt;<br />
&lt;STATUSDETAILS&gt;Handset setting: mms with pass via xhtml;&lt;/STATUSDETAILS&gt;<br />
&lt;/POSTBACK&gt;<br />
</code></small></p>
<p><strong><strong>N202 Example:</strong></strong></p>
<p><small><code>&lt;?xml version='1.0'?&gt;<br>
&lt;POSTBACK xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" <br>
xsi:noNamespaceSchemaLocation ="http://www.skycore.com/schema/postback.xsd"&gt;<br>
&lt;ORIGIN&gt;MMS_MT&lt;/ORIGIN&gt;<br />
&lt;CODE&gt;N202&lt;/CODE&gt;<br />
&lt;SENTAS&gt;SMS&lt;/SENTAS&gt;<br />
&lt;STATUS&gt;Message Sent/Delivered&lt;/STATUS&gt;<br />
&lt;TO&gt;16502424956&lt;/TO&gt;<br />
&lt;TRACKINGID&gt;TU1TXzU5Nzg3Nw==&lt;/TRACKINGID&gt;<br />
&lt;SPID&gt;0001140&lt;/SPID&gt;<br />
&lt;TIMESTAMP&gt;2012-06-07T07:28:09-05:00&lt;/TIMESTAMP&gt;<br />
&lt;AGGREGATORID&gt;11529-64807-97508-73852-97658&lt;/AGGREGATORID&gt;<br />
&lt;/POSTBACK&gt;<br />
</code></small></p>

<p><strong>d)MMS sending Fails</strong></p>
<p>Sometimes system is unable to send MMS out. In this situations we send postback E101. Postback will contain following nodes:</p>
<p>CODE, ORIGIN</p>
<p>MMSID &#8211; ID of the MMS</p>
<p>TO &#8211; MMS receiver</p>
<p>SPID &#8211; carrier ID &#8211; please check API documentation Appendinx E</p>
<p>TRACKINGID &#8211; ID returned via API &#8211; this postback can be matched with API response using this field.</p>
<p>TIMESTAMP &#8211; timestamp of the MMS was sent (N101) or when MMS was delivered (N102)</p>
<p>STATUS &#8211; For E101 notification status can be "Message Failed".</p>
<p>STATUSDETAILS &#8211; For E101 notification when status is "Message Failed" postback will contain this node with error details.

<p><strong>E101 Example:</strong><br />
<small><code>&lt;?xml version='1.0'?&gt;<br>
&lt;POSTBACK xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" <br>
xsi:noNamespaceSchemaLocation ="http://www.skycore.com/schema/postback.xsd"&gt;<br>
&lt;ORIGIN&gt;MMS_MT&lt;/ORIGIN&gt;<br />
&lt;CODE&gt;E101&lt;/CODE&gt;<br />
&lt;STATUS&gt;Message Failed&lt;/STATUS&gt;<br />
&lt;MMSID&gt;39755&lt;/MMSID&gt;<br />
&lt;TO&gt;16502424956&lt;/TO&gt;<br />
&lt;TRACKINGID&gt;TU1TXzU5Nzg3Nw==&lt;/TRACKINGID&gt;<br />
&lt;SPID&gt;0001140&lt;/SPID&gt;<br />
&lt;STATUSDETAILS&gt;Error fetching object(Database Error: Could not find number/email imported in database)&lt;STATUSDETAILS&gt;<br />
&lt;/POSTBACK&gt;<br />
</code></small></p>

<h5><strong>e)  Save MMS</strong></h5>
<p>When MMS is saved (using API or our MMS Composer) we generate postback notification. When saving was successful we generate N003:</p>
<p><small><code>&lt;?xml version='1.0'?&gt;<br>
&lt;POSTBACK&gt;<br>
&lt;ORIGIN&gt;MMS_MT&lt;/ORIGIN&gt;<br />
&lt;CODE&gt;N003&lt;/CODE&gt;<br />
&lt;MMSID&gt;35674&lt;/MMSID&gt;<br />
&lt;/POSTBACK&gt;</code></small></p>
<p>If encoding of the Content failed we generate postback E002 containgin MMSID and AUDIONAME/VIDEONAME pointing ti the content that failed to encode proerly. Below is example of E002:</p>
<p><small><code>&lt;?xml version='1.0'?&gt;<br>
&lt;POSTBACK&gt;<br>
&lt;ORIGIN&gt;MMS_MT&lt;/ORIGIN&gt;<br />
&lt;CODE&gt;E002&lt;/CODE&gt;<br />
&lt;MMSID&gt;35674&lt;/MMSID&gt;<br />
&lt;AUDIONAME&gt;sample.mp3&lt;/AUDIONAME&gt;<br />
&lt;/POSTBACK&gt;</code></small></p>



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
