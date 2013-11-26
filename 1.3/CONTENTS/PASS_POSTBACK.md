<a href="/1.3/README.md">Back to the Table of Contents</a>
<h2>Passes&nbsp;Postback</h2>
<div id="page-content"><p><strong>Brief Overview:</strong></p>
<p>This document will provide a technical description of the PASS POSTBACK API. 
This API allows to send Pass information back to your server whenever pass generation is triggered.</p>
<p><strong>PASS GENERATION</strong></p>
<p>If pass generate postback API is enabled, then you will receive Postback notification for every pass generated in your account.
All the postbacks are sent as HTTP POST requests on the URL you have used to set it up on Account API settings.</p>
<p><a name="the_xml_bundle1"></a> <strong>The GENERATE PASS XML Bundle:</strong></p>
<p>The XML bundle has the following anatomy:</p>
<pre>
&lt;POSTBACK xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:noNamespaceSchemaLocation ="http://www.skycore.com/schema/pass-postback.xsd"&gt;
    &lt;ORIGIN&gt;GENERATE_PASS&lt;/ORIGIN&gt;
    &lt;STATUSCODE&gt;N801&lt;/STATUSCODE&gt;
    &lt;REFERENCEDBY&gt;Email&lt;/REFERENCEDBY&gt;
    &lt;REFERENCEVALUE&gt;vikmut@mail.com&lt;/REFERENCEVALUE&gt;
    &lt;CUSTOMPASSID&gt;ID-123323&lt;/CUSTOMPASSID&gt;
    &lt;PASSDATAID&gt;40556&lt;/PASSDATAID&gt;
    &lt;SERIALNUMBER&gt;5294CE37878AE-112613-113711&lt;/SERIALNUMBER&gt;
    &lt;TIMESTAMP&gt;2013-11-26T11:37:11-05:00&lt;/TIMESTAMP&gt;
    &lt;PASSDATA&gt;
        &lt;BARCODEVALUE&gt;XSSDEW2223&lt;/BARCODEVALUE&gt;
        &lt;BARCODETEXT&gt;XSSDEW2223&lt;/BARCODETEXT&gt;
        &lt;HEADERLABEL1&gt;Name&lt;/HEADERLABEL1&gt;
        &lt;HEADERVALUE1&gt;John&lt;/HEADERVALUE1&gt;
        &lt;PRIMARYLABEL1&gt;Occupation&lt;/PRIMARYLABEL1&gt;
        &lt;PRIMARYVALUE1&gt;Software Developer&lt;/PRIMARYVALUE1&gt;
        &lt;SECLABEL1&gt;Salary&lt;/SECLABEL1&gt;
        &lt;SECVALUE1&gt;$120,000.00&lt;/SECVALUE1&gt;
        &lt;SECLABEL2&gt;Experience&lt;/SECLABEL2&gt;
        &lt;SECVALUE2&gt;5+ Years&lt;/SECVALUE2&gt;
        &lt;SECLABEL3&gt;XXXXX&lt;/SECLABEL3&gt;
        &lt;SECVALUE3&gt;XXXXX&lt;/SECVALUE3&gt;
        &lt;SECLABEL4&gt;XXXXX&lt;/SECLABEL4&gt;
        &lt;SECVALUE4&gt;XXXXX&lt;/SECVALUE4&gt;
        &lt;AUXLABEL1&gt;XXXXX&lt;/AUXLABEL1&gt;
        &lt;AUXVALUE1&gt;Company&lt;/AUXVALUE1&gt;
        &lt;AUXLABEL2&gt;Sky Technologies Ltd.&lt;/AUXLABEL2&gt;
        &lt;AUXVALUE2&gt;111 Technology Dr, Boston MA 02111&lt;/AUXVALUE2&gt;
        &lt;AUXLABEL3&gt;XXXXX&lt;/AUXLABEL3&gt;
        &lt;AUXVALUE3&gt;XXXXX&lt;/AUXVALUE3&gt;
        &lt;AUXLABEL4&gt;XXXXX&lt;/AUXLABEL4&gt;
        &lt;AUXVALUE4&gt;XXXXX&lt;/AUXVALUE4&gt;
        &lt;BACKLABEL1&gt;Terms and Conditions&lt;/BACKLABEL1&gt;
        &lt;BACKVALUE1&gt;Please show this pass at the event entrance to get in.&lt;/BACKVALUE1&gt;
        &lt;BACKLABEL2&gt;XXXXX&lt;/BACKLABEL2&gt;
        &lt;BACKVALUE2&gt;XXXXX&lt;/BACKVALUE2&gt;
        &lt;BACKLABEL3&gt;XXXXX&lt;/BACKLABEL3&gt;
        &lt;BACKVALUE3&gt;XXXXX&lt;/BACKVALUE3&gt;
        &lt;BACKLABEL4&gt;XXXXX&lt;/BACKLABEL4&gt;
        &lt;BACKVALUE4&gt;XXXXX&lt;/BACKVALUE4&gt;
        &lt;RELLATITUDE1&gt;42.35799&lt;/RELLATITUDE1&gt;
        &lt;RELLONGITUDE1&gt;-71.137081&lt;/RELLONGITUDE1&gt;
        &lt;RELTEXT1&gt;Software Developers Association Event&lt;/RELTEXT1&gt;
        &lt;RELLATITUDE2&gt;42.35799&lt;/RELLATITUDE2&gt;
        &lt;RELLONGITUDE2&gt;-71.137081&lt;/RELLONGITUDE2&gt;
        &lt;RELTEXT2&gt;Software Developers Association Event&lt;/RELTEXT2&gt;
        &lt;RELLATITUDE3&gt;42.35799&lt;/RELLATITUDE3&gt;
        &lt;RELLONGITUDE3&gt;-71.137081&lt;/RELLONGITUDE3&gt;
        &lt;RELTEXT3&gt;Software Developers Association Event&lt;/RELTEXT3&gt;
        &lt;RELLATITUDE4&gt;42.35799&lt;/RELLATITUDE4&gt;
        &lt;RELLONGITUDE4&gt;-71.137081&lt;/RELLONGITUDE4&gt;
        &lt;RELTEXT4&gt;Software Developers Association Event&lt;/RELTEXT4&gt;
        &lt;RELLATITUDE5&gt;42.35799&lt;/RELLATITUDE5&gt;
        &lt;RELLONGITUDE5&gt;-71.137081&lt;/RELLONGITUDE5&gt;
        &lt;RELTEXT5&gt;Software Developers Association Event&lt;/RELTEXT5&gt;
        &lt;RELLATITUDE6&gt;42.35799&lt;/RELLATITUDE6&gt;
        &lt;RELLONGITUDE6&gt;-71.137081&lt;/RELLONGITUDE6&gt;
        &lt;RELTEXT6&gt;Software Developers Association Event&lt;/RELTEXT6&gt;
        &lt;RELLATITUDE7&gt;42.35799&lt;/RELLATITUDE7&gt;
        &lt;RELLONGITUDE7&gt;-71.137081&lt;/RELLONGITUDE7&gt;
        &lt;RELTEXT7&gt;Software Developers Association Event&lt;/RELTEXT7&gt;
        &lt;RELLATITUDE8&gt;42.35799&lt;/RELLATITUDE8&gt;
        &lt;RELLONGITUDE8&gt;-71.137081&lt;/RELLONGITUDE8&gt;
        &lt;RELTEXT8&gt;Software Developers Association Event&lt;/RELTEXT8&gt;
        &lt;RELLATITUDE9&gt;42.35799&lt;/RELLATITUDE9&gt;
        &lt;RELLONGITUDE9&gt;-71.137081&lt;/RELLONGITUDE9&gt;
        &lt;RELTEXT9&gt;Software Developers Association Event&lt;/RELTEXT9&gt;
        &lt;RELLATITUDE10&gt;42.35799&lt;/RELLATITUDE10&gt;
        &lt;RELLONGITUDE10&gt;-71.137081&lt;/RELLONGITUDE10&gt;
        &lt;RELTEXT10&gt;Software Developers Association Event&lt;/RELTEXT10&gt;
    &lt;/PASSDATA&gt;
