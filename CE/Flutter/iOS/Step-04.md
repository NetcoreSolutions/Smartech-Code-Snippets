## Step 3: Initialize Netcore CEE SDK
Import Smartech SDK in AppDelegate class.

Objective-C code snippet
```objectivec
#import <Smartech/Smartech.h>
```
Swift code snippet
```swift
import Smartech
```
##
Call a method to initialize Smartech SDK in the `didFinishLaunchingWithOptions` method of the AppDelegate class

Objective-C code snippet

```objectivec
- (BOOL)application:(UIApplication *)application didFinishLaunchingWithOptions:(NSDictionary *)launchOptions {
	//...
	[[Smartech sharedInstance] initSDKWithDelegate:(id)self withLaunchOptions:launchOptions];
	//...
	return YES;
}
```
Swift code snippet

```swift
func  application(_  application: UIApplication, didFinishLaunchingWithOptions  launchOptions:[UIApplication.LaunchOptionsKey: Any]?) -> Bool {
	//...
	Smartech.sharedInstance().initSDK(with: self, withLaunchOptions: launchOptions)
	//...
	return  true
}
```