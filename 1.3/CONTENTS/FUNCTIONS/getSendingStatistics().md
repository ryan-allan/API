<a href="/1.3/README.md">BACK TO TABLE OF CONTENTS</a>
<BR>
<a href="API_FUNCTIONS.md">BACK TO API FUNCTIONS</a>
<BR>
<BR>

<h1>getSendingStatistics()</h1>
<BR>

<p><strong>Synopsis:</strong><br />
This API requests a report of all messaging transactions between two dates. The server returns the path to an XML file containing the meta data.</p>
<div><strong>Request:</strong></div>
<pre>&lt;REQUEST&gt;
    &lt;ACTION&gt;getSendingStatus &lt;/ACTION&gt;
    &lt;API_KEY&gt;API KEY&lt;/API_KEY&gt;
    &lt;START_DATE&gt;StartDate&lt;/START_DATE&gt;
    &lt;END_DATE&gt;EndDate&lt;/ END_DATE&gt;
&lt;/REQUEST&gt;</pre>
<div><strong>Request Parameters:</strong></div>
<pre><strong>Mandatory:</strong> Action, API_KEY, EndDate, StartDate
<strong>Optional:</strong> N/A</pre>
<strong>Response Parameters:</strong><br />

    Errorcode, Errorinfo, MMSID, Status

<strong>Related Errorcodes: </strong><br />

    E506, E507, E508, E509, E510

<div><strong>Request Example:</strong></div>
<pre>&lt;REQUEST&gt;
  &lt;ACTION&gt;getSendingStatus&lt;/ACTION&gt;
	&lt;API_KEY&gt;qTFkykO9JTfahCOqJ0V2Wf5Cg1t8iWlZ&lt;/API_KEY&gt;
	&lt;START_DATE&gt;2010-10-01 12:00:00&lt;/START_DATE&gt;
	&lt;END_DATE&gt;2010-11-01 12:00:00&lt;/END_DATE&gt;
&lt;/REQUEST&gt;</pre>
<p><strong>Response Example:</strong><br />
Responses will be a link to a XML file containing the report. All results are saved to file which must be downloaded by the requestor. Detailed Information about the report will be in Appendix C.</p>
