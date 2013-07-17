<a href="/1.3/README.md">BACK TO TABLE OF CONTENTS</a>
<BR>
<a href="API_METHODS.md">BACK TO API FUNCTIONS</a>
<BR>
<BR>

<h1>updatePass()</h1>
<BR>

<p><strong>Synopsis:</strong><br />
This API function updates a pass with the data supplied in the API. This will also trigger the updates to the pass that was installed on the device.</p>
<div><strong>Request: XML</strong></div>
<pre>&lt;REQUEST&gt;
    &lt;ACTION&gt;updatePass&lt;/ACTION&gt;
    &lt;API_KEY&gt;apiKey&lt;/API_KEY&gt;
    &lt;PASSDATAID&gt;passDataID&lt;/PASSDATAID&gt;
    &lt;PASSDATA&gt;
        &lt;BARCODEVALUE&gt;barcodeValue&lt;/BARCODEVALUE&gt;
        &lt;BARCODETEXT&gt;barcodeText&lt;/BARCODETEXT&gt;
        &lt;HEADERLABEL1&gt;headerLabel1&lt;/HEADERLABEL1&gt;
        &lt;HEADERVALUE1&gt;headerValue1&lt;/HEADERVALUE1&gt;
        &lt;PRIMARYLABEL1&gt;primaryLabel1&lt;/PRIMARYLABEL1&gt;
        &lt;PRIMARYVALUE1&gt;primaryValue1&lt;/PRIMARYVALUE1&gt; 
        &lt;PRIMARYLABEL2&gt;primaryLabel2&lt;/PRIMARYLABEL2&gt;
        &lt;PRIMARYVALUE2&gt;primaryValue2&lt;/PRIMARYVALUE2&gt; 
        &lt;SECLABEL1&gt;secLabel1&lt;/SECLABEL1&gt;
        &lt;SECVALUE1&gt;secValue1&lt;/SECVALUE1&gt;
        &lt;SECLABEL2&gt;sedLabel2&lt;/SECLABEL2&gt;
        &lt;SECVALUE2&gt;secValue2&lt;/SECVALUE2&gt;
        &lt;SECLABEL3&gt;sedLabel3&lt;/SECLABEL3&gt;
        &lt;SECVALUE3&gt;secValue3&lt;/SECVALUE3&gt;
        &lt;SECLABEL4&gt;sedLabel4&lt;/SECLABEL4&gt;
        &lt;SECVALUE4&gt;secValue4&lt;/SECVALUE4&gt;
        &lt;AUXLABEL1&gt;auxLabel1&lt;/AUXLABEL1&gt;
        &lt;AUXVALUE1&gt;auxValue1&lt;/AUXVALUE1&gt;
        &lt;AUXLABEL2&gt;auxLabel2&lt;/AUXLABEL2&gt;
        &lt;AUXVALUE2&gt;auxValue2&lt;/AUXVALUE2&gt;
        &lt;AUXLABEL3&gt;auxLabel3&lt;/AUXLABEL3&gt;
        &lt;AUXVALUE3&gt;auxValue3&lt;/AUXVALUE3&gt;
        &lt;AUXLABEL4&gt;auxLabel4&lt;/AUXLABEL4&gt;
        &lt;AUXVALUE4&gt;auxValue4&lt;/AUXVALUE4&gt;
        &lt;BACKLABEL1&gt;backLabel1&lt;/BACKLABEL1&gt;
        &lt;BACKVALUE1&gt;backValue1&lt;/BACKVALUE1&gt;
        &lt;BACKLABEL2&gt;backLabel2&lt;/BACKLABEL2&gt;
        &lt;BACKVALUE2&gt;backValue2&lt;/BACKVALUE2&gt;
        &lt;BACKLABEL3&gt;backLabel3&lt;/BACKLABEL3&gt;
        &lt;BACKVALUE3&gt;backValue3&lt;/BACKVALUE3&gt;
        &lt;BACKLABEL4&gt;backLabel4&lt;/BACKLABEL4&gt;
        &lt;BACKVALUE4&gt;backValue4&lt;/BACKVALUE4&gt;
    &lt;/PASSDATA&gt;    
