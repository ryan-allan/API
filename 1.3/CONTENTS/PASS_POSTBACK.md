<a href="/1.3/README.md">Back to the Table of Contents</a>
<h2>Passbook&nbsp;Pass&nbsp;Postback</h2>
<div id="page-content"><p><strong>Brief Overview:</strong></p>
<p>This document will provide a technical description of the PASS POSTBACK API. This API allows to send Pass information back to your server.</p>
<p><strong>PASS GENERATION</strong></p>
<p>If pass generate postback API is enabled, then you will receive Postback notification for every pass generated in your account.
All the postbacks are sent as HTTP POST requests on the URL you have used to set it up on Account API settings.</p>
<p><a name="the_xml_bundle1"></a> <strong>The GENERATE PASS XML Bundle:</strong></p>
<p>The XML bundle has the following anatomy:</p>
<p>
&lt;POSTBACK xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:noNamespaceSchemaLocation ="http://www.skycore.com/schema/pass-postback.xsd"&gt;<br />
&lt;ORIGIN&gt;GENERATE_PASS&lt;/ORIGIN&gt;<br />
&lt;STATUSCODE&gt;N801&lt;/STATUSCODE&gt;<br />
&lt;REFERENCEDBY&gt;Email&lt;/REFERENCEDBY&gt;<br/>
&lt;REFERENCEVALUE&gt;vikmut@mail.com&lt;/REFERENCEVALUE&gt;<br/>
&lt;CUSTOMPASSID&gt;ID-123323&lt;/CUSTOMPASSID&gt;<br/>
&lt;PASSDATAID&gt;40556&lt;/PASSDATAID&gt;<br/>
&lt;SERIALNUMBER&gt;5294CE37878AE-112613-113711&lt;/SERIALNUMBER&gt;<br/>
&lt;TIMESTAMP&gt;2013-11-26T11:37:11-05:00&lt;/TIMESTAMP&gt;<br/>
&lt;PASSDATA&gt;<br/>
&lt;BARCODEVALUE&gt;test&lt;/BARCODEVALUE&gt;<br/>
&lt;BARCODETEXT&gt;test&lt;/BARCODETEXT&gt;<br/>
&lt;HEADERLABEL1&gt;Test&lt;/HEADERLABEL1&gt;<br/>
&lt;HEADERVALUE1&gt;Test&lt;/HEADERVALUE1&gt;<br/>
&lt;PRIMARYLABEL1&gt;Test&lt;/PRIMARYLABEL1&gt;<br/>
&lt;PRIMARYVALUE1&gt;Test&lt;/PRIMARYVALUE1&gt;<br/>
&lt;SECLABEL1&gt;Test&lt;/SECLABEL1&gt;<br/>
&lt;SECVALUE1&gt;Test&lt;/SECVALUE1&gt;<br/>
&lt;SECLABEL2&gt;Test&lt;/SECLABEL2&gt;<br/>
&lt;SECVALUE2&gt;Test&lt;/SECVALUE2&gt;<br/>
&lt;SECLABEL3&gt;Test&lt;/SECLABEL3&gt;<br/>
&lt;SECVALUE3&gt;Test&lt;/SECVALUE3&gt;<br/>
&lt;SECLABEL4&gt;Test&lt;/SECLABEL4&gt;<br/>
&lt;SECVALUE4&gt;Test&lt;/SECVALUE4&gt;<br/>
&lt;AUXLABEL1&gt;Test&lt;/AUXLABEL1&gt;<br/>
&lt;AUXVALUE1&gt;Test&lt;/AUXVALUE1&gt;<br/>
&lt;AUXLABEL2&gt;Test&lt;/AUXLABEL2&gt;<br/>
&lt;AUXVALUE2&gt;Test&lt;/AUXVALUE2&gt;<br/>
&lt;AUXLABEL3&gt;Test&lt;/AUXLABEL3&gt;<br/>
&lt;AUXVALUE3&gt;Test&lt;/AUXVALUE3&gt;<br/>
&lt;AUXLABEL4&gt;Test&lt;/AUXLABEL4&gt;<br/>
&lt;AUXVALUE4&gt;Test&lt;/AUXVALUE4&gt;<br/>
&lt;BACKLABEL1&gt;Test&lt;/BACKLABEL1&gt;<br/>
&lt;BACKVALUE1&gt;Test&lt;/BACKVALUE1&gt;<br/>
&lt;BACKLABEL2&gt;Test&lt;/BACKLABEL2&gt;<br/>
&lt;BACKVALUE2&gt;Test&lt;/BACKVALUE2&gt;<br/>
&lt;BACKLABEL3&gt;Test&lt;/BACKLABEL3&gt;<br/>
&lt;BACKVALUE3&gt;Test&lt;/BACKVALUE3&gt;<br/>
&lt;BACKLABEL4&gt;Test&lt;/BACKLABEL4&gt;<br/>
&lt;BACKVALUE4&gt;Test&lt;/BACKVALUE4&gt;<br/>
&lt;RELLATITUDE1&gt;42.35799&lt;/RELLATITUDE1&gt;<br/>
&lt;RELLONGITUDE1&gt;-71.137081&lt;/RELLONGITUDE1&gt;<br/>
&lt;RELTEXT1&gt;Software Developers Association Event&lt;/RELTEXT1&gt;<br/>
&lt;RELLATITUDE2&gt;42.35799&lt;/RELLATITUDE2&gt;<br/>
&lt;RELLONGITUDE2&gt;-71.137081&lt;/RELLONGITUDE2&gt;<br/>
&lt;RELTEXT2&gt;Software Developers Association Event&lt;/RELTEXT2&gt;<br/>
&lt;RELLATITUDE3&gt;42.35799&lt;/RELLATITUDE3&gt;<br/>
&lt;RELLONGITUDE3&gt;-71.137081&lt;/RELLONGITUDE3&gt;<br/>
&lt;RELTEXT3&gt;Software Developers Association Event&lt;/RELTEXT3&gt;<br/>
&lt;RELLATITUDE4&gt;42.35799&lt;/RELLATITUDE4&gt;<br/>
&lt;RELLONGITUDE4&gt;-71.137081&lt;/RELLONGITUDE4&gt;<br/>
&lt;RELTEXT4&gt;Software Developers Association Event&lt;/RELTEXT4&gt;<br/>
&lt;RELLATITUDE5&gt;42.35799&lt;/RELLATITUDE5&gt;<br/>
&lt;RELLONGITUDE5&gt;-71.137081&lt;/RELLONGITUDE5&gt;<br/>
&lt;RELTEXT5&gt;Software Developers Association Event&lt;/RELTEXT5&gt;<br/>
&lt;RELLATITUDE6&gt;42.35799&lt;/RELLATITUDE6&gt;<br/>
&lt;RELLONGITUDE6&gt;-71.137081&lt;/RELLONGITUDE6&gt;<br/>
&lt;RELTEXT6&gt;Software Developers Association Event&lt;/RELTEXT6&gt;<br/>
&lt;RELLATITUDE7&gt;42.35799&lt;/RELLATITUDE7&gt;<br/>
&lt;RELLONGITUDE7&gt;-71.137081&lt;/RELLONGITUDE7&gt;<br/>
&lt;RELTEXT7&gt;Software Developers Association Event&lt;/RELTEXT7&gt;<br/>
&lt;RELLATITUDE8&gt;42.35799&lt;/RELLATITUDE8&gt;<br/>
&lt;RELLONGITUDE8&gt;-71.137081&lt;/RELLONGITUDE8&gt;<br/>
&lt;RELTEXT8&gt;Software Developers Association Event&lt;/RELTEXT8&gt;<br/>
&lt;RELLATITUDE9&gt;42.35799&lt;/RELLATITUDE9&gt;<br/>
&lt;RELLONGITUDE9&gt;-71.137081&lt;/RELLONGITUDE9&gt;<br/>
&lt;RELTEXT9&gt;Software Developers Association Event&lt;/RELTEXT9&gt;<br/>
&lt;RELLATITUDE10&gt;42.35799&lt;/RELLATITUDE10&gt;<br/>
&lt;RELLONGITUDE10&gt;-71.137081&lt;/RELLONGITUDE10&gt;<br/>
&lt;RELTEXT10&gt;Software Developers Association Event&lt;/RELTEXT10&gt;<br/>
&lt;/PASSDATA&gt;
&lt;/POSTBACK&gt;</p>

