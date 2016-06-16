  
  
<card><h1>Deep Linking in App Ads</h1><button href="https://www.facebook.com/ads/create" target="_blank" size="large" use="special">
Werbeanzeige erstellen
</button><button href="/tools/app-ads-helper/" size="large" target="_blank" use="confirm">
App Ads-Setup überprüfen
</button></card>

<card><p>Beim Deep Linking sendest du Personen direkt zu Informationen, an denen sie interessiert sind, wenn sie deine App zum ersten Mal öffnen. Du kannst Deep Links in jedem Werbeanzeigenformat verwenden: Mobile App Install Ads und Mobile App Engagement Ads.</p>

<h4>Vorteile für deine Werbeanzeigen</h4>

<p>Indem du Deep Linking für deine Apps Ads verwendest, beseitigst du zusätzliche Schritte zwischen dem Klicken auf die Werbeanzeige und dem Erreichen des für den Nutzer interessanten Inhalts (z. B. das Urlaubsangebot). So bietest du eine nahtlosere Kundenerfahrung. Ohne Deep Links müssen Personen manuell nach dem gewünschten Inhalt suchen und du riskierst, dass sie das Interesse verlieren.</p><hr/><h4>- <a href="#how-it-works">So funktioniert's</a></h4>

<h4>- <a href="#step-by-step">Schritt-für-Schritt Anleitung</a></h4></card>

<card><h2 id="how-it-works">So funktioniert's</h2>

<ol><li>Deine Werbeanzeige enthält <strong>personalisierten Inhalt</strong> (in unserem Beispiel eine <em>Urlaubsreise nach San Francisco</em>). </li>
<li>Personen <strong>laden deine App herunter</strong>.</li>
<li>Über einen Deep Link gelangen Personen direkt zum <strong>Impulsgeber</strong>, der <em>Urlaubsreise nach San Francisco</em>.</li>
</ol><asset width="700" handle="GJBexwATfcaVWBAGAJ8XMGMAAAAAbj0JAAAD"/><p>Da Personen die App-Nutzung an einer Stelle beginnen, die mit dem Grund für das Klicken auf die Werbeanzeige in Zusammenhang steht, ist es wahrscheinlicher, dass sie direkt mit dem Inhalt deiner App interagieren.</p></card>


<card><h2 id="step-by-step">Schritt-für-Schritt Anleitung</h2>

<h4>1. <a href="#os">Setup für iOS und Android</a></h4>

<h4>2. <a href="#sdk">Facebook-SDK</a></h4>

<h4>3. <a href="#settings">Facebook-App-Einstellungen</a></h4>

<h4>4. <a href="#deferred-deep-linking">Zurückgestelltes Deep Linking</a></h4>

<h4>5. <a href="#verify">Deep Link Setup überprüfen</a></h4>

<h4>6. <a href="#create-deeplink-ad">Deep Linking deiner Werbeanzeige hinzufügen</a></h4><hr/><h3 id="os">1. Setup für iOS und Android</h3>

<h4 id="ios">iOS</h4>

<p>Du kannst Deep Links einfach mit dem Bolts-Framework bearbeiten. Weitere Informationen zum Framework findest du auf Github: https://github.com/BoltsFramework/Bolts-iOS.</p>

<p>Wenn du das Bolts-Framework nicht verwenden möchtest, befolge z. B. eines der folgenden Tutorials:</p>

