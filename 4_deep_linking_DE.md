
# Deep Linking in App Ads

[Werbeanzeige erstellen](https://www.facebook.com/ads/create) [App Ads-Setup überprüfen](/tools/app-ads-helper/) 

---

Beim Deep Linking sendest du Personen direkt zu Informationen, an denen sie interessiert sind, wenn sie deine App zum ersten Mal öffnen. Du kannst Deep Links in jedem Werbeanzeigenformat verwenden: Mobile App Install Ads und Mobile App Engagement Ads.#### Vorteile für deine WerbeanzeigenIndem du Deep Linking für deine Apps Ads verwendest, beseitigst du zusätzliche Schritte zwischen dem Klicken auf die Werbeanzeige und dem Erreichen des für den Nutzer interessanten Inhalts (z. B. das Urlaubsangebot). So bietest du eine nahtlosere Kundenerfahrung. Ohne Deep Links müssen Personen manuell nach dem gewünschten Inhalt suchen und du riskierst, dass sie das Interesse verlieren.

---
#### - [So funktioniert's](#how-it-works) #### - [Schritt-für-Schritt Anleitung](#step-by-step) 

---



## So funktioniert's

Deine Werbeanzeige enthält **personalisierten Inhalt** (in unserem Beispiel eine **Urlaubsreise nach San Francisco**). 
Personen **laden deine App herunter**.
Über einen Deep Link gelangen Personen direkt zum **Impulsgeber**, der **Urlaubsreise nach San Francisco**.

![IMAGE](https://scontent-iad3-1.xx.fbcdn.net/t39.2365-6/13065872_1706822516243731_1664096159_n.png) 
Da Personen die App-Nutzung an einer Stelle beginnen, die mit dem Grund für das Klicken auf die Werbeanzeige in Zusammenhang steht, ist es wahrscheinlicher, dass sie direkt mit dem Inhalt deiner App interagieren.

---



## Schritt-für-Schritt Anleitung

#### 1. [Setup für iOS und Android](#os) #### 2. [Facebook-SDK](#sdk) #### 3. [Facebook-App-Einstellungen](#settings) #### 4. [Zurückgestelltes Deep Linking](#deferred-deep-linking) #### 5. [Deep Link Setup überprüfen](#verify) #### 6. [Deep Linking deiner Werbeanzeige hinzufügen](#create-deeplink-ad) 

---


### 1. Setup für iOS und Android

#### iOSDu kannst Deep Links einfach mit dem Bolts-Framework bearbeiten. Weitere Informationen zum Framework findest du auf Github: https://github.com/BoltsFramework/Bolts-iOS.Wenn du das Bolts-Framework nicht verwenden möchtest, befolge z. B. eines der folgenden Tutorials:
[Objective-C: Custom URL Schemes](/l.php?d=AQG2C-rVgpEQJlFRtlY8HZuO-A6s2tZrAraUeKdDB0TdmbUgBedLFomX8zc&u=http%3A%2F%2Fwww.idev101.com%2Fcode%2FObjective-C%2Fcustom_url_schemes.html&h=VAQEzbHo2&s=1)  auf idev101.com
[Deep Linking in iOS](/l.php?d=AQGgxRluIFq3jd_9KCk6SRierRGf2u6RgUx1UQuGgZyzxG3gtRsixbVSFcQ&u=http%3A%2F%2Fblog.originate.com%2Fblog%2F2014%2F04%2F22%2Fdeeplinking-in-ios%2F&h=DAQGnG4OL&s=1)  auf blog.originate.com
#### AndroidLies dir das offizielle Tutorial [Enabling Deep Links for App Content](/l.php?d=AQHuyomnrxqGPIjsAZQRyAL6uK88_P3ZkmtHNSaGWSeqsa_FUufxPUyy3jc&u=https%3A%2F%2Fdeveloper.android.com%2Ftraining%2Fapp-indexing%2Fdeep-linking.html&h=nAQFY4nJ1&s=1)  auf android.com durch.

### 2. Facebook-SDK

Befolge unsere Schritt-für-Schritt Anleitung für das [Facebook-SDK Setup](/docs/ads-for-apps-dev/sdk#step-by-step) . In diesem Leitfaden erhältst du Anleitungen zum:
Abrufen einer Facebook-App-ID 
Hinzufügen des Facebook-SDK zu deiner App 
Nachverfolgen von Installationen aktivieren
[Facebook-SDK Setup](/docs/ads-for-apps-dev/sdk#step-by-step) 

### 3. Facebook-App-Einstellungen

Wenn du das anfängliche Facebook-SDK Setup abgeschlossen hast, musst du Deep Linking-Informationen in deinen **[Facebook-App-Einstellungen](/apps) ** hinzufügen.#### iOS-Einstellungen
**URL-Schemasuffix**: Füge dein URL-Schema ohne ```://```
 hinzu (z. B. ```mytravelapp```
, wenn das URL-Schema ```mytravelapp://```
 lautet).
**App Store-ID**: Du kannst deine App Store-ID beispielsweise aus deiner App Store-URL abrufen: **https://itunes.apple.com/us/app/my-app/```APP_STORE_ID```
**.
#### Android-Einstellungen
**ClassName**: Suche den ClassName der Startaktivität in der Datei ```AndroidManifest.xml```
. Der Klassenname sollte das Format ```com.example.androidapp.MainActivity```
 aufweisen.

![IMAGE](https://scontent-iad3-1.xx.fbcdn.net/t39.2178-6/11414380_410471802465873_567428398_n.png) 
*iOS – Navigiere zum Dashboard > Einstellungen > iOS*

![IMAGE](https://fbcdn-dragon-a.akamaihd.net/hphotos-ak-xtf1/t39.2178-6/11409193_475280685982125_1690853610_n.png) 
*Android – Navigiere zum Dashboard > Einstellungen > Android*


### 4. Zurückgestelltes Deep Linking (optional)

Mit dem zurückgestellten Deep Linking kannst du Personen zu einer benutzerdefinierten Ansicht leiten, **nachdem** sie deine App über den App Store installiert haben.#### Wann brauchst du das zurückgestellte Deep Linking?Du **musst** das zurückgestellte Deep Linking zu Werbeanzeigen, die Deep Linking verwenden, hinzufügen, wenn deine Zielgruppe aus Personen besteht, die deine App noch nicht installiert haben. Wenn du nur Personen ansprichst, die deine App bereits installiert haben, musst du kein zurückgestelltes Deep Linking hinzufügen.#### Zurückgestelltes Deep Linking mit App-LinksDas Facebook-SDK für iOS und Android umfasst das Produkt [App-Links](/docs/applinks) . Damit kannst du das zurückgestellte Deep Linking in deiner App unterstützen. Füge deiner App zusätzlich zur Deep Link-Implementierung einfach den folgenden Code hinzu, um zurückgestellte Deep Links zu bearbeiten:**iOS SDK**
``` 
// Füge Bolts.framework zu deinem Projekt hinzu (Teil des FB-SDK)
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
         // App-Link-Daten verarbeiten
     }
 }
);

```



---
**Klassenreferenz:** iOS > [FBSDKAppLinkUtility](/docs/reference/ios/current/class/FBSDKAppLinkUtility#fetchDeferredAppLink)  | Android > [AppLinkData](/docs/reference/android/current/class/AppLinkData/) 

### 5. Deep Link Setup überprüfen

Du kannst die Facebook-SDK- und Deep Link Setup in unserem **[App Ads Hilfstool](/tools/app-ads-helper/) ** im Abschnitt „Tools und Unterstützung“ überprüfen. Wir empfehlen, dein Setup zu überprüfen, bevor du Werbeanzeigen mit Deep Links schaltest.[Deep Link Setup überprüfen](/tools/app-ads-helper/) 

### 6. Deep Linking deiner Werbeanzeige hinzufügen

Befolge unseren Leitfaden zum **[Erstellen von App Ads](/docs/ads-for-apps-dev/creating-ads) **. Achte beim Erstellen deiner Werbeanzeige auf die folgenden Einstellungen:
**Zielplattform**: Verwende in **„Wen möchtest du mit deinen Werbeanzeigen erreichen?“**:

**iOS**: ```iOS only```
 für die Einstellung **Plattform**.
**Android**: ```Android only```
 für die Einstellung **Plattform**.
**Deep Link hinzufügen**: Füge in **„Welchen Text und welche Links möchtest du verwenden?“** deinen Deep Link hinzu (z. B. ```mytravelapp://tripId=SF```
, wie im folgenden Screenshot gezeigt).


---

![IMAGE](https://fbcdn-dragon-a.akamaihd.net/hphotos-ak-xfa1/t39.2178-6/11404834_489536244544067_2128620228_n.png) 
*Screenshot: Deep Linking deiner Werbeanzeige hinzufügen*


---



## Nächste Schritte

[Werbeanzeige erstellen](https://www.facebook.com/ads/create) [So erstellst du eine Engagement Ad](/docs/app-ads/formats/engagement-ads) [Nachverfolgen von Installationen und App-internen Conversions](/docs/app-ads/measuring/installs-and-in-app-conversions) 

---