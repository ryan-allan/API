<a href="/1.3/README.md">Back to the Table of Contents</a>&nbsp;&nbsp;|&nbsp;&nbsp;<a href="API_APPENDIX.md">Back to Appendix List</a>
<h2>APPENDIX A</h2>
<div class="text-2"><a id="appendix-b"></a><strong>KEY TERM DEFINITIONS</strong></div>

<table border = "1">

<tr><td width="30%"><b>ACTION</b></td><td> This is the name of the function you want to execute with the API.</td></tr>
<tr><td><b>API_KEY</b></td><td> Random key that is assigned to an account that can be used for authorization instead of USER/PASS. You can find and regenerate this key on the 'API Settings' page.</td></tr>
<tr><td><b>BARCODEID</b></td><td> The alphanumeric value that is encoded inside a barcode that was sent using the 'sendMMSBarcode' function.</td></tr>
<tr><td><b>BARCODEVALUE</b></td><td> The barcode value or Id that will be encoded into the barcode image on the pass.</td></tr>
<tr><td><b>BARCODETEXT</b></td><td> Added text that will be shown below the barcode image on the pass.</td></tr>
<tr><td><b>BRANDNAME</b></td><td> The company, brand, or individual that will appear as the sender’s name for the campaign.</td></tr>
<tr><td><b>CAMPAIGNID</b></td><td> The ID(integer) of the campaign to which the user will be subscribed.</td></tr>
<tr><td><b>CAMPAIGNNAME</b></td><td> The name for a new campaign created with either the createMMSCampaign or createEmailCampaign function</td></tr>
<tr><td><b>CAMPAIGNREF</b></td><td> Depending on your API settings, you may be required to subscribe a user first before sending them messages. If you are required to subscribe a user first, then a valid Campaign Reference is required. This would be the campaign ID(integer) to which the user is subscribed.</td></tr>
<tr><td><b>CTA</b></td><td> This will prompt a mobile owner with a subscribe/unsubscribe confirmation via SMS Opt-in request (yes/no).</td></tr>
<tr><td><b>CUSTOMTEXT</b></td><td> This is custom text that will overwrite a given slide text used in a sendSavedMMS function call.</td></tr>
<tr><td><b>CUSTOMTITLE</b></td><td> This is a custom title that will overwrite the MMS Subject used in a sendSavedMMS function call.</td></tr>
<tr><td><b>DURATION</b></td><td> The duration of a slide displayed in seconds (integer).</td></tr>
<tr><td><b>DATABASEID</b></td><td> The identification code for a Barcode Database(integer).</td></tr>
<tr><td><b>DDMTITLE</b></td><td> Title for a DDM message (Device Discovery Message) used in the sendSavedMMS function.</td></tr>
<tr><td><b>DDMTEXT</b></td><td> Text/Body for DDM message (Device Discovery Message) used in the sendSavedMMS function.</td></tr>
<tr><td><b>DDMTIMEOUT</b></td><td>  The time(in minutes) for a DDM message (Device Discovery Message) used in the 'sendSavedMMS' function. After this time expires, we send an MMS even if there is not a DDM result received.</td></tr>
<tr><td><b>EMAIL</b></td><td> A valid email address.</td></tr>
<tr><td><b>EMAILID</b></td><td> The ID(integer) for an email template.</td></tr>
<tr><td><b>END_DATE</b></td><td> The end date of the sending statistics used in the 'getSendingStatistics' function. The format should be "YYYY-MM-DD hh:mm:ss" (ignoring quotations).</td></tr>
<tr><td><b>FROM</b></td><td> A valid shortcode or longcode for the sender address(string). When sending to a list of many numbers using the 'sendSavedContent' function and if the 'FROM' value cannot be used for a certain country, then the system will re-write the sender address to use a valid shortcode for those numbers.</td></tr>
<tr><td><b>HISTORYID</b></td><td> This is a permanent reference number used to indentify the SMS/MMS message sending in our History. The 'HISTORYID' is used in the API reports.</td></tr>
<tr><td><b>MAILINGADDRESS</b></td><td> This is the physical address that will appear in your email footers. You are required to provide your physical address in accordance with the "CAN-SPAM Act of 2003". Please make sure to include your company name and country in the address.</td></tr>
<tr><td><b>MMSID</b></td><td> The ID(integer) of a saved MMS.</td></tr>
<tr><td><b>MMSINBOXID</b></td><td> The ID(integer) of a saved MMS to be removed inside the 'removeMMSInboxContent' function.</td></tr>
<tr><td><b>MOBILE</b></td><td> A Phone Number used inside the 'subscribe'/'unsubscribe' function.</td></tr>
<tr><td><b>NEWPASS</b></td><td> A Password for a new account created with the 'createUser' function.</td></tr>
<tr><td><b>NEWUSER</b></td><td> A Username for a new account created with the 'createUser' function.</td></tr>
<tr><td><b>NOTIFY</b></td><td> A mobile owner will be notified about being subscribed/unsubscribed via a confirmation SMS (yes/no).</td></tr>
<tr><td><b>ORIGIN</b></td><td> This identifies the Postback. It can be SMS_MT, MMS_MT or SUB.</td></tr>
<tr><td><b>PASS</b></td><td> A valid, md5() encoded account password.</td></tr>
<tr><td><b>PASSDATA</b></td><td>  All the data that goes on the pass(Array).</td></tr>
<tr><td><b>PASSDATAID</b></td><td> A valid Pass Data Row ID(integer).</td></tr>
<tr><td><b>PASSTEMPLATEID</b></td><td> Valid Pass Template ID(integer).</td></tr>
<tr><td><b>SCHEDULEDID</b></td><td> This is a reference ID(integer) for a sending campaign. It is used for every number belonging to that campaign. When campaign sending is processed, the system will generate postback notifications linking SCHEDULEDID with TRACKINGID and HISTORYID.</td></tr>
<tr><td><b>SEQUENCE</b></td><td> This encloses all MMS slide presentation data from one or multiple slides (up to a maximum of 8).</td></tr>
<tr><td><b>SLIDE</b></td><td> This represents a single slide within the MMS sequence the could include IMAGE/URL/TEXT/PIC etc. (There are special rules for slides within the 'saveMMS' special consideration section).</td></tr>
<tr><td><b>SPID</b></td><td> The carrier ID(integer). See <a href="/1.3/CONTENTS/APPENDIX/APPENDIX_E.md">Appendix E</a>.</td></tr>
<tr><td><b>START_DATE</b></td><td> The start date for sending statistics used in the 'getSendingStatistics' function. The format should be "YYYY-MM-DD hh:mm:ss" (ignoring quotations).</td></tr>
<tr><td><b>TEXT</b></td><td> SMS message limited to 160 characters (string).</td></tr>
<tr><td><b>TO</b></td><td> This is the message recipient's phone number in an international format.</td></tr>
<tr><td><b>TOCAMPAIGN</b></td><td> The ID(integer) of a campaign for which you want to schedule an MMS using the 'sendSavedMMSCampaign' function.</td></tr>
<tr><td><b>TRACKINGID</b></td><td> On success, the API returns with the tracking ID(integer) to identify sent messages.  On failure, no tracking ID is returned. This is the internal reference number for SMS/MMS sending, it is a temporary ID and (where possible) HISTORYID should be used. Once the message sending is processed you shall receive a postback containing both TRACKINGID and HISTORYID.</td></tr>
<tr><td><b>TRANSACTIONID</b></td><td> The ID(integer) that will be encoded into a delivered barcode(string).</td></tr>
<tr><td><b>TIMEZONE</b></td><td> A time zone abbreviation associated with the phone number used inside the 'subscribe' function.</td></tr>
<tr><td><b>USER</b></td><td> A valid account username.</td></tr>

</table>

