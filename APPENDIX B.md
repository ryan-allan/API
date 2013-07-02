<html>
<body>

<div class="text-2"><a id="appendix-b"></a><strong>Appendix B Error, Notification and Protocol code reference</strong></div>
<p><strong>i. Error Codes </strong></p>
<table class="toc" style="font-size:11px;">
<tbody>
<tr>
<td>E100 Invalid request. Make request via GET method or send valid XML inside &#8216;xml&#8217; field via POST.</td>
<td>E712 The &#8216;text&#8217; is required</td>
</tr>
<tr>
<td>E101 &#8216;action&#8217; required/Invalid Action</td>
<td>E713 There is billing problem on your account</td>
</tr>
<tr>
<td>E102 &#8216;user&#8217; or &#8216;api_key&#8217; required</td>
<td>E714 Missing/Invalid CampaignID</td>
</tr>
<tr>
<td>E103 &#8216;pass&#8217; md5(password) required</td>
<td>E715 Number is not subscribed to this campaign</td>
</tr>
<tr>
<td>E104 User Authentication FAILED</td>
<td>E801 &#8216;passTemplateID&#8217; is required.</td>
</tr>
<tr>
<td>E105 This account has no API rights</td>
<td>E802 Invalid &#8216;PassTemplateID&#8217;. Pass template is either deleted or do not belong to this user.</td>
</tr>
<tr>
<td>E106 You can call API every X seconds</td>
<td>E803 &#8216;BarcodeValue&#8217; is required.</td>
</tr>
<tr>
<td>E107 This account has no rights to use this action</td>
<td>E804 &#8216;Email&#8217; is invalid.</td>
</tr>
<tr>
<td>E108 XML Parse error: $error</td>
<td>E805 &#8216;Phone&#8217; is invalid.</td>
</tr>
<tr>
<td>E109 API not activated</td>
<td>E806 &#8216;PassDataID&#8217; was not created. Internal error occurred.</td>
</tr>
<tr>
<td>E110 Invalid receiver number</td>
<td>E807 &#8216;PassDataID&#8217; is required.</td>
</tr>
<tr>
<td>E111 Invalid shortcode</td>
<td>E808 Invalid &#8216;PassDataID&#8217;. Pass is either deleted or does not belong to this user.</td>
</tr>
<tr>
<td>E150 The &#8216;newuser&#8217; is required</td>
<td>E809 Pass was not updated. Internal error occured.</td>
</tr>
<tr>
<td>E151 &#8216;newuser&#8217; already exists</td>
<td>E810 &#8216;Pass Template &#8216;Header-1&#8242; value type has to be &#8216;Text&#8217; to allow &#8216;Header-1&#8242; API value&#8217;</td>
</tr>
<tr>
<td>E152 The &#8216;newpass&#8217; is required</td>
<td>E811 &#8216;Pass Template &#8216;Primary-1&#8242; value type has to be &#8216;Text&#8217; to allow &#8216;Primary-1&#8242; API value&#8217;</td>
</tr>
<tr>
<td>E153 User was not created. Internal error occurred</td>
<td>E812 &#8216;Pass Template &#8216;Primary-2&#8242; value type has to be &#8216;Text&#8217; to allow &#8216;Primary-2&#8242; API value&#8217;</td>
</tr>
<tr>
<td>E154 User was not created. Internal error occurred.</td>
<td>E813 &#8216;Pass Template &#8216;Secondary-1&#8242; value type has to be &#8216;Text&#8217; to allow &#8216;Secondary-1&#8242; API value&#8217;</td>
</tr>
<tr>
<td>E170 &#8216;campaignname is required</td>
<td>E814 &#8216;Pass Template &#8216;Secondary-2&#8242; value type has to be &#8216;Text&#8217; to allow &#8216;Secondary-2&#8242; API value&#8217;</td>
</tr>
<tr>
<td>E171 &#8216;brandname&#8217; is required</td>
<td>E815 &#8216;Pass Template &#8216;Secondary-3&#8242; value type has to be &#8216;Text&#8217; to allow &#8216;Secondary-3&#8242; API value&#8217;</td>
</tr>
<tr>
<td>E172 Campaign was not created. Internal error occured. Please try again later.</td>
<td>E816 &#8216;Pass Template &#8216;Secondary-4&#8242; value type has to be &#8216;Text&#8217; to allow &#8216;Secondary-4&#8242; API value&#8217;</td>
</tr>
<tr>
<td>E173 &#8216;mailingaddress&#8217; is required</td>
<td>E817 &#8216;Pass Template &#8216;Auxiliary-1&#8242; value type has to be &#8216;Text&#8217; to allow &#8216;Auxiliary-1&#8242; API value&#8217;</td>
</tr>
<tr>
<td>E201 The receiver number is required</td>
<td>E818 &#8216;Pass Template &#8216;Auxiliary-2&#8242; value type has to be &#8216;Text&#8217; to allow &#8216;Auxiliary-2&#8242; API value&#8217;</td>
</tr>
<tr>
<td>E225 Too many Slides</td>
<td>E819 &#8216;Pass Template &#8216;Auxiliary-3&#8242; value type has to be &#8216;Text&#8217; to allow &#8216;Auxiliary-3&#8242; API value&#8217;</td>
</tr>
<tr>
<td>E226 Audio and Video not allowed in same slide</td>
<td>E820 &#8216;Pass Template &#8216;Auxiliary-4&#8242; value type has to be &#8216;Text&#8217; to allow &#8216;Auxiliary-4&#8242; API value&#8217;</td>
</tr>
<tr>
<td>E227 Video and Image not allowed in same slide</td>
<td>E821 Pass was not deleted. Internal error occured.</td>
</tr>
<tr>
<td>E228 Text more than X characters</td>
<td>E822 There is no pass found in this MMS Template to send.</td>
</tr>
<tr>
<td>E229 Content not allowed</td>
<td>E823 There is no pass found in this Email template to send.</td>
</tr>
<tr>
<td>E230 Bad X slide duration</td>
<td>E824 Invalid call to the API. There is no pass data supplied.</td>
</tr>
<tr>
<td>E241 This content does not exist</td>
<td>E825 The pass contained in the MMS template do not allow MMS delivery.</td>
</tr>
<tr>
<td>E301 The &#8216;name&#8217; is required</td>
<td>E826 The pass contained in the Email template do not allow Email delivery.</td>
</tr>
<tr>
<td>E302 No slides</td>
<td>E901 The &#8216;mobile&#8217; is required</td>
</tr>
<tr>
<td>E303 Slide X is empty</td>
<td>E902 The &#8216;campaignid&#8217; is required</td>
</tr>
<tr>
<td>E331 Image in slide X is too big</td>
<td>E903 Invalid campaignid</td>
</tr>
<tr>
<td>E332 Audio in slide X is too big</td>
<td>E904 Could not subscribe this number</td>
</tr>
<tr>
<td>E333 Video in slide X is too big</td>
<td>E905 Could not unsubscribe this number</td>
</tr>
<tr>
<td>E334 Text in slide X is too long</td>
<td>E911 The &#8216;email&#8217; is required</td>
</tr>
<tr>
<td>E341 Image file in slide X is corrupted</td>
<td>E912 Invalid campaignid</td>
</tr>
<tr>
<td>E351 Could not copy Image in slide X</td>
<td>E913 Could not subscribe this email</td>
</tr>
<tr>
<td>E401 Invalid email</td>
<td>E914 Could not unsubscribe this email</td>
</tr>
<tr>
<td>E402 Invalid emailid</td>
<td></td>
</tr>
<tr>
<td>E403 Could not send email due to missing dataset entry</td>
<td></td>
</tr>
<tr>
<td>E503 Internal error</td>
<td></td>
</tr>
<tr>
<td>E506 &#8216;start_date&#8217;/'end_date&#8217; is required</td>
<td></td>
</tr>
<tr>
<td>E507 Invalid &#8216;start_date&#8217;/'end_date&#8217; format</td>
<td></td>
</tr>
<tr>
<td>E508 Invalid &#8216;start_date&#8217;/'end_date&#8217; format</td>
<td></td>
</tr>
<tr>
<td>E509 Lookup period is too long</td>
<td></td>
</tr>
<tr>
<td>E510 Lookup too frequent (you need to set time between the lookups)</td>
<td></td>
</tr>
<tr>
<td>E620 The &#8216;mmsid&#8217; is required</td>
<td></td>
</tr>
<tr>
<td>E621 The &#8216;to&#8217; is required</td>
<td></td>
</tr>
<tr>
<td>E623 The &#8216;to&#8217; field can contain up to 100 numbers</td>
<td></td>
</tr>
<tr>
<td>E624 The &#8216;tocampaign&#8217; is required</td>
<td></td>
</tr>
<tr>
<td>E626 Content unavailable. Encoding in progress, try again later.</td>
<td></td>
</tr>
<tr>
<td>E628 Operator Not supported</td>
<td></td>
</tr>
<tr>
<td>E629 Unrecognized content type</td>
<td></td>
</tr>
<tr>
<td>E630 The &#8216;databaseid&#8217; is required</td>
<td></td>
</tr>
<tr>
<td>E631 The &#8216;barcodeid&#8217; is required</td>
<td></td>
</tr>
<tr>
<td>E632 Invalid &#8216;databaseid&#8217;</td>
<td></td>
</tr>
<tr>
<td>E640 The &#8216;mmsinboxid&#8217; is required</td>
<td></td>
</tr>
<tr>
<td>E641 Invalid MMS Inbox ID</td>
<td></td>
</tr>
<tr>
<td>E642 MMS Inbox content is empty.</td>
<td></td>
</tr>
<tr>
<td>E643 Could not clean up MMS Inbox content.</td>
<td></td>
</tr>
</tbody>
</table>
<p><strong>ii. Postback Notification Codes</strong></p>
<table class="toc" id="toc" style="font-size:11px;">
<tbody>
<tr>
<td>E001 &#8211; encoding of mobile video failed</td>
</tr>
<tr>
<td>E002 &#8211; encoding of MMS audio failed</td>
</tr>
<tr>
<td>E003 &#8211; encoding of MMS video failed</td>
</tr>
<tr>
<td>E012 &#8211; encoding of MMS audio failed</td>
</tr>
<tr>
<td>E013 &#8211; encoding of MMS video failed</td>
</tr>
<tr>
<td>N003 &#8211; content was stored / encoded correctly</td>
</tr>
<tr>
<td>N013 &#8211; content was stored / encoded correctly and sending was triggered</td>
</tr>
<tr>
<td>N101 &#8211; when content sending started</td>
</tr>
<tr>
<td>N102 &#8211; when we get the Delivery report with either success or error</td>
</tr>
<tr>
<td>N301 &#8211; number subscribed</td>
</tr>
<tr>
<td>N302 &#8211; number unsubscribed</td>
</tr>
</tbody>
</table>
<p><strong>iii. SMS Protocol code look up</strong></p>
<table class="SMS-code-look-up" style="font-size:11px;">
<tbody>
<tr>
<th><strong>Protocol</strong></th>
<th><strong>Status</strong></th>
<th><strong>Success</strong></th>
<th class="nobrd"><strong>Notification Information</strong></th>
</tr>
<tr>
<td>1</td>
<td>92100</td>
<td>no</td>
<td>No Route</td>
</tr>
<tr>
<td>1</td>
<td>92101</td>
<td>no</td>
<td>No Credits</td>
</tr>
<tr>
<td>1</td>
<td>92102</td>
<td>no</td>
<td>Overspending</td>
</tr>
<tr>
<td>1</td>
<td>92110</td>
<td>no</td>
<td>No ProgramID</td>
</tr>
<tr>
<td>1</td>
<td>92111</td>
<td>no</td>
<td>TMobile Missing RefID</td>
</tr>
<tr>
<td>2</td>
<td>0</td>
<td>yes</td>
<td>Message sent</td>
</tr>
<tr>
<td>2</td>
<td>1</td>
<td>yes</td>
<td>Processing request</td>
</tr>
<tr>
<td>2</td>
<td>2</td>
<td>yes</td>
<td>Message queued</td>
</tr>
<tr>
<td>2</td>
<td>3</td>
<td>yes</td>
<td>Message buffered with carrier and waiting for delivery response</td>
</tr>
<tr>
<td>2</td>
<td>4</td>
<td>yes</td>
<td>Message delivered</td>
</tr>
<tr>
<td>2</td>
<td>5</td>
<td>yes</td>
<td>Message transferred to carrier and waiting for buffered response</td>
</tr>
<tr>
<td>2</td>
<td>301</td>
<td>no</td>
<td>Only one top level request element is permitted</td>
</tr>
<tr>
<td>2</td>
<td>303</td>
<td>no</td>
<td>The required version attribute of the request element was not found in the request</td>
</tr>
<tr>
<td>2</td>
<td>304</td>
<td>no</td>
<td>The required protocol attribute of the request element was not found in the request</td>
</tr>
<tr>
<td>2</td>
<td>306</td>
<td>no</td>
<td>The XML POST parameter cannot be empty</td>
</tr>
<tr>
<td>2</td>
<td>307</td>
<td>no</td>
<td>The request was an ill-formed XML document</td>
</tr>
<tr>
<td>2</td>
<td>310</td>
<td>no</td>
<td>If the force option is going to be set, it can only be set to one or zero</td>
</tr>
<tr>
<td>2</td>
<td>311</td>
<td>no</td>
<td>Method option is no longer used</td>
</tr>
<tr>
<td>2</td>
<td>321</td>
<td>no</td>
<td>Invalid request version</td>
</tr>
<tr>
<td>2</td>
<td>322</td>
<td>no</td>
<td>Invalid request protocol</td>
</tr>
<tr>
<td>2</td>
<td>323</td>
<td>no</td>
<td>Invalid request type</td>
</tr>
<tr>
<td>2</td>
<td>330</td>
<td>no</td>
<td>Invalid number of page elements</td>
</tr>
<tr>
<td>2</td>
<td>331</td>
<td>no</td>
<td>Client not found</td>
</tr>
<tr>
<td>2</td>
<td>337</td>
<td>no</td>
<td>Invalid carrier ID value</td>
</tr>
<tr>
<td>2</td>
<td>338</td>
<td>no</td>
<td>Message Service Id and destination carrier attributes cannot be used at same time</td>
</tr>
<tr>
<td>2</td>
<td>339</td>
<td>no</td>
<td>Invalid destination carrier ID value</td>
</tr>
<tr>
<td>2</td>
<td>340</td>
<td>no</td>
<td>Invalid source carrier ID value</td>
</tr>
<tr>
<td>2</td>
<td>341</td>
<td>no</td>
<td>Transaction failed; Carrier ID does not exist</td>
</tr>
<tr>
<td>2</td>
<td>342</td>
<td>no</td>
<td>A message service ID is required</td>
</tr>
<tr>
<td>2</td>
<td>343</td>
<td>no</td>
<td>The message service ID is discontinued</td>
</tr>
<tr>
<td>2</td>
<td>344</td>
<td>no</td>
<td>The message service ID is beta</td>
</tr>
<tr>
<td>2</td>
<td>345</td>
<td>no</td>
<td>Unable to determine carrier ID from destination address</td>
</tr>
<tr>
<td>2</td>
<td>349</td>
<td>no</td>
<td>Destination address contains non-numeric characters</td>
</tr>
<tr>
<td>2</td>
<td>350</td>
<td>no</td>
<td>A destination address is required</td>
</tr>
<tr>
<td>2</td>
<td>351</td>
<td>no</td>
<td>Transaction failed: Invalid destination address value</td>
</tr>
<tr>
<td>2</td>
<td>352</td>
<td>no</td>
<td>Invalid destination address country code</td>
</tr>
<tr>
<td>2</td>
<td>353</td>
<td>no</td>
<td>Message text or data is required</td>
</tr>
<tr>
<td>2</td>
<td>354</td>
<td>no</td>
<td>Message text is not long enough</td>
</tr>
<tr>
<td>2</td>
<td>355</td>
<td>no</td>
<td>Message text is too long</td>
</tr>
<tr>
<td>2</td>
<td>356</td>
<td>no</td>
<td>Message from is required</td>
</tr>
<tr>
<td>2</td>
<td>357</td>
<td>no</td>
<td>Message from is not long enough</td>
</tr>
<tr>
<td>2</td>
<td>358</td>
<td>no</td>
<td>Message from is too long</td>
</tr>
<tr>
<td>2</td>
<td>359</td>
<td>no</td>
<td>Message callback is required</td>
</tr>
<tr>
<td>2</td>
<td>360</td>
<td>no</td>
<td>Message callback is not long enough</td>
</tr>
<tr>
<td>2</td>
<td>361</td>
<td>no</td>
<td>Message callback is too long</td>
</tr>
<tr>
<td>2</td>
<td>362</td>
<td>no</td>
<td>Message callback contains non-numeric characters</td>
</tr>
<tr>
<td>2</td>
<td>363</td>
<td>no</td>
<td>Invalid callback number used</td>
</tr>
<tr>
<td>2</td>
<td>364</td>
<td>no</td>
<td>Callback and destination address cannot be identical</td>
</tr>
<tr>
<td>2</td>
<td>365</td>
<td>no</td>
<td>Strict international addressing is enforced, please use a + sign, country code, and national number</td>
</tr>
<tr>
<td>2</td>
<td>366</td>
<td>no</td>
<td>Invalid message length control option</td>
</tr>
<tr>
<td>2</td>
<td>367</td>
<td>no</td>
<td>Invalid source TON value</td>
</tr>
<tr>
<td>2</td>
<td>368</td>
<td>no</td>
<td>Invalid source address value</td>
</tr>
<tr>
<td>2</td>
<td>369</td>
<td>no</td>
<td>Account not permitted to use an alphanumeric source address</td>
</tr>
<tr>
<td>2</td>
<td>370</td>
<td>no</td>
<td>Account not permitted to use a short code source address</td>
</tr>
<tr>
<td>2</td>
<td>371</td>
<td>no</td>
<td>Callback attribute and source element cannot be used at same time</td>
</tr>
<tr>
<td>2</td>
<td>372</td>
<td>no</td>
<td>Pin attribute and destination element cannot be used at same time</td>
</tr>
<tr>
<td>2</td>
<td>373</td>
<td>no</td>
<td>Invalid destination TON value</td>
</tr>
<tr>
<td>2</td>
<td>374</td>
<td>no</td>
<td>Preview lookup request failed</td>
</tr>
<tr>
<td>2</td>
<td>375</td>
<td>no</td>
<td>Source address denied</td>
</tr>
<tr>
<td>2</td>
<td>376</td>
<td>no</td>
<td>Account not permitted to use premium billing options</td>
</tr>
<tr>
<td>2</td>
<td>377</td>
<td>no</td>
<td>Invalid premium billing charge type</td>
</tr>
<tr>
<td>2</td>
<td>378</td>
<td>no</td>
<td>Invalid premium billing charge amount</td>
</tr>
<tr>
<td>2</td>
<td>379</td>
<td>no</td>
<td>Invalid user data header</td>
</tr>
<tr>
<td>2</td>
<td>380</td>
<td>no</td>
<td>Invalid data coding scheme</td>
</tr>
<tr>
<td>2</td>
<td>381</td>
<td>no</td>
<td>Invalid characters used with selected data coding scheme</td>
</tr>
<tr>
<td>2</td>
<td>382</td>
<td>no</td>
<td>Invalid source or destination port</td>
</tr>
<tr>
<td>2</td>
<td>383</td>
<td>no</td>
<td>Message data and text attributes cannot be used at same time</td>
</tr>
<tr>
<td>2</td>
<td>384</td>
<td>no</td>
<td>Invalid message data</td>
</tr>
<tr>
<td>2</td>
<td>385</td>
<td>no</td>
<td>Invalid or unsupported ringtone format</td>
</tr>
<tr>
<td>2</td>
<td>386</td>
<td>no</td>
<td>Invalid or unsupported image format</td>
</tr>
<tr>
<td>2</td>
<td>387</td>
<td>no</td>
<td>Must provide a valid phone type to send images or ringtones</td>
</tr>
<tr>
<td>2</td>
<td>388</td>
<td>no</td>
<td>Binary messaging is not supported for this carrier</td>
</tr>
<tr>
<td>2</td>
<td>389</td>
<td>no</td>
<td>A valid image type must be specified</td>
</tr>
<tr>
<td>2</td>
<td>390</td>
<td>no</td>
<td>Must provide a numeric country and network code</td>
</tr>
<tr>
<td>2</td>
<td>391</td>
<td>no</td>
<td>Must provide ringtone data</td>
</tr>
<tr>
<td>2</td>
<td>392</td>
<td>no</td>
<td>Must provide image data</td>
</tr>
<tr>
<td>2</td>
<td>393</td>
<td>no</td>
<td>Must provide at least a screen saver or a ringtone to send a profile</td>
</tr>
<tr>
<td>2</td>
<td>394</td>
<td>no</td>
<td>Invalid option type for the phone specified</td>
</tr>
<tr>
<td>2</td>
<td>395</td>
<td>no</td>
<td>Must provide a country code and a network code to send a logo</td>
</tr>
<tr>
<td>2</td>
<td>396</td>
<td>no</td>
<td>Smart messages cannot use more than 3 messages to transfer</td>
</tr>
<tr>
<td>2</td>
<td>397</td>
<td>no</td>
<td>WAP Pushes require the optional URL parameter to be included</td>
</tr>
<tr>
<td>2</td>
<td>398</td>
<td>no</td>
<td>WAP Pushes not supported for this type of carrier</td>
</tr>
<tr>
<td>2</td>
<td>399</td>
<td>no</td>
<td>Binary data with a User Data Header is not allowed for your account</td>
</tr>
<tr>
<td>2</td>
<td>400</td>
<td>no</td>
<td>General error occurred while delivering the message to the<br />
carrier</td>
</tr>
<tr>
<td>2</td>
<td>401</td>
<td>no</td>
<td>General error occurred while delivering the message to the<br />
carrier</td>
</tr>
<tr>
<td>2</td>
<td>410</td>
<td>no</td>
<td>Message recipient not found on carrier</td>
</tr>
<tr>
<td>2</td>
<td>411</td>
<td>no</td>
<td>Message recipient not found on carrier</td>
</tr>
<tr>
<td>2</td>
<td>420</td>
<td>no</td>
<td>Invalid subscriber ID or subscriber password</td>
</tr>
<tr>
<td>2</td>
<td>430</td>
<td>no</td>
<td>Demo or commercial access is required</td>
</tr>
<tr>
<td>2</td>
<td>431</td>
<td>no</td>
<td>Invalid Subscriber ID</td>
</tr>
<tr>
<td>2</td>
<td>432</td>
<td>no</td>
<td>Account access permanently blocked</td>
</tr>
<tr>
<td>2</td>
<td>433</td>
<td>no</td>
<td>Account access denied</td>
</tr>
<tr>
<td>2</td>
<td>434</td>
<td>no</td>
<td>Account access has expired</td>
</tr>
<tr>
<td>2</td>
<td>451</td>
<td>no</td>
<td>Account mobile originated deliver profile incorrectly setup</td>
</tr>
<tr>
<td>2</td>
<td>460</td>
<td>no</td>
<td>Account entry not found in billing database</td>
</tr>
<tr>
<td>2</td>
<td>461</td>
<td>no</td>
<td>Must include source address if premium billing requested</td>
</tr>
<tr>
<td>2</td>
<td>507</td>
<td>no</td>
<td>Carrier facility not supported</td>
</tr>
<tr>
<td>2</td>
<td>508</td>
<td>no</td>
<td>Carrier absent subscriber</td>
</tr>
<tr>
<td>2</td>
<td>509</td>
<td>no</td>
<td>Carrier delivery failed</td>
</tr>
<tr>
<td>2</td>
<td>510</td>
<td>no</td>
<td>Carrier protocol error</td>
</tr>
<tr>
<td>2</td>
<td>511</td>
<td>no</td>
<td>Carrier MS not equipped</td>
</tr>
<tr>
<td>2</td>
<td>512</td>
<td>no</td>
<td>Carrier unknown SC</td>
</tr>
<tr>
<td>2</td>
<td>513</td>
<td>no</td>
<td>Carrier illegal MS</td>
</tr>
<tr>
<td>2</td>
<td>514</td>
<td>no</td>
<td>Carrier MS not a subscriber</td>
</tr>
<tr>
<td>2</td>
<td>560</td>
<td>no</td>
<td>Message recipient not authorized by carrier to receive the<br />
message</td>
</tr>
<tr>
<td>2</td>
<td>561</td>
<td>no</td>
<td>Content blocked by carrier</td>
</tr>
<tr>
<td>2</td>
<td>562</td>
<td>no</td>
<td>Short code not active</td>
</tr>
<tr>
<td>2</td>
<td>563</td>
<td>no</td>
<td>Short code expired</td>
</tr>
<tr>
<td>2</td>
<td>564</td>
<td>no</td>
<td>Short code blocked</td>
</tr>
<tr>
<td>2</td>
<td>565</td>
<td>no</td>
<td>Reseller address blocked by carrier</td>
</tr>
<tr>
<td>2</td>
<td>566</td>
<td>no</td>
<td>Destination address blocked by carrier</td>
</tr>
<tr>
<td>2</td>
<td>568</td>
<td>no</td>
<td>Destination address not provisioned for SMS</td>
</tr>
<tr>
<td>2</td>
<td>569</td>
<td>no</td>
<td>Destination address suspended by carrier</td>
</tr>
<tr>
<td>2</td>
<td>570</td>
<td>no</td>
<td>Invalid charge amount: charge amount not allowed for charge type</td>
</tr>
<tr>
<td>2</td>
<td>571</td>
<td>no</td>
<td>Campaign rejected by carrier</td>
</tr>
<tr>
<td>2</td>
<td>572</td>
<td>no</td>
<td>Campaign information is not provisioned for this carrier or is not active</td>
</tr>
<tr>
<td>2</td>
<td>800</td>
<td>no</td>
<td>Invalid number of service elements in request</td>
</tr>
<tr>
<td>2</td>
<td>801</td>
<td>no</td>
<td>General error while retrieving the service list</td>
</tr>
<tr>
<td>2</td>
<td>802</td>
<td>no</td>
<td>Service ID is required</td>
</tr>
<tr>
<td>2</td>
<td>803</td>
<td>no</td>
<td>Invalid service ID since it was null</td>
</tr>
<tr>
<td>2</td>
<td>810</td>
<td>no</td>
<td>Failed message delivery</td>
</tr>
<tr>
<td>2</td>
<td>811</td>
<td>no</td>
<td>Message Delivery Error: Message expired by carrier</td>
</tr>
<tr>
<td>2</td>
<td>815</td>
<td>no</td>
<td>Message Delivery Error &#8211; Message submitted to but not acknowledged by carrier</td>
</tr>
<tr>
<td>2</td>
<td>1000</td>
<td>no</td>
<td>System error: General error occured while processing request</td>
</tr>
<tr>
<td>2</td>
<td>1001</td>
<td>no</td>
<td>System error: Duplicate Ticket ID</td>
</tr>
<tr>
<td>2</td>
<td>1010</td>
<td>no</td>
<td>Temporary system error</td>
</tr>
<tr>
<td>2</td>
<td>1020</td>
<td>no</td>
<td>Temporary external system error</td>
</tr>
<tr>
<td>2</td>
<td>1030</td>
<td>no</td>
<td>External system error</td>
</tr>
<tr>
<td>2</td>
<td>2001</td>
<td>no</td>
<td>Invalid subscription authentication</td>
</tr>
<tr>
<td>2</td>
<td>2002</td>
<td>no</td>
<td>Subscriber/account ID has been de-activated</td>
</tr>
<tr>
<td>2</td>
<td>2003</td>
<td>no</td>
<td>Subscriber/account ID has been deleted</td>
</tr>
<tr>
<td>2</td>
<td>2010</td>
<td>no</td>
<td>General billing error</td>
</tr>
<tr>
<td>2</td>
<td>2011</td>
<td>no</td>
<td>Transaction failed: Message delivery expired, no charge was made</td>
</tr>
<tr>
<td>2</td>
<td>2012</td>
<td>no</td>
<td>Transaction failed: Consumer canceled the transaction</td>
</tr>
<tr>
<td>2</td>
<td>2013</td>
<td>no</td>
<td>Message still in process</td>
</tr>
<tr>
<td>2</td>
<td>2014</td>
<td>no</td>
<td>Transaction failed: Wireless subscriber is ineligible for billing on carrier</td>
</tr>
<tr>
<td>2</td>
<td>2015</td>
<td>no</td>
<td>Transaction failed: Wireless subscriber&#8217;s account is deactivated</td>
</tr>
<tr>
<td>2</td>
<td>2016</td>
<td>no</td>
<td>Unspecified error</td>
</tr>
<tr>
<td>2</td>
<td>2017</td>
<td>no</td>
<td>Message has been deleted by carrier</td>
</tr>
<tr>
<td>2</td>
<td>2018</td>
<td>no</td>
<td>Subscriber payment method is invalid</td>
</tr>
<tr>
<td>2</td>
<td>2019</td>
<td>no</td>
<td>Undeliverable to user</td>
</tr>
<tr>
<td>2</td>
<td>2020</td>
<td>no</td>
<td>Transaction failed: Wireless subscriber over spending limit</td>
</tr>
<tr>
<td>2</td>
<td>2021</td>
<td>no</td>
<td>Service not available for user</td>
</tr>
<tr>
<td>2</td>
<td>2022</td>
<td>no</td>
<td>Transaction failed: Wireless subscriber not eligible for premium billing: Subscriber setting</td>
</tr>
<tr>
<td>2</td>
<td>2023</td>
<td>no</td>
<td>User not found on carrier network</td>
</tr>
<tr>
<td>2</td>
<td>2024</td>
<td>no</td>
<td>Transaction failed: Wireless subscriber&#8217;s account closed, suspended or locked.</td>
</tr>
<tr>
<td>2</td>
<td>2025</td>
<td>no</td>
<td>Transaction failed: Carrier does not support premium billing with the supplied short code</td>
</tr>
<tr>
<td>2</td>
<td>2026</td>
<td>no</td>
<td>Transaction failed: Ineligible product</td>
</tr>
<tr>
<td>2</td>
<td>2027</td>
<td>no</td>
<td>Transaction failed: Wireless network operator temporary system<br />
error</td>
</tr>
<tr>
<td>2</td>
<td>2028</td>
<td>no</td>
<td>Wireless subscriber has run out of prepaid credits</td>
</tr>
<tr>
<td>2</td>
<td>2029</td>
<td>no</td>
<td>Wireless subscriber not eligible for premium billing: blocked MDN</td>
</tr>
<tr>
<td>2</td>
<td>2030</td>
<td>no</td>
<td>Transaction failed: Wireless subscriber not eligible for premium<br />
billing: Reseller</td>
</tr>
<tr>
<td>2</td>
<td>2031</td>
<td>no</td>
<td>Short code is currently in test mode, only whitelisted handsets are permitted</td>
</tr>
<tr>
<td>2</td>
<td>2032</td>
<td>no</td>
<td>Short code is not certified on carrier</td>
</tr>
<tr>
<td>2</td>
<td>2033</td>
<td>no</td>
<td>Short code not permitted for this carrier</td>
</tr>
<tr>
<td>2</td>
<td>2034</td>
<td>no</td>
<td>Short code and price point combination is not allowed for this carrier</td>
</tr>
<tr>
<td>2</td>
<td>2035</td>
<td>no</td>
<td>Transaction failed: Wireless subscriber not found</td>
</tr>
<tr>
<td>2</td>
<td>2036</td>
<td>no</td>
<td>Tax failed on transaction</td>
</tr>
<tr>
<td>2</td>
<td>2037</td>
<td>no</td>
<td>Transaction failed: Does not meet minimum charge amount</td>
</tr>
<tr>
<td>2</td>
<td>2038</td>
<td>no</td>
<td>Transaction failed: Amount exceeds specified maximum</td>
</tr>
<tr>
<td>2</td>
<td>2039</td>
<td>no</td>
<td>Advice-of-Charge Timed Out</td>
</tr>
<tr>
<td>2</td>
<td>2040</td>
<td>no</td>
<td>Transaction failed: Charge duration exceeded</td>
</tr>
<tr>
<td>2</td>
<td>2041</td>
<td>no</td>
<td>Transaction failed: Unable to process request; previous billing request still being processed; Advice-of-Charge re-sent</td>
</tr>
<tr>
<td>2</td>
<td>2042</td>
<td>no</td>
<td>Refund denied: Transaction already refunded</td>
</tr>
<tr>
<td>2</td>
<td>2043</td>
<td>no</td>
<td>Request Failed: No transaction found matching provided data</td>
</tr>
<tr>
<td>2</td>
<td>2044</td>
<td>no</td>
<td>Invalid URL</td>
</tr>
<tr>
<td>2</td>
<td>2045</td>
<td>no</td>
<td>Carrier not supported</td>
</tr>
<tr>
<td>2</td>
<td>2046</td>
<td>no</td>
<td>Invalid sessionId</td>
</tr>
<tr>
<td>2</td>
<td>2047</td>
<td>no</td>
<td>Invalid ticketid</td>
</tr>
<tr>
<td>2</td>
<td>2048</td>
<td>no</td>
<td>Validation Error</td>
</tr>
<tr>
<td>2</td>
<td>2049</td>
<td>no</td>
<td>Transaction failed: Request with no associated charge; failed by<br />
OpenMarket</td>
</tr>
<tr>
<td>2</td>
<td>2050</td>
<td>no</td>
<td>Transaction failed: The transaction has been denied by the<br />
carrier&#8217;s billing system</td>
</tr>
<tr>
<td>2</td>
<td>2051</td>
<td>no</td>
<td>Supplied ticketId is either in a processed state or failed state</td>
</tr>
<tr>
<td>2</td>
<td>2052</td>
<td>no</td>
<td>Transaction failed: Campaign information is not provisioned for this carrier or is not active</td>
</tr>
<tr>
<td>2</td>
<td>2053</td>
<td>no</td>
<td>Transaction failed: Advice of charge message exceeded maximum length</td>
</tr>
<tr>
<td>2</td>
<td>2054</td>
<td>no</td>
<td>Transaction failed:  Wireless subscriber?s account closed</td>
</tr>
<tr>
<td>2</td>
<td>2056</td>
<td>no</td>
<td>Transaction failed: Campaign rejected by carrier</td>
</tr>
<tr>
<td>2</td>
<td>2100</td>
<td>no</td>
<td>Invalid request&#8211;&lt;request parameter&gt; is missing</td>
</tr>
<tr>
<td>2</td>
<td>2101</td>
<td>no</td>
<td>Account is not authorized</td>
</tr>
<tr>
<td>2</td>
<td>2102</td>
<td>no</td>
<td>Account is not authorized to use short code</td>
</tr>
<tr>
<td>2</td>
<td>2104</td>
<td>no</td>
<td>Transaction failed: Refund cannot be processed against a failed charge</td>
</tr>
<tr>
<td>2</td>
<td>2120</td>
<td>no</td>
<td>Account does not have permission to refund the charge</td>
</tr>
<tr>
<td>2</td>
<td>2121</td>
<td>no</td>
<td>Refund cannot exceed the original transaction amount</td>
</tr>
<tr>
<td>2</td>
<td>2122</td>
<td>no</td>
<td>ProgramId is a required field for this carrier</td>
</tr>
<tr>
<td>2</td>
<td>2123</td>
<td>no</td>
<td>The carrier does not support refunds to be processed</td>
</tr>
<tr>
<td>2</td>
<td>2124</td>
<td>no</td>
<td>The carrier does not support partial refunds</td>
</tr>
<tr>
<td>2</td>
<td>2125</td>
<td>no</td>
<td>Refund cannot be processed as it exceeds the allowable time period since the charge</td>
</tr>
<tr>
<td>2</td>
<td>2126</td>
<td>no</td>
<td>Carrier information cannot be found from the WAP header</td>
</tr>
<tr>
<td>2</td>
<td>3041</td>
<td>no</td>
<td>Standard rate message blocked by the OpenMarket deactivated numbers firewall</td>
</tr>
<tr>
<td>2</td>
<td>3042</td>
<td>no</td>
<td>Premium rate message blocked by the OpenMarket deactivated numbers firewall</td>
</tr>
<tr>
<td>2</td>
<td>4000</td>
<td>no</td>
<td>Transaction failed: Merchant account not permitted to use the<br />
subscription service</td>
</tr>
<tr>
<td>2</td>
<td>4001</td>
<td>no</td>
<td>Short code is not provisioned to use the subscription service<br />
for this carrier</td>
</tr>
<tr>
<td>2</td>
<td>4010</td>
<td>no</td>
<td>Transaction failed: Subscription already exists</td>
</tr>
<tr>
<td>2</td>
<td>4011</td>
<td>no</td>
<td>Transaction failed: Unable to process request; previous billing request still being processed</td>
</tr>
<tr>
<td>2</td>
<td>4012</td>
<td>no</td>
<td>Transaction failed: Subscription already exists on carrier; possible phone number change</td>
</tr>
<tr>
<td>2</td>
<td>4013</td>
<td>no</td>
<td>Transaction failed: Unable to process request; previous billing request is pending consumer response</td>
</tr>
<tr>
<td>2</td>
<td>4020</td>
<td>no</td>
<td>Transaction failed: Subscription not found</td>
</tr>
<tr>
<td>2</td>
<td>4021</td>
<td>no</td>
<td>Transaction failed: Subscription already expired</td>
</tr>
<tr>
<td>2</td>
<td>4030</td>
<td>no</td>
<td>Renewal error: subscription already billed for this period</td>
</tr>
<tr>
<td>2</td>
<td>4031</td>
<td>no</td>
<td>Renewal error: Subscription renewal status cannot be determined</td>
</tr>
<tr>
<td>2</td>
<td>4032</td>
<td>no</td>
<td>Renewal error: Subscription already expired</td>
</tr>
<tr>
<td>2</td>
<td>4033</td>
<td>no</td>
<td>Subscription successfully cancelled, message delivery failed.</td>
</tr>
<tr>
<td>2</td>
<td>4035</td>
<td>no</td>
<td>Renewal Error: Subscription renewal failed by carrier</td>
</tr>
<tr>
<td>2</td>
<td>4050</td>
<td>no</td>
<td>Conclude error: subscription already concluded.</td>
</tr>
<tr>
<td>2</td>
<td>4051</td>
<td>no</td>
<td>Conclude error: Subscription cannot be concluded while in indeterminate state.</td>
</tr>
<tr>
<td>2</td>
<td>4052</td>
<td>no</td>
<td>Transaction failed: Received notification of account deactivation; failed by OpenMarket</td>
</tr>
<tr>
<td>2</td>
<td>4054</td>
<td>no</td>
<td>Renewal error: Subscription already revoked</td>
</tr>
<tr>
<td>2</td>
<td>4055</td>
<td>no</td>
<td>Conclude error: Subscription cannot be concluded while a renewal is pending</td>
</tr>
<tr>
<td>3</td>
<td>1</td>
<td>yes</td>
<td>delivery success</td>
</tr>
<tr>
<td>3</td>
<td>2</td>
<td>no</td>
<td>delivery failure</td>
</tr>
<tr>
<td>3</td>
<td>4</td>
<td>yes</td>
<td>msg buffered</td>
</tr>
<tr>
<td>3</td>
<td>8</td>
<td>yes</td>
<td>smsc submit</td>
</tr>
<tr>
<td>3</td>
<td>16</td>
<td>no</td>
<td>smsc reject (error)</td>
</tr>
<tr>
<td>4</td>
<td>0</td>
<td>yes</td>
<td>Successfully executed</td>
</tr>
<tr>
<td>4</td>
<td>1</td>
<td>no</td>
<td>Invalid login or un-authorized API usage</td>
</tr>
<tr>
<td>4</td>
<td>2</td>
<td>no</td>
<td>Consumer is blocked by IPX</td>
</tr>
<tr>
<td>4</td>
<td>3</td>
<td>no</td>
<td>Operation is not provisioned by IPX</td>
</tr>
<tr>
<td>4</td>
<td>4</td>
<td>no</td>
<td>The consumer is unknown to IPX</td>
</tr>
<tr>
<td>4</td>
<td>5</td>
<td>no</td>
<td>Consumer has blocked this service in IPX</td>
</tr>
<tr>
<td>4</td>
<td>6</td>
<td>no</td>
<td>The originating address is not supported</td>
</tr>
<tr>
<td>4</td>
<td>7</td>
<td>no</td>
<td>Alpha originating address not supported by account</td>
</tr>
<tr>
<td>4</td>
<td>8</td>
<td>no</td>
<td>MSISDN originating address not supported by account</td>
</tr>
<tr>
<td>4</td>
<td>9</td>
<td>no</td>
<td>GSM extended not supported by account</td>
</tr>
<tr>
<td>4</td>
<td>10</td>
<td>no</td>
<td>Unicode not supported by account</td>
</tr>
<tr>
<td>4</td>
<td>11</td>
<td>no</td>
<td>Status report not supported by account</td>
</tr>
<tr>
<td>4</td>
<td>12</td>
<td>no</td>
<td>Required capability not supported</td>
</tr>
<tr>
<td>4</td>
<td>13</td>
<td>no</td>
<td>Could not route message</td>
</tr>
<tr>
<td>4</td>
<td>14</td>
<td>no</td>
<td>The content provider max throttling rate is exceeded</td>
</tr>
<tr>
<td>4</td>
<td>15</td>
<td>no</td>
<td>The account max throttling rate is exceeded</td>
</tr>
<tr>
<td>4</td>
<td>16</td>
<td>no</td>
<td>Protocol ID not supported by account</td>
</tr>
<tr>
<td>4</td>
<td>50</td>
<td>no</td>
<td>Partial success: (&lt;1&gt;;&lt;2&gt;;&lt;n&gt;)</td>
</tr>
<tr>
<td>4</td>
<td>99</td>
<td>no</td>
<td>Internal server error</td>
</tr>
<tr>
<td>4</td>
<td>100</td>
<td>no</td>
<td>Invalid destination address</td>
</tr>
<tr>
<td>4</td>
<td>101</td>
<td>no</td>
<td>Invalid tariff class (price)</td>
</tr>
<tr>
<td>4</td>
<td>102</td>
<td>no</td>
<td>Invalid referenced (linked) ID</td>
</tr>
<tr>
<td>4</td>
<td>103</td>
<td>no</td>
<td>Invalid account name</td>
</tr>
<tr>
<td>4</td>
<td>104</td>
<td>no</td>
<td>Invalid content category</td>
</tr>
<tr>
<td>4</td>
<td>105</td>
<td>no</td>
<td>Invalid content meta data</td>
</tr>
<tr>
<td>4</td>
<td>106</td>
<td>no</td>
<td>Invalid originating address</td>
</tr>
<tr>
<td>4</td>
<td>107</td>
<td>no</td>
<td>Invalid alphanumeric originating address</td>
</tr>
<tr>
<td>4</td>
<td>108</td>
<td>no</td>
<td>Invalid validity time</td>
</tr>
<tr>
<td>4</td>
<td>109</td>
<td>no</td>
<td>Invalid delivery time</td>
</tr>
<tr>
<td>4</td>
<td>110</td>
<td>no</td>
<td>Invalid message content/user data</td>
</tr>
<tr>
<td>4</td>
<td>111</td>
<td>no</td>
<td>Invalid message length</td>
</tr>
<tr>
<td>4</td>
<td>112</td>
<td>no</td>
<td>Invalid user data header</td>
</tr>
<tr>
<td>4</td>
<td>113</td>
<td>no</td>
<td>Invalid data coding scheme</td>
</tr>
<tr>
<td>4</td>
<td>114</td>
<td>no</td>
<td>Invalid protocol ID</td>
</tr>
<tr>
<td>4</td>
<td>115</td>
<td>no</td>
<td>Invalid status report flags</td>
</tr>
<tr>
<td>4</td>
<td>116</td>
<td>no</td>
<td>Invalid TON</td>
</tr>
<tr>
<td>4</td>
<td>117</td>
<td>no</td>
<td>Invalid VAT</td>
</tr>
<tr>
<td>4</td>
<td>200</td>
<td>no</td>
<td>Operator integration error</td>
</tr>
<tr>
<td>4</td>
<td>201</td>
<td>no</td>
<td>Communication problems</td>
</tr>
<tr>
<td>4</td>
<td>202</td>
<td>no</td>
<td>Read timeout</td>
</tr>
<tr>
<td>4</td>
<td>299</td>
<td>no</td>
<td>Integration error</td>
</tr>
</tbody>
</table>
<div class="text-2"><a href="http://blog.skycore.com/skycore-api-v1-3-appendix-a#appendix-a">APPENDIX A</a></div>
<div class="text-2"><a href="http://blog.skycore.com/skycore-api-v1-3-appendix-c#appendix-c">APPENDIX C</a></div>
<div class="text-2"><a href="http://blog.skycore.com/skycore-api-v1-3-appendix-d#appendix-d">APPENDIX D</a></div>
<div class="text-2"><a href="http://blog.skycore.com/skycore-api-v1-3-appendix-e#appendix-e">APPENDIX E</a></div>
<div id="__tbSetup"></div>
<p>//</p>
<div id="jp-post-flair" class="sharedaddy sd-like-enabled sd-sharing-enabled"><div class="sharedaddy sd-sharing-enabled"><div class="robots-nocontent sd-block sd-social sd-social-icon-text sd-sharing"><h3 class="sd-title">Share this:</h3><div class="sd-content"><ul><li class="share-email"><a rel="nofollow" class="share-email sd-button share-icon" href="http://blog.skycore.com/skycore-api-v1-3-appendix-b/?share=email" target="_blank" title="Click to email this to a friend"><span>Email</span></a></li><li class="share-twitter"><a rel="nofollow" class="share-twitter sd-button share-icon" href="http://blog.skycore.com/skycore-api-v1-3-appendix-b/?share=twitter" target="_blank" title="Click to share on Twitter" id="sharing-twitter-709"><span>Twitter</span></a></li><li class="share-linkedin"><a rel="nofollow" class="share-linkedin sd-button share-icon" href="http://blog.skycore.com/skycore-api-v1-3-appendix-b/?share=linkedin" target="_blank" title="Click to share on LinkedIn" id="sharing-linkedin-709"><span>LinkedIn</span></a></li><li class="share-facebook"><a rel="nofollow" class="share-facebook sd-button share-icon" href="http://blog.skycore.com/skycore-api-v1-3-appendix-b/?share=facebook" target="_blank" title="Share on Facebook" id="sharing-facebook-709"><span>Facebook</span></a></li><li class="share-google-plus-1"><a rel="nofollow" class="share-google-plus-1 sd-button share-icon" href="http://blog.skycore.com/skycore-api-v1-3-appendix-b/?share=google-plus-1" target="_blank" title="Click to share on Google+" id="sharing-google-709"><span>Google +1</span></a></li><li class="share-end"></li></ul></div></div></div><div class='sharedaddy sd-block sd-like jetpack-likes-widget-wrapper jetpack-likes-widget-unloaded' id='like-post-wrapper-30180251-709-51d337b9dba86' data-src='http://widgets.wp.com/likes/#blog_id=30180251&amp;post_id=709&amp;origin=http://blogskycore.wordpress.com&amp;obj_id=30180251-709-51d337b9dba86' data-name='like-post-frame-30180251-709-51d337b9dba86'><h3 class='sd-title'>Like this:</h3><div class='post-likes-widget-placeholder' style='height:55px'><span class='button'><span>Like</span></span> <span class="loading">Loading...</span></div><span class='sd-text-color'></span><a class='sd-link-color'></a></div></div></div>

  			
			</div>

		
	
	