<p><a name="breaking_down_each_notification"></a> <strong>Breaking down Each Notification</strong></p>
<p>Many of the tags are self-explanatory.</p>
<ul>
<li>&lt;ORIGIN&gt;&lt;/ORIGIN&gt; tags contain the origin type. This explains the type of postback notification.</li>
<li>&lt;STATUSCODE&gt;&lt;/STATUSCODE&gt; tags contain the notification code for success/failure. These codes are explained under <a href="/1.3/CONTENTS/APPENDIX/APPENDIX_B.md">APENDIX B</a></li>
<li>&lt;REFERENCEDBY&gt;&lt;/REFERENCEDBY&gt; tags contains the reference value type that was used to generate this pass i.e., email, phone, etc.</li>
<li>&lt;REFERENCEVALUE&gt;&lt;/REFERENCEVALUE&gt; tags contain a reference value that was used to generate the pass.</li>
<li>&lt;CUSTOMPASSID&gt;&lt;/CUSTOMPASSID&gt; tags contain the custom pass id. This is the optional pass id that is passed when making a Pass generate/Add pass data API request to reference this pass in future requests.</li>
<li>&lt;PASSDATAID&gt;&lt;/PASSDATAID&gt; tags contain the data id which is generated by our system when we create a new pass.</li>
<li>&lt;SERIALNUMBER&gt;&lt;/SERIALNUMBER&gt; tags contain the pass serial number. This is unique number generated for each pass.</li>
<li>&lt;TIMESTAMP&gt;&lt;/TIMESTAMP&gt; tags contain the timestamp when this pass was generated.</li>
<li>&lt;PASSDATA&gt;&lt;/PASSDATA&gt; tags contain the all the data that was on the pass.</li>
</ul>
<p><a name="setting_your_postback_url"></a> <strong>Setting your Postback URL:</strong></p>
<p>You can set your pass postback URL by logging into your account and going to &#8216;Account&#8217; tab and selecting the 
&#8216;API settings&#8217; button. Enter the URL under the setting &#8216;Pass Postback URL&#8217; and make sure that the URL is &#8216;working&#8217;. Also, make sure &#8216;Pass Generate Postback&#8217; setting is ON. Every pass generation triggered will start sending messages to your URL in the XML format shown above.</p>
