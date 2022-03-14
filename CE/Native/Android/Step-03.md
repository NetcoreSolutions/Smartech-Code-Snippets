# Android - Native Initialize

## Step 2: Initialize Smartech SDK

2.1 Put your Smartech panel's app Id in the meta-data tag of your application's manifest file, it should be added within the application tag, but outside of any component within the application tag.

To get Smartech App ID, follow steps given [here](https://cedocs.netcorecloud.com/docs/android-app-id-creation), else please get in touch with your account manager to get the value of SMT_APP_ID

```sh
<meta-data android:name="SMT_APP_ID" android:value="YOUR_SMARTECH_APP_ID_HERE" />
```

2.2 Add the below mentioned code in the onCreate() method of your Application class to initialize the Smartech SDK.

Java Code Snippet
```java
@Override
public  void  onCreate() {
	super.onCreate();
	Smartech.getInstance(new  WeakReference<>(context)).initializeSdk(this);
}
```

Kotlin Code Snippet
```kotlin
override  fun  onCreate() {
	super.onCreate()
	Smartech.getInstance(WeakReference(applicationContext)).initializeSdk(this)
}
```