<div id="comments">

	<h3 id="comments-title">1 Comment</h3>

	<ol class="commentlist"></ol>

				<h4>Trackbacks</h4>
		<ol class="pingslist">
				<li class="pingback">
		<a href='http://blog.skycore.com/2012/01/30/skycore-api-v1-3-documentation/' rel='external nofollow' class='url'>Skycore API v1.3 Documentation &laquo; Skycore Mobile Blog</a>	</li><!-- #comment-## -->
		</ol>
	
	


								<div id="respond" class="comment-respond">
				<h3 id="reply-title" class="comment-reply-title">Leave a Reply <small><a rel="nofollow" id="cancel-comment-reply-link" href="/skycore-api-v1-3-appendix-b/#respond" style="display:none;">Cancel reply</a></small></h3>
									<form action="http://blog.skycore.com/wp-comments-post.php" method="post" id="commentform" class="comment-form">
																										


												<input type="hidden" id="highlander_comment_nonce" name="highlander_comment_nonce" value="62f223b657" /><input type="hidden" name="_wp_http_referer" value="/skycore-api-v1-3-appendix-b/" />
<input type="hidden" name="hc_post_as" id="hc_post_as" value="guest" />

<div class="comment-form-field comment-textarea">
	<label for="comment">Enter your comment here...</label>
	<div id="comment-form-comment"><textarea id="comment" name="comment" title="Enter your comment here..."></textarea></div>
