<a href="/1.3/README.md">Back to the Table of Contents</a>
<h2>SMS/MMS MO Postbacks</h2>
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

<h2>Types of SMS MO:</h2>

<strong>SMS MO Received</strong>
<p><strong>Synopsis: </strong>This Postback provides a notification when SMS MO is received. This postback will contain following nodes:</p>

<p>CODE, ORIGIN</p>
<p>FROM &#8211; SMS sender mobile number</p>
<p>TO &#8211; shortcode the SMS was sent to</p>
<p>TEXT &#8211; this is actuall text that was sent by the sender</p>
<p>RECEIVED &#8211; timestamp of the SMS received by our server</p>
<p><strong>This postback has the following anatomy:</strong></p>

<pre>
&lt;?xml version='1.0'?&gt;
&lt;POSTBACK xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:noNamespaceSchemaLocation="http://www.skycore.com/schema/postback.xsd"&gt;
&lt;ORIGIN&gt;SMS_MO&lt;/ORIGIN&gt;
&lt;CODE&gt;N211&lt;/CODE&gt;
&lt;FROM&gt;16311112222&lt;/FROM&gt;
&lt;TO&gt;60856&lt;/TO&gt;
&lt;TEXT&gt;MYKEYCODE&lt;/TEXT&gt;
&lt;RECEIVED&gt;2012-04-16T09:05:56-04:00&lt;/RECEIVED&gt;
&lt;/POSTBACK&gt;
</pre>

<strong>SMS MO Received Bundle</strong>
<p><strong>Synopsis: </strong>This Postback provides a bundle of SMS MO Received postbacks. The bundle will contain following nodes:</p>

<p>CODE, ORIGIN</p>
<p>NOTIFICATION &#8211; Identifies each individual notification</p>
<p>BODY &#8211; Indicates the start of the body of information</p>
<p>FROM &#8211; SMS sender mobile number</p>
<p>TO &#8211; shortcode the SMS was sent to</p>
<p>KEYWORD &#8211; this is actual text that was sent by the sender</p>
<p>RECEIVED &#8211; timestamp of the SMS received by our server</p>
<p><strong>This postback bundle has the following anatomy:</strong></p>

<pre>
&lt;POSTBACK&gt;
&lt;NOTIFICATION id=&#8221;264&#8243; created=&#8221;2011-09-28 17:31:02.835577-04&#8243;&gt;
&lt;ORIGIN&gt;SMS_MO&lt;/ORIGIN&gt;
&lt;CODE&gt;N211&lt;/CODE&gt;
&lt;BODY&gt;
&lt;FROM&gt;15552312102&lt;/FROM&gt;
&lt;TO&gt;86717&lt;/TO&gt;
&lt;KEYWORD&gt;STOP&lt;/KEYWORD&gt;
&lt;RECEIVED&gt;2011-09-28 17:31:02.278751-04&lt;/RECEIVED&gt;
&lt;/BODY&gt;
&lt;/NOTIFICATION&gt;
&lt;/POSTBACK&gt;
</pre>

<h2>Types of MMS MO:</h2>

<strong>SMS MO Received</strong>
<p><strong>Synopsis: </strong>This Postback provides a notification when SMS MO is received. This postback will contain following nodes:</p>

<p>CODE, ORIGIN</p>
<p>FROM &#8211; SMS sender mobile number</p>
<p>TO &#8211; shortcode the SMS was sent to</p>
<p>TEXT &#8211; this is actuall text that was sent by the sender</p>
<p>RECEIVED &#8211; timestamp of the SMS received by our server</p>
<p><strong>This postback has the following anatomy:</strong></p>

<pre>
&lt;?xml version='1.0'?&gt;
&lt;POSTBACK xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:noNamespaceSchemaLocation="http://www.skycore.com/schema/postback.xsd"&gt;
&lt;ORIGIN&gt;SMS_MO&lt;/ORIGIN&gt;
&lt;CODE&gt;N211&lt;/CODE&gt;
&lt;FROM&gt;16311112222&lt;/FROM&gt;
&lt;TO&gt;60856&lt;/TO&gt;
&lt;TEXT&gt;MYKEYCODE&lt;/TEXT&gt;
&lt;RECEIVED&gt;2012-04-16T09:05:56-04:00&lt;/RECEIVED&gt;
&lt;/POSTBACK&gt;
</pre>


<p><strong>MMS MO Received</strong></p>
<p><strong>Synopsis: </strong>This Postback provides a notification when MMS MO is received. This postback will contain following nodes:</p>

<p>CODE, ORIGIN</p>
<p>NOTIFICATION &#8211; SMS sender mobile number</p>
<p>FROM &#8211; tags contain the phone number, including the country code, of the sender.</p>
<p>TO &#8211; tags contain the destination shortcode.</p>
<p>KEYWORD &#8211; tags contain the keyword recognized that was passed in the MMS.</p>
<p>TRACKINGID &#8211; tags contain a tracking ID, which contains the ID we've assigned this MMS MO on our system.</p>
<p>SPID &#8211; tags contain the SPID of the sender's carrier.</p>
<p>TIMESTAMP &#8211; tags contain the timestamp that our system received the MMS MO.</p>
<p>CONTENT &#8211; contains the file nodes sent in the MMS MO</p>
<p>FILE &#8211; contains a single URL to a picture, video, audio or text file sent in the MMS MOThe URL points to the location of the content on our servers. For those developing the back-end handling of the postback URL, you may choose to download/store these content files for whatever purpose you see fit. You may also choose to store the URLs for download at a future time.</p>
<p><strong>This postback has the following anatomy:</strong></p>
<pre>
&lt;POSTBACK&gt;
&lt;NOTIFICATION&gt;
&lt;ORIGIN&gt;MMS_MO&lt;/ORIGIN&gt;
&lt;CODE&gt;N401&lt;/CODE&gt;
&lt;FROM&gt;13217949521&lt;/FROM&gt;
&lt;TO&gt;74700&lt;/TO&gt;
&lt;KEYWORD&gt;all&lt;/KEYWORD>
&lt;TRACKINGID&gt;MMS_MO_iLnCRrL6&lt;/TRACKINGID&gt;
&lt;SPID&gt;0001470&lt;/SPID&gt;
&lt;TIMESTAMP&gt;2014-02-03T11:19:49-05:00&lt;/TIMESTAMP&gt;
&lt;CONTENT&gt;
&lt;FILE&gt;URL of Content Here&lt;/FILE&gt;
&lt;FILE&gt;URL of Content Here&lt;/FILE&gt;
&lt;FILE&gt;URL of Content Here&lt;/FILE&gt;
&lt;/CONTENT&gt;
&lt;/NOTIFICATION&gt;
&lt;/POSTBACK&gt;
</pre>
