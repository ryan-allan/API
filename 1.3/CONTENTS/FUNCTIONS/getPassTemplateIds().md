<a href="/1.3/README.md">Back to the Table of Contents</a>&nbsp;&nbsp;|&nbsp;&nbsp;<a href="API_FUNCTIONS.md">Back to API Methods</a>
<h2>getPassTemplateIds()</h2>
<p><strong>Synopsis:</strong><br />
This API function returns a list of Pass Template Ids for that account.</p>
<div><strong>Request: XML</strong></div>
<pre>&lt;REQUEST&gt;
    &lt;ACTION&gt;getPassTemplateIds&lt;/ACTION&gt;
    &lt;API_KEY&gt;apiKey&lt;/API_KEY&gt;
&lt;/REQUEST&gt;</pre>
<div><strong>Request: GET</strong></div>
<pre>API_URL?action=getpasstemplateids&amp;api_key=apiKey</pre>
<div><strong>Request Parameters:</strong></div>
<pre><strong>Mandatory:</strong>
action, apikey
<strong>Optional:</strong>
--
</pre>
<strong>Response Parameters:</strong><br />
status, passtemplateids, Errorcode, Errorinfo

<strong>Related Errorcodes: </strong><br />
E800
<div><strong>Request Example:</strong></div>
<pre>&lt;REQUEST&gt;
    &lt;ACTION&gt;getPassTemplateIds&lt;/ACTION&gt;
    &lt;API_KEY&gt;qTFkykO9JTfahCOqJ0V2Wf5Cg1t8iWlZ&lt;/API_KEY&gt;    
&lt;/REQUEST&gt;</pre>
<div><strong>Response Example: Success</strong></div>
<pre>&lt;RESPONSE&gt;
    &lt;STATUS&gt;Success&lt;/STATUS&gt;
    &lt;PASSTEMPLATEIDS&gt;30011,30234,30634&lt;/PASSTEMPLATEIDS&gt;
&lt;/RESPONSE&gt;</pre>
<div><strong>Response Example: Failure</strong></div>
<pre>&lt;RESPONSE&gt;
    &lt;STATUS&gt;Failure&lt;/STATUS&gt;
    &lt;ERRORCODE&gt;E800&lt;/ERRORCODE&gt;
    &lt;ERRORINFO&gt;No Pass Templates were created in this account&lt;/ERRORINFO&gt;
&lt;/RESPONSE&gt;</pre>