</div>

<div id="comment-form-identity">

	<div id="comment-form-nascar">
		<p>Fill in your details below or click an icon to log in:</p>
		<ul>
			<li class="selected" style="display:none;">
				<a href="#comment-form-guest" id="postas-guest" title="Guest">
					<span></span>
				</a>
			</li>
			<li>
				<a href="#comment-form-load-service:WordPress.com" id="postas-wordpress" title="WordPress.com">
					<span></span>
				</a>
			</li>
			<li>
				<a href="#comment-form-load-service:Twitter" id="postas-twitter" title="Twitter">
					<span></span>
				</a>
			</li>
			<li>
				<a href="#comment-form-load-service:Facebook" id="postas-facebook" title="Facebook">
					<span></span>
				</a>
			</li>
		</ul>
	</div>

	<div id="comment-form-guest" class="comment-form-service selected">
		<div class="comment-form-padder">
			<div class="comment-form-avatar">
<a href="https://gravatar.com/site/signup/" target="_blank">				<img src="http://1.gravatar.com/avatar/ad516503a11cd5ca435acc9bb6523536?s=25&amp;d=identicon&amp;forcedefault=y&amp;r=G" alt="Gravatar" width="25" class="no-grav" />
</a>			</div>

				<div class="comment-form-fields">
				<div class="comment-form-field comment-form-email">
					<label for="email">Email <span class="required">(required)</span> <span class="nopublish">(Address never made public)</span></label>
					<div class="comment-form-input"><input id="email" name="email" type="email" value="" /></div>
				</div>
				<div class="comment-form-field comment-form-author">
					<label for="author">Name <span class="required">(required)</span></label>
					<div class="comment-form-input"><input id="author" name="author" type="text" value="" /></div>
				</div>
				<div class="comment-form-field comment-form-url">
					<label for="url">Website</label>
					<div class="comment-form-input"><input id="url" name="url" type="text" value="" /></div>
				</div>
			</div>
	
		</div>
	</div>

	<div id="comment-form-wordpress" class="comment-form-service">
		<div class="comment-form-padder">
			<div class="comment-form-avatar">
				<img src="http://s2.wp.com/wp-content/mu-plugins/highlander-comments/images/wplogo.png?m=1289230950g" alt="WordPress.com Logo" width="25" class="no-grav" />
			</div>

				<div class="comment-form-fields">
				<input type="hidden" name="wp_avatar" id="wordpress-avatar" class="comment-meta-wordpress" value="" />
				<input type="hidden" name="wp_user_id" id="wordpress-user_id" class="comment-meta-wordpress" value="" />
				<input type="hidden" name="wp_access_token" id="wordpress-access_token" class="comment-meta-wordpress" value="" />
				<p class="comment-form-posting-as pa-wordpress"><strong></strong> You are commenting using your WordPress.com account. <span class="comment-form-log-out">(&nbsp;<a href="javascript:HighlanderComments.doExternalLogout( 'wordpress' );">Log&nbsp;Out</a>&nbsp;/&nbsp;<a href="#" onclick="javascript:HighlanderComments.switchAccount();return false;">Change</a>&nbsp;)</span></p>
			</div>
	
		</div>
	</div>

	<div id="comment-form-twitter" class="comment-form-service">
		<div class="comment-form-padder">
			<div class="comment-form-avatar">
				<img src="http://1.gravatar.com/avatar/ad516503a11cd5ca435acc9bb6523536?s=25&amp;d=identicon&amp;forcedefault=y&amp;r=G" alt="Twitter picture" width="25" class="no-grav" />
			</div>

				<div class="comment-form-fields">
				<input type="hidden" name="twitter_avatar" id="twitter-avatar" class="comment-meta-twitter" value="" />
				<input type="hidden" name="twitter_user_id" id="twitter-user_id" class="comment-meta-twitter" value="" />
				<input type="hidden" name="twitter_access_token" id="twitter-access_token" class="comment-meta-twitter" value="" />
				<p class="comment-form-posting-as pa-twitter"><strong></strong> You are commenting using your Twitter account. <span class="comment-form-log-out">(&nbsp;<a href="javascript:HighlanderComments.doExternalLogout( 'twitter' );">Log&nbsp;Out</a>&nbsp;/&nbsp;<a href="#" onclick="javascript:HighlanderComments.switchAccount();return false;">Change</a>&nbsp;)</span></p>
			</div>
	
		</div>
	</div>

	<div id="comment-form-facebook" class="comment-form-service">
		<div class="comment-form-padder">
			<div class="comment-form-avatar">
				<img src="http://1.gravatar.com/avatar/ad516503a11cd5ca435acc9bb6523536?s=25&amp;d=identicon&amp;forcedefault=y&amp;r=G" alt="Facebook photo" width="25" class="no-grav" />
			</div>

				<div class="comment-form-fields">
				<input type="hidden" name="fb_avatar" id="facebook-avatar" class="comment-meta-facebook" value="" />
				<input type="hidden" name="fb_user_id" id="facebook-user_id" class="comment-meta-facebook" value="" />
				<input type="hidden" name="fb_access_token" id="facebook-access_token" class="comment-meta-facebook" value="" />
				<p class="comment-form-posting-as pa-facebook"><strong></strong> You are commenting using your Facebook account. <span class="comment-form-log-out">(&nbsp;<a href="javascript:HighlanderComments.doExternalLogout( 'facebook' );">Log&nbsp;Out</a>&nbsp;/&nbsp;<a href="#" onclick="javascript:HighlanderComments.switchAccount();return false;">Change</a>&nbsp;)</span></p>
			</div>
	
		</div>
	</div>


	<div id="comment-form-load-service" class="comment-form-service">
		<div class="comment-form-posting-as-cancel"><a href="javascript:HighlanderComments.cancelExternalWindow();">Cancel</a></div>
		<p>Connecting to %s</p>
	</div>

	
