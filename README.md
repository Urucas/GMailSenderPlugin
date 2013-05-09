GMailSenderPlugin Beta
======================

Phonegap 2.5.0 Beta Plugin for Android to send emails without intents, using your gmail account user and password. 

Based on javamail-android source <br />
https://code.google.com/p/javamail-android/

And Jon Simon example <br />
http://www.jondev.net/articles/Sending_Emails_without_User_Intervention_%28no_Intents%29_in_Android

Installation
============

* Add to Build Path the **activation.jar**, **mail.jar**, **additional.jar** from /libs  

* Add the plugin markup to the **config.xml** file of the phonegap project 
``<plugin name="GmailsenderPlugin" value="com.urucas.plugins.GmailsenderPlugin"/> ``

* Replace your user and password on the GmailsenderPlugin.java class
<code>
  private Mail m = new Mail("youremail@gmail.com", "yourpassword");
</code>

Usage
=====

<code>
cordova.exec(
  function(a){ /* success callback */ }, 
  function(err) { /* error callback */ }, 
  "GmailsenderPlugin", 
  "send",
  [["mail1@gmail.com","mail2@gmail.com"], "This is the subject", "This is the body"]
);
</code>

License
=======
The source Code is available under same licenses as javamail which is :

* CDDL-1.0
* GPL-2.0
* BSD
