# Firebase-Authentication

Firstly Enabling Firebase Authentication

1. First thing you need to do is go to https://firebase.google.com/ and make an account to gain access to their console. After you gain access to the console you can start by creating your first project.

2. Give the package name of your project (mine is com.firebaseintegration) in which you are going to integrate the Firebase. Here the google-services.json file will be downloaded when you press add app button.

3. Next go to your project dashboard. Find the Auth and click get started. Go to set up sign in method and choose Email & Password and enable it.

After than start to creating project.

1. Open AndroidManifest.xml and add the INTERNET permission as we need to make network calls.
<uses-permission android:name="android.permission.INTERNET" />

2.Paste the google-services.json file to your project’s app folder. This step is very important as your project won’t build without this file.

3. Now open the build.gradle located in project’s home directory and add firebase dependency.

dependencies {
        classpath 'com.android.tools.build:gradle:2.1.2'

	//add this line in project
        classpath 'com.google.gms:google-services:3.0.0'
    }


4. Open app/build.gradle and add firebase auth dependency. At the very bottom of the file, add apply plugin: ‘com.google.gms.google-services’

dependencies {
    compile "com.google.firebase:firebase-auth:9.0.2"
}
 
apply plugin: 'com.google.gms.google-services'
