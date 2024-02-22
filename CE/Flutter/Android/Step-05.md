# Step 4: Configuring Deeplink scheme

You are required to define a [custom URL scheme](https://developer.android.com/training/app-links/deep-linking) for pairing your device as a test device. Kindly follow the below steps to configure a custom URL scheme.

## Changes in AndroidManifest.xml

Add the following intent filter to the activity that you want to handle the deep link for adding a test device in the AndroidManifest.xml file.

``` Xml
<intent-filter>
<action android:name="android.intent.action.VIEW" />
<category android:name="android.intent.category.DEFAULT" />
<category android:name="android.intent.category.BROWSABLE" />
<data android:scheme="<your-custom-scheme>"
android:host="smartech_sdk_td" />
</intent-filter>
```
## Changes in the Activity that is assigned to handle the deep link

Java Code Snippet
```Java
class YourActivity extends  AppCompatActivity {
	...
	@Override
	protected void onCreate(Bundle  savedInstanceState) {
		...
		boolean isSmartechHandledDeeplink = Smartech.getInstance(new WeakReference<>(this)).isDeepLinkFromSmartech(getIntent());
		if (!isSmartechHandledDeeplink) {
		//Handle deeplink on app side
		}
		...
	}
	...
}
```
  Kotlin Code Snippet
```Kotlin
class YourActivity :  AppCompatActivity() {
	...
	override fun onCreate(savedInstanceState: Bundle?)
	{
		...
		val isSmartechHandledDeeplink = getInstance(WeakReference(this)).isDeepLinkFromSmartech(intent)
		if (!isSmartechHandledDeeplink) {
		//Handle deeplink on app side
		}
		...
	}
	...
}
```

## Note: Please install your build on your device and compile it before proceeding to next step.