<a href="/1.3/README.md">Back to the Table of Contents</a>&nbsp;&nbsp;|&nbsp;&nbsp;<a href="API_METHODS.md">Back to API Methods</a>
<h2>getPassTemplate()</h2>
<p><strong>Synopsis:</strong><br />
This API function returns the pass template information when given passTemplateId or mmsId or emailId.</p>
<div><strong>Request: XML</strong></div>
<pre>&lt;REQUEST&gt;
    &lt;ACTION&gt;getPassTemplate&lt;/ACTION&gt;
    &lt;API_KEY&gt;apiKey&lt;/API_KEY&gt;
    &lt;PASSTEMPLATEID&gt;passTemplateId&lt;/PASSTEMPLATEID&gt;
&lt;/REQUEST&gt;</pre>
<pre>&lt;REQUEST&gt;
    &lt;ACTION&gt;getPassTemplate&lt;/ACTION&gt;
    &lt;API_KEY&gt;apiKey&lt;/API_KEY&gt;
    &lt;MMSID&gt;mmsId&lt;/MMSID&gt;
&lt;/REQUEST&gt;</pre>
<pre>&lt;REQUEST&gt;
    &lt;ACTION&gt;getPassTemplate&lt;/ACTION&gt;
    &lt;API_KEY&gt;apiKey&lt;/API_KEY&gt;
    &lt;EMAILID&gt;emailId&lt;/EMAILID&gt;
&lt;/REQUEST&gt;</pre>

<div><strong>Request: GET</strong></div>
<pre>API_URL?action=getpasstemplate&amp;api_key=apiKey&amp;passtemplateid=passTemplateId</pre>
<pre>API_URL?action=getpasstemplate&amp;api_key=apiKey&amp;emailid=emailId</pre>
<pre>API_URL?action=getpasstemplate&amp;api_key=apiKey&amp;mmsid=mmsId</pre>

<div><strong>Request Parameters:</strong></div>
<pre><strong>Mandatory:</strong>
action, apikey, mmsid, emailid, passtemplateid
<strong>Optional:</strong>
--
</pre>
<strong>Response Parameters:</strong><br />
status, Errorcode, Errorinfo, passTemplateId, passTemplate

<strong>Related Errorcodes: </strong><br />
E174, E402, E802, E822, E823, E828, E827
<div><strong>Request Example:</strong></div>
<pre>&lt;REQUEST&gt;
    &lt;ACTION&gt;getPassTemplateIds&lt;/ACTION&gt;
    &lt;API_KEY&gt;qTFkykO9JTfahCOqJ0V2Wf5Cg1t8iWlZ&lt;/API_KEY&gt;
    &lt;PASSTEMPLATEID&gt;234&lt;/PASSTEMPLATEID&gt;
&lt;/REQUEST&gt;</pre>
<div><strong>Response Example: Success</strong></div>
<pre>&lt;RESPONSE&gt;
    &lt;STATUS&gt;Success&lt;/STATUS&gt;
    &lt;PASSTEMPLATEID&gt;1233&lt;/PASSTEMPLATEID&gt;
    &lt;PASSTEMPLATE&gt;
        &lt;PASSNAME&gt;PizzaCoupon-X12&lt;/PASSNAME&gt;
        &lt;PASSTYPE&gt;Coupon&lt;/PASSTYPE&gt;
        &lt;ORGANIZATION&gt;Pizza Den&lt;/ORGANIZATION&gt;
        &lt;DESCRIPTION&gt;$10 off $35 purchase&lt;/DESCRIPTION&gt;
        &lt;BARCODEVALUE&gt;XXXX-XXXX&lt;/BARCODEVALUE&gt;
        &lt;BARCODETEXT&gt;XXXX-XXXX&lt;/BARCODETEXT&gt;
        &lt;HEADERFIELDS&gt;1&lt;/HEADERFIELDS&gt;
        &lt;HEADERLABEL1&gt;&lt;/HEADERLABEL1&gt;
        &lt;HEADERVALUE1&gt;&lt;/HEADERVALUE1&gt;
        &lt;PRIMARYFIELDS&gt;1&lt;/PRIMARYFIELDS&gt;
        &lt;PRIMARYLABEL1&gt;$10 off $35&lt;/PRIMARYLABEL1&gt;
        &lt;PRIMARYVALUE1&gt;(Conditions apply.)&lt;/PRIMARYVALUE1&gt; 
        &lt;SECFIELDS&gt;1&lt;/SECFIELDS&gt;
        &lt;SECLABEL1&gt;Expires&lt;/SECLABEL1&gt;
        &lt;SECVALUE1&gt;July 31, 2013&lt;/SECVALUE1&gt;
        &lt;AUXFIELDS&gt;1&lt;/AUXFIELDS&gt;
        &lt;AUXLABEL1&gt;Terms&lt;/AUXLABEL1&gt;
        &lt;AUXVALUE1&gt;Excludes TX,FL,RI,VT,UT,WA,WI&lt;/AUXVALUE1&gt;
        &lt;BACKFIELDS&gt;1&lt;/BACKFIELDS&gt;
        &lt;BACKLABEL1&gt;Terms and Conditions&lt;/BACKLABEL1&gt;
        &lt;BACKVALUE1&gt;1 coupon valid for one family.&lt;/BACKVALUE1&gt;
    &lt;/PASSTEMPLATE&gt;
&lt;/RESPONSE&gt;</pre>
<div><strong>Response Example: Failure</strong></div>
<pre>&lt;RESPONSE&gt;
    &lt;STATUS&gt;Failure&lt;/STATUS&gt;
    &lt;ERRORCODE&gt;E802&lt;/ERRORCODE&gt;
    &lt;ERRORINFO&gt;Invalid 'PassTemplateID'. Pass template is either deleted or do not belong to this user&lt;/ERRORINFO&gt;
&lt;/RESPONSE&gt;</pre>
