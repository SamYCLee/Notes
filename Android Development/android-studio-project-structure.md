# Android Studio Project Structure

## Caption

This note is dedicated for explaining different files created during the initialization of the project in Android Studio.

## Folder and Files

----

### **Manifests Folder**

This folder contains `AndroidManifest.xml`. This file describes all the components of your Android app and is read by the Android runtime system when your app is executed.

### **Java Folder**

All your Kotlin language files are organized here; Android projects keep all Kotlin language files in this folder, together with any Java sources. The java folder contains three subfolders:

- *com.example.myfirstapp* (or the domain name you have specified)
  - This folder contains the Kotlin source code files for your app.

- *com.example.myfirstapp (androidTest)*
  - This folder is where you would put your instrumented tests, which are tests that run on an Android device. It starts out with a skeleton test file.

- *com.example.myfirstapp (test)*
  - This folder is where you would put your instrumented tests, which are tests that run on an Android device. It starts out with a skeleton test file.

### **Res Folder**

This folder contains all the resources for your app, including images, layout files, strings, icons, and styling. It includes these subfolders:

- *drawable*
  - All your app's images will be stored in this folder.

- *layout*
  - This folder contains the UI layout files for your activities, such as `activity_main.xml`. It also contains `content_main.xml`, `fragment_first.xml`, and `fragment_second.xml`.

- *menu*
  - This folder contains XML files describing any menus in your app.

- *mipmap*
  - This folder contains the launcher icons for your app

- *navigation*
  - This folder contains the navigation graph, which tells Android Studio how to navigate between different parts of your application.

- *values*
  - Contains resources, such as strings and colors, used in your app.

## Reference

> https://developer.android.com/codelabs/build-your-first-android-app-kotlin?authuser=1#2