</div>

<script type="text/javascript">
jQuery(document).ready(function(){
	var input = document.createElement( 'input' ),
	    comment = jQuery( '#comment' );

	if ( 'placeholder' in input ) {
		comment.attr( 'placeholder', jQuery( '.comment-textarea label' ).remove().text() );
	}

	// Expando Mode: start small, then auto-resize on first click + text length
	jQuery( '#comment-form-identity' ).hide();
	jQuery( '#comment-form-subscribe' ).hide();
	jQuery( '#commentform .form-submit' ).hide();

	comment.css( { 'height':'10px' } ).one( 'focus', function() {
		var timer = setInterval( HighlanderComments.resizeCallback, 10 )
		jQuery( this ).animate( { 'height': HighlanderComments.initialHeight } ).delay( 100 ).queue( function(n) { clearInterval( timer ); HighlanderComments.resizeCallback(); n(); } );
		jQuery( '#comment-form-identity' ).slideDown();
		jQuery( '#comment-form-subscribe' ).slideDown();
		jQuery( '#commentform .form-submit' ).slideDown();
	});
});
</script>

<div id="comment-form-subscribe">
	<p class="comment-subscription-form"><input type="checkbox" name="subscribe" id="subscribe" value="subscribe" style="width: auto;" tabindex="6"/> <label class="subscribe-label" id="subscribe-label" for="subscribe" style="display: inline;">Notify me of follow-up comments via email.</label></p><p class="post-subscription-form"><input type="checkbox" name="subscribe_blog" id="subscribe_blog" value="subscribe" style="width: auto;" tabindex="7"/> <label class="subscribe-label" id="subscribe-blog-label" for="subscribe_blog"  style="display: inline;">Notify me of new posts via email.</label></p></div>

												<p class="form-submit">
							<input name="submit" type="submit" id="comment-submit" value="Post Comment" />
							<input type='hidden' name='comment_post_ID' value='709' id='comment_post_ID' />
