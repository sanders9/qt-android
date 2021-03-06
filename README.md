# qt-android

This repository is a tutorial explaining how to integrate Qt in an Android Studio project. The main purpose is to create and retrieve data from a native sqlite3 database using Qt5Sql and Qt5Core. This last one will allow us to use the signals and slots features implemented in the Qt framework

Throughout this project I will explain the different folders located in this repository 

**Note : People interested about this project must be familiar with Android Studio, the Qt framework and the Android SDK and NDK**

##1. the *libs/* folder

This folder contains jar files needed for the qt framework. I found and import them from a qt project for android. 
I needed to include all of them because of the following error :

*java.lang.UnsatisfiedLinkError: JNI_ERR returned from JNI_OnLoad. I had created a post on stackoverflow website (have a look on : http://stackoverflow.com/questions/36413504/java-lang-unsatisfiedlinkerror-jni-err-returned-from-jni-onload)*

##2. the *src/main/assets/database* folder

This folder contains the sqlite database used in this tutorial. It is contains one table and three columns *name / first_name / age*

##3. the *src/main/assets/sqldrivers* folder

In this tutorial I use the QSqlDatabase class to query a sqlite database (see above). The plugin used by Qt to communicate with the QSqlite API needs some drivers. These last ones are located in this folder. It must be copied on the mobile phone and add  to the library path list.

##4. the *src/main/java/* folder

This folder contains java classes whose QtServiceAPI.java allows us to use native code

After retrieving data from the sqlite database, I notify the java part using a callback (cf QtDatabaseResponseListener.java)

##5. the *src/main/jni/qt-library* folder



## Known issues and limitations

* This integration of the qt framework only works on Android devices <= API 21 (= Android Lollipop)
* QSqlDatabase : Driver not loaded. Have a look on this stackoverflow post : http://stackoverflow.com/questions/38638483/qsqldatabase-driver-not-loaded-driver-not-loaded

## Point to develop
* SQsqlDatabase not loaded
* QCoreApplication.exec()




## The repository is coming...


