<a href="/TABLE%20OF%20CONTENTS.md">BACK TO TABLE OF CONTENTS</a>
<BR>
<a href="/API%20FUNCTIONS.md">BACK TO API FUNCTIONS</a>
<BR>
<BR>

<h1>loginUser()</h1>
<BR>

<p><strong>Synopsis:</strong><br />
This API function creates a session for an account so that widgets can be launched and linked to it such as the SWF MMS Composer Object or the MMS Preview SWF Objects.</p>
<div><strong>Request:</strong></div>
<pre>&lt;REQUEST&gt;
  &lt;ACTION&gt;loginUser&lt;/ACTION&gt;
	&lt;API_KEY&gt;API KEY&lt;/API_KEY&gt;
&lt;/REQUEST&gt;</pre>
<div><strong>Request Parameters:</strong></div>
<pre><strong>Mandatory:</strong> Action, API_KEY
<strong>Optional:</strong> N/A</pre>
<strong>Response Parameters:</strong><br />

    Status, SessionID
    
<strong>Related Error codes:</strong> 

    N/A

<div><strong>Request Example:</strong></div>
<pre>&lt;REQUEST&gt;
	&lt;ACTION&gt;loginUSer&lt;/ACTION&gt;
	&lt;API_KEY&gt;qTFkykO9JTfahCOqJ0V2Wf5Cg1t8iWlZ&lt;/API_KEY&gt;
&lt;/REQUEST&gt;</pre>
<div><strong>Response Example: Success</strong></div>
<pre>&lt;RESPONSE&gt;
	&lt;STATUS&gt;Success&lt;/STATUS&gt;
	&lt;SESSIONID&gt;asdfsadfsadfsdf&lt;/SESSIONID&gt;
&lt;/RESPONSE&gt;</pre>
<div><strong>Response Example: Failure</strong></div>
<pre>&lt;RESPONSE&gt;
	&lt;STATUS&gt;Failure&lt;/STATUS&gt;
	&lt;ERRORCODE&gt;E170&lt;/ERRORCODE&gt;
	&lt;ERRORINFO&gt; Invalid &lt;/ERRORINFO&gt;
&lt;/RESPONSE&gt;</pre>