<input type='hidden' name='comment_parent' id='comment_parent' value='0' />
						</p>
						
<input type="hidden" name="genseq" value="1372796857" />
<p style="display: none;"><input type="hidden" id="akismet_comment_nonce" name="akismet_comment_nonce" value="e2c2eb20e4" /></p><script type='text/javascript' src='http://s2.wp.com/wp-content/mu-plugins/akismet-2.5/form.js?m=1308783962g'></script>
<p style="display: none;"><input type="hidden" id="ak_js" name="ak_js" value="108"/></p>					</form>
							</div><!-- #respond -->
			<div style="clear: both"></div>			
</div><!-- #comments -->
	</div><!-- #content -->


<div id="sidebar">
	<div id="search-2" class="section widget-container widget widget_search">
<form method="get" id="searchform" action="http://blog.skycore.com//">
	<label for="s" class="assistive-text">Search</label>
	<input id="s" name="s" class="search-input" type="text" value="" placeholder="Type keywords and press Enter" />
	<input type="submit" class="submit assistive-text" name="submit" id="searchsubmit" value="Search" />
</form></div><div id="pages-2" class="section widget-container widget widget_pages"><h3 class="widget-title">API Documentation</h3>		<ul>
			<li class="page_item page-item-1046"><a href="http://blog.skycore.com/skycore-api-v1-3-documentation/">Skycore API v1.3&nbsp;Documentation</a></li>
