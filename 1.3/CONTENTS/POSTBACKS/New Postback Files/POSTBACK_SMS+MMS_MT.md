<h2>SMS/MMS MT Postbacks</h2>
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
