<a href="/1.3/README.md">Back to the Table of Contents</a>&nbsp;&nbsp;|&nbsp;&nbsp;<a href="API_APPENDIX.md">Back to Appendix List</a>
<h2>APPENDIX A</h2>
<div class="text-2"><a id="appendix-b"></a><strong>KEY TERM DEFINITIONS</strong></div>

<table border = "1">

<tr><td width="30%"><b>ACTION</b></td><td>This is the function name you want to execute with the API.</td></tr>
<tr><td><b>API_KEY</b></td><td> Random key assigned to account that can be used for authorization instead of USER/PASS. You can find and regenerate this key on 'API Settigs' page</td></tr>
<tr><td><b>BRANDNAME</b></td><td> The company, brand, or individual that will appear as the sender’s name for campaign.</td></tr>
<tr><td><b>BARCODEID</b></td><td> Value encoded inside barcode sent using 'sendMMSBarcode' function</td></tr>
<tr><td><b>CAMPAIGNID</b></td><td> ID of the campaign to subscribe the user to (integer)</td></tr>
<tr><td><b>CAMPAIGNNAME</b></td><td> Name for new campaign created with createMMSCampaign or createEmailCampaign function</td></tr>
<tr><td><b>CAMPAIGNREF</b></td><td> Depending on your API settings you may be required to subscribe a user first before sending them messages. If you are required to subscribe a user first then a valid Campaign Reference is required. This would be the campaign ID to which the user is subscribed.</td></tr>
<tr><td><b>CTA</b></td><td> mobile owner will be prompted for subscribing/unsubscribing confirmation via SMS. They will be sent a SMS Opt-in request (yes/no)</td></tr>
<tr><td><b>CUSTOMTEXT</b></td><td> Custom text that will overwrite given slide text used in sendSavedMMS function</td></tr>
<tr><td><b>CUSTOMTITLE</b></td><td> Custom Title that will overwrite MMS Subject used in sendSavedMMS function</td></tr>
<tr><td><b>DURATION</b></td><td> Duration of the slide displayed in seconds (integer)</td></tr>
<tr><td><b>DATABASEID</b></td><td> The identification code for Barcode Database(integer)</td></tr>
<tr><td><b>DDMTITLE</b></td><td> Title for DDM message (Device Discover Message) used in sendSavedMMS function</td></tr>
<tr><td><b>DDMTEXT</b></td><td> Text/Body for DDM message (Device Discover Message) used in sendSavedMMS function</td></tr>
<tr><td><b>DDMTIMEOUT</b></td><td>  Timeout (in minutes) for DDM message (Device Discover Message) used in sendSavedMMS function. After this time we send MMS even if there is no DDM result received.</td></tr>
<tr><td><b>END_DATE</b></td><td> End date for sending statisticks used in 'getSendingStatistics' function. The format should be YYYY-MM-DD hh:mm:ss</td></tr>
<tr><td><b>EMAIL</b></td><td> valid email address</td></tr>
<tr><td><b>EMAILID</b></td><td> The identification code for email template</td></tr>
<tr><td><b>FROM</b></td><td> A valid shortcode or longcode for the sender address (string). When sending to a list of many numbers (SendSavedContent) if the FROM value cannot be used for a certain country the system will re-write the sender address to use a valid shortcode for those numbers.</td></tr>
<tr><td><b>HISTORYID</b></td><td> This is permanent refference number used to indentify the SMS/MMS messae sending in our History. HISTORYID is used API reports.</td></tr>
<tr><td><b>MAILINGADDRESS</b></td><td> This is the physical address that will appear in your email footers. You are required to provide your physical address in accordance with the CAN-SPAM act of 2003. Please make sure to include your company name and country in the address.</td></tr>
<tr><td><b>MMSID</b></td><td> The identification code of saved MMS</td></tr>
<tr><td><b>MMSINBOXID</b></td><td> ID of saved MMS to be removed inside removeMMSInboxContent function</td></tr>
<tr><td><b>MOBILE</b></td><td> Phone Number used inside 'subscribe'/'unsubscribe' function</td></tr>
<tr><td><b>NEWUSER</b></td><td> Username for new account created with 'createUser' function</td></tr>
<tr><td><b>NEWPASS</b></td><td> Password for new account created with 'createUser' function</td></tr>
<tr><td><b>NOTIFY</b></td><td> mobile owner will be notified via SMS about being subscribed/unsubscribed. They will be sent confirmation SMS (yes/no)</td></tr>
<tr><td><b>ORIGIN</b></td><td> This identifies the Postback. It can be SMS_MT, MMS_MT or SUB.</td></tr>
<tr><td><b>PASS</b></td><td> Valid, md5() encoded account password</td></tr>
<tr><td><b>SCHEDULEDID</b></td><td> This is refference ID for sending campaign. It is common for every number belonging to that campaign. When campaign sending is processed system will generate postback notifications linking SCHEDULEDID with TRACKINGID and HISTORYID.</td></tr>
<tr><td><b>SEQUENCE</b></td><td> encloses all MMS slide presentation data, encloses one or multiple SLIDEs (up to a max of 8)</td></tr>
<tr><td><b>SLIDE</b></td><td> Represents a single slide within the MMS sequence could include IMAGE/URL/TEXT/PIC etc. (special rules for slides within save MMS special consideration section)</td></tr>
<tr><td><b>SPID</b></td><td> The carrier ID (integer – appendix D)</td></tr>
<tr><td><b>START_DATE</b></td><td> Start date for sending statisticks used in 'getSendingStatistics' function. The format should be YYYY-MM-DD hh:mm:ss</td></tr>
<tr><td><b>TRACKINGID</b></td><td> On success API returns with the tracking ID to identify messages seding, on failures no tracking ID is returned. It is the internal reference number for SMS/MMS sending, it is temporary ID and where possible HISTORYID should be used. Once the message sending is processed you shall receive the postback containing both TRACKINGID and HISTORYID.</td></tr>
<tr><td><b>TRANSACTIONID</b></td><td> The identification that will be encoded into delivered barcode(string)</td></tr>
<tr><td><b>TEXT</b></td><td> SMS message limited to 160 characters (string)</td></tr>
<tr><td><b>TO</b></td><td> the message recipients phone number in international format.</td></tr>
<tr><td><b>TOCAMPAIGN</b></td><td> ID of campaign you want to schedule MMS to using sendSavedMMSCampaign function</td></tr>
<tr><td><b>TZ</b></td><td> Time zone abbreviation associated with the phone number used inside 'subscribe' function</td></tr>
<tr><td><b>USER</b></td><td> Valid account username</td></tr>
<tr><td><b>PASSTEMPLATEID</b></td><td> Valid Pass Template ID (Integer)</td></tr>
<tr><td><b>PASSDATAID</b></td><td> Valid Pass Data Row ID (Integer)</td></tr>
<tr><td><b>PASSDATA</b></td><td>  All the data that goes on the pass (Array)</td></tr>
<tr><td><b>BARCODEVALUE</b></td><td>  Barcode value or Id that will be encoded into the barcode on the pass</td></tr>
<tr><td><b>BARCODETEXT</b></td><td> Barcode text that will be shown below the barcode image on the pass</td></tr>

</table>
