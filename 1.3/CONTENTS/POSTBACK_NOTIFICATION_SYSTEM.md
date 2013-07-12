<meta property="og:description" content="Overview: Postback Notification System The Postback system notifies remote servers about different events related to the account. For each event, a notification in XML format is inserted into a Pos..." />
<meta property="og:site_name" content="Skycore Mobile Blog" />
<meta name="twitter:site" content="@wordpressdotcom" />
<meta name="twitter:card" content="summary" />
<meta name="twitter:creator" content="@wordpressdotcom" />
<link rel="shortcut icon" type="image/x-icon" href="http://s2.wp.com/i/favicon.ico?m=1311975824g" sizes="16x16 24x24 32x32 48x48" />
<link rel="icon" type="image/x-icon" href="http://s2.wp.com/i/favicon.ico?m=1311975824g" sizes="16x16 24x24 32x32 48x48" />
<link rel="apple-touch-icon-precomposed" href="http://s0.wp.com/i/webclip.png?m=1355642671g" />
<link rel='openid.server' href='http://blogskycore.wordpress.com/?openidserver=1' />
<link rel='openid.delegate' href='http://blogskycore.wordpress.com/' />
<link rel="search" type="application/opensearchdescription+xml" href="http://blog.skycore.com/osd.xml" title="Skycore Mobile Blog" />
<link rel="search" type="application/opensearchdescription+xml" href="http://wordpress.com/opensearch.xml" title="WordPress.com" />
  	<style>
		/* <![CDATA[ */
		/* Block: reblog */
		
		.reblog-from img                   { margin: 0 10px 0 0; vertical-align: middle; padding: 0; border: 0; }
		.reblogger-note img.avatar         { float: left; padding: 0; border: 0; }
		.reblogger-note-content            { margin: 0 0 20px; }
		.reblog-post .wpcom-enhanced-excerpt-content { border-left: 3px solid #eee; padding-left: 15px; }
		.reblog-post ul.thumb-list         { display: block; list-style: none; margin: 2px 0; padding: 0; clear: both; }
		.reblog-post ul.thumb-list li      { display: inline; margin: 0; padding: 0 1px; border: 0; }
		.reblog-post ul.thumb-list li a    { margin: 0; padding: 0; border: 0; }
		.reblog-post ul.thumb-list li img  { margin: 0; padding: 0; border: 0; }
		
		.reblog-post .wpcom-enhanced-excerpt { clear: both; }
		
		.reblog-post .wpcom-enhanced-excerpt address,
		.reblog-post .wpcom-enhanced-excerpt li,
		.reblog-post .wpcom-enhanced-excerpt h1,
		.reblog-post .wpcom-enhanced-excerpt h2,
		.reblog-post .wpcom-enhanced-excerpt h3,
		.reblog-post .wpcom-enhanced-excerpt h4,
		.reblog-post .wpcom-enhanced-excerpt h5,
		.reblog-post .wpcom-enhanced-excerpt h6,
		.reblog-post .wpcom-enhanced-excerpt p { font-size: 100% !important; }
		
		.reblog-post .wpcom-enhanced-excerpt blockquote,
		.reblog-post .wpcom-enhanced-excerpt pre,
		.reblog-post .wpcom-enhanced-excerpt code,
		.reblog-post .wpcom-enhanced-excerpt q { font-size: 98% !important; }
		

		/* ]]> */
		</style>
		<meta name="application-name" content="Skycore Mobile Blog" /><meta name="msapplication-window" content="width=device-width;height=device-height" /><meta name="msapplication-task" content="name=Subscribe;action-uri=http://blog.skycore.com/feed/;icon-uri=http://s2.wp.com/i/favicon.ico" /><meta name="msapplication-task" content="name=Sign up for a free blog;action-uri=http://wordpress.com/signup/;icon-uri=http://s2.wp.com/i/favicon.ico" /><meta name="msapplication-task" content="name=WordPress.com Support;action-uri=http://support.wordpress.com/;icon-uri=http://s2.wp.com/i/favicon.ico" /><meta name="msapplication-task" content="name=WordPress.com Forums;action-uri=http://forums.wordpress.com/;icon-uri=http://s2.wp.com/i/favicon.ico" /><meta name="title" content="Skycore API v1.3 Postback API&nbsp;Documentation | Skycore Mobile Blog on WordPress.com" />
<meta name="description" content="" />
		<style type="text/css">

					#site-title {
				width: 950px;
			}
			#site-description {
				display: none;
			}
		
		
				</style>
	<style type="text/css" id="custom-background-css">
