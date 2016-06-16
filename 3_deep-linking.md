#Deep Linking in App Ads

[Create Ad](https://www.facebook.com/ads/create) [Verify Your App Ads Setup](/tools/app-ads-helper/) 

---



With deep linking you send people directly to information they are interested in when they open your app for the first time. You can use deep links in any ad format: Mobile App Install Ads and Mobile App Engagement Ads. 

####Why this is Helping your Ads
By using deep linking for your app ads, you are removing extra steps between clicking the ad and getting to content that interested them (for example the the vacation offer) provides a more seamless customer experience. Without deep links, people will have to search for the content they are looking for manually and you risk them dropping off. 



---


#### - [How it works](#how-it-works)
#### - [Step-by-Step Guide](#step-by-step)



---


##How it works {#how-it-works}
1. Your ad will show **personalized content**, in our example a *vacation to San Francisco*. 
2. People will **download your app**.
3. Via a deep link people will come back to their **point of inspiration**, the *vacation to San Francisco*.


![IMAGE](https://scontent-iad3-1.xx.fbcdn.net/t39.2365-6/13065872_1706822516243731_1664096159_n.png) 



As people will start in a place which is related to their moment when the tapped the ad, they are more likely to directly engage with the content of your app.
 


---


##Step-by-Step Guide {#step-by-step}

####1. [iOS & Android Setup](#os)
####2. [Facebook SDK](#sdk)
####3. [Facebook App Settings](#settings)
####4. [Deferred Deep Linking](#deferred-deep-linking)
####5. [Verify Deep Link Setup](#verify)
####6. [Add Deep Link to your Ad](#create-deeplink-ad)



---


###1. iOS & Android Setup {#os}

####iOS {#ios}

You can easily handle deep links using the Bolts Framework. You can learn more about the Framework on Github: https://github.com/BoltsFramework/Bolts-iOS.
 
If you do not want to use the Bolts Framework, follow for example one of these tutorials:

- [Objective-C: Custom URL Schemes](http://www.idev101.com/code/Objective-C/custom_url_schemes.html) on idev101.com
- [Deep Linking in iOS](http://blog.originate.com/blog/2014/04/22/deeplinking-in-ios/)  on blog.originate.com

####Android {#android}

Read the official tutorial [Enabling Deep Links for App Content](https://developer.android.com/training/app-indexing/deep-linking.html) on android.com.

###2. Facebook SDK {#sdk}

Follow our step-by-step guide [Facebook SDK Setup](/docs/ads-for-apps-dev/sdk#step-by-step). The guide will show you how to:

1. Get a Facebook App ID 
2. Add Facebook SDK to your app 
3. Enable Install Tracking


[Facebook SDK Setup](/docs/ads-for-apps-dev/sdk#step-by-step) 


###3. Facebook App Settings {#settings}

Once you completed the initial Facebook SDK Setup you need to add deep linking information in your **[Facebook app settings](/apps)**. 

####iOS Settings {#settings-ios}

- **URL Scheme Suffix**: Add your URL scheme without `://`, e.g. `mytravelapp` if your URL scheme is `mytravelapp://`.
- **App Store ID**: You can get your App Store ID for example from your App Store URL: *https://itunes.apple.com/us/app/my-app/`APP_STORE_ID`*.

####Android Settings {#android-settings}

- **ClassName**: Find the ClassName of the launch activity in the file `AndroidManifest.xml`. The class name should take the form `com.example.androidapp.MainActivity`.


![IMAGE](https://scontent-iad3-1.xx.fbcdn.net/t39.2178-6/11414380_410471802465873_567428398_n.png) 
iOS - Navigate to Dashboard > Settings > iOS

![IMAGE](https://fbcdn-dragon-a.akamaihd.net/hphotos-ak-xtf1/t39.2178-6/11409193_475280685982125_1690853610_n.png) 
Android - Navigate to Dashboard > Settings > Android




###4. Deferred Deep Linking (optional) {#deferred-deep-linking}
Deferred deep linking allows you to send people to a custom view **after they installed** your app via the app store. 

####When do You Need Deferred Deep Linking?
You **must** add deferred deep linking to an ad using deep linking, if you target people who did not install your app yet. If you are only targeting people who already installed your app, you do not need to add deferred deep linking.

#### Deferred Deep Linking with App Links
The Facebook SDK for iOS and Android includes the product [App Links](/docs/applinks), which will enable you to support deferred deep linking in your app. In addition to your deep link implementation, just add the following code to your app to handle deferred deep links:

  
  
**iOS SDK**
``` 
// Add Bolts.framework to your project (part of the FB SDK)
#import <Bolts/Bolts.h> 
#import <FBSDKCoreKit/FBSDKCoreKit.h>

- (BOOL)application:(UIApplication *)application didFinishLaunchingWithOptions:(NSDictionary *)launchOptions {
  if (launchOptions[UIApplicationLaunchOptionsURLKey] == nil) {
    [FBSDKAppLinkUtility fetchDeferredAppLink:^(NSURL *url, NSError *error) {
      if (error) {
        NSLog(@"Received error while fetching deferred app link %@", error);
      }
      if (url) {
        [[UIApplication sharedApplication] openURL:url];
      }
    }];
  }
  return YES;
}
```

**Android SDK**
``` 
AppLinkData.fetchDeferredAppLinkData(this, 
  new AppLinkData.CompletionHandler() {
     @Override
     public void onDeferredAppLinkDataFetched(AppLinkData appLinkData) {
         // Process app link data
     }
 }
);

```



  ---

**Class Reference:** iOS > [FBSDKAppLinkUtility](/docs/reference/ios/current/class/FBSDKAppLinkUtility#fetchDeferredAppLink) | Android > [AppLinkData](/docs/reference/android/current/class/AppLinkData/)  

###5. Verify Deep Link Setup {#verify}
You can verify your Facebook SDK and deep link setup within our **[App Ads Helper](/tools/app-ads-helper/)** in the tools & support section. We recommend to verify your setup before you start running deep link ads.

[Verify Deep Link Setup](/tools/app-ads-helper/) 

 

###6. Add Deep Link to your Ad {#create-deeplink-ad}

Follow our guide **[Creating App Ads](/docs/ads-for-apps-dev/creating-ads)**. When creating your ad pay attention to the following settings:

1. **Target Platform**: In *"Who do you want your ads to reach?"* use:
- **iOS**: `iOS only` for the setting **platform**.
- **Android**: `Android only` for the setting **platform**.
2. **Add Deep Link**: In *"What text and links do you want to use?"* add your deep link, e.g. `mytravelapp://tripId=SF` as shown in the screenshot below.



---

![IMAGE](https://fbcdn-dragon-a.akamaihd.net/hphotos-ak-xfa1/t39.2178-6/11404834_489536244544067_2128620228_n.png) 
Screenshot: Add Deep Link to your Ad


---


##Next Steps {#next}


[Create Ad](https://www.facebook.com/ads/create) [How to Create an Engagement Ad](/docs/app-ads/formats/engagement-ads) [Install and In-App Conversion Tracking](/docs/app-ads/measuring/installs-and-in-app-conversions) 

---