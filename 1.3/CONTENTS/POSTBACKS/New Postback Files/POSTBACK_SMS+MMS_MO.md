<a href="/1.3/README.md">Back to the Table of Contents</a>&nbsp;&nbsp;|&nbsp;&nbsp;<a href="/1.3/CONTENTS/POSTBACKS/New%20Postback%20Files/POSTBACK_SYSTEM_OVERVIEW.md">Postback System Overview</a>
<h2>SMS/MMS MO Postbacks</h2>
<div id="page-content"><strong>Brief Overview:</strong>
This document will provide a technical description of the MMS/SMS MO postback API. Briefly, this API allows those with an SMS/MMS MO-enabled shortcode to forward received messages (MMS/SMS MO) to their server.

<strong>SMS/MMS MO-Specific URL:</strong>
A separate Postback URL specifically for SMS/MMS MO's(Mobile Originated) maybe be set via the API Settings tab of your account.  If it is not set, all postbacks will be sent to the Postback URL that is set.

<strong>SMS MO General Information:</strong>
To receive SMS MO postback notifications you need to have that option enabled in your account. Once the SMS MO 
postback is enabled you will start receiving HTTP Posts on URL of your choice for each SMS MO received related to 
your account.

<strong>MMS MO General Information</strong>
To receive MMS MO postback notification you need to have that option enabled in your account and you need to 
configure it within the particular MMS MO campaign.  Once the MMS MO postback is enabled you will start receiving 
HTTP Posts on URL of your choice for each MMS MO received on the MMS MO Keyword. If you have (optionally) enabled 
the MMS MO moderation panel then the postback notifictions will only be sent upon manual approval by the moderator.



<strong>The SMS MO</strong>
<p><strong>Synopsis: </strong>This Postback provides a notification when SMS MO is received.</p>
<strong><p>This postback will contain following nodes:</p></strong>

CODE, ORIGIN<BR/>
FROM &#8211; SMS sender mobile number<BR/>
TO &#8211; shortcode the SMS was sent to<BR/>
TEXT &#8211; this is actuall text that was sent by the sender<BR/>
RECEIVED &#8211; timestamp of the SMS received by our server<BR/>

<p><strong>This postback has the following anatomy:</strong></p>
<pre>
<p>&lt;POSTBACK&gt;
&lt;ORIGIN&gt;MMS_MO&lt;/ORIGIN&gt;
&lt;CODE&gt;N401&lt;/CODE&gt;
&lt;FROM&gt;15552312102&lt;/FROM&gt;
&lt;TO&gt;86717&lt;/TO&gt;
&lt;KEYWORD&gt;testoffer&lt;/KEYWORD&gt;
&lt;TRACKINGID&gt;MMS_MO_vp8Vsf2M&lt;/TRACKINGID&gt;
&lt;SPID&gt;0001650&lt;/SPID&gt;
&lt;TIMESTAMP&gt;2011-09-28T15:25:30-04:00&lt;/TIMESTAMP&gt;
&lt;CONTENT&gt;
&lt;FILE&gt;&#8230;URL of Content Here&#8230;&lt;/FILE&gt;
&lt;FILE&gt;&#8230;URL of Content Here&#8230;&lt;/FILE&gt;
&lt;FILE&gt;&#8230;URL of Content Here&#8230;&lt;/FILE&gt;
&lt;/CONTENT&gt;
&lt;/POSTBACK&gt;</p>
</pre>


<p><strong>The MMS MO</strong></p>
<p><strong>Synopsis: </strong>This Postback provides a notification when MMS MO is received.</p> 
<strong><p>This postback will contain following nodes:</p></strong>

CODE, ORIGIN<BR/>
NOTIFICATION &#8211; SMS sender mobile number<BR/>
FROM &#8211; tags contain the phone number, including the country code, of the sender.<BR/>
TO &#8211; tags contain the destination shortcode.<BR/>
KEYWORD &#8211; tags contain the keyword recognized that was passed in the MMS.<BR/>
TRACKINGID &#8211; tags contain a tracking ID, which contains the ID we've assigned this MMS MO on our system.<BR/>
SPID &#8211; tags contain the SPID of the sender's carrier.<BR/>
TIMESTAMP &#8211; tags contain the timestamp that our system received the MMS MO.<BR/>
CONTENT &#8211; contains the file nodes sent in the MMS MO<BR/>
FILE &#8211; contains a single URL to a picture, video, audio or text file sent in the MMS MO.  The URL points to the location of the content on our servers. For those developing the back-end handling of the postback URL, you may choose to download/store these content files for whatever purpose you see fit. You may also choose to store the URLs for download at a future time.<BR/>
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
