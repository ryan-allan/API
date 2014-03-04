<a name="DocTop"><a href="/1.3/README.md">Back to the Table of Contents</a>&nbsp;&nbsp;|&nbsp;&nbsp;<a href="/1.3/CONTENTS/POSTBACKS/POSTBACK_SYSTEM_OVERVIEW.md">Postback System Overview</a>
<h2>SMS/MMS MT Postbacks</h2>
<div id="page-content"><strong>Brief Overview:</strong>
This document will provide a technical description of the MMS/SMS MT postback API.  Briefly, this API allows those with SMS/MMS MT postbacks enabled to generate and forward SMS/MMS MT postbacks to their server.  For MMS, we have two methods for delivering content; Binary and xHTML. We send different postbacks depending on which method is used.

<strong>Current list of the SMS/MMS MT Postback Types</strong>
 
[SMS MT Sent](#Sent)                            
[SMS MT Status](#Status)                        
[MMS MT (Binary)](#Binary)                       
[MMS MT (xHTML)](#xHTML)                        
[MMS MT (Binary degrade to xHTML and sent as SMS link)](#Degrade)  
[MMS MT (Sending Failure)](#SendFail)      
[MMS MT (Save MMS)](#SaveMMS) <BR />
[MMS MT (Save MMS Content Failure)](#ContentFail)

<h3>MT Postback Definitions</h3>

<a name="Sent"><strong>SMS MT Sent</strong>
<p><strong>Synopsis:</strong>This postback provides a notification when the SMS is sent out from our server.</p>
<strong><p>This postback will contain the following nodes:</p></strong>
CODE, ORIGIN<BR/>
STATUS &#8211; Indicate if the SMS was sent out successfully - allowed values are "Message Sent" or "Message Failed"<BR/>
TO &#8211; SMS receiver<BR/>
TRACKINGID &#8211; ID returned via API &#8211; this postback can be matched with API response using this field<BR/>
SPID &#8211; Carrier Identification - please reffer to <a href="/1.3/CONTENTS/APPENDIX/APPENDIX_E.md">APPENDIX E</a> for more details<BR/>
TIMESTAMP &#8211; timestamp of the SMS sending<BR/>

<p><strong>This postback has the following anatomy:</strong></p>
<pre>
&lt;?xml version='1.0'?&gt;
&lt;POSTBACK xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
xsi:noNamespaceSchemaLocation ="http://www.skycore.com/schema/postback.xsd"&gt;
  &lt;ORIGIN&gt;SMS_MT&lt;/ORIGIN&gt;
  &lt;CODE&gt;N201&lt;/CODE&gt;
  &lt;STATUS&gt;Message Sent&lt;/STATUS&gt;
  &lt;TO&gt;16503333058&lt;/TO&gt;
  &lt;TRACKINGID&gt;U01TXzgwNjc4&lt;/TRACKINGID&gt;
  &lt;SPID&gt;0001470&lt;/SPID&gt;
  &lt;TIMESTAMP&gt;2013-11-05T05:41:08-05:00&lt;/TIMESTAMP&gt;
&lt;/POSTBACK&gt;
</pre>
[Back To The Top](#DocTop)<BR />
<BR />
<a name="Status"><strong>SMS MT Status</strong>
<p><strong>Synopsis:</strong> This postback provides a notification about the status of an SMS.</p>
<strong><p>This postback will contain the following nodes:</p></strong>
CODE, ORIGIN<BR/>
STATUS &#8211; Indicate if the SMS was sent out successfully - allowed values are "Message Sent/Delivered" or "Message Sent/Failed"<BR/>
TO &#8211; SMS receiver<BR/>
TRACKINGID &#8211; ID returned via API &#8211; this postback can be matched with API response using this field.<BR/>
SPID &#8211; Carrier Identification - please reffer to <a href="/1.3/CONTENTS/APPENDIX/APPENDIX_E.md">APPENDIX E</a> for more details<BR/>
TIMESTAMP &#8211; timestamp of the SMS Delivery Receipt<BR/>
AGGREGATOR &#8211; SMS aggregator ID<BR/>
STATUSDETAILS &#8211; node with some additional information passed to us from the aggregator/carrier<BR/>

<p><strong>This postback has the following anatomy:</strong></p>
<pre>
&lt;?xml version='1.0'?&gt;
&lt;POSTBACK xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
xsi:noNamespaceSchemaLocation ="http://www.skycore.com/schema/postback.xsd"&gt;
  &lt;ORIGIN&gt;SMS_MT&lt;/ORIGIN&gt;
  &lt;CODE&gt;N202&lt;/CODE&gt;
  &lt;STATUS&gt;Message Sent/Delivered&lt;/STATUS&gt;
  &lt;TO&gt;16503333058&lt;/TO&gt;
  &lt;TRACKINGID&gt;U01TXzgwNjc4&lt;/TRACKINGID&gt;
  &lt;SPID&gt;0001470&lt;/SPID&gt;
  &lt;TIMESTAMP&gt;2013-11-05T05:41:15-05:00&lt;/TIMESTAMP&gt;
  &lt;AGGREGATORID&gt;11529-64807-97508-73852-97658&lt;/AGGREGATORID&gt;
&lt;/POSTBACK&gt;
</pre>
[Back To The Top](#DocTop)<BR />
<BR />
<a name="Binary"><strong>MMS MT (Binary)</strong>
<p><strong>Synopsis:</strong> In binary sending, we deliver a postback notification called &#8220;N101&#8243; immediately after we begin to process the MMS. Upon receiving Delivery Report (DLR), the system generates Postback notification &#8220;N102&#8243; with the handset name. N101 and N102 notifications are linked by TRACKINGID.<p>
<strong><p>These postbacks will contain the following nodes:</p></strong>
CODE, ORIGIN<BR/>
SENTAS &#8211; indicates if the MMS was delivered as MMS (binary delivery) or SMS (xHTML). Binary delivery will always be MMS<BR/>
MMSID &#8211; ID of the MMS<BR/>
TO &#8211; MMS receiver<BR/>
SPID &#8211; carrier ID &#8211; please check API documentation <a href="/1.3/CONTENTS/APPENDIX/APPENDIX_E.md">APPENDIX E</a><BR/>
TRACKINGID &#8211; ID returned via API &#8211; this postback can be matched with API response using this field.<BR/>
TIMESTAMP &#8211; timestamp of the MMS was sent (N101) or when MMS was delivered (N102)<BR/>
HANDSET &#8211; handset profile returned inside Delivery Receipt. This is present only in N102 notification<BR/>
STATUS &#8211; For N101 notification status can be "Message Sent". For N102 notification status can be "Message Sent/Delivered", "Message Sent/Expired" or "Message Sent/Rejected"<BR/>
STATUSDETAILS &#8211; For N101 notification when status is "Message Failed" postback will contain this node with error details.<BR/>
AGGREGATORID &#8211; Only in N102 notification, contain Aggregator ID of the sending.<BR/>

<p><strong>The N101 anatomy:</strong></p>
<pre>
&lt;?xml version='1.0'?&gt;
&lt;POSTBACK xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
xsi:noNamespaceSchemaLocation ="http://www.skycore.com/schema/postback.xsd"&gt;
  &lt;ORIGIN&gt;MMS_MT&lt;/ORIGIN&gt;
  &lt;CODE&gt;N101&lt;/CODE&gt;
  &lt;SENTAS&gt;MMS&lt;/SENTAS&gt;
  &lt;STATUS&gt;Message Sent&lt;/STATUS&gt;
  &lt;MMSID&gt;39597&lt;/MMSID&gt;
  &lt;TO&gt;16501112222&lt;/TO&gt;
  &lt;TRACKINGID&gt;TU1TXzU5Nzg3OQ==&lt;/TRACKINGID&gt;
  &lt;SPID&gt;0001570&lt;/SPID&gt;
  &lt;TIMESTAMP&gt;2012-06-07T07:27:29-05:00&lt;/TIMESTAMP&gt;
&lt;/POSTBACK&gt;
</pre>

<p><strong>The N102 anatomy:</strong></p>
<pre>
&lt;?xml version='1.0'?&gt;
&lt;POSTBACK xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
xsi:noNamespaceSchemaLocation ="http://www.skycore.com/schema/postback.xsd"&gt;
  &lt;ORIGIN&gt;MMS_MT&lt;/ORIGIN&gt;
  &lt;CODE&gt;N102&lt;/CODE&gt;
  &lt;SENTAS&gt;MMS&lt;/SENTAS&gt;
  &lt;STATUS&gt;Message Sent/Delivered&lt;/STATUS&gt;
  &lt;MMSID&gt;39597&lt;/MMSID&gt;
  &lt;TO&gt;16501112222&lt;/TO&gt;
  &lt;TRACKINGID&gt;TU1TXzU5Nzg3OQ==&lt;/TRACKINGID&gt;
  &lt;SPID&gt;0001570&lt;/SPID&gt;
  &lt;TIMESTAMP&gt;2012-06-07T07:27:34-05:00&lt;/TIMESTAMP&gt;
  &lt;HANDSET&gt;motol7c&lt;/HANDSET&gt;
  &lt;AGGREGATORID&gt;11529-64807-97508-73852-97658&lt;/AGGREGATORID&gt;
&lt;/POSTBACK&gt;
</pre>
[Back To The Top](#DocTop)<BR />
<BR />
<a name="xHTML"><strong>MMS MT (xHTML)</strong>
<p><strong>Synopsis:</strong> In this method we deliver MMS as SMS link to the content, we send one Postback N101 notifying that we started to process the message. When we receive Delivery Report(DLR) for SMS, we generate Postback notification N202.</p>
<strong><p>These postbacks will contain the following nodes:</p></strong>
CODE, ORIGIN<BR/>
SENTAS &#8211; this node indicate if MMS was delivered as MMS (binary delivery) or SMS (xHTML). For xHTML delivery it will always be SMS<BR/>
MMSID &#8211; ID of the MMS<BR/>
TO &#8211; MMS receiver<BR/>
SPID &#8211; carrier ID &#8211; please check API documentation <a href="/1.3/CONTENTS/APPENDIX/APPENDIX_E.md">APPENDIX E</a><BR/>
TRACKINGID &#8211; ID returned via API &#8211; this postback can be matched with API response using this field.<BR/>
TIMESTAMP &#8211; timestamp of the MMS was sent (N101) or when SMS was delivered (N202)<BR/>
STATUS &#8211; For N101 notification status can be "Message Sent". For N202 notification status can be "Message<BR/> Sent/Delivered" or "Message Sent/Failed"<BR/>
AGGREGATORID &#8211; Only in N202 notification, contain Aggregator ID of the sending.<BR/>
STATUSDETAILS &#8211; node with some additional information passed to us from the aggregator/carrier<BR/>

<p><strong>The N101 anatomy:</strong></p>
<pre>
&lt;?xml version='1.0'?&gt;
&lt;POSTBACK xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
xsi:noNamespaceSchemaLocation ="http://www.skycore.com/schema/postback.xsd"&gt;
  &lt;ORIGIN&gt;MMS_MT&lt;/ORIGIN&gt;
  &lt;CODE&gt;N101&lt;/CODE&gt;
  &lt;SENTAS&gt;SMS&lt;/SENTAS&gt;
  &lt;STATUS&gt;Message Sent&lt;/STATUS&gt;
  &lt;MMSID&gt;39755&lt;/MMSID&gt;
  &lt;TO&gt;16502424956&lt;/TO&gt;
  &lt;TRACKINGID&gt;TU1TXzU5Nzg3Nw==&lt;/TRACKINGID&gt;
  &lt;SPID&gt;0001140&lt;/SPID&gt;
  &lt;TIMESTAMP&gt;2012-06-07T07:27:34-05:00&lt;/TIMESTAMP&gt;
&lt;/POSTBACK&gt;
</pre>

<p><strong>The N202 anatomy:</strong></p>
<pre>
&lt;?xml version='1.0'?&gt;
&lt;POSTBACK xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
xsi:noNamespaceSchemaLocation ="http://www.skycore.com/schema/postback.xsd"&gt;
  &lt;ORIGIN&gt;MMS_MT&lt;/ORIGIN&gt;
  &lt;CODE&gt;N202&lt;/CODE&gt;
  &lt;SENTAS&gt;SMS&lt;/SENTAS&gt;
  &lt;STATUS&gt;Message Sent/Delivered&lt;/STATUS&gt;
  &lt;TO&gt;16502424956&lt;/TO&gt;
  &lt;TRACKINGID&gt;TU1TXzU5Nzg3Nw==&lt;/TRACKINGID&gt;
  &lt;SPID&gt;0001140&lt;/SPID&gt;
  &lt;TIMESTAMP&gt;2012-06-07T07:28:09-05:00&lt;/TIMESTAMP&gt;
  &lt;AGGREGATORID&gt;11529-64807-97508-73852-97658&lt;/AGGREGATORID&gt;
&lt;/POSTBACK&gt;
</pre>
[Back To The Top](#DocTop)<BR />
<BR />
<a name="Degrade"><strong>MMS MT (Binary Degraded to xHTML and Delivered as an SMS Link)</strong>
<p><strong>Synopsis:</strong> In some rare cases we degrade the binary MMS and deliver it as an SMS link; this may be due to the MMS being too big to deliver as binary.  We send one Postback N101 notifying that we started to process the message - in this case the postback will contain an additional STATUSDETAILS node describing why it is being delivered as xHTML (This is the only difference from xHTML delivery).  When we receive the Delivery Report(DLR) for SMS, we generate a Postback N202. 
<strong><p>These postbacks will contain the following nodes:</p></strong>
CODE, ORIGIN<BR/>
SENTAS &#8211; this node indicate if MMS was delivered as MMS (binary delivery) or SMS (xHTML). For xHTML delivery it will always be SMS<BR/>
MMSID &#8211; ID of the MMS<BR/>
TO &#8211; MMS receiver<BR/>
SPID &#8211; carrier ID &#8211; please check API documentation <a href="/1.3/CONTENTS/APPENDIX/APPENDIX_E.md">APPENDIX E</a><BR/>
TRACKINGID &#8211; ID returned via API &#8211; this postback can be matched with API response using this field.<BR/>
TIMESTAMP &#8211; timestamp of the MMS was sent (N101) or when SMS was delivered (N202)<BR/>
STATUS &#8211; For N101 notification status can be "Message Sent". For N202 notification status can be "Message Sent/Delivered" or "Message Sent/Failed"<BR/>
STATUSDETAILS &#8211; For N101 notification this node will contain details why the MMS is being delivered as xHTML.<BR/>
AGGREGATORID &#8211; Only in N202 notification, contain Aggregator ID of the sending.<BR/>

<p><strong>The N101 anatomy:</strong></p>
<pre>
&lt;?xml version='1.0'?&gt;
&lt;POSTBACK xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
xsi:noNamespaceSchemaLocation ="http://www.skycore.com/schema/postback.xsd"&gt;
  &lt;ORIGIN&gt;MMS_MT&lt;/ORIGIN&gt;
  &lt;CODE&gt;N101&lt;/CODE&gt;
  &lt;SENTAS&gt;SMS&lt;/SENTAS&gt;
  &lt;STATUS&gt;Message Sent&lt;/STATUS&gt;
  &lt;MMSID&gt;39755&lt;/MMSID&gt;
  &lt;TO&gt;16502424956&lt;/TO&gt;
  &lt;TRACKINGID&gt;TU1TXzU5Nzg3Nw==&lt;/TRACKINGID&gt;
  &lt;SPID&gt;0001140&lt;/SPID&gt;
  &lt;TIMESTAMP&gt;2012-06-07T07:27:34-05:00&lt;/TIMESTAMP&gt;
  &lt;STATUSDETAILS&gt;Handset setting: mms with pass via xHTML;&lt;/STATUSDETAILS&gt;
&lt;/POSTBACK&gt;
</pre>

<p><strong><strong>The N202 anatomy:</strong></strong></p>
<pre>
&lt;?xml version='1.0'?&gt;
&lt;POSTBACK xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
xsi:noNamespaceSchemaLocation ="http://www.skycore.com/schema/postback.xsd"&gt;
  &lt;ORIGIN&gt;MMS_MT&lt;/ORIGIN&gt;
  &lt;CODE&gt;N202&lt;/CODE&gt;
  &lt;SENTAS&gt;SMS&lt;/SENTAS&gt;
  &lt;STATUS&gt;Message Sent/Delivered&lt;/STATUS&gt;
  &lt;TO&gt;16502424956&lt;/TO&gt;
  &lt;TRACKINGID&gt;TU1TXzU5Nzg3Nw==&lt;/TRACKINGID&gt;
  &lt;SPID&gt;0001140&lt;/SPID&gt;
  &lt;TIMESTAMP&gt;2012-06-07T07:28:09-05:00&lt;/TIMESTAMP&gt;
  &lt;AGGREGATORID&gt;11529-64807-97508-73852-97658&lt;/AGGREGATORID&gt;
&lt;/POSTBACK&gt;
</pre>
[Back To The Top](#DocTop)<BR />
<BR />
<a name="SendFail"><strong>MMS MT (Sending Failure)</strong>
<p><strong>Synopsis:</strong> Sometimes the system is unable to send an MMS out. In this situations we send a postback E101. 
<strong><p>This postback will contain the following nodes:</p></strong>
CODE, ORIGIN<BR/>
MMSID &#8211; ID of the MMS<BR/>
TO &#8211; MMS receiver<BR/>
SPID &#8211; carrier ID &#8211; please check API documentation <a href="/1.3/CONTENTS/APPENDIX/APPENDIX_E.md">APPENDIX E</a><BR/>
TRACKINGID &#8211; ID returned via API &#8211; this postback can be matched with API response using this field.<BR/>
TIMESTAMP &#8211; timestamp of the MMS was sent (N101) or when MMS was delivered (N102)<BR/>
STATUS &#8211; For E101 notification status can be "Message Failed".<BR/>
STATUSDETAILS &#8211; For E101 notification when status is "Message Failed" postback will contain this node with error details.<BR/>

<p><strong>The E101 anatomy:</strong></p>
<pre>
&lt;?xml version='1.0'?&gt;
&lt;POSTBACK xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
xsi:noNamespaceSchemaLocation ="http://www.skycore.com/schema/postback.xsd"&gt;
  &lt;ORIGIN&gt;MMS_MT&lt;/ORIGIN&gt;
  &lt;CODE&gt;E101&lt;/CODE&gt;
  &lt;STATUS&gt;Message Failed&lt;/STATUS&gt;
  &lt;MMSID&gt;39755&lt;/MMSID&gt;
  &lt;TO&gt;16502424956&lt;/TO&gt;
  &lt;TRACKINGID&gt;TU1TXzU5Nzg3Nw==&lt;/TRACKINGID&gt;
  &lt;SPID&gt;0001140&lt;/SPID&gt;
  &lt;STATUSDETAILS&gt;Error fetching object(Database Error: Could not find number/email imported in database)
&lt;/POSTBACK&gt;
</pre>
[Back To The Top](#DocTop)<BR />
<BR />
<a name="SaveMMS"> <strong>MMS MT (Save MMS)</strong>
<p><strong>Synopsis:</strong> When MMS is saved (using API or our MMS Composer) we generate postback notification. When saving was successful we generate N003.</p>
<strong><p>This postback will contain the following nodes:</p></strong>
CODE, ORIGIN<BR/>
MMSID &#8211; ID of the MMS<BR/>

<p><strong>The N003 anatomy:</strong></p>
<pre>
&lt;?xml version='1.0'?&gt;
&lt;POSTBACK&gt;
  &lt;ORIGIN&gt;MMS_MT&lt;/ORIGIN&gt;
  &lt;CODE&gt;N003&lt;/CODE&gt;
  &lt;MMSID&gt;35674&lt;/MMSID&gt;
&lt;/POSTBACK&gt;
</pre>
[Back To The Top](#DocTop)<BR />
<BR />
<a name="ContentFail"> <strong>MMS MT (Save MMS Content Failure)</strong>
<p><strong>Synopsis:</strong> If encoding of the Content failed we generate postback E002 containgin MMSID and AUDIONAME/VIDEONAME pointing to the content that failed to encode properly.</p>
<strong><p>This postback will contain the following nodes:</p></strong>
CODE, ORIGIN<BR/>
MMSID &#8211; ID of the MMS<BR/>
AUDIONAME &#8211; points to audio content that failed to encode properly<BR/>
VIDEONAME &#8211; points to video content that failed to encode properly<BR/>

<p><strong>The E002 anatomy:</strong>
<pre>
&lt;?xml version='1.0'?&gt;
&lt;POSTBACK&gt;
  &lt;ORIGIN&gt;MMS_MT&lt;/ORIGIN&gt;
  &lt;CODE&gt;E002&lt;/CODE&gt;
  &lt;MMSID&gt;35674&lt;/MMSID&gt;
  &lt;AUDIONAME&gt;sample.mp3&lt;/AUDIONAME&gt;
&lt;/POSTBACK&gt;
</pre>
[Back To The Top](#DocTop)<BR />
