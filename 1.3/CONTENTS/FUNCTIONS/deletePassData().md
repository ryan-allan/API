<a href="/1.3/CONTENTS.md">BACK TO TABLE OF CONTENTS</a>
<BR>
<a href="API%20FUNCTIONS.md">BACK TO API FUNCTIONS</a>
<BR>
<BR>

<h1>deletePassData()</h1>
<BR>

<p><strong>Synopsis:</strong><br />
This API function deletes the pass data row. This will avoid generating pass with this data for any future requests.</p>
<div><strong>Request:</strong></div>
<pre>&lt;REQUEST&gt;
    &lt;ACTION&gt;deletePassData&lt;/ACTION&gt;
    &lt;API_KEY&gt;apiKey&lt;/API_KEY&gt;
    &lt;PASSDATAID&gt;passDataID&lt;/PASSDATAID&gt;
&lt;/REQUEST&gt;</pre>
<div><strong>Request Parameters:</strong></div>
<pre><strong>Mandatory:</strong> action, apiKey, passDataId
<strong>Optional:</strong> N/A</pre>
<strong>Response Parameters:</strong><br />

    status, Errorcode, Errorinfo

<strong>Related Errorcodes: </strong><br />

    E807, E808, E821
    
<div><strong>Request Example:</strong></div>
<pre>&lt;REQUEST&gt;
    &lt;ACTION&gt;deletePassData&lt;/ACTION&gt;
    &lt;API_KEY&gt;qTFkykO9JTfahCOqJ0V2Wf5Cg1t8iWlZ&lt;/API_KEY&gt;
    &lt;PASSDATAID&gt;1233&lt;/PASSDATAID&gt;
&lt;/REQUEST&gt;</pre>
<div><strong>Response Example: Success</strong></div>
<pre>&lt;RESPONSE&gt;
    &lt;STATUS&gt;Success&lt;/STATUS&gt;
&lt;/RESPONSE&gt;</pre>
<div><strong>Response Example: Failure</strong></div>
<pre>&lt;RESPONSE&gt;
    &lt;STATUS&gt;Failure&lt;/STATUS&gt;
    &lt;ERRORCODE&gt;E821&lt;/ERRORCODE&gt;
    &lt;ERRORINFO&gt;Pass was not deleted. Internal error occured.&lt;/ERRORINFO&gt;
&lt;/RESPONSE&gt;</pre>
