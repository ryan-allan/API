<a href="/1.3/README.md">Back to the Table of Contents</a>
<h2>Overview: Postback Notification System</h2>

<strong>What is a postback?</strong>
<ul>
<li>A postback is a notification sent via a single HTTP POST request in XML format to a user-specified URL containing information regarding SMS/MMS MO(Mobile Originated), SMS/MMS MT(Mobile Terminated), or Pass Generation events relative to the user's account.</li>
</ul>

<strong>How do postbacks work?</strong>
<ul>
<li>Specific events trigger their respective postbacks and are placed in a queue.</li>
<li>Postbacks in the queue are then processed and sent out every second to the user-specified URL.</li>
<li>Upon a server's reception of the postback, we expect the server to respond with a properly formatted HTTP header containing an HTTP 200 code.</li>
</ul>

<strong>Important Notes</strong>
<ul>
<li>If establishing a connection to the user-specified Postback URL takes longer than 10 seconds, the connection will time out and fail.  After that, we will attempt to resend the postback every 5 minutes up to a total of 5 times.</li>
<li>If the HTTP response from the user's server is not provided or the HTTP code is not 200, we consider the postback a failed request and we will attempt to resend the postback every 5 minutes up to a total of 5 times.</li>
<li> The following tags are always a part of our postbacks:
  <ul>
  <li>ORIGIN &#8211; identifies origin type of the postback</li>
  <li>CODE &#8211; identifies situation for which the postback was generated</li>
  </ul>
</ul>

<strong>Postback Groups</strong>
<ul>
<li><a href="/1.3/CONTENTS/POSTBACKS/New%20Postback%20Files/POSTBACKS_GENERAL.md">General System Postbacks</a></li>
<li><a href="/1.3/CONTENTS/POSTBACKS/New%20Postback%20Files/POSTBACK_SMS+MMS_MO.md">SMS/MMS MO Postbacks</a></li>
<li><a href="/1.3/CONTENTS/POSTBACKS/New%20Postback%20Files/POSTBACK_SMS+MMS_MT.md">SMS/MMS MT Postbacks</a></li>
<li><a href="/1.3/CONTENTS/POSTBACKS/New%20Postback%20Files/POSTBACK_PASSES.md">Pass Generation Postbacks</a></li>
</ul>
