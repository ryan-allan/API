<a href="https://github.com/SkycoreMobile/api/blob/master/1.3/CONTENTS.md">BACK TO TABLE OF CONTENTS</a>
<BR>
<BR>
<a href="APPENDIX%20A.md">APPENDIX A</a>
<BR>
<a href="APPENDIX%20B.md">APPENDIX B</a>
<BR>
<a href="APPENDIX%20C.md">APPENDIX C</a>
<BR>
<a href="APPENDIX%20E.md/">APPENDIX E</a>
<BR>

<h1>APPENDIX D</h1>
<h2></h2>

<BR>

<strong>Special Considerations</strong>


<p><strong>International format numbers: </strong> a number format that includes the country, carrier and phone numbers 
without any dialing prefixes (eg 00 or 001) or special characters such as the plus symbol (e.g. &#8217;642111111&#8242; 
not &#8216;+642111111&#8242;). For example the US number (774)-319-9144 in international number format would be 
17743199144 because the USA country code is 1.</p>

<p><strong>Text message lengths:</strong> a text message limit of 160 characters is imposed to prevent the splitting of 
messages into multiple texts in the SMS system.</p>
<p><strong>Sending limitations:</strong> We have implemented throughput limit on your account. If your API requests 
exceed the throughput on your account then you may have some latency in the delivery of your messages.</p>

<p><strong>Postback:</strong> All pending notification are bulked together and wrapped with tag then sent in one http 
request to the Postback URL. If establishing a connection to the Postback URL takes longer than 10 seconds, the 
connection will time out and fail. We expect the remote server to respond with a proper http header containing 200 HTTP 
code, which is considered as successful status. If no response is given or the HTTP code is not 200 we will consider it
a failed request and will retry five minutes later up to 5 times.</p>
