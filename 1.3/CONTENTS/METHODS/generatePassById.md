<a href="/1.3/README.md">Back to the Table of Contents</a>&nbsp;&nbsp;|&nbsp;&nbsp;<a href="API_METHODS.md">Back to API Methods</a>
<h2>generatePassById</h2>
<p><strong>Synopsis:</strong><br />
This API function triggers the passbook pass generation for the given 'passDataID'. 'passDataID' is generated whenever pass data is added to the pass database using the addPassData () API request. 
On success, the API returns important values such as 'passDataId', 'serialNumber', 'customPassId', 'passLink' and 'downloadUrl'. All these values need to be stored along with passData on your side which will come in use for making pass updates in the future. More explanation about these values are given below: <br/>
<b>serialNumber</b> - This is the serial number generated for the pass which identifies this pass uniquely. <br/> 
<b>customPassId</b> - This is the Identifier from your system to identify this pass or pass data uniquely. This value will be empty of it was never passed in addPassData() API request i.e., while generate passDataId.<br/> 
<b>passLink</b> - This is the pass installation link which allow users to install or download pass to their phones based on User-Agent detection. <br/> 
<b>downloadUrl</b> - This URL can be used to download PKPass directly to your server. <br/><br/>
For more info see below for Mandatory/Optional fields and Error codes.</p>
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
status, Errorcode, Errorinfo, passDownloadLink

<strong>Related Errorcodes: </strong><br />
E807, E808, E830, E831
    
<div><strong>Request Example:</strong></div>
<pre>&lt;REQUEST&gt;
        &lt;ACTION&gt;generatePassById&lt;/ACTION&gt;
        &lt;API_KEY&gt;qTFkykO9JTfahCOqJ0V2Wf5Cg1t8iWlZ&lt;/API_KEY&gt;
        &lt;PASSDATAID&gt;63202e8e947626dae377ab2463ca31dhwtdjdien&lt;/PASSDATAID&gt;
    &lt;/REQUEST&gt;</pre>
<div><strong>Response Example: Success</strong></div>
<pre>&lt;RESPONSE&gt;
        &lt;STATUS&gt;Success&lt;/STATUS&gt;
        &lt;PASSDATAID&gt;63202e8e947626dae377ab2463ca31dhwtdjdien&lt;/PASSDATAID&gt;
        &lt;SERIALNUMBER&gt;KJSD3432-232232-2323N32&lt;/SERIALNUMBER&gt;
        &lt;CUSTOMPASSID&gt;CONT-ID-SKU:112324&lt;/CUSTOMPASSID&gt;
        &lt;PASSLINK&gt;https://d2c.skycore.com/passes/downloadpass.php?pass=4jfjhsus&lt;/PASSLINK&gt;
        &lt;DOWNLOADURL&gt;https://d2c.skycore.com/passes/downloadpass.php?pass=4jfjhsus&amp;download=1&lt;/DOWNLOADURL&gt;
&lt;/RESPONSE&gt;</pre>
<div><strong>Response Example: Failure</strong></div>
<pre>&lt;RESPONSE&gt;
    &lt;STATUS&gt;Failure&lt;/STATUS&gt;
    &lt;ERRORCODE&gt;E830&lt;/ERRORCODE&gt;
    &lt;ERRORINFO&gt;Passbook Pass was not generated. Internal error occured.&lt;/ERRORINFO&gt;
&lt;/RESPONSE&gt;</pre>
