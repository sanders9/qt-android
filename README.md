# qt-android

This repository is a tutorial explaining how to integrate Qt in an Android Studio project. The main purpose is to create and retrieve data from a native sqlite3 database using Qt5Sql and Qt5Core. This last one will allow us to use the signals and slots features implemented in the Qt framework

Throughout this project I will explain the different folders located in this repository 

**Note : People interested about this project must be familiar with Android Studio, the Qt framework and the Android SDK and NDK**

##1. the *libs/* folder

This folder contains jar files needed for the qt framework. I found and import them from a qt project for android. 
I needed to include all of them because of the following error :

*java.lang.UnsatisfiedLinkError: JNI_ERR returned from JNI_OnLoad. I had created a post on stackoverflow website (have a look on : http://stackoverflow.com/questions/36413504/java-lang-unsatisfiedlinkerror-jni-err-returned-from-jni-onload)*

##2. the *src/main/java/* folder

This folder contains java classes whose the class allowing to use native code (cf QtServiceAPI.java).

After retrieving data from the sqlite database, I notify the java part using java callback (cf QtDatabaseResponseListener)

##3. the *src/main/jni/* folder



## Known issues and limitations

* This integration of the qt framework only works on Android devices <= API 21 (= Android Lollipop)
* QSqlDatabase : Driver not loaded Have a look on this stackoverflow post : http://stackoverflow.com/questions/38638483/qsqldatabase-driver-not-loaded-driver-not-loaded




## The repository is coming...


