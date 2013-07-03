<a href="/TABLE%20OF%20CONTENTS.md">BACK TO TABLE OF CONTENTS</a>
<BR>
<a href="/API%20FUNCTIONS.md">BACK TO API FUNCTIONS</a>
<BR>
<BR>


<h1>sendSavedEmail()</h1>
<BR>

<p><strong>Synopsis:</strong><br />
This API sends stored email template from a specified account using a EMAILID to one EMAIL address.</p>
<p><strong>Request:</strong></p>
<pre>&lt;REQUEST&gt;
  &lt;ACTION&gt;sendSavedEmail&lt;/ACTION&gt;
	&lt;API_KEY&gt;API KEY&lt;/API_KEY&gt;
	&lt;EMAILID&gt;EMAILID&lt;/EMAILID&gt;
	&lt;EMAIL&gt;EMAIL&lt;/EMAIL&gt;
&lt;/REQUEST&gt;</pre>
<div><strong>Request Parameters:</strong></div>
<pre><strong>Mandatory:</strong> Action, API_KEY, EMAILID, Email
<strong>Optional:</strong>N/A</pre>
<strong>Response Parameters:</strong>

    EMAILID, Status, Email, TrackingID, Errorcode, Errorinfo

<strong>Related Errorcodes: </strong><br />

    E401, E402, E403, E713
    
<div><strong>Request Example:</strong></div>
<pre>&lt;REQUEST&gt;
	&lt;ACTION&gt;sendSavedEmail&lt;/ACTION&gt;
	&lt;API_KEY&gt;qTFkykO9JTfahCOqJ0V2Wf5Cg1t8iWlZ&lt;/API_KEY&gt;
	&lt;EMAIL&gt;john@email.com&lt;/EMAIL&gt;
	&lt;EMAILID&gt;1234&lt;/EMAILID&gt;
&lt;/REQUEST&gt;</pre>
<div><strong>Response Example: Success</strong></div>
<pre>&lt;RESPONSE&gt;
    &lt;STATUS&gt;Success&lt;/STATUS&gt;
    &lt;EMAILID&gt;1234&lt;/EMAILID&gt;
    &lt;TRACKINGID&gt;EMAIL_12346&lt;/TRACKINGID&gt;
    &lt;EMAIL&gt;john@email.com&lt;/EMAIL&gt;
&lt;/RESPONSE&gt;</pre>
<div><strong>Response Example: Failure</strong></div>
<pre>&lt;RESPONSE&gt;
	 &lt;STATUS&gt;Failure&lt;/STATUS&gt;
	 &lt;ERRORCODE&gt;E713&lt;/ERRORCODE&gt;
         &lt;EMAIL&gt;john@email.com&lt;/EMAIL&gt;
         &lt;EMAILID&gt;1234&lt;/EMAILID&gt;
	 &lt;ERRORINFO&gt;There is billing problem on your account&lt;/ERRORINFO&gt;
&lt;/RESPONSE&gt;</pre>
