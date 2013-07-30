<a href="/1.3/README.md">Back to the Table of Contents</a>&nbsp;&nbsp;|&nbsp;&nbsp;<a href="API_METHODS.md">Back to API Methods</a>
<h2>generatePassById</h2>
<p><strong>Synopsis:</strong><br />
This API function triggers the passbook pass generation for the given passDataID. On success, returns a link to download the generated passbook pass (i.e., pkpass file).
For more info see below for Mandatory/Optional fields and Error codes.
</p>
<div><strong>Request:</strong></div>
<pre>&lt;REQUEST&gt;
        &lt;ACTION&gt;generatePassById&lt;/ACTION&gt;
        &lt;API_KEY&gt;apiKey&lt;/API_KEY&gt;
        &lt;PASSDATAID&gt;passDataID&lt;/PASSDATAID&gt;
    &lt;/REQUEST&gt;</pre>
<div><strong>Request Parameters:</strong></div>
<pre><strong>Mandatory:</strong> action, apiKey, passDataId
<strong>Optional:</strong> N/A</pre>
<strong>Response Parameters:</strong><br />
status, Errorcode, Errorinfo
<strong>Related Errorcodes: </strong><br />
E807, E808, E830, E831
    
<div><strong>Request Example:</strong></div>
<pre>&lt;REQUEST&gt;
        &lt;ACTION&gt;generatePassById&lt;/ACTION&gt;
        &lt;API_KEY&gt;qTFkykO9JTfahCOqJ0V2Wf5Cg1t8iWlZ&lt;/API_KEY&gt;
        &lt;PASSDATAID&gt;1233&lt;/PASSDATAID&gt;
    &lt;/REQUEST&gt;</pre>
<div><strong>Response Example: Success</strong></div>
<pre>&lt;RESPONSE&gt;
    &lt;STATUS&gt;Success&lt;/STATUS&gt;
    &lt;PASSLINK&gt;https://d2c.skycore.com/passes/downloadpass.php?pass=4jfjhsus&lt;/PASSLINK&gt;
&lt;/RESPONSE&gt;</pre>
<div><strong>Response Example: Failure</strong></div>
<pre>&lt;RESPONSE&gt;
    &lt;STATUS&gt;Failure&lt;/STATUS&gt;
    &lt;ERRORCODE&gt;E830&lt;/ERRORCODE&gt;
    &lt;ERRORINFO&gt;Passbook Pass was not generated. Internal error occured.&lt;/ERRORINFO&gt;
&lt;/RESPONSE&gt;</pre>
