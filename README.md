GMailSenderPlugin
=================

Phonegap 2.5.0 Plugin for Android to send email without intents, using your gmail account user and password. 

Based on javamail-android source 
https://code.google.com/p/javamail-android/

and Jon Simon example; 
http://www.jondev.net/articles/Sending_Emails_without_User_Intervention_%28no_Intents%29_in_Android



To start using this plugin:

1. Add the plugin to the config.xml file of the phonegap project; 
<plugin name="GmailsenderPlugin" value="com.urucas.plugins.GmailsenderPlugin"/>

2. Add to Build Path the java files; activation.jar, mail.jar and additional.jar

3. Add your user and password on the GmailsenderPlugin.java Mail

4. Call the plugin function on your javascript source after the deviceReady: 
cordova.exec(function(a){ /* success callback */ }, function(err) { /* error callback */ }, "GmailsenderPlugin", "send",[["mail1@gmail.com","mail2@gmail.com"], "This is the subject", "This is the body"]);