&lt;/REQUEST&gt;</pre>
<div><strong>Request: GET</strong></div>
<pre>API_URL?action=updatepass&amp;api_key=apiKey&amp;passtemplateid=PassTemplateID
&amp;pd_barcodevalue=barcodeValue&amp;pd_barcodetext=barcodeText
&amp;pd_headerlabel1=headerLabel1&amp;pd_headervalue1=headerValue1
&amp;pd_primarylabel1=primaryLabel1&amp;pd_primaryvalue1=primaryValue1
&amp;pd_primarylabel2=primaryLabel2&amp;pd_primaryvalue2=primaryValue2
&amp;pd_seclabel1=secLabel1&amp;pd_secvalue1=secValue1&amp;pd_seclabel2=secLabel2
&amp;pd_secvalue2=secValue2&amp;pd_seclabel3=secLabel3&amp;pd_secvalue3=secValue3
&amp;pd_seclabel4=secLabel4&amp;pd_secvalue4=secValue4&amp;pd_auxlabel1=auxLabel1
&amp;pd_auxvalue1=auxValue1&amp;pd_auxlabel2=auxLabel2&amp;pd_auxvalue2=auxValue2
&amp;pd_auxlabel3=auxLabel3&amp;pd_auxvalue3=auxValue3&amp;pd_auxlabel4=auxLabel4
&amp;pd_auxvalue4=auxValue4&amp;pd_backlabel1=backLabel1&amp;pd_backvalue1=backValue1
&amp;pd_backlabel2=backLabel2&amp;pd_backvalue2=backValue2&amp;pd_backlabel3=backLabel3
&amp;pd_backvalue3=backValue3&amp;pd_backlabel4=backLabel4&amp;pd_backvalue4=backValue4
</pre>
<div><strong>Request Parameters:</strong></div>
<pre><strong>Mandatory:</strong> 
action, apiKey, passDataID
<strong>Optional: </strong>
barcodeValue ( if "Barcode = Allowed" &amp;&amp; "Barcode Type = Dynamic" &amp;&amp; "Barcode Value Source = API" for Pass Template otherwise IGNORED ), 
barcodeText (if "Barcode = Allowed" &amp;&amp; "Barcode Alternate Text = API" for Pass Template otherwise IGNORED), hLabel1, hString1, pLabel1, pString1,
pLabel2, pString2 - if "Pass Template Type = Boarding Pass" otherwise IGNORED, 
sLabel1, sString1, sLabel2, sString2, sLabel3, sString3, sLabel4, sString4, 
aLabel1, aString1, aLabel2, aString2, aLabel3, aString3, aLabel4, aString4, 
bLabel1, bString1, bLabel2, bString2, bLabel3, bString3, bLabel4, bString4</pre>

<strong>Response Parameters:</strong><br />

    status, passDataId, updateStatusID, Errorcode, Errorinfo

<strong>Related Errorcodes: </strong><br />

    E802, E803, E807, E808, E809, E810, E811, E812, E813, E814, E815, E816, E817, E818, E819, E820

<div><strong>Request Example:</strong></div>
<pre>&lt;REQUEST&gt;
    &lt;ACTION&gt;updatePass&lt;/ACTION&gt;
    &lt;API_KEY&gt;qTFkykO9JTfahCOqJ0V2Wf5Cg1t8iWlZ&lt;/API_KEY&gt;
    &lt;PASSDATAID&gt;1233&lt;/PASSDATAID&gt;
    &lt;PASSDATA&gt;
        &lt;BARCODEVALUE&gt;3434578961A&lt;/BARCODEVALUE&gt;
        &lt;BARCODETEXT&gt;PASS-343-457&lt;/BARCODETEXT&gt;
        &lt;HEADERLABEL1&gt;SEAT&lt;/HEADERLABEL1&gt;
        &lt;HEADERVALUE1&gt;100C&lt;/HEADERVALUE1&gt;
        &lt;SECLABEL1&gt;Date&lt;/SECLABEL1&gt;
        &lt;SECVALUE1&gt;3rd July, 2013&lt;/SECVALUE1&gt;
        &lt;BACKVALUE4&gt;Important - Change&lt;/BACKVALUE4&gt;
        &lt;BACKVALUE4&gt;New ticket issued. Schedule preponed by one day.&lt;/BACKVALUE4&gt;
    &lt;/PASSDATA&gt;    
&lt;/REQUEST&gt;</pre>
<div><strong>Response Example: Success</strong></div>
<pre>&lt;RESPONSE&gt;
    &lt;STATUS&gt;Success&lt;/STATUS&gt;
    &lt;PASSDATAID&gt;1233&lt;/PASSDATAID&gt;
    &lt;UPDATESTATUSID&gt;1007&lt;/UPDATESTATUSID&gt;
&lt;/RESPONSE&gt;</pre>
<div><strong>Response Example: Failure</strong></div>
<pre>&lt;RESPONSE&gt;
    &lt;STATUS&gt;Failure&lt;/STATUS&gt;
    &lt;ERRORCODE&gt;E809&lt;/ERRORCODE&gt;
    &lt;ERRORINFO&gt;Pass was not updated. Internal error occured.&lt;/ERRORINFO&gt;
&lt;/RESPONSE&gt;</pre>
