# Creating App Ads
Learn how to run ads for your mobile or desktop app in Facebook's news feed.

__[Mobile App Ads](#mobile-ads)__  
Promote your app on mobile devices.

__[Desktop App Ads](#desktop-ads)__  
Promote your canvas app on desktop.

__[Create Your First Ad](#create)__  
Prerequisites and step-by-step guide.


---
[Create Ad](https://www.facebook.com/ads/create/) [Verify Your App Ads Setup](/tools/app-ads-helper/) 

---

 
##Mobile App Ads {#mobile-ads}

With **mobile app ads**, you can promote your mobile app in the Facebook mobile News Feed. Each ad will be delivered as a sponsored story labeled **Suggested App**. People can like, comment, share and, most important, install your app with a simple tap.

 
?[Sponsored Story - See screenshot below]([asset:685288151617574])

####Ad Layout {#mobile-ads-layout}

The sponsored story shows your ad copy in the Facebook mobile ad unit. The ad unit is made up by your app's name and your ad creative.

?[Call-To-Action button - See screenshot below]([asset:1446586538986555])

####Call to Action {#mobile-ads-cta}
A customizable call to action button (e.g., **Install Now**) is placed in the bottom right of the ad. 


?[Store Page - See screenshot below]([asset:854022798010170])

####App Store {#mobile-ads-store}
If people tap the call to action button, they will be redirect to your apps's Google Play or Apple App Store page (for install ads), or a specific part of your app (for engagement ads). 

?[](https://fbcdn-dragon-a.akamaihd.net/hphotos-ak-xap1/t39.2365-6/13065813_951534138299702_629518971_n.png) 
[Design Guidelines for Mobile App Ads](https://www.facebook.com/business/ads-guide/app-installs/mobile-app/) 

---

 
##Desktop App Ads {#desktop-ads}

With **desktop app ads** you can promote your desktop app in the News Feed on *facebook.com*. In addition you can also book ads in the right hand column. 



?[Sponsored Story - See screenshot below]([asset:685288151617574])

####Ad Layout: News Feed {#desktop-ads-layout}
Your ads show a short message and a card introducing your app. The card is made up by your app's name and an image.

?[Right Column Ad - See screenshot below]([asset:1446586538986555])

####Ad Layout: Right Column {#desktop-ads-right-column}
This ad format is placed in the right colum next to the News Feed.
Besides size and arrangement differences this ad will not show an app icon.


?[Call-To-Action button - See screenshot below]([asset:854022798010170])

####Call-to-Action {#mobile-ads-cta}
A Call-To-Action button is placed in the bottom right of the ad, either *"Play Now"* or *"Use Now"*. If people click the Call-To-Action button they will be asked to accept your app's permission prompt. If a person agrees it will be counted as an install, allowing you to measure and optimize your ads based on installs.

After accepting the permission request people will be redirected to your app URL.

?[](https://scontent-iad3-1.xx.fbcdn.net/t39.2178-6/11891345_1181178455231619_1911494679_n.jpg) 
[Design Guidelines for Desktop App Ads](https://www.facebook.com/business/ads-guide/app-installs/desktop-app/) 

---


##Create Your First Ad {#create}

###Prerequisites {#create-prerequisites}
Before creating an ad you need to fulfill the these prerequisites:

- **Mobile Apps**: Your app must be available in the Apple App or Google Play store.
- **Desktop Apps**: Your app must be a [Facebook Canvas](#link) app.
- **Facebook Page**: You need to be admin of a Facebook page. 
- **Image(s)**: You need at least one image to create an ad.
- **Ads Account**: If you haven’t advertised with Facebook before, you may need to set up a payment source in the [Facebook Ads Manager](https://www.facebook.com/ads/manager).
- **For Amazon Apps:** You need to configure your Amazon Appstore url in the app settings under the Android platform with your Facebook App ID. We require your Amazon Appstore app have a corresponding Facebook app within your app settings

####Link Ad Accounts

To measure installs in the [Facebook Ads Manager](https://www.facebook.com/ads/manager) or if you want other people or companies to run ads on behalf of your app, you have to associate [advertising accounts](https://www.facebook.com/ads/manager/account/settings/) with your app using the app dashboard. Use the button below to navigate to the advanced app settings and add accounts via the `Authorized Ad Account IDs` input field. 


[Link Ad Accounts](/apps/) 

---
 

####Recommended
- **Facebook SDK**: Take advantage of our advanced targeting, measurement and optimization tools by [adding the Facebook SDK](/docs/app-ads/sdk) for iOS or Android to your app. This step is optional but highly recommended.
- **Exclude People who Installed Your App**: [Read our guide below](#exclude-users).




---


###Step-by-Step {#create-step-by-step}
The Ads Create Wizard will guide you through all necessary steps to create an ad. When changing parameters you will be able to preview the result of each setting, for example how your ad will look like.


?[](https://fbcdn-dragon-a.akamaihd.net/hphotos-ak-xtp1/t39.2178-6/11057091_893120464081049_587314363_n.png) 



1. **Get Started:** Use the **Create Ad** button below and choose **Get installs of your app** to set the objective "App Installs".
2. **App**: Pick your mobile or desktop app by using the typeahead or copy and paste your app's Google Play or Apple App Store URL into the form.
3. **For Multi-Platform Apps:** You can only promote one platform at a time. Select a platform, later repeat all steps to create ads for other platforms.
4. **Audience:** Who do you want your ads to reach?
5. **Budget**: How much do you want to spend?
6. **Media**: Upload or pick at least one images for your ad. The recommended image size is `1200X628` pixel.  Use may also use a video.
7. **Text & Links**: Set what text and links do you want to use. Connect your ad to your Facebook Page, pick a Call-To-Action.
8. **Place Order:** Use the "Place Order" button so book your ad. You may use the "Review Order" to verify your ad configuration.



---
[Create Ad](https://www.facebook.com/ads/create/) 

---


##Exclude People who Installed Your App {#exclude-users}



This section does not apply to [engagement ads](/docs/app-ads/formats/engagement-ads), but only for install ads.


---


**For Android**, people who installed your app are automatically excluded as long as you provide us your app's package name in the app settings page.

  
 

**For  iOS 9.0+**, the only way to exclude users is forwarding app events to Facebook. We are able to exclude users for 180 days after their most recent app event (whether it is an install, app open or in-app event). If you use a Mobile Measurement Partner (MMP) that only sends install events, after 180 days, those users with the app installed will begin to see install ads again even if they are using the app consistently.

**For iOS 8.x and below**, we are able to exclude users if we can detect that your app is already installed on their device.  To allow us to detect if your app is installed, you must do one of the following:

1. Configure your application's `Info.plist` file so that  `fb{your-fb-app-id}` is a registered URL scheme for your app.  If Facebook detects that `fb{your-fb-app-id}` is a registered URL scheme on the device, we'll know your app is already installed and we can exclude that user. See  [Configure Xcode Project](/docs/ios/getting-started#xcode) for instructions on how to configure your app's `Info.plist`.  You might have already done this if you're using the Facebook SDK.
  
2. Provide a “Deep Link” URL when creating an ad.  A deep link is a URL that directly opens your application on the device.  For example, `yelp:///search?terms=burritos` is a deep link that directly opens the Yelp application.  If Facebook can detect that your deep link URL's scheme is a registered scheme on the device, we'll know your app is installed and we can exclude that user.


---



##Next Steps {#next}
After you get your ad up and running, we recommend that you integrate the Facebook into your app to take advantage of our advanced measurement and optimization tools. 

[Using the SDK with App Ads](/docs/app-ads/sdk) [Learn how to Measure App Installs](/docs/app-ads/measuring/installs-and-in-app-conversions) [Deep Linking in App Ads](/docs/app-ads/deep-linking) 

---