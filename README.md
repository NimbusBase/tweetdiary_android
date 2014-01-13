# Nimbusbase android  sqlite  sync  demo
==================
## Tweetdiary  android

* build target : android 4.2

* App link : [Google Play](https://play.google.com/store/apps/details?id=com.nimbusbase.tweetdiary).
 


* Main sync code   (in SwipeActivity.java):
```java 
		// four variables for GDriveModel: 
		//	1, the  Activity to run the sync process;
		//  2, the  App name;
		//  3, the  sqlite database  file name;
		//  4, the  tables need to  sync, if  set null will sync  all tables;
		gdriveModel = new GDriveModel(SwipeActivity.this.getActivity(), "diary_app", "D", new String[] { "Entry" });

		// google  authorize;
		gdriveModel.authorize();

		//sync data per  3s
		gdriveModel.syncThread(3000);
		 
```