&lt;/POSTBACK&gt;</pre>

<p><a name="breaking_down_each_notification"></a> <strong>Breaking down Each Notification</strong></p>
<p>Many of the tags are self-explanatory.</p>
<pre>
&lt;ORIGIN&gt;&lt;/ORIGIN&gt; tags contain the origin type. This explains the type of postback notification.
&lt;STATUSCODE&gt;&lt;/STATUSCODE&gt; tags contain the notification code for success/failure. These codes are explained under <a href="/1.3/CONTENTS/APPENDIX/APPENDIX_B.md">APENDIX B</a>
&lt;REFERENCEDBY&gt;&lt;/REFERENCEDBY&gt; tags contains the reference value type that was used to generate this pass i.e., email, phone, etc.
&lt;REFERENCEVALUE&gt;&lt;/REFERENCEVALUE&gt; tags contain a reference value that was used to generate the pass.
&lt;CUSTOMPASSID&gt;&lt;/CUSTOMPASSID&gt; tags contain the custom pass id. This is the optional pass id that is passed when making a Pass generate/Add pass data API request to reference this pass in future requests.
&lt;PASSDATAID&gt;&lt;/PASSDATAID&gt; tags contain the data id which is generated by our system when we create a new pass.
&lt;SERIALNUMBER&gt;&lt;/SERIALNUMBER&gt; tags contain the pass serial number. This is unique number generated for each pass.
&lt;TIMESTAMP&gt;&lt;/TIMESTAMP&gt; tags contain the timestamp when this pass was generated.
&lt;PASSDATA&gt;&lt;/PASSDATA&gt; tags contain the all the data that was on the pass.
</pre>
<p><a name="setting_your_postback_url"></a> <strong>Setting your Postback URL:</strong></p>
<p>You can set your pass postback URL by logging into your account and going to &#8216;Account&#8217; tab and selecting the 
&#8216;API settings&#8217; button. Enter the URL under the setting &#8216;Pass Postback URL&#8217; and make sure that the URL is &#8216;working&#8217;. Also, make sure &#8216;Pass Generate Postback&#8217; setting is ON. Every pass generation triggered will start sending messages to your URL in the XML format shown above.</p>
