<b>Appendix A Parameters</b>

<BR>
<BR>

<b>BRANDNAME –</b> The company, brand, or individual that will appear as the sender’s name for campaign.
<BR>
<b>CAMPAIGNID -</b> ID of the campaign to subscribe the user to (integer)
<BR>
<b>CAMPAIGNREF –</b> Depending on your API settings you may be required to subscribe a user first before sending them messages. If you are required to subscribe a user first then a valid Campaign Reference is required. This would be the campaign ID to which the user is subscribed.
<BR>
<b>CTA – </b> mobile owner will be prompted for subscribing/unsubscribing confirmation via SMS. They will be sent a SMS Opt-in request (yes/no)
<BR>
<b>DURATION –</b> Duration of the slide displayed in seconds (integer)
<BR>
<b>DATABASEID –</b> The identification code for Barcode Database(integer)
<BR>
<b>ENDDATE -</b> The format should be YYYY-MM-DD hh:mm:ss
<BR>
<b>EMAIL –</b> valid email address
<BR>
<b>EMAILID –</b> The identification code for email template
<BR>
<b>FROM –</b> A valid shortcode or longcode for the sender address (string). When sending to a list of many numbers (SendSavedContent) if the FROM value cannot be used for a certain country the system will re-write the sender address to use a valid shortcode for those numbers.
<BR>
<b>HISTORYID –</b> This is permanent refference number used to indentify the SMS/MMS messae sending in our History. HISTORYID is used API reports.
<BR>
<b>MAILINGADDRESS -</b> This is the physical address that will appear in your email footers. You are required to provide your physical address in accordance with the CAN-SPAM act of 2003. Please make sure to include your company name and country in the address.
<BR>
<b>MMSID -</b> The identification code of saved MMS
<BR>
<b>NOTIFY –</b> mobile owner will be notified via SMS about being subscribed/unsubscribed. They will be sent confirmation SMS (yes/no)
<BR>
<b>ORIGIN –</b> This identifies the Postback. It can be SMS_MT, MMS_MT or SUB.
<BR>
<b>PASSWORD -</b> Valid account password (32 hexadecimal hashed password)
<BR>
<b>SCHEDULEDID –</b> This is refference ID for sending campaign. It is common for every number belonging to that campaign. When campaign sending is processed system will generate postback notifications linking SCHEDULEDID with TRACKINGID and HISTORYID.
<BR>
<b>SEQUENCE -</b> encloses all MMS slide presentation data, encloses one or multiple SLIDEs (up to a max of 8)
<BR>
<b>SLIDE -</b> Represents a single slide within the MMS sequence could include IMAGE/URL/TEXT/PIC etc. (special rules for slides within save MMS special consideration section)
<BR>
<b>SPID –</b> The carrier ID (integer – appendix D)
<BR>
<b>STARTDATE –</b> The format should be YYYY-MM-DD hh:mm:ss
<BR>
<b>TRACKINGID –</b> On success API returns with the tracking ID to identify messages seding, on failures no tracking ID is returned. It is the internal reference number for SMS/MMS sending, it is temporary ID and where possible HISTORYID should be used. Once the message sending is processed you shall receive the postback containing both TRACKINGID and HISTORYID.
<BR>
<b>TRANSACTIONID –</b> The identification that will be encoded into delivered barcode(string)
<BR>
<b>TEXT –</b> SMS message limited to 160 characters (string)
<BR>
<b>TO –</b> the message recipients phone number in international format.
<BR>
<b>USER -</b> Valid account username
<BR>
<b>PASSTEMPLATEID -</b> Valid Pass Template ID (Integer)
<BR>
<b>PASSDATAID -</b> Valid Pass Data Row ID (Integer)
<BR>
<b>PASSDATA -</b> All the data that goes on the pass (Array)
<BR>
<b>BARCODEVALUE -</b> Barcode value or Id that will be encoded into the barcode on the pass
<BR>
<b>BARCODETEXT -</b> Barcode text that will be shown below the barcode image on the pass

