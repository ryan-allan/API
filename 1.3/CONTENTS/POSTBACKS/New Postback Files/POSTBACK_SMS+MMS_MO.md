<a href="/1.3/README.md">Back to the Table of Contents</a>
<h2>SMS/MMS MO Postbacks</h2>
<div id="page-content"><p><strong>Brief Overview:</strong></p>
<p>This document will provide a technical description of the MMS/SMS MO POSTBACK API. In brief, this API allows those with an 
SMS/MMS MO-enabled shortcode to forward received messages (MMS/SMS MO) to your server.</p>

<strong>SMS MO General Information:</strong>
To receive SMS MO postback notification you need to have that option enabled in your account. Once the SMS MO 
postback is enabled you will start receiving HTTP Posts on URL of your choice for each SMS MO received related to 
your account.

<h4>Types of SMS MO:</h4>

<strong>SMS MO Received</strong>
<p><strong>Synopsis: </strong>This Postback provides a notification when SMS MO is received. Postback will contain following nodes:</p>

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
<p>FROM &#8211; SMS sender mobile number</p>
<p>TO &#8211; shortcode the SMS was sent to</p>
<p>TEXT &#8211; this is actuall text that was sent by the sender</p>
<p>RECEIVED &#8211; timestamp of the SMS received by our server</p>
<p><strong>This postback has the following anatomy:</strong></p>
<p>This bundle has the following anatomy:</p>

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

<p><strong>MMS MO</strong></p>
<p>To receive MMS MO postback notification you need to have that option enabled in your account and you need to 
configure it within the particular MMS MO campaign.  Once the MMS MO postback is enabled you will start receiving 
HTTP Posts on URL of your choice for each MMS MO received on the MMS MO Keyword. If you have (optionally) enabled 
the MMS MO moderation panel then the postback notifictions will only be sent upon manual approval by the moderator.</p>

<p><a name="the_xml_bundle"></a> <strong>The MMS MO XML Bundle:</strong></p>
<p>The XML bundle has the following anatomy:</p>
<pre>
&lt;POSTBACK&gt;
&lt;NOTIFICATION&gt;
&lt;ORIGIN>MMS_MO&lt;/ORIGIN&gt;
&lt;CODE>N401&lt;/CODE&gt;
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

<p>Each MMS MO message is represented by a &lt;NOTIFICATION&gt; tag and all of the nodes and data contained within. When
new MMS MO are received by our system, and approved in the moderation panel, they are bundled as shown, and sent to your
postback URL using a process that runs every 1 minute. Each bundle can contain up to 300 notification nodes, each 
representing a different incoming message.</p>

<p>The content node contains all of the pictures, videos, audio, text, and smil that compose the received MMS MO message. 
The URL points to the location of the content on our servers. For those developing the back-end handling of the postback
URL, you may choose to download/store these content files for whatever purpose you see fit. You may also choose to store
the URLs for download at a future time.</p>

<p><a name="breaking_down_each_notification"></a> <strong>Breaking down Each Notification</strong></p>
<p>Many of the tags are self-explanatory.</p>
<ul>
<li>&lt;FROM&gt;&lt;/FROM&gt; tags contain the phone number, including the country code, of the sender.</li>
<li>&lt;TO&gt;&lt;/TO&gt; tags contain the destination shortcode. In the above example, shortcode is 86717.</li>
<li>&lt;KEYWORD&gt;&lt;/KEYWORD&gt; tags contain the keyword recognized that was passed in the MMS.</li>
<li>&lt;TRACKINGID&gt;&lt;/TRACKINGID&gt; tags contain a tracking ID, which contains the ID we&#8217;ve assigned this MMS 
MO on our system.</li>
<li>&lt;RECEIVED&gt;&lt;/RECEIVED&gt; tags contain the timestamp when the SMS MO was received by our side.</li>
<li>&lt;SPID&gt;&lt;/SPID&gt; tags contain the SPID of the sender&#8217;s carrier. In the above example, 000165 
corresponds to the mobile carrier Sprint. For the full list of SPIDs and their corresponding carriers, please refer to 
the SPID reference table in the last section.</li>
<li>&lt;TIMESTAMP&gt;&lt;/TIMESTAMP&gt; tags contain the timestamp that our system received the MMS MO. This is different
from the &#8216;created&#8217; attribute under the notification tag, which represents the time we sent the message to 
your postback URL.</li>
</ul>
<p><a name="setting_your_postback_url"></a> <strong>Setting your Postback URL:</strong></p>
<p>You can set your postback URL by logging into your account and going to &#8216;Account&#8217; tab and selecting the 
&#8216;API settings&#8217; button. Enter the URL under the setting &#8216;API Postback URL&#8217; and make sure that the &#8216;enabled&#8217; and &#8216;MMS MO postback&#8217; checkboxes are selected. Hit the save button and any MMS MO campaign you&#8217;ve created with &#8216;Postback Processing&#8217; enabled will start sending messages to your URL in the XML format shown above.</p>
