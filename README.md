# Tweetdiary android: A Nimbusbase android sqlite sync demo 

This demo for NimbusBase shows how we sync structure data by replicating whatever is in the local sqlite database and then storing it on top of Google Drive. Please view or run.

* build target: android 4.2

* App link: [Google Play](https://play.google.com/store/apps/details?id=com.nimbusbase.tweetdiary).
 


* The main sync code for NimbusBase is in [SwipeActivity.java](https://github.com/NimbusBase/tweetdiary_android/blob/master/tweetdiary/src/com/nimbusbase/tweetdiary/ui/SwipeActivity.java):
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
