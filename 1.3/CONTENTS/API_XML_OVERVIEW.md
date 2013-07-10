<a href="/1.3/README.md">BACK TO TABLE OF CONTENTS</a>
<BR>
<BR>

<h1>API XML Overview</h1>

<b>Request</b>

To make an API call you need to send an HTTP request to an API URL. There are two ways of making API requests:

     GET request
     POST with XML request – XML needs to be passed inside an ‘xml’ variable. This documentation will 
                             show XML request examples.

<b>Authentication :</b>

Authenticating an API call can be done in two ways:

    Using API KEY   – Each request must contain API KEY that is used for authentication. 
                      The API KEY is a random, unique string that can be retrieved from the API Settings page.
                           
    Using user/pass - Each request must contain username and MD5() encoded password.

<b>Related Error codes:</b>

     E100, E101, E102, E103, E104, E105, E106, E107, E108, E109

<b>Response Example:</b>

    <RESPONSE>
    
        <STATUS>Failure</STATUS>
        
        <ERRORCODE>E101</ERRORCODE>
        
        <ERRORINFO>'action' required</ERRORINFO>
        
    </RESPONSE>