<ul><li><a href="/l.php?d=AQG2C-rVgpEQJlFRtlY8HZuO-A6s2tZrAraUeKdDB0TdmbUgBedLFomX8zc&amp;u=http%3A%2F%2Fwww.idev101.com%2Fcode%2FObjective-C%2Fcustom_url_schemes.html&amp;h=VAQEzbHo2&amp;s=1" target="_blank" rel="nofollow" onmouseover="LinkshimAsyncLink.swap(this, &quot;http:\/\/www.idev101.com\/code\/Objective-C\/custom_url_schemes.html&quot;);" onclick="LinkshimAsyncLink.swap(this, &quot;\/l.php?d=AQG2C-rVgpEQJlFRtlY8HZuO-A6s2tZrAraUeKdDB0TdmbUgBedLFomX8zc&amp;u=http\u00253A\u00252F\u00252Fwww.idev101.com\u00252Fcode\u00252FObjective-C\u00252Fcustom_url_schemes.html&amp;h=VAQEzbHo2&amp;s=1&quot;);">Objective-C: Custom URL Schemes</a> auf idev101.com</li>
<li><a href="/l.php?d=AQGgxRluIFq3jd_9KCk6SRierRGf2u6RgUx1UQuGgZyzxG3gtRsixbVSFcQ&amp;u=http%3A%2F%2Fblog.originate.com%2Fblog%2F2014%2F04%2F22%2Fdeeplinking-in-ios%2F&amp;h=DAQGnG4OL&amp;s=1" target="_blank" rel="nofollow" onmouseover="LinkshimAsyncLink.swap(this, &quot;http:\/\/blog.originate.com\/blog\/2014\/04\/22\/deeplinking-in-ios\/&quot;);" onclick="LinkshimAsyncLink.swap(this, &quot;\/l.php?d=AQGgxRluIFq3jd_9KCk6SRierRGf2u6RgUx1UQuGgZyzxG3gtRsixbVSFcQ&amp;u=http\u00253A\u00252F\u00252Fblog.originate.com\u00252Fblog\u00252F2014\u00252F04\u00252F22\u00252Fdeeplinking-in-ios\u00252F&amp;h=DAQGnG4OL&amp;s=1&quot;);">Deep Linking in iOS</a> auf blog.originate.com</li>
</ul><h4 id="android">Android</h4>

<p>Lies dir das offizielle Tutorial <a href="/l.php?d=AQHuyomnrxqGPIjsAZQRyAL6uK88_P3ZkmtHNSaGWSeqsa_FUufxPUyy3jc&amp;u=https%3A%2F%2Fdeveloper.android.com%2Ftraining%2Fapp-indexing%2Fdeep-linking.html&amp;h=nAQFY4nJ1&amp;s=1" target="_blank" rel="nofollow" onmouseover="LinkshimAsyncLink.swap(this, &quot;https:\/\/developer.android.com\/training\/app-indexing\/deep-linking.html&quot;);" onclick="LinkshimAsyncLink.swap(this, &quot;\/l.php?d=AQHuyomnrxqGPIjsAZQRyAL6uK88_P3ZkmtHNSaGWSeqsa_FUufxPUyy3jc&amp;u=https\u00253A\u00252F\u00252Fdeveloper.android.com\u00252Ftraining\u00252Fapp-indexing\u00252Fdeep-linking.html&amp;h=nAQFY4nJ1&amp;s=1&quot;);">Enabling Deep Links for App Content</a> auf android.com durch.</p>

<h3 id="sdk">2. Facebook-SDK</h3>

<p>Befolge unsere Schritt-für-Schritt Anleitung für das <a href="/docs/ads-for-apps-dev/sdk#step-by-step">Facebook-SDK Setup</a>. In diesem Leitfaden erhältst du Anleitungen zum:</p>

<ol><li>Abrufen einer Facebook-App-ID </li>
<li>Hinzufügen des Facebook-SDK zu deiner App </li>
<li>Nachverfolgen von Installationen aktivieren</li>
</ol><button href="/docs/ads-for-apps-dev/sdk#step-by-step" size="medium">
Facebook-SDK Setup
</button><h3 id="settings">3. Facebook-App-Einstellungen</h3>

<p>Wenn du das anfängliche Facebook-SDK Setup abgeschlossen hast, musst du Deep Linking-Informationen in deinen <strong><a href="/apps">Facebook-App-Einstellungen</a></strong> hinzufügen.</p>

<h4 id="settings-ios">iOS-Einstellungen</h4>

<ul><li><strong>URL-Schemasuffix</strong>: Füge dein URL-Schema ohne <code>://</code> hinzu (z. B. <code>mytravelapp</code>, wenn das URL-Schema <code>mytravelapp://</code> lautet).</li>
<li><strong>App Store-ID</strong>: Du kannst deine App Store-ID beispielsweise aus deiner App Store-URL abrufen: <em>https://itunes.apple.com/us/app/my-app/<code>APP_STORE_ID</code></em>.</li>
</ul><h4 id="android-settings">Android-Einstellungen</h4>

<ul><li><strong>ClassName</strong>: Suche den ClassName der Startaktivität in der Datei <code>AndroidManifest.xml</code>. Der Klassenname sollte das Format <code>com.example.androidapp.MainActivity</code> aufweisen.</li>
</ul><asset-image-card assetid="410471799132540" caption="iOS – Navigiere zum Dashboard &gt; Einstellungen &gt; iOS"/><asset-image-card assetid="475280682648792" caption="Android – Navigiere zum Dashboard &gt; Einstellungen &gt; Android"/><h3 id="deferred-deep-linking">4. Zurückgestelltes Deep Linking (optional)</h3>

