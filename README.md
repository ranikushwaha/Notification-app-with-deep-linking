# Notification-app-with-deep-linking
Implementing notifications and deep linking functionality in an Android application using Kotlin. 
Certainly! Here's a step-by-step process how i implement a simple static notification on button click and deep linking in an Android app using Kotlin and a BroadcastReceiver:

Step 1: Set up your Android project

Create a new Android project in Android Studio.
Step 2: Design your app layout

Open your app's activity and add a button element.
Step 3: Create a BroadcastReceiver

Create a new Kotlin class, such as MyBroadcastReceiver, which extends BroadcastReceiver.
Override the onReceive method in your MyBroadcastReceiver class.
Inside the onReceive method, build and display a static notification using the NotificationCompat.Builder class.
Step 4: Register the BroadcastReceiver

Open your app's AndroidManifest.xml file.
Add a receiver element inside the application element, specifying the name of your MyBroadcastReceiver class as the receiver's name.
Add an intent-filter element inside the receiver element, specifying the action you want to trigger the BroadcastReceiver (e.g., android.intent.action.MY_BROADCAST).
Step 5: Handle the button click event

Open your app's activity Kotlin file (e.g., MainActivity.kt).
Inside the onCreate method, initialize the button.
Set an OnClickListener for the button.
Inside the OnClickListener, create an intent with the action specified in the BroadcastReceiver's intent-filter.
Call sendBroadcast with the intent.
Step 6: Handle deep linking

Determine the deep link URL structure you want to use in your app.
In your app's manifest file, define an intent filter for the activity you want to open when the deep link is clicked.
Create a new activity or modify an existing one to handle the deep link.
In the activity's onCreate method, parse the deep link data using the intent's data.
Step 7: Testing

Deploy your app to a test device or emulator.
Launch the app and tap the button.
Verify that the static notification is displayed correctly on the test device.
Tap on the notification and ensure that the app opens the correct activity based on the deep link URL.
That's it! By following these steps, you should be able to implement showing a simple static notification on button click and deep linking in your Android app using Kotlin and a BroadcastReceiver.
