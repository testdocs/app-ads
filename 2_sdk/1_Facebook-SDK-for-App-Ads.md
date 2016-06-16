#Facebook SDK for App Ads
 
[Create Ad](https://www.facebook.com/ads/create) [Verify Your App Ads Setup](/tools/app-ads-helper/) 
---



Add the **Facebook SDK** for [iOS](/docs/ios), [Android](/docs/android) or [JavaScript](/docs/javascript) to your app to:

* **Measure installs**
* **Measure app events**
* **Add deep linking to your ads**
* **Bring people back to your app**
* **Improve targeting**
* **Encourage purchases**
* **Create re-engagement ads**
* **Measure in-app conversions**


To learn more about these topics read our guides for [measuring](/docs/app-ads/measuring), [targeting](/docs/app-ads/targeting) and [customizing ad formats](/docs/app-ads/formats).


---



##Step-by-Step: Facebook SDK Setup {#step-by-step}

###1. Facebook App ID {#app-id}

You need a Facebook App ID to use the Facebook SDK for iOS, Android or JavaScript (Web). You can use an [existing app](/apps) if you already have one. Otherwise use our [Quick Start](/quickstarts) to create a new app. If you need help follow our how-to [Register and Configure an App](/docs/apps/register).
 
[Quick Start: Add a New App](/quickstarts/) 

 
>  

###2. Link Ad Accounts

To measure installs in the [Facebook Ads Manager](https://www.facebook.com/ads/manager) you have to associate [advertising accounts](https://www.facebook.com/ads/manager/account/settings/) with your app using the app dashboard. 

1. Go to the [app dashboard](https://developers.facebook.com/apps/)
2. Choose your app.
3. Navigate to "Settings > Advanced" and add accounts via the `Authorized Ad Account IDs` input field. 

[App Dashboard](https://developers.facebook.com/apps/) 



###3. Add the Facebook SDK to your app {#sdk}
Follow the instructions of our "Getting started" guides to add the Facebook SDK to your app:

[iOS](/docs/ios/getting-started) [Android](/docs/android/getting-started) [JavaScript](/docs/javascript/quickstart) 
  

>  

**For iOS / Android:** You do not need to add any functionality like Sharing or Login with Facebook.

###4. Enable Install Tracking {#install-tracking}
To enable install tracking call the App Events logger once your application becomes active.
 
### iOS SDK
```
- (void)applicationDidBecomeActive:(UIApplication *)application {
   [FBSDKAppEvents activateApp];
}
```

### Android SDK
``` 
@Override
protected void onResume() { 
  super.onResume(); 
  AppEventsLogger.activateApp(this); 
  // ...
}

// Optional: App Deactivation Event 
@Override
protected void onPause() { 
  super.onPause(); 
  AppEventsLogger.deactivateApp(this);
} 
```



---

**Desktop Canvas Apps**: By integrating [Facebook Login](/docs/facebook-login/login-flow-for-web) to your Facebook Canvas, App Launches and App Installs are logged automatically. **Other Web Apps**: We do not support install tracking for web apps not hosted on facebook.com.
  
###5. More Tracking Methods {#more-tracking-methods}
If you want to track other app events like a person making a purchase, visit our **[App Events](/docs/app-events)** guide. 

####Example: Log Purchase 
 
### iOS SDK
```
[FBSDKAppEvents logPurchase:4.32 currency:@"USD"]; 
```

### JavaScript SDK
``` 
var params = {}; // optional parameters like `CONTENT_ID`
FB.AppEvents.logPurchase(4.32, "USD", params);
```

### Android SDK
``` 
logger.logPurchase(BigDecimal.valueOf(4.32), Currency.getInstance("USD"));
```

 

---
  
####Example: Custom Event


### iOS SDK
```
[FBSDKAppEvents logEvent:@"myCustomEventName"];
```

### JavaScript SDK
``` 
FB.AppEvents.logEvent("myCustomEventName");
```

### Android SDK
``` 
logger.logEvent("myCustomEventName");
```

 
 
  ---

[App Events Guide](/docs/app-events) 
---


##Verify Setup (for iOS/Android) {#verify-setup}

Once you completed the step-by-step guide and use your app tracking will start.  You can verify that app events and the Facebook SDK are working properly via the [App Ads Helper](/tools/app-ads-helper/):


[Verify Setup](/tools/app-ads-helper/) 

---

 
###Keep in Mind {#reminder}
- **App ID:** The app ID used in your app must match the app ID used in your ad.
- **Advertising Accounts**: If you want other people or companies to run ads on behalf of your app, you can associate advertising accounts with your app via the [App Dashboard](/apps/89000000000000/settings/): From the settings tab, choose *Advanced > Advertising Accounts*.


---


##Next Steps {#next}

[Enable Deep Linking in your App](/docs/app-ads/deep-linking) [Create Ad](https://www.facebook.com/ads/create/?objective=MOBILE_APP_INSTALLS) 
---