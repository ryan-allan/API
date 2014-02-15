<a name="DocTop"><a href="/1.3/README.md">Back to the Table of Contents</a>&nbsp;&nbsp;|&nbsp;&nbsp;<a href="/1.3/CONTENTS/POSTBACKS/POSTBACK_SYSTEM_OVERVIEW.md">Postback System Overview</a>
<h2>SMS/MMS MT Postbacks</h2>
<div id="page-content"><strong>Brief Overview:</strong>
This document will provide a technical description of the MMS/SMS MT postback API.  Briefly, this API allows those with SMS/MMS MT postbacks enabled to generate and forward SMS/MMS MT postbacks to their server.  For MMS, we have two methods for delivering content; binary and XHTML. We send different Postbacks depending on which method is used.

<strong>Current list of the SMS/MMS MT Postbacks</strong>
 
[SMS MT Sent](#Sent)                            
[SMS MT Status](#Status)                        
[MMS MT (Binary)](#Binary)                       
[MMS MT (XHTML)](#XHTML)                        
[MMS MT (Binary degrade to XHTML and sent as SMS link](#Degrade)  
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
<p><strong>Synopsis:</strong> In binary sending, we deliver a postback notification called &#8220;N101&#8243; immediately after we begin to process the MMS. Upon receiving Delivery Report (DLR), the system generates