<li class="page_item page-item-1052"><a href="http://blog.skycore.com/skycore-api-v1-3-sms_mms_mo/">Skycore API v1.3 Documentation MMS MO / SMS&nbsp;MO</a></li>
<li class="page_item page-item-953"><a href="http://blog.skycore.com/postback-notification-system/">Skycore API v1.3 Postback API&nbsp;Documentation</a></li>
<li class="page_item page-item-704"><a href="http://blog.skycore.com/skycore-api-v1-3-appendix-a/">Skycore API v1.3 Documentation : APPENDIX&nbsp;A</a></li>
<li class="page_item page-item-709 current_page_item"><a href="http://blog.skycore.com/skycore-api-v1-3-appendix-b/">Skycore API v1.3 Documentation: APPENDIX&nbsp;B</a></li>
<li class="page_item page-item-843"><a href="http://blog.skycore.com/skycore-api-v1-3-appendix-c/">Skycore API v1.3 Documentation: APPENDIX&nbsp;C</a></li>
<li class="page_item page-item-711"><a href="http://blog.skycore.com/skycore-api-v1-3-appendix-d/">Skycore API v1.3 Documentation: APPENDIX&nbsp;D</a></li>
<li class="page_item page-item-714"><a href="http://blog.skycore.com/skycore-api-v1-3-appendix-e/">Skycore API v1.3 Documentation: APPENDIX&nbsp;E</a></li>
		</ul>
		</div>		<div id="recent-posts-2" class="section widget-container widget widget_recent_entries">		<h3 class="widget-title">Recent Posts</h3>		<ul>
					<li>
				<a href="http://blog.skycore.com/2013/06/20/mobile-wallet-detection-launched-for-qr-code-marketers/" title="Mobile Wallet Detection Launched for QR Code&nbsp;Marketers">Mobile Wallet Detection Launched for QR Code&nbsp;Marketers</a>
						</li>
					<li>
				<a href="http://blog.skycore.com/2013/06/20/the-importance-of-mobile-wallet-detection-for-qr-marketing/" title="The Importance of Mobile Wallet Detection for QR&nbsp;Marketing">The Importance of Mobile Wallet Detection for QR&nbsp;Marketing</a>
						</li>
					<li>
				<a href="http://blog.skycore.com/2013/06/15/why-deliver-passbook-passes-via-mms/" title="Why deliver Passbook Passes via&nbsp;MMS?">Why deliver Passbook Passes via&nbsp;MMS?</a>
						</li>
					<li>
				<a href="http://blog.skycore.com/2013/06/13/platform-update-like-to-pass-and-campaign-to-pass-features/" title="Platform Update: Like-to-Pass and Campaign-to-Pass&nbsp;Features">Platform Update: Like-to-Pass and Campaign-to-Pass&nbsp;Features</a>
						</li>
					<li>
				<a href="http://blog.skycore.com/2013/06/12/use-mobile-to-track-cross-channel-marketing/" title="Use Mobile to Track Cross Channel&nbsp;Marketing">Use Mobile to Track Cross Channel&nbsp;Marketing</a>
						</li>
					<li>
				<a href="http://blog.skycore.com/2013/06/10/passbook-pass-location-relevancy-data/" title="Passbook Pass Location Relevancy&nbsp;Data">Passbook Pass Location Relevancy&nbsp;Data</a>
						</li>
					<li>
				<a href="http://blog.skycore.com/2013/06/05/marketing-with-qr-codes-pre-and-post-scan-marketing/" title="Marketing With QR Codes: Pre and Post Scan&nbsp;Marketing">Marketing With QR Codes: Pre and Post Scan&nbsp;Marketing</a>
						</li>
					<li>
				<a href="http://blog.skycore.com/2013/05/23/skycore-announces-cross-carrier-support-for-mms-delivery-of-passbook-passes/" title="Skycore Announces Cross-Carrier Support for MMS Delivery of Passbook&nbsp;Passes">Skycore Announces Cross-Carrier Support for MMS Delivery of Passbook&nbsp;Passes</a>
						</li>
					<li>
				<a href="http://blog.skycore.com/2013/05/22/att-vip-bash-2013/" title="AT&amp;T VIP Bash&nbsp;2013">AT&amp;T VIP Bash&nbsp;2013</a>
						</li>
					<li>
				<a href="http://blog.skycore.com/2013/05/12/platform-update-sms-inbox/" title="Platform Update: SMS&nbsp;Inbox">Platform Update: SMS&nbsp;Inbox</a>
						</li>
					<li>
				<a href="http://blog.skycore.com/2013/05/12/platform-update-new-mms-device-discovery-feature-and-logic/" title="Platform Update: New MMS Device Discovery Feature and&nbsp;Logic">Platform Update: New MMS Device Discovery Feature and&nbsp;Logic</a>
						</li>
					<li>
				<a href="http://blog.skycore.com/2013/05/01/platform-update-instant-pass-on-mobile-web/" title="Platform Update: &#8216;Instant Pass’ on Mobile&nbsp;web">Platform Update: &#8216;Instant Pass’ on Mobile&nbsp;web</a>
						</li>
					<li>
				<a href="http://blog.skycore.com/2013/04/24/what-you-should-have-learned-about-the-tcpa-from-sms-spam-lawsuits/" title="What You Should Have Learned About the TCPA From SMS Spam&nbsp;Lawsuits">What You Should Have Learned About the TCPA From SMS Spam&nbsp;Lawsuits</a>
						</li>
					<li>
				<a href="http://blog.skycore.com/2013/04/19/why-ctia-compliance-is-important-to-mobile-marketers/" title="Why CTIA Compliance is Important to Mobile&nbsp;Marketers">Why CTIA Compliance is Important to Mobile&nbsp;Marketers</a>
						</li>
					<li>
				<a href="http://blog.skycore.com/2013/03/24/skycore-com-is-now-using-responsive-design/" title="Skycore.com is now using Responsive&nbsp;Design">Skycore.com is now using Responsive&nbsp;Design</a>
						</li>
					<li>
				<a href="http://blog.skycore.com/2013/03/22/is-sms-secure/" title="Is SMS&nbsp;Secure?">Is SMS&nbsp;Secure?</a>
						</li>
					<li>
				<a href="http://blog.skycore.com/2013/02/21/skycore-adds-dynamic-passbook-pass-insertion-into-smsmms-email-mobile-web-for-personalized-cards-coupons-and-ids/" title="Skycore Adds Dynamic Passbook Pass Insertion Into SMS/MMS, Email &amp; Mobile Web for Personalized Cards, Coupons and&nbsp;IDs">Skycore Adds Dynamic Passbook Pass Insertion Into SMS/MMS, Email &amp; Mobile Web for Personalized Cards, Coupons and&nbsp;IDs</a>
						</li>
					<li>
				<a href="http://blog.skycore.com/2013/02/20/platform-update-create-and-deliver-passes-for-passbook/" title="Platform Update: Create and Deliver Passes for&nbsp;Passbook">Platform Update: Create and Deliver Passes for&nbsp;Passbook</a>
						</li>
					<li>
				<a href="http://blog.skycore.com/2013/02/17/the-misuse-doctrine-and-helferich/" title="The Misuse Doctrine and Helferich Patent&nbsp;Licensing">The Misuse Doctrine and Helferich Patent&nbsp;Licensing</a>
						</li>
					<li>
				<a href="http://blog.skycore.com/2013/02/11/passwallet-codereadr-now-beam-and-redeem-passes-via-nfc/" title="PassWallet &amp; codeREADr Now Beam and Redeem Passes via&nbsp;NFC">PassWallet &amp; codeREADr Now Beam and Redeem Passes via&nbsp;NFC</a>
						</li>
					<li>
				<a href="http://blog.skycore.com/2013/01/31/apples-latest-update-helps-to-educate-users-on-passbook/" title="Apple’s Latest Update Helps to Educate Users on&nbsp;Passbook">Apple’s Latest Update Helps to Educate Users on&nbsp;Passbook</a>
						</li>
					<li>
				<a href="http://blog.skycore.com/2013/01/31/platform-update-embed-iframes-in-mobile-web-pages-to-display-third-party-content/" title="Platform Update: Embed iFrames in Mobile Web Pages to Display Third Party&nbsp;Content.">Platform Update: Embed iFrames in Mobile Web Pages to Display Third Party&nbsp;Content.</a>
						</li>
					<li>
				<a href="http://blog.skycore.com/2013/01/27/apis-for-sending-sms-and-mms/" title="API’s for sending SMS and&nbsp;MMS">API’s for sending SMS and&nbsp;MMS</a>
						</li>
					<li>
				<a href="http://blog.skycore.com/2013/01/22/platform-update-click-to-call/" title="Platform Update: Click to&nbsp;Call">Platform Update: Click to&nbsp;Call</a>
						</li>
					<li>
				<a href="http://blog.skycore.com/2013/01/16/platform-update-mms-video-size-preview-in-workspace/" title="Platform Update: MMS Video Size Preview in&nbsp;Workspace">Platform Update: MMS Video Size Preview in&nbsp;Workspace</a>
						</li>
					<li>
				<a href="http://blog.skycore.com/2013/01/15/platform-update-email-spam-checker/" title="Platform Update: Spam Check Function for&nbsp;Email">Platform Update: Spam Check Function for&nbsp;Email</a>
						</li>
					<li>
				<a href="http://blog.skycore.com/2012/12/31/nfc-tap-to-coupon-in-retail-and-packaging/" title="NFC Tap to Coupon in Retail and&nbsp;Packaging">NFC Tap to Coupon in Retail and&nbsp;Packaging</a>
						</li>
					<li>
				<a href="http://blog.skycore.com/2012/12/19/the-optimal-resolution-for-your-2013-mms-campaign/" title="The Optimal MMS Image Resolution for Mobile Marketing in&nbsp;2013">The Optimal MMS Image Resolution for Mobile Marketing in&nbsp;2013</a>
						</li>
					<li>
				<a href="http://blog.skycore.com/2012/12/05/platform-update-ftp-sftp-incoming-mms-messages-to-your-server-in-batches/" title="Platform Update: FTP / SFTP Incoming MMS Messages to your Server in&nbsp;Batches">Platform Update: FTP / SFTP Incoming MMS Messages to your Server in&nbsp;Batches</a>
						</li>
					<li>
				<a href="http://blog.skycore.com/2012/12/04/5-ways-to-make-your-mobile-email-campaigns-more-effective/" title="5 Ways to Make Your Mobile Email Campaigns More&nbsp;Effective">5 Ways to Make Your Mobile Email Campaigns More&nbsp;Effective</a>
						</li>
				</ul>
		</div><div id="categories-2" class="section widget-container widget widget_categories"><h3 class="widget-title">Categories</h3>		<ul>
	<li class="cat-item cat-item-273"><a href="http://blog.skycore.com/category/blog/" title="View all posts filed under Blog">Blog</a>
</li>
	<li class="cat-item cat-item-49664"><a href="http://blog.skycore.com/category/case-studies/" title="View all posts filed under Case Studies">Case Studies</a>
</li>
	<li class="cat-item cat-item-12686512"><a href="http://blog.skycore.com/category/platform-updates/" title="View all posts filed under Platform Updates">Platform Updates</a>
</li>
	<li class="cat-item cat-item-30350"><a href="http://blog.skycore.com/category/press-releases/" title="View all posts filed under Press Releases">Press Releases</a>
</li>
	<li class="cat-item cat-item-1"><a href="http://blog.skycore.com/category/uncategorized/" title="View all posts filed under Uncategorized">Uncategorized</a>
</li>
		</ul>