<p>Mit dem zurückgestellten Deep Linking kannst du Personen zu einer benutzerdefinierten Ansicht leiten, <strong>nachdem</strong> sie deine App über den App Store installiert haben.</p>

<h4>Wann brauchst du das zurückgestellte Deep Linking?</h4>

<p>Du <strong>musst</strong> das zurückgestellte Deep Linking zu Werbeanzeigen, die Deep Linking verwenden, hinzufügen, wenn deine Zielgruppe aus Personen besteht, die deine App noch nicht installiert haben. Wenn du nur Personen ansprichst, die deine App bereits installiert haben, musst du kein zurückgestelltes Deep Linking hinzufügen.</p>

<h4>Zurückgestelltes Deep Linking mit App-Links</h4>

<p>Das Facebook-SDK für iOS und Android umfasst das Produkt <a href="/docs/applinks">App-Links</a>. Damit kannst du das zurückgestellte Deep Linking in deiner App unterstützen. Füge deiner App zusätzlich zur Deep Link-Implementierung einfach den folgenden Code hinzu, um zurückgestellte Deep Links zu bearbeiten:</p> 
<code tab="iossdk">
<![CDATA[ 
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
]]> 
</code> 

<code tab="androidsdk"> 
AppLinkData.fetchDeferredAppLinkData(this, 
  new AppLinkData.CompletionHandler() {
     @Override
     public void onDeferredAppLinkDataFetched(AppLinkData appLinkData) {
         // App-Link-Daten verarbeiten
     }
 }
);

</code>


<hr/><p><strong>Klassenreferenz:</strong> iOS &gt; <a href="/docs/reference/ios/current/class/FBSDKAppLinkUtility#fetchDeferredAppLink">FBSDKAppLinkUtility</a> | Android &gt; <a href="/docs/reference/android/current/class/AppLinkData/">AppLinkData</a></p>

<h3 id="verify">5. Deep Link Setup überprüfen</h3>

<p>Du kannst die Facebook-SDK- und Deep Link Setup in unserem <strong><a href="/tools/app-ads-helper/">App Ads Hilfstool</a></strong> im Abschnitt „Tools und Unterstützung“ überprüfen. Wir empfehlen, dein Setup zu überprüfen, bevor du Werbeanzeigen mit Deep Links schaltest.</p><button href="/tools/app-ads-helper/" size="large" use="confirm">
Deep Link Setup überprüfen
</button><h3 id="create-deeplink-ad">6. Deep Linking deiner Werbeanzeige hinzufügen</h3>

<p>Befolge unseren Leitfaden zum <strong><a href="/docs/ads-for-apps-dev/creating-ads">Erstellen von App Ads</a></strong>. Achte beim Erstellen deiner Werbeanzeige auf die folgenden Einstellungen:</p>

<ol><li><strong>Zielplattform</strong>: Verwende in <em>„Wen möchtest du mit deinen Werbeanzeigen erreichen?“</em>:

<ul><li><strong>iOS</strong>: <code>iOS only</code> für die Einstellung <strong>Plattform</strong>.</li>
<li><strong>Android</strong>: <code>Android only</code> für die Einstellung <strong>Plattform</strong>.</li>
</ul></li>
<li><strong>Deep Link hinzufügen</strong>: Füge in <em>„Welchen Text und welche Links möchtest du verwenden?“</em> deinen Deep Link hinzu (z. B. <code>mytravelapp://tripId=SF</code>, wie im folgenden Screenshot gezeigt).</li>
</ol><hr/><asset-image-card assetid="489536241210734" caption="Screenshot: Deep Linking deiner Werbeanzeige hinzufügen"/></card>


<card><h2 id="next">Nächste Schritte</h2><button href="https://www.facebook.com/ads/create" target="_blank" size="large" use="special">
Werbeanzeige erstellen
</button><button href="/docs/app-ads/formats/engagement-ads" size="large">
So erstellst du eine Engagement Ad
</button><button href="/docs/app-ads/measuring/installs-and-in-app-conversions" size="large">
Nachverfolgen von Installationen und App-internen Conversions
</button></card>
 