body.custom-background { background-color: #F8F8F8; background-image: url('http://blogskycore.files.wordpress.com/2013/01/blog-bg1.png'); background-repeat: repeat-x; background-position: top left; background-attachment: scroll; }
</style>
<style id="syntaxhighlighteranchor"></style>
<script type="text/javascript">
(function(doc) {
	var config = { kitId: 'lre5qja', scriptTimeout: 3000 },
	h=doc.getElementsByTagName("html")[0];h.className+=" wf-loading";var t=setTimeout(function(){h.className=h.className.replace(/(\s|^)wf-loading(\s|$)/g," ");h.className+="wf-inactive"},config.scriptTimeout);var tk=doc.createElement("script"),d=false;tk.src='//use.typekit.net/'+config.kitId+'.js';tk.type="text/javascript";tk.async="true";tk.onload=tk.onreadystatechange=function(){var a=this.readyState;if(d||a&&a!="complete"&&a!="loaded")return;d=true;clearTimeout(t);try{Typekit.load(config)}catch(b){}};var s=doc.getElementsByTagName("script")[0];s.parentNode.insertBefore(tk,s)
})(document);
</script>
<style type="text/css">/* Site Title */ .wf-loading #site-title { visibility: hidden; } .wf-active #site-title { font-family: arimo-1,arimo-2,"Molengo","Lucida Sans Unicode","Lucida Grande",Garuda,sans-serif; font-style: normal; font-weight: 700; font-variant: normal; } 
/* Headings */ .wf-loading h1,.wf-loading h2,.wf-loading h3,.wf-loading h4,.wf-loading h5,.wf-loading h6 { visibility: hidden; } .wf-active h1,.wf-active h2,.wf-active h3,.wf-active h4,.wf-active h5,.wf-active h6 { font-family: arimo-1,arimo-2,"Lucida Sans Unicode","Lucida Grande",Garuda,sans-serif; font-style: normal; font-weight: 700; font-variant: normal; } .wf-loading .post-title { visibility: hidden; } .wf-active .post-title { font-family: arimo-1,arimo-2,"Molengo","Lucida Sans Unicode","Lucida Grande",Garuda,sans-serif; font-style: normal; font-weight: 700; font-variant: normal; } .wf-loading .page-title { visibility: hidden; } .wf-active .page-title { font-family: arimo-1,arimo-2,"Molengo","Lucida Sans Unicode","Lucida Grande",Garuda,sans-serif; font-style: normal; font-weight: 700; font-variant: normal; } .wf-loading #entry-author-info h2 { visibility: hidden; } .wf-active #entry-author-info h2 { font-weight: 700; } .wf-loading #sidebar .section h3 { visibility: hidden; } .wf-active #sidebar .section h3 { font-family: arimo-1,arimo-2,"Molengo","Lucida Sans Unicode","Lucida Grande",Garuda,sans-serif; font-style: normal; font-weight: 700; font-variant: normal; } 
/* Body Text */ .wf-loading body { visibility: hidden; } .wf-active body { font-family: ff-basic-gothic-web-pro-1,ff-basic-gothic-web-pro-2,Arial,Helvetica,Verdana,"Lucida Sans Unicode","Lucida Grande",Garuda,sans-serif; font-variant: normal; } .wf-loading #access { visibility: hidden; } .wf-active #access { font-family: ff-basic-gothic-web-pro-1,ff-basic-gothic-web-pro-2,Helvetica,Arial,sans-serif; font-variant: normal; } .wf-loading #access li a { visibility: hidden; } .wf-active #access li a { font-family: ff-basic-gothic-web-pro-1,ff-basic-gothic-web-pro-2,"AvenirBold","Helvetica Neue",Arial,Helvetica,Geneva,sans-serif; font-variant: normal; } .wf-loading #header { visibility: hidden; } .wf-active #header { font-family: ff-basic-gothic-web-pro-1,ff-basic-gothic-web-pro-2,"Lucida Sans Unicode","Lucida Grande",Garuda,sans-serif; font-variant: normal; } .wf-loading #site-description { visibility: hidden; } .wf-active #site-description { font-family: ff-basic-gothic-web-pro-1,ff-basic-gothic-web-pro-2,Cantarell,"Lucida Sans Unicode","Lucida Grande",Garuda,sans-serif; font-variant: normal; } .wf-loading #content a.more-link { visibility: hidden; } .wf-active #content a.more-link { font-family: ff-basic-gothic-web-pro-1,ff-basic-gothic-web-pro-2,"Lucida Sans Unicode","Lucida Grande",Garuda,sans-serif; font-variant: normal; } .wf-loading .page-link { visibility: hidden; } .wf-active .page-link { font-family: ff-basic-gothic-web-pro-1,ff-basic-gothic-web-pro-2,"Lucida Sans Unicode","Lucida Grande",Garuda,sans-serif; font-variant: normal; } 
</style>
		<link rel="stylesheet" id="custom-css-css" type="text/css" href="http://s0.wp.com/?custom-css=1&#038;csblog=22Dgf&#038;cscache=6&#038;csrev=98" />
		</head>

<body class="page page-id-953 page-template-default custom-background typekit-enabled mp6 highlander-enabled highlander-light">

<div id="access">
	<div class="menu-header"><ul id="menu-headermenu" class="menu"><li id="menu-item-371" class="menu-item menu-item-type-custom menu-item-object-custom menu-item-371"><a title="www.skycore.com" href="http://www.skycore.com/index.php"></a></li>
<li id="menu-item-372" class="menu-item menu-item-type-custom menu-item-object-custom menu-item-372"><a title="Sign in" href="http://www.skycore.com/login.php">Sign in</a></li>
<li id="menu-item-373" class="menu-item menu-item-type-custom menu-item-object-custom menu-item-373"><a title="Free Trial" href="http://www.skycore.com/signup.php">Free Trial</a></li>
<li id="menu-item-379" class="menu-item menu-item-type-custom menu-item-object-custom menu-item-379"><a title="Blog" href="http://blog.skycore.com/category/press-releases/">Blog</a></li>
<li id="menu-item-465" class="menu-item menu-item-type-custom menu-item-object-custom menu-item-465"><a title="Pricing" href="http://www.skycore.com/plans_and_pricing.php">Pricing</a></li>
<li id="menu-item-778" class="menu-item menu-item-type-custom menu-item-object-custom menu-item-778"><a title="Features" href="http://www.skycore.com/messaging-tools.php">Features</a></li>
</ul></div></div><!-- #access -->

<div id="wrapper" class="clearfix">
			<div id="header">
			<h1 id="site-title"><a href="http://blog.skycore.com/" title="Skycore Mobile Blog" rel="home">Skycore Mobile Blog</a></h1>
			<div id="site-description"></div>
		</div><!-- #header -->
	
<div id="container">

	<div id="content" class="narrow">

	
		
			<div id="post-953" class="post-953 page type-page status-publish hentry post">

				
				<h1 class="post-title">Skycore API v1.3 Postback API&nbsp;Documentation</h1>
				<div id="page-content"><h1>Overview: Postback Notification System</h1>
<p>The Postback system notifies remote servers about different events related to the account. For each event, a notification in XML format is inserted into a Postback queue. The  notifications in the Postback queue are processed as a batch every minute. The notifications for each account are batched together and wrapped with &lt;POSTBACK&gt; XML tag then sent in one HTTP request to the Postback URL. The Postback URL is an address on your server where you would like to receive these notifications and is defined in your API Account settings. If establishing a connection to the Postback URL takes longer than 10 seconds, the connection will time out and fail. if establishing a connection is successful, we expect the remote server to respond with a properly formed HTTP header containing 200 HTTP code. If no HTTP response is provided or the HTTP code is not 200, we consider the Postback Notification a failed request and will retry five minutes later up to five times.</p>
<h1>Postback Groups</h1>
<p>Our servers generate different Postbacks, which we divide into three groups. There are sub-groups within each Postback group. Each postback contain few unified fields:</p>
<p>NOTIFICATION id &#8211; unique ID of each notification</p>
<p>NOTIFICATION created -  timestamp when postback is generated</p>
<p>ORIGIN &#8211; identifies origin of the postback</p>
<p>CODE &#8211; identifies situation when postback is generated</p>
<p>BODY &#8211; postback body, different for each ORIGIN/CODE &#8211; this will be described for each case.</p>
<p><strong>Group #1- SMS</strong></p>
<p><strong>a) Synopsis: </strong>This Postback provides a notification when the SMS is sent out from our server. Inside the postback BODY we have following information:</p>
<p>HISTORYID &#8211; ID in our history. This postback can be matched with history report using this field.</p>
<p>TO &#8211; SMS receiver</p>
<p>TRACKINGID &#8211; ID returned via API &#8211; this postback can be matched with API response using this field.</p>
<p>TIMESTAMP &#8211; timestamp of the SMS was sent</p>
<p><strong>Postback Notification Example:</strong></p>
<p><small><code>&lt;NOTIFICATION id="521395" created="2012-06-07 04:52:07.563447-04"&gt;<br />
&lt;ORIGIN&gt;SMS_MT&lt;/ORIGIN&gt;<br />
&lt;CODE&gt;N201&lt;/CODE&gt;<br />
&lt;BODY&gt;<br />
&lt;HISTORYID&gt;455795&lt;/HISTORYID&gt;<br />
&lt;TO&gt;16501112222&lt;/TO&gt;<br />
&lt;TRACKINGID&gt;SMS_45695&lt;/TRACKINGID&gt;<br />
&lt;TIMESTAMP&gt;2012-06-07 04:52:07.374174-04&lt;/TIMESTAMP&gt;<br />
&lt;/BODY&gt;<br />
&lt;/NOTIFICATION&gt;<br />
</code></small></p>
<p><strong>b) Synopsis:</strong> This Postback provides a notification about the status of an SMS. Inside the postback BODY we have following information:</p>
<p>HISTORYID &#8211; ID in our history. This postback can be matched with history report using this field.</p>
<p>TO &#8211; SMS receiver</p>
<p>TRACKINGID &#8211; ID returned via API &#8211; this postback can be matched with API response using this field.</p>
<p>TIMESTAMP &#8211; timestamp of the SMS was sent</p>
<p>STATUS protocole/status &#8211; this is actual status of the SMS &#8211; to understand that values please reffer to API documentation APPENDIX B part iii.</p>
<p><strong>Postback Notification Example:</strong></p>
<p><code><small>&lt;NOTIFICATION id="521396" created="2012-06-07 04:55:09.985645-04"&gt;<br />
&lt;ORIGIN&gt;SMS_MT&lt;/ORIGIN&gt;<br />
&lt;CODE&gt;N202&lt;/CODE&gt;<br />
&lt;BODY&gt;<br />
&lt;HISTORYID&gt;455801&lt;/HISTORYID&gt;<br />
&lt;TO&gt;16501112222&lt;/TO&gt;<br />
&lt;TRACKINGID&gt;SMS_45697&lt;/TRACKINGID&gt;<br />
&lt;STATUS protocole="3" status="1"/&gt;<br />
&lt;TIMESTAMP&gt;2012-06-07 04:55:09.90765-04&lt;/TIMESTAMP&gt;<br />
&lt;/BODY&gt;<br />
&lt;/NOTIFICATION&gt;<br />
</small></code></p>
<p><strong>c) Synopsis: </strong>This Postback provides a notification when SMS MO is received. Inside the postback BODY we have following information:</p>
<p>FROM &#8211; SMS sender mobile number</p>
<p>TO &#8211; shortcode the SMS was sent to</p>
<p>TEXT &#8211; this is actuall text that was sent by the sender</p>
<p>RECEIVED &#8211; timestamp of the SMS received by our server</p>
<p><strong>Postback Notification Example:</strong></p>
<p><small><code>&lt;NOTIFICATION id="521495" created="2012-04-16 09:05:56.954258-04"&gt;<br />
&lt;ORIGIN&gt;SMS_MO&lt;/ORIGIN&gt;<br />
&lt;CODE&gt;N211&lt;/CODE&gt;<br />
&lt;BODY&gt;<br />
&lt;FROM&gt;16311112222&lt;/FROM&gt;<br />
&lt;TO&gt;60856&lt;/TO&gt;<br />
&lt;TEXT&gt;MYKEYCODE&lt;/TEXT&gt;<br />
&lt;RECEIVED&gt;2012-04-16 09:05:56.153785-04&lt;/RECEIVED&gt;<br />
&lt;/BODY&gt;<br />
&lt;/NOTIFICATION&gt;<br />
</code></small></p>
<p><strong>Group #2-MMS</strong></p>
<p>For MMS, we have two methods for delivering content. In addition, we send different Postbacks depending on which method is used.</p>
<p><strong>a) The Binary Method</strong></p>
<p>In binary sending, we deliver a Postback notification called &#8220;N101&#8243; immediately after we begin to process the MMS. Upon receiving Delivery Report (DLR), the system generates Postback notification &#8220;N102&#8243; with the handset name. N101 and N102 notifications are linked by both an ID in our history table (HISTORYID) and a sending que ID (TRACKINGID). Inside BODY element those postbacks contain following fields:</p>
<p>HISTORYID &#8211; ID in our history. This postback can be matched with history report using this field.</p>
<p>MMSID &#8211; ID of the MMS</p>
<p>TO &#8211; MMS receiver</p>
<p>SPID &#8211; carrier ID &#8211; please check API documentation Appendinx E</p>
<p>TRACKINGID &#8211; ID returned via API &#8211; this postback can be matched with API response using this field.</p>
<p>TIMESTAMP &#8211; timestamp of the MMS was sent (N101) or when MMS was delivered (N102)</p>
<p>HANDSET &#8211; handset profile returned inside Delivery Receipt.</p>
<p>STATUS &#8211; delivery status received in Delivery Receipt.</p>
<p><strong> N101 Example:</strong></p>
<p><small><code>&lt;NOTIFICATION id="521495" created="2012-06-07 07:27:29.954258-04"&gt;<br />
&lt;ORIGIN&gt;MMS_MT&lt;/ORIGIN&gt;<br />
&lt;CODE&gt;N101&lt;/CODE&gt;<br />
&lt;BODY&gt;<br />
&lt;HISTORYID&gt;455811&lt;/HISTORYID&gt;<br />
&lt;MMSID&gt;39597&lt;/MMSID&gt;<br />
&lt;TO&gt;16501112222&lt;/TO&gt;<br />
&lt;TRACKINGID&gt;MMS_389076&lt;/TRACKINGID&gt;<br />
&lt;SPID&gt;000157&lt;/SPID&gt;<br />
&lt;TIMESTAMP&gt;2012-06-07 07:27:29&lt;/TIMESTAMP&gt;<br />
&lt;/BODY&gt;<br />
&lt;/NOTIFICATION&gt;<br />
</code></small></p>
<h3><strong><strong>N102 Example:</strong></strong></h3>
<p><small><code>&lt;NOTIFICATION id="521495" created="2012-06-07 07:27:34.398593-04"&gt;<br />
&lt;ORIGIN&gt;MMS_MT&lt;/ORIGIN&gt;<br />
&lt;CODE&gt;N102&lt;/CODE&gt;<br />
&lt;BODY&gt;<br />
&lt;HISTORYID&gt;455811&lt;/HISTORYID&gt;<br />
&lt;MMSID&gt;39597&lt;/MMSID&gt;<br />
&lt;TO&gt;16501112222&lt;/TO&gt;<br />
&lt;TRACKINGID&gt;MMS_389076&lt;/TRACKINGID&gt;<br />
&lt;SPID&gt;000157&lt;/SPID&gt;<br />
&lt;HANDSET&gt;motol7c&lt;/HANDSET&gt;<br />
&lt;STATUS celly="20" provider="1000" text="Retrieved" description="" /&gt;<br />
&lt;TIMESTAMP&gt;2012-06-07 07:27:34-04&lt;/TIMESTAMP&gt;<br />
&lt;/BODY&gt;<br />
&lt;/NOTIFICATION&gt;<br />
</code></small></p>
<p><strong>b) The XHTML Method</strong></p>
<p>For XHTML, we send one Postback N101 notifying that we started to process the message. N102 is generated once the SMS with a link to the content is sent out. When we receive Delivery Report(DLR) for SMS, we generate Postback notification N202. N101, N102 and N202 are described above.</p>
<p><strong>PLEASE NOTE:</strong></p>
<p>Notification N101 is linked to N102 via TRACKINGID and HISTORYID</p>
<p>Notification N102 contain additional field SMSID and is linked to N202 via SMSID in N102 and TRACKINGID in N202</p>
<p><strong>N101 Example:</strong><br />
<small><code> &lt;NOTIFICATION id="521536" created="2012-06-07 07:27:34.398593-04"&gt;<br />
&lt;ORIGIN&gt;MMS_MT&lt;/ORIGIN&gt;<br />
&lt;CODE&gt;N101&lt;/CODE&gt;<br />
&lt;BODY&gt;<br />
&lt;HISTORYID&gt;455800&lt;/HISTORYID&gt;<br />
&lt;MMSID&gt;39755&lt;/MMSID&gt;<br />
&lt;TO&gt;16502424956&lt;/TO&gt;<br />
&lt;TRACKINGID&gt;MMS_389068&lt;/TRACKINGID&gt;<br />
&lt;SPID&gt;000114&lt;/SPID&gt;<br />
&lt;TIMESTAMP&gt;2012-06-07 07:27:34&lt;/TIMESTAMP&gt;<br />
&lt;/BODY&gt;<br />
&lt;/NOTIFICATION&gt;<br />
</code></small></p>
<p><strong><strong>N102 Example:</strong></strong></p>
<p><small><code>&lt;NOTIFICATION id="521537" created="2012-06-07 07:28:01.138593-04"&gt;<br />
&lt;ORIGIN&gt;MMS_MT&lt;/ORIGIN&gt;<br />
&lt;CODE&gt;N102&lt;/CODE&gt;<br />
&lt;BODY&gt;<br />
&lt;HISTORYID&gt;455800&lt;/HISTORYID&gt;<br />
&lt;MMSID&gt;39755&lt;/MMSID&gt;<br />
&lt;TO&gt;16502424956&lt;/TO&gt;<br />
&lt;TRACKINGID&gt;MMS_389068&lt;/TRACKINGID&gt;<br />
&lt;SMSID&gt;SMS_45697&lt;/SMSID&gt;<br />
&lt;STATUS celly="10" provider="1000" /&gt;<br />
&lt;TIMESTAMP&gt;2012-06-07 07:28:01.030338-04&lt;/TIMESTAMP&gt;<br />
&lt;/BODY&gt;<br />
&lt;/NOTIFICATION&gt;<br />
</code></small></p>
<p><strong><strong>N202 Example:</strong></strong></p>
<p><small><code>&lt;NOTIFICATION id="521538" created="2012-06-07 07:28:09.398593-04"&gt;<br />
&lt;ORIGIN&gt;SMS_MT&lt;/ORIGIN&gt;<br />
&lt;CODE&gt;N202&lt;/CODE&gt;<br />
&lt;BODY&gt;<br />
&lt;HISTORYID&gt;455801&lt;/HISTORYID&gt;<br />
&lt;TO&gt;16502424956&lt;/TO&gt;<br />
&lt;TRACKINGID&gt;SMS_45697&lt;/TRACKINGID&gt;<br />
&lt;STATUS protocole="3" status="1"/&gt;<br />
&lt;TIMESTAMP&gt;2012-06-07 07:28:09.90765-04&lt;/TIMESTAMP&gt;<br />
&lt;/BODY&gt;<br />
&lt;/NOTIFICATION&gt;<br />
</code></small></p>
<h5><strong>c)  Save MMS</strong></h5>
<p>When MMS is saved (using API or our MMS Composer) we generate postback notification. When saving was successful we generate N003:</p>
<p><small><code>&lt;NOTIFICATION CREATED="2011-01-01 20:09:12.975911-04"ID="325"&gt;<br />
&lt;ORIGIN&gt;MMS_MT&lt;/ORIGIN&gt;<br />
&lt;CODE&gt;N003&lt;/CODE&gt;<br />
&lt;BODY&gt;<br />
&lt;MMSID&gt;35674&lt;/MMSID&gt;<br />
&lt;/BODY&gt;<br />
&lt;/NOTIFICATION&gt;</code></small></p>
<p>If encoding of the Content failed we generate postback E002 containgin MMSID and AUDIONAME/VIDEONAME pointing ti the content that failed to encode proerly. Below is example of E002:</p>
<p><small><code>&lt;NOTIFICATION ID="325" CREATED="2011-01-01 20:09:12.975911-04"&gt;<br />
&lt;ORIGIN&gt;MMS_MT&lt;/ORIGIN&gt;<br />
&lt;CODE&gt;E002&lt;/CODE&gt;<br />
&lt;BODY&gt;<br />
&lt;MMSID&gt;35674&lt;/MMSID&gt;<br />
&lt;AUDIONAME&gt;sample.mp3&lt;/AUDIONAME&gt;<br />
&lt;/BODY&gt;<br />
&lt;/NOTIFICATION&gt;</code></small></p>
<p><strong>Group #3- Subscribe/Unsubscribe for Phone/Email</strong></p>
<p><strong>a) Synopsis:</strong> This Postback notification subscribes a phone number to a specific campaign. Inside BODY element those postbacks contain following fields:</p>
<p>MOBILE &#8211; subscriber&#8217;s mobile</p>
<p>CAMPAIGNID &#8211; ID of the campaign</p>
<p>SUBID &#8211; subscription ID</p>
<p><strong>Postback Notification Example:</strong></p>
<p><small><code>&lt;NOTIFICATION id="532168" created="2012-04-16 09:05:56.954258-04"&gt;<br />
&lt;ORIGIN&gt;SUB&lt;/ORIGIN&gt;<br />
&lt;CODE&gt;N301&lt;/CODE&gt;<br />
&lt;BODY&gt;<br />
&lt;MOBILE&gt;16501112222&lt;/MOBILE&gt;<br />
&lt;CAMPAIGNID&gt;1478&lt;/CAMPAIGNID&gt;<br />
&lt;SUBID&gt;656655&lt;/SUBID&gt;<br />
&lt;/BODY&gt;<br />
&lt;/NOTIFICATION&gt;<br />
</code></small></p>
<p><strong>b) Synopsis:</strong> This Postback notification unsubscribes a phone number from a specific campaign. Inside BODY element those postbacks contain following fields:</p>
<p>MOBILE &#8211; subscriber&#8217;s mobile</p>
<p>CAMPAIGNID &#8211; ID of the campaign</p>
<p>SUBID &#8211; subscription ID</p>
<p><strong>Postback Notification Example:</strong></p>
<p><small><code>&lt;NOTIFICATION id="532169" created="2012-04-16 09:15:56.784653-04"&gt;<br />
&lt;ORIGIN&gt;SUB&lt;/ORIGIN&gt;<br />
&lt;CODE&gt;N302&lt;/CODE&gt;<br />
&lt;BODY&gt;<br />
&lt;MOBILE&gt;16502424956&lt;/MOBILE&gt;<br />
&lt;CAMPAIGNID&gt;1478&lt;/CAMPAIGNID&gt;<br />
&lt;SUBID&gt;656655&lt;/SUBID&gt;<br />
&lt;/BODY&gt;<br />
&lt;/NOTIFICATION&gt;<br />
</code></small></p>
<p><strong>c) Synopsis:</strong> This Postback notification subscribes an email to a specific campaign. Inside BODY element those postbacks contain following fields:</p>
<p>EMAIL &#8211; subscriber&#8217;s email</p>
<p>CAMPAIGNID &#8211; ID of the campaign</p>
<p>SUBID &#8211; subscription ID</p>
<p><strong>Postback Notification Example:</strong></p>
<p><small><code>&lt;NOTIFICATION id="521354" created="2012-04-16 19:15:56.954258-04"&gt;<br />
&lt;ORIGIN&gt;EMAIL_SUB&lt;/ORIGIN&gt;<br />
&lt;CODE&gt;N303&lt;/CODE&gt;<br />
&lt;BODY&gt;<br />
&lt;EMAIL&gt;jacek@skycore.com&lt;/EMAIL&gt;<br />
&lt;CAMPAIGNID&gt;89&lt;/CAMPAIGNID&gt;<br />
&lt;SUBID&gt;12913&lt;/SUBID&gt;<br />
&lt;/BODY&gt;<br />
&lt;/NOTIFICATION&gt;<br />
</code></small></p>
<p><strong>d) Synopsis:</strong> This Postback notification unsubscribes an email from a specific campaign. Inside BODY element those postbacks contain following fields:</p>
<p>EMAIL &#8211; subscriber&#8217;s email</p>
<p>CAMPAIGNID &#8211; ID of the campaign</p>
<p>SUBID &#8211; subscription ID</p>
<p><strong>Postback Notification Example:</strong></p>
<p><small><code>&lt;NOTIFICATION id="521355" created="2012-04-16 19:15:47.598472-04"&gt;<br />
&lt;ORIGIN&gt;EMAIL_SUB&lt;/ORIGIN&gt;<br />
&lt;CODE&gt;N304&lt;/CODE&gt;<br />
&lt;BODY&gt;<br />
&lt;EMAIL&gt;jacek@skycore.com&lt;/EMAIL&gt;<br />
&lt;CAMPAIGNID&gt;89&lt;/CAMPAIGNID&gt;<br />
&lt;SUBID&gt;12913&lt;/SUBID&gt;<br />
&lt;/BODY&gt;<br />
&lt;/NOTIFICATION&gt;<br />
</code></small></p>