</div><div id="archives-2" class="section widget-container widget widget_archive"><h3 class="widget-title">Archives</h3>		<ul>
			<li><a href='http://blog.skycore.com/2013/06/' title='June 2013'>June 2013</a></li>
	<li><a href='http://blog.skycore.com/2013/05/' title='May 2013'>May 2013</a></li>
	<li><a href='http://blog.skycore.com/2013/04/' title='April 2013'>April 2013</a></li>
	<li><a href='http://blog.skycore.com/2013/03/' title='March 2013'>March 2013</a></li>
	<li><a href='http://blog.skycore.com/2013/02/' title='February 2013'>February 2013</a></li>
	<li><a href='http://blog.skycore.com/2013/01/' title='January 2013'>January 2013</a></li>
	<li><a href='http://blog.skycore.com/2012/12/' title='December 2012'>December 2012</a></li>
	<li><a href='http://blog.skycore.com/2012/11/' title='November 2012'>November 2012</a></li>
	<li><a href='http://blog.skycore.com/2012/10/' title='October 2012'>October 2012</a></li>
	<li><a href='http://blog.skycore.com/2012/09/' title='September 2012'>September 2012</a></li>
	<li><a href='http://blog.skycore.com/2012/08/' title='August 2012'>August 2012</a></li>
	<li><a href='http://blog.skycore.com/2012/07/' title='July 2012'>July 2012</a></li>
	<li><a href='http://blog.skycore.com/2012/06/' title='June 2012'>June 2012</a></li>
	<li><a href='http://blog.skycore.com/2012/05/' title='May 2012'>May 2012</a></li>
	<li><a href='http://blog.skycore.com/2012/04/' title='April 2012'>April 2012</a></li>
	<li><a href='http://blog.skycore.com/2012/03/' title='March 2012'>March 2012</a></li>
	<li><a href='http://blog.skycore.com/2012/02/' title='February 2012'>February 2012</a></li>
	<li><a href='http://blog.skycore.com/2011/12/' title='December 2011'>December 2011</a></li>
	<li><a href='http://blog.skycore.com/2011/09/' title='September 2011'>September 2011</a></li>
	<li><a href='http://blog.skycore.com/2011/08/' title='August 2011'>August 2011</a></li>
	<li><a href='http://blog.skycore.com/2011/07/' title='July 2011'>July 2011</a></li>
	<li><a href='http://blog.skycore.com/2011/06/' title='June 2011'>June 2011</a></li>
	<li><a href='http://blog.skycore.com/2011/05/' title='May 2011'>May 2011</a></li>
	<li><a href='http://blog.skycore.com/2011/03/' title='March 2011'>March 2011</a></li>
	<li><a href='http://blog.skycore.com/2010/12/' title='December 2010'>December 2010</a></li>
	<li><a href='http://blog.skycore.com/2010/10/' title='October 2010'>October 2010</a></li>
	<li><a href='http://blog.skycore.com/2010/09/' title='September 2010'>September 2010</a></li>
	<li><a href='http://blog.skycore.com/2010/08/' title='August 2010'>August 2010</a></li>
	<li><a href='http://blog.skycore.com/2010/06/' title='June 2010'>June 2010</a></li>
	<li><a href='http://blog.skycore.com/2010/01/' title='January 2010'>January 2010</a></li>
	<li><a href='http://blog.skycore.com/2009/07/' title='July 2009'>July 2009</a></li>
	<li><a href='http://blog.skycore.com/2009/05/' title='May 2009'>May 2009</a></li>
	<li><a href='http://blog.skycore.com/2009/04/' title='April 2009'>April 2009</a></li>
	<li><a href='http://blog.skycore.com/2009/03/' title='March 2009'>March 2009</a></li>
	<li><a href='http://blog.skycore.com/2009/02/' title='February 2009'>February 2009</a></li>
	<li><a href='http://blog.skycore.com/2009/01/' title='January 2009'>January 2009</a></li>
	<li><a href='http://blog.skycore.com/2008/11/' title='November 2008'>November 2008</a></li>
	<li><a href='http://blog.skycore.com/2008/08/' title='August 2008'>August 2008</a></li>
	<li><a href='http://blog.skycore.com/2008/07/' title='July 2008'>July 2008</a></li>
	<li><a href='http://blog.skycore.com/2008/03/' title='March 2008'>March 2008</a></li>
	<li><a href='http://blog.skycore.com/2008/02/' title='February 2008'>February 2008</a></li>
	<li><a href='http://blog.skycore.com/2008/01/' title='January 2008'>January 2008</a></li>
	<li><a href='http://blog.skycore.com/2007/12/' title='December 2007'>December 2007</a></li>
	<li><a href='http://blog.skycore.com/2007/11/' title='November 2007'>November 2007</a></li>
	<li><a href='http://blog.skycore.com/2007/09/' title='September 2007'>September 2007</a></li>
		</ul>
</div></div><!--# sidebar -->
</div><!--#container-->

<div id="footer">

	<div id="footer-menu">

		
	</div>

	<div id="footer-credit">
		<a href="http://wordpress.com/?ref=footer" rel="generator">Blog at WordPress.com</a>.
		<a href="http://theme.wordpress.com/credits/blog.skycore.com/" title="Learn about customizing this theme with the Custom Design upgrade">Customized Shaan Theme</a>. 	</div>

</div><!--#footer-->

<div class="clear"></div>
</div><!--#wrapper -->

<!-- Do not remove this, it's required for certain plugins which generally use this hook to reference JavaScript files. -->

<script type="text/javascript">
var _qevents = _qevents || [], wpcomQuantcastData = {"qacct":"p-18-mFEk4J448M","labels":",language.en,type.wpcom"};
function wpcomQuantcastPixel( labels, options ) {
	var i, defaults = wpcomQuantcastData, data = { event: 'ajax' };

	labels  = labels  || '';
	options = options || {};

	if ( typeof labels != 'string' )
		options = labels;

	for ( i in defaults ) {
		data[i] = defaults[i];
	}

	for ( i in options ) {
		data[i] = options[i];
	}

	if ( data.labels ) {
		data.labels += ',' + labels;
	} else {
		data.labels = labels;
	}

	_qevents.push( data );
};
(function() {var elem = document.createElement('script');elem.src = (document.location.protocol == "https:" ? "https://secure" : "http://edge") + ".quantserve.com/quant.js";elem.async = true;elem.type = "text/javascript";var scpt = document.getElementsByTagName('script')[0];scpt.parentNode.insertBefore(elem, scpt);  })();
_qevents.push( wpcomQuantcastData );
</script>
<noscript><div style="display: none;"><img src="//pixel.quantserve.com/pixel/p-18-mFEk4J448M.gif?labels=%2Clanguage.en%2Ctype.wpcom" height="1" width="1" alt="" /></div></noscript>

<script type='text/javascript' src='//0.gravatar.com/js/gprofiles.js?ver=201327ac'></script>
<script type='text/javascript'>
/* <![CDATA[ */
var WPGroHo = {"my_hash":""};
/* ]]> */
</script>
<script type='text/javascript' src='http://s0.wp.com/wp-content/mu-plugins/gravatar-hovercards/wpgroho.js?m=1351637563g'></script>
<script>jQuery(document).ready(function($){ Gravatar.profile_cb = function( h, d ) { WPGroHo.syncProfileData( h, d );	}; Gravatar.my_hash = WPGroHo.my_hash; Gravatar.init( 'body', '#wp-admin-bar-my-account' ); });</script>	<div style="display:none">
	</div>
