<b>saveMMS()</b>
<BR>
<b>Synopsis</b>:
&nbsp;
This API stores an MMS from XML. The MMS may contain slides embedded with video, audio, images and text. 
Once the MMS is saved it can be utilized by other functions through the MMSID returned.

<b>Request</b>:

<textarea disabled="true" style="border: none;background-color:white;">
  <p>

	<REQUEST>
    		<ACTION>saveMMS</ACTION>
    		<API_KEY>API KEY</API_KEY>
    		<SUBJECT>Subject </SUBJECT>
   		<CONTENT>
       			<NAME>Name to save it as</NAME>
        		<SEQUENCE>
           			<SLIDE duration="Duration in seconds">
                			<IMAGE>
                				<URL>URL</URL>
                			</IMAGE>
                			<AUDIO>
                				<URL>URL</URL>
                			</AUDIO>
                			<TEXT>Plain Text</TEXT>
            			</SLIDE>
            			<SLIDE>
	            			…
            			</SLIDE>
			    </SEQUENCE>
   		</CONTENT>
	</REQUEST>

	
</textarea>
</p>
<b>Request Parameters:</b>
<BR>
<BR>
	<b>Mandatory:</b> 
		
		Action, API_KEY, Name, Subject, Content, Sequence, Slide
&nbsp;	
	<b>Optional:</b> 
		
		Image, Audio, Video, URL, Text, Duration
&nbsp;	
	<b>Response Parameters:</b>
		
		Status, TrackingID, Errorcode, Errorinfo, MMSID
<BR>
	<b>Related Errorcodes:</b> 
		
		E225, E226, E227, E228, E229, E230, E331, E332, E333, E334, E341, E351

<b>Request Example:</b>

<textarea disabled="true" style="border: none;background-color:white;">
	<p>

		<REQUEST>
			<ACTION>saveMMS</ACTION>
			<API_KEY>qTFkykO9JTfahCOqJ0V2Wf5Cg1t8iWlZ</API_KEY>
			<SUBJECT>The subject </SUBJECT>
			<CONTENT>
				<NAME>fishtank</NAME>
				<SEQUENCE>
					<SLIDE duration="5">
						<IMAGE>
						<URL>http://www.yoursite.com/images/1.jpg</URL>
						</IMAGE>
						<AUDIO>
						<URL>http://www.yoursite.com/audio/1.mp3</URL>
						</AUDIO>
						<TEXT>
							Here is some text tralalala....
						</TEXT>
					</SLIDE>
				</SEQUENCE>
			</CONTENT>
		 </REQUEST>
 
 
</textarea>

<b>Response Example:</b> Success

<textarea disabled="true" style="border: none;background-color:white;">
	<p>
	
		<RESPONSE>
			<STATUS>Success</STATUS>
			<MMSID>35674</MMSID>
		</RESPONSE>
		
		
</textarea>

<b>Response Example:</b> Failure

<textarea disabled="true" style="border: none;background-color:white;">
	<p>
	
		<RESPONSE>
			<STATUS>Failure</STATUS>
			<ERRORCODE>E111</ERRORCODE>
			<ERRORINFO>Invalid shortcode</ERRORINFO>
		</RESPONSE>
		
		
</textarea>

<b>Postback Notifications</b>
<BR>
	When the MMS is saved system will generate a Postback notification and unlock MMS for further use. 
	If MMS contain audio/video Postback will be sent when encoding of MMS Audio/Video is finished, otherwise 
	Postback notification will be sent instantly. Below is example of Postback notification when MMS saved 
	successfully:

<textarea disabled="true" style="border: none;background-color:white;">
	<p>
	
		<NOTIFICATION CREATED="2011-01-01 20:09:12.975911-04"ID="325">
			<ORIGIN>MMS_MT</ORIGIN>
			<CODE>N003</CODE>
			<BODY>
				<MMSID>35674</MMSID>
			</BODY>
		</NOTIFICATION>
		
		
</textarea>

If there was an error encoding MMS audio/video system will generate notification:

<textarea disabled="true" style="border: none;background-color:white;">
	<p>
	
		<NOTIFICATION ID="325" CREATED="2011-01-01 20:09:12.975911-04">
			<ORIGIN>MMS_MT</ORIGIN>
			<CODE>E002</CODE>
			<BODY>
				<MMSID>35674</MMSID>
				<AUDIONAME>sample.mp3</AUDIONAME>
			</BODY>
		</NOTIFICATION>
		
		
</textarea>

<b>Special Considerations for saveMMS:</b>
<BR>
The API SHALL reformat the content when necessary so that it can be delivered to the end users handset in the best possible way.
Delivery success takes precedence over audio and video content quality and occasionally the picture quality will be reduced to fit handset message size requirements. Video SHALL be reduced in quality to fit delivery limitations and if it still does not fit it will be delivered as XHTML/SMS.
Each request MUST contain at least one slide which MAY contain text and/or image and/or video and/or sound. The API SHALL support up to 8 slides for each MMS submission.
The API SHALL NOT support multiple files of the same MIME type on the same slide. Slides with image SHALL NOT support video but SHALL support audio. Slides with audio SHALL NOT support video. Slides with video SHALL only support text. Slides with text SHALL support up to 500 characters in any slide.
URLS within the text MAY be replaced by a link shortening URL depending on the API account settings.
All slides MAY contain a duration for playback. Default slide duration is 5 seconds. Slide duration will be overwritten if the file duration exceeds the xml duration.
URLs provided MUST contain the full path to the mime files.
Slide Duration SHOULD NOT exceed 30 seconds and SHALL NOT exceeds 60 seconds.
MMS is delivered to the handset using title: NAME from ACCOUNT, if SUBJECT is not passed.
MMS containing audio/video can be used only when audio/video encoding is completed. After submission you will not be given a successful acknowledgement of audio/video encoding when a message is submitted. The HTTP status of audio/video encoding after it has been completed will be sent to your Postback URL.
Supported Media: TEXT/PLAIN, GIF/JPG/PNG, MP3/WAV, 3GP, MP4, MPEG, MPG, AVI, WMV
There is a maximum source file size for each supported source file submitted. You can find out what the current maximum is by visiting your API settings.
