<a href="/1.3/README.md">Back to the Table of Contents</a>&nbsp;&nbsp;|&nbsp;&nbsp;<a href="API_METHODS.md">Back to API Methods</a>
<h2>createEmailCampaign</h2>
<p><strong>Synopsis:</strong><br />
This API function creates new email campaign within the account holders account and returns a CampaignID. 
Campaign will be created under <i>campaignname</i> in our system. <i>Campaignname</i> will be sent to users in opt-in/opt-out emails. 
<i>Brandname</i> will be used in 'from' field of all sent emails. 
<i>Mailingadress</i> will be inserted into email footer.
<div><strong>Request:</strong></div>
<pre>&lt;REQUEST&gt;
  &lt;ACTION&gt;createEmailCampaign&lt;/ACTION&gt;
	&lt;API_KEY&gt;API KEY&lt;/API_KEY&gt;
	&lt;CAMPAIGNNAME&gt;Camapign Name&lt;/CAMPAIGNNAME&gt;
	&lt;BRANDNAME&gt;Brand name&lt;/BRANDNAME&gt;
        &lt;MAILINGADDRESS&gt;Mailing Address&lt;/MAILINGADDRESS&gt;
&lt;/REQUEST&gt;</pre>
<div><strong>Request Parameters:</strong></div>
<pre><strong>Mandatory:</strong> Action, API_KEY, CampaignName, BrandName, MailingAddress</pre>
<strong>Response Parameters:</strong><br />
CampaignID, CampaignName, BrandName, MailingAddress, ErrorInfo, Errorcode
<strong>Related Error codes:</strong><br />
E170, E171, E172, E173    
<div><strong>Request Examples</strong></div>
XML:
<pre>&lt;REQUEST&gt;
	&lt;ACTION&gt;createEmailCampaign&lt;/ACTION&gt;
	&lt;API_KEY&gt;qTFkykO9JTfahCOqJ0V2Wf5Cg1t8iWlZ&lt;/API_KEY&gt;
	&lt;CAMPAIGNNAME&gt;Winter Sale&lt;/CAMPAIGNNAME&gt;
	&lt;BRANDNAME&gt;Codereadr&lt;/BRANDNAME&gt;
        &lt;MAILINGADDRESS&gt;Skycore, LLC 
            214 Lincoln Street, Suite 360
            Allston, MA 02134&lt;/MAILINGADDRESS&gt;
&lt;/REQUEST&gt;</pre>
GET:
<pre>https://secure.skycore.com/API/wxml/1.3/index.php?action=createemailcampaign&api_key=qTFkykO9JTfahCOqJ0V2Wf5Cg1t8iWlZ
&campaignname=Winter+Sale&brandname=Codereadr
&mailingaddress=Skycore%2C+LLC%0A214+Lincoln+Street%2C+Suite+360%0AAllston%2C+MA+02134</pre>
<div><strong>Response Example: Success</strong></div>
<pre>&lt;RESPONSE&gt;
	&lt;STATUS&gt;Success&lt;/STATUS&gt;
	&lt;CAMPAIGNID&gt;1116&lt;/CAMPAIGNID&gt;
	&lt;CAMPAIGNNAME&gt;Winter Sale&lt;/CAMPAIGNNAME&gt;
 	&lt;BRANDNAME&gt;Codereadr&lt;/BRANDNAME&gt;
        &lt;MAILINGADDRESS&gt;Skycore, LLC 
            214 Lincoln Street, Suite 360
            Allston, MA 02134&lt;/MAILINGADDRESS&gt;
        &lt;/RESPONSE&gt;</pre>
<div><strong>Response Example: Failure</strong></div>
<pre>&lt;RESPONSE&gt;
	&lt;STATUS&gt;Failure&lt;/STATUS&gt;
	&lt;ERRORCODE&gt;E173&lt;/ERRORCODE&gt;
	&lt;ERRORINFO&gt;mailingaddress is required&lt;/ERRORINFO&gt;
&lt;/RESPONSE&gt;</pre>
