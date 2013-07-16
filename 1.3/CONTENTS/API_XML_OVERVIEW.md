<a href="/1.3/README.md">Back to the Table of Contents</a>
<h2>API XML Overview</h2>
<b>Request</b>
To make an API call you need to send an HTTP request to an API URL. There are two ways of making API requests:<br/>
GET Request 
POST with XML Request – XML needs to be passed inside an 'xml' variable. This documentation will show XML request examples.
<br/><br/>
<b>Authentication :</b>
Authenticating an API call can be done in two ways:
Using apikey    – Each request must contain API KEY that is used for authentication. The API KEY is a random, unique string that can be retrieved from the API Settings page.
Using user/pass - Each request must contain username and MD5() encoded password.
<br/><br/>
<b>Related Error codes:</b><br/>
E100, E101, E102, E103, E104, E105, E106, E107, E108, E109
<br/><br/>
<b>Response Example:</b><br/>
&lt;RESPONSE&gt;<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&lt;STATUS&gt;Failure&lt;/STATUS&gt;<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&lt;ERRORCODE&gt;E101&lt;/ERRORCODE&gt;<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&lt;ERRORINFO&gt; 'action' required&lt;/ERRORINFO&gt;<br/>
&lt;/RESPONSE&gt;