<script type='text/javascript'>
/* <![CDATA[ */
var HighlanderComments = {"loggingInText":"Logging In\u2026","submittingText":"Posting Comment\u2026","postCommentText":"Post Comment","connectingToText":"Connecting to %s","commentingAsText":"%1$s: You are commenting using your %2$s account.","logoutText":"Log Out","loginText":"Log In","connectURL":"http:\/\/blogskycore.wordpress.com\/public.api\/connect\/?action=request","logoutURL":"http:\/\/blogskycore.wordpress.com\/wp-login.php?action=logout&_wpnonce=dd7d4b108a","homeURL":"http:\/\/blog.skycore.com\/","postID":"709","gravDefault":"identicon","enterACommentError":"Please enter a comment","enterEmailError":"Please enter your email address here","invalidEmailError":"Invalid email address","enterAuthorError":"Please enter your name here","gravatarFromEmail":"This picture will show whenever you leave a comment. Click to customize it.","logInToExternalAccount":"Log in to use details from one of these accounts.","change":"Change","changeAccount":"Change Account","comment_registration":"","userIsLoggedIn":"","isJetpack":"0"};
/* ]]> */
</script>
<script type='text/javascript' src='http://s2.wp.com/_static/??/wp-content/js/jquery/jquery.autoresize.js,/wp-content/mu-plugins/highlander-comments/script.js?m=1369800175j'></script>

	<script type="text/javascript">
		WPCOM_sharing_counts = {"http:\/\/blog.skycore.com\/skycore-api-v1-3-appendix-b\/":709}	</script>
	<div id="sharing_email" style="display: none;">
		<form action="/skycore-api-v1-3-appendix-b/" method="post">
			<label for="target_email">Send to Email Address</label>
			<input type="text" name="target_email" id="target_email" value="" />

			
				<label for="source_name">Your Name</label>
				<input type="text" name="source_name" id="source_name" value="" />

				<label for="source_email">Your Email Address</label>
				<input type="text" name="source_email" id="source_email" value="" />

			
			<div class="recaptcha" id="sharing_recaptcha"></div><input type="hidden" name="recaptcha_public_key" id="recaptcha_public_key" value="6LcYW8MSAAAAADBAuEH9yaPcF7lWh11Iq62ZKtoo" />
			<img style="float: right; display: none" class="loading" src="http://s2.wp.com/wp-content/mu-plugins/post-flair/sharing/images/loading.gif?m=1315610318g" alt="loading" width="16" height="16" />
			<input type="submit" value="Send Email" class="sharing_send" />
			<a href="#cancel" class="sharing_cancel">Cancel</a>

			<div class="errors errors-1" style="display: none;">
				Post was not sent - check your email addresses!			</div>

			<div class="errors errors-2" style="display: none;">
				Email check failed, please try again			</div>

			<div class="errors errors-3" style="display: none;">
				Sorry, your blog cannot share posts by email.			</div>
		</form>
	</div>
		<script type="text/javascript">
		jQuery(document).on( 'ready post-load', function(){
			jQuery( 'a.share-twitter' ).on( 'click', function() {
				window.open( jQuery(this).attr( 'href' ), 'wpcomtwitter', 'menubar=1,resizable=1,width=600,height=350' );
				return false;
			});
		});
		</script>
				<script type="text/javascript">
		jQuery(document).on( 'ready post-load', function(){
			jQuery( 'a.share-linkedin' ).on( 'click', function() {
				window.open( jQuery(this).attr( 'href' ), 'wpcomlinkedin', 'menubar=1,resizable=1,width=580,height=450' );
				return false;
			});
		});
		</script>
				<script type="text/javascript">
		jQuery(document).on( 'ready post-load', function(){
			jQuery( 'a.share-facebook' ).on( 'click', function() {
				window.open( jQuery(this).attr( 'href' ), 'wpcomfacebook', 'menubar=1,resizable=1,width=600,height=400' );
				return false;
			});
		});
		</script>
				<script type="text/javascript">
		jQuery(document).on( 'ready post-load', function(){
			jQuery( 'a.share-google-plus-1' ).on( 'click', function() {
				window.open( jQuery(this).attr( 'href' ), 'wpcomgoogle-plus-1', 'menubar=1,resizable=1,width=600,height=600' );
				return false;
			});
		});
		</script>
				<iframe src='http://widgets.wp.com/likes/master.html?ver=20130620a#ver=20130620a&amp;mp6=1' scrolling='no' id='likes-master' name='likes-master' style='display:none;'></iframe>
		<div id='likes-other-gravatars'><div class="likes-text"><span>%d</span> bloggers like this:</div><ul class="wpl-avatars sd-like-gravatars"></ul></div>
		<script type="text/javascript">
		//<![CDATA[
			var jetpackLikesWidgetQueue = [];
			var jetpackLikesMasterReady = false;

			function JetpackLikespostMessage( message, target ) {
				if ( "string" === typeof message ){
					try{
						message = JSON.parse( message );
					}
					catch(e) {
						return;
					}
				}

				pm( {
					target: target,
					type: 'likesMessage',
					data: message,
					origin: '*'
				} );
			}

			function JetpackLikesMessageListener( event ) {
				if ( "undefined" == typeof event.event )
					return;

				if ( 'masterReady' == event.event ) {
					jQuery( document ).ready( function() {
						jetpackLikesMasterReady = true;

						var stylesData = {
								event: 'injectStyles'
						};

						if ( jQuery( 'iframe.admin-bar-likes-widget' ).length > 0 ) {
							JetpackLikespostMessage( { event: 'adminBarEnabled' }, window.frames[ 'likes-master' ] );

							stylesData.adminBarStyles = {
								background: jQuery( '#wpadminbar .quicklinks li#wp-admin-bar-wpl-like > a' ).css( 'background' )
							};
						}

						if ( !window.addEventListener )
							jQuery( '#wp-admin-bar-admin-bar-likes-widget' ).hide();

						stylesData.textStyles = {
							color: jQuery( '.sd-text-color').css( 'color' ),
							fontFamily: jQuery( '.sd-text-color' ).css( 'font-family' ),
							fontSize: jQuery( '.sd-text-color' ).css( 'font-size' ),
							direction: jQuery( '.sd-text-color' ).css( 'direction' ),
							fontWeight: jQuery( '.sd-text-color' ).css( 'font-weight' ),
							fontStyle: jQuery( '.sd-text-color' ).css( 'font-style' ),
							textDecoration: jQuery( '.sd-text-color' ).css('text-decoration')
						};

						stylesData.linkStyles = {
							color: jQuery( '.sd-link-color' ).css('color'),
							fontFamily: jQuery( '.sd-link-color' ).css('font-family'),
							fontSize: jQuery( '.sd-link-color' ).css('font-size'),
							textDecoration: jQuery( '.sd-link-color' ).css('text-decoration'),
							fontWeight: jQuery( '.sd-link-color' ).css( 'font-weight' ),
							fontStyle: jQuery( '.sd-link-color' ).css( 'font-style' )
						};

						JetpackLikespostMessage( stylesData, window.frames[ 'likes-master' ] );

						var requests = [];
						jQuery( '.jetpack-likes-widget-wrapper' ).each( function( i ) {
							var regex = /like-(post|comment)-wrapper-(\d+)-(\d+)-(\w+)/;
							var match = regex.exec( this.id );
							if ( ! match || match.length != 5 )
								return;

							var info = {
								blog_id: match[2],
								width:   this.width
							};

							if ( 'post' == match[1] ) {
								info.post_id = match[3];
							} else if ( 'comment' == match[1] ) {
								info.comment_id = match[3];
							}

							info.obj_id = match[4];

							requests.push( info );
						});

						JetpackLikespostMessage( { event: 'initialBatch', requests: requests }, window.frames['likes-master'] );

						jQuery( document ).on( 'inview', 'div.jetpack-likes-widget-unloaded', function() {
							jetpackLikesWidgetQueue.push( this.id );
						});
					});
				}

				if ( 'showLikeWidget' == event.event ) {
					setTimeout( JetpackLikesWidgetQueueHandler, 10 );
					jQuery( '#' + event.id + ' .post-likes-widget-placeholder'  ).fadeOut( 'fast', function() {
						jQuery( '#' + event.id + ' .post-likes-widget' ).fadeIn( 'fast', function() {
							JetpackLikespostMessage( { event: 'likeWidgetDisplayed', blog_id: event.blog_id, post_id: event.post_id, obj_id: event.obj_id }, window.frames['likes-master'] );
						});
					});
				}

				if ( 'showOtherGravatars' == event.event ) {
					var $container = jQuery( '#likes-other-gravatars' );
					var $list = $container.find( 'ul' );

					$container.hide();
					$list.html( '' );

					$container.find( '.likes-text span' ).text( event.total );

					jQuery.each( event.likers, function( i, liker ) {
						$list.append( '<li class="' + liker.css_class + '"><a href="' + liker.profile_URL + '" class="wpl-liker" rel="nofollow" target="_parent"><img src="' + liker.avatar_URL + '" alt="' + liker.name + '" width="30" height="30" style="padding-right: 3px;" /></a></li>');
					} );

					var offset = jQuery( "[name='" + event.parent + "']" ).offset();

					$container.css( 'left', offset.left + event.position.left - 10 + 'px' );
					$container.css( 'top', offset.top + event.position.top - 33 + 'px' );

					var rowLength = Math.floor( event.width / 37 );
					var height = ( Math.ceil( event.likers.length / rowLength ) * 37 ) + 13;
					if ( height > 204 ) {
						height = 204;
					}

					$container.css( 'height', height + 'px' );
					$container.css( 'width', rowLength * 37 - 7 + 'px' );

					$list.css( 'width', rowLength * 37 + 'px' );

					$container.fadeIn( 'slow' );

					var scrollbarWidth = $list[0].offsetWidth - $list[0].clientWidth;
					if ( scrollbarWidth > 0 ) {
						$container.width( $container.width() + scrollbarWidth );
						$list.width( $list.width() + scrollbarWidth );
					}
				}
			}

			pm.bind( 'likesMessage', function(e) { JetpackLikesMessageListener(e); } );

			jQuery( document ).click( function( e ) {
				var $container = jQuery( '#likes-other-gravatars' );

				if ( $container.has( e.target ).length === 0 ) {
					$container.fadeOut( 'slow' );
				}
			});

			function JetpackLikesWidgetQueueHandler() {
				var wrapperID;
				if ( ! jetpackLikesMasterReady ) {
					setTimeout( JetpackLikesWidgetQueueHandler, 500 );
					return;
				}

				if ( jetpackLikesWidgetQueue.length > 0 ) {
					// We may have a widget that needs creating now
					var found = false;
					while( jetpackLikesWidgetQueue.length > 0 ) {
						// Grab the first member of the queue that isn't already loading.
						wrapperID = jetpackLikesWidgetQueue.splice( 0, 1 )[0];
						if ( jQuery( '#' + wrapperID ).hasClass( 'jetpack-likes-widget-unloaded' ) ) {
							found = true;
							break;
						}
					}
					if ( ! found ) {
						setTimeout( JetpackLikesWidgetQueueHandler, 500 );
						return;
					}
				} else if ( jQuery( 'div.jetpack-likes-widget-unloaded' ).length > 0 ) {
					// Get the next unloaded widget
					wrapperID = jQuery( 'div.jetpack-likes-widget-unloaded' ).first()[0].id;
					if ( ! wrapperID ) {
						// Everything is currently loaded
						setTimeout( JetpackLikesWidgetQueueHandler, 500 );
						return;
					}
				}

				var $wrapper = jQuery( '#' + wrapperID );
				$wrapper.find( 'iframe' ).remove();

				if ( $wrapper.hasClass( 'slim-likes-widget' ) ) {
					$wrapper.find( '.post-likes-widget-placeholder' ).after( "<iframe class='post-likes-widget jetpack-likes-widget' name='" + $wrapper.data( 'name' ) + "' height='22px' width='68px' frameBorder='0' scrolling='no' src='" + $wrapper.data( 'src' ) + "'></iframe>" );
				} else {
					$wrapper.find( '.post-likes-widget-placeholder' ).after( "<iframe class='post-likes-widget jetpack-likes-widget' name='" + $wrapper.data( 'name' ) + "' height='55px' width='100%' frameBorder='0' src='" + $wrapper.data( 'src' ) + "'></iframe>" );
				}

				$wrapper.removeClass( 'jetpack-likes-widget-unloaded' ).addClass( 'jetpack-likes-widget-loading' );

				$wrapper.find( 'iframe' ).load( function( e ) {
					var $iframe = jQuery( e.target );
					$wrapper.removeClass( 'jetpack-likes-widget-loading' ).addClass( 'jetpack-likes-widget-loaded' );

					JetpackLikespostMessage( { event: 'loadLikeWidget', name: $iframe.attr( 'name' ), width: $iframe.width() }, window.frames[ 'likes-master' ] );

					if ( $wrapper.hasClass( 'slim-likes-widget' ) ) {
						$wrapper.find( 'iframe' ).Jetpack( 'resizeable' );
					}
				});
				setTimeout( JetpackLikesWidgetQueueHandler, 250 );
			}
			JetpackLikesWidgetQueueHandler();
		//]]>
		</script>
<script type='text/javascript'>
/* <![CDATA[ */
var recaptcha_options = {"lang":"en"};
/* ]]> */
</script>
<script type='text/javascript' src='http://s0.wp.com/_static/??/wp-content/js/devicepx.js,/wp-content/mu-plugins/post-flair/sharing/sharing.js?m=1372783419j'></script>
<script type="text/javascript">
// <![CDATA[
(function() {
try{
  if ( window.external &&'msIsSiteMode' in window.external) {
    if (window.external.msIsSiteMode()) {
      var jl = document.createElement('script');
      jl.type='text/javascript';
      jl.async=true;
      jl.src='/wp-content/plugins/ie-sitemode/custom-jumplist.php';
      var s = document.getElementsByTagName('script')[0];
      s.parentNode.insertBefore(jl, s);
    }
  }
}catch(e){}
})();
// ]]>
</script><script src="http://s.stats.wordpress.com/w.js?21" type="text/javascript"></script>
<script type="text/javascript">
st_go({'blog':'30180251','v':'wpcom','tz':'-4','user_id':'0','post':'709','subd':'blogskycore'});
ex_go({'crypt':'UE40eW5QN0p8M2Y/RE1LVmwrVi5vQS5fVFtfdHBbPyw1VXIrU3hWLHhmcmw0bWUwNis5Vk1qSEpzeXBoR2E/dmFIcl9HLjd1TGgrJm9kalImVUZGNEZjYjVlR1gseHYlYnEsJU1POUJZa0dXUU5JUndCTEcwN01HZD1ocnlyUk1yaXpWbS8vMzNsWmF0SnUmWWpDN1ZpUkd3Q0dyPVQmbS1QWiY3fHNvUTN6aW1WSDh+Q0lIMltfK0NKVS1NM29HSFYxZi0/dVpfekZQLW9KT2guMDBSVXpwZXRmcUdwMiZlbEpDN1RROXZKMDclJW5nZkd6fnB0TjBvYyVjcUdLXzB0Yjd2QUJIdmJLNTAwOXIuS05ZLGpUQnk0Y3E1'});
addLoadEvent(function(){linktracker_init('30180251',709);});
	</script>
<noscript><img src="http://stats.wordpress.com/b.gif?v=noscript" style="height:0px;width:0px;overflow:hidden" alt="" /></noscript>
<script>
if ( 'object' === typeof wpcom_mobile_user_agent_info ) {

	wpcom_mobile_user_agent_info.init();
	var mobileStatsQueryString = "";
	
	if( false !== wpcom_mobile_user_agent_info.matchedPlatformName )
		mobileStatsQueryString += "&x_" + 'mobile_platforms' + '=' + wpcom_mobile_user_agent_info.matchedPlatformName;
	
	if( false !== wpcom_mobile_user_agent_info.matchedUserAgentName )
		mobileStatsQueryString += "&x_" + 'mobile_devices' + '=' + wpcom_mobile_user_agent_info.matchedUserAgentName;
	
	if( wpcom_mobile_user_agent_info.isIPad() )
		mobileStatsQueryString += "&x_" + 'ipad_views' + '=' + 'views';

	if( "" != mobileStatsQueryString ) {
		new Image().src = document.location.protocol + '//stats.wordpress.com/g.gif?v=wpcom-no-pv' + mobileStatsQueryString + '&baba=' + Math.random();
	}
	
}
</script>
</body>
</html>
