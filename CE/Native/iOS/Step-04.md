## Step 3: Configure Apps Info.plist with SmartechKeys

You need to add a key named `SmartechKeys` with type Dictionary. Add the following keys and values with their types to the `SmartechKeys`

| Key | Data type | Description |
|--|--|--|
| SmartechAppGroup | String | The app group that is selected in capabilities section. It is used to share data between App and Extensions. |
| SmartechAppId | String | The app id received from Smartech panel under assets section. |
| SmartechAutoFetchLocation | Boolean | This key decides whether you want to automatically send the location with all the events or not. Set value as true/false as per the requirement. |
| SmartechUseAdvId | Boolean | This key decides whether to use ADID (Advertising Id) or not. Set value as true/false as per the requirement. |

You can paste the following sinppet in `Info.plist` of your app and set the appropriate values for the keys.
```xml
<!---For Smartech-->
<key>SmartechKeys</key>
<dict>
	<key>SmartechAppGroup</key>
	<string>group.com.CompanyName.ProductName</string>
	<key>SmartechAppId</key>
	<string>abcdef123456abcdef123456abcd1234</string>
	<key>SmartechUseAdvId</key>
	<true/>
	<key>SmartechAutoFetchLocation</key>
	<true/>
</dict>
<!--- -->
```
Following is the image representation of apps `Info.plist` for key `SmartechKeys`:

![](https://files.readme.io/16a81d1-Screenshot_2020-06-17_at_1.52.28_AM.png  "SmartechKeys.png")