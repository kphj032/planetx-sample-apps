i. Introduction - "SNS All Viewer"
	
	1. Title : SNS All Viewer (for android)
	
	2. Description : Service for gathered view Facebook, Google+ and Twitter comments.
              
    	3. API Usage : Social Component API



ii.Sample Project Configuration
	
	1. AndroidManifest.xml file in /OpenPlatform_SNS  : It declared permission and Activity for property whenever you use Planet X library.

	2. libs folder in /OpenPlatform_SNS/libs

		- SKPOP_SDK.jar : Planet X server interface

		- SKPOP_SDK_OAuth.jar : OneID certification

		- google-play-services.jar : Google+ interface

		- twitter4j-core-2.1.3-SNAPSHOT.jar : Twitter interface

	3. Defines.java in /OpenPlatform_SNS/src/com/skp/opx/core/client : It defined OAuth Key, SNS key, each API's 

	   URI and project configuration.

	   	- Must redefine below content for running this application in Define.java

		  /** Authentication */
 		  public final class OAuth {
  		  	public static final String CLIENT_ID    = "< your key here >";
 			public static final String SECRET        = "< your key here >";
  			public static final String KEY              = "< your key here >";
  		  }
 


iii. Prerequisite
	
	1. Register at One ID or Switch to One ID. 
                 
		: Must register for One ID(https://oneid.skplanet.co.kr), thereby using this application.

	2. Register at developer's center
	
		: Must acquire AppKey issued by the Planet X, thereby running this application.
                    
		  Therefore must register at https://developers.skplanetx.com. If you already have it, agree user agreement. 

	3. Register application

	   1) In the "My Center: App Station", register application.

	   2) Acquire API Authentication Key. 
                    
		- It used for authentication Planet X API call.
                 
		- It consists of App Key, Client ID and Client secret, App key. These values applied for below iv. Configuration section.

	   3) Must select "SK Planet One ID" and "Social" service area, thereby using this application.
          	 
	4. Register at third party's service(Facebook, Twitter, Google+) for testing. 
 

iv. Configuration

	1. Building Environment: Above Android SDK API level 10

	2. Running Environment: Above Android OS 2.3(Codename: Gingerbread 2.3) (We recommend emulator version of ICS because of some bug issues.) 

	3. Extract ZIP file. Next import at Eclipse's File munu.

	4. Edit API Authentication Key value at Define.java in OpenPlatform_SNS/src/com/skp/opx/core/client/

	5. Application Registration and Configuration for third party's service
	 
	   1) When you register application on third party's service, rename package name for preventing duplication package.

	        : Run eclipse > Package Explore > Android Tools > Rename Application Package

	   2) Register application and Acquire Application keys at each third party's service developer center not planetx developer's center.

	       Refer to "https://developers.skplanetx.com/apidoc/eng/social"
	
	              	- Facebook : Facebook AppKey Register

		- Twitter : twitter AppKey Register  
		
		- Google+ : Google+ AppKey Register
	  
	   3) Register key and ID values issued by third party's service at developer's center(https://developers.skplanetx.com).

		: In the "My Center: App Station: Social Provider", input key and ID values issued by third party's service

	   4) Edit key and ID values issued by third party's service at Define.java in OpenPlatform_SNS/src/com/skp/opx/core/client/

		: Edit Twitter Key class and Facebook Key class.

 		  /** Twitter callback uri, consumer key, consume secret key */
 		  public static final class Twitter_Key{
 		  	public static final String TWITTER_LINK_ID    	    = "< your key here >";
  			public static final String TWITTER_CALLBACK_URL     = "< your key here >";
  			public static final String TWITTER_CONSUMER_KEY     = "< your key here >";
  			public static final String TWITTER_CONSUMER_SECRET  = "< your key here >";
 		  }
 
 		  /** Facebook App ID & Auth code */
 		  public static final class Facebook_Key {
  		  	public static final String FACEBOOK_APP_ID   = "< your key here >";
 		  }



vi. Contact us for Sample Project

	Ask any questions for detail, "Community: Contact Us"(https://developers.skplanetx.com/community/contact-us/enrollment)

 

