<b>API XML Overview</b>

<b>Request</b>

To make API call you need to send HTTP request to API URL. There are two ways of making API requests:

     GET request
     POST with XML request – XML needs to be passed inside ‘xml’ variable. This documentation will 
                             show XML request examples.

<b>Authentication</b>

<b>Authenticating API call can be done in two ways:</b>

    Using API KEY – Each request must contain API KEY that is used for authentication. 
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
