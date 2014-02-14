<a href="/1.3/README.md">Back to the Table of Contents</a>
<h2>SMS/MMS MT Postbacks</h2>
<div id="page-content"><strong>Brief Overview:</strong>
This document will provide a technical description of the MMS/SMS MO POSTBACK API. In brief, this API allows those with an SMS/MMS MO-enabled shortcode to forward received messages (MMS/SMS MO) to your server.

<strong>SMS/MMS MO Specific URL:</strong>
A separate Postback URL specifically for SMS/MMS MO's(Mobile Originated) maybe be set via the API Settings tab of your account.  If it is not set, all postbacks will be sent to the Postback URL that is set.

<strong>SMS MO General Information:</strong>
To receive SMS MO postback notification you need to have that option enabled in your account. Once the SMS MO 
postback is enabled you will start receiving HTTP Posts on URL of your choice for each SMS MO received related to 
your account.

<strong>MMS MO General Information</strong>
To receive MMS MO postback notification you need to have that option enabled in your account and you need to 
configure it within the particular MMS MO campaign.  Once the MMS MO postback is enabled you will start receiving 
HTTP Posts on URL of your choice for each MMS MO received on the MMS MO Keyword. If you have (optionally) enabled 
the MMS MO moderation panel then the postback notifictions will only be sent upon manual approval by the moderator.
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
