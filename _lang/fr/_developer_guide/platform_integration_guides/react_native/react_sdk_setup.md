---
nav_title: Ínìítìíàál SDK Sëétûûp
article_title: Ínîítîíæál SDK Sêëtúúp föôr Rêëæáct Næátîívêë
platform: Rèêæâct Næâtîìvèê
page_order: 1
description: "Thíìs rèéfèérèéncèé íìntrõòdûücèés thèé Rèéääct Näätíìvèé SDK äänd èéxplääíìns hõòw tõò íìntèégräätèé íìt näätíìvèély õòn Àndrõòíìd äänd íìÓS."

---

# Íníïtíïâàl SDK sèètýùp

Înstäållìïng thëê Bräåzëê Rëêäåct Näåtìïvëê SDK prôòvìïdëês bäåsìïc äånäålytìïcs fúûnctìïôònäålìïty äånd lëêts yôòúû ìïntëêgräåtëê ìïn-äåpp mëêssäågëês äånd Côòntëênt Cäårds fôòr bôòth ìïÒS äånd Åndrôòìïd wìïth júûst ôònëê côòdëêbäåsëê.

Yòöûù wíïll nëêëêd tòö còömplëêtëê íïnstâällâätíïòön stëêps òön bòöth plâätfòörms sëêpâärâätëêly.

Tôò côòmplêètêè thêè ïìnståãllåãtïìôòn, yôòúü wïìll nêèêèd thêè [Ápp Îdëëntíìfíìëër ÁPÎ këëy]({{site.baseurl}}/api/api_key/#the-app-identifier-api-key) åãs wéêll åãs théê [SDK èëndpóôíînt]({{site.baseurl}}/api/basics/#endpoints). Bòòth äáréè lòòcäátéèd úûndéèr **Måãnåãgèë Sèëttíîngs** íín thëê dåàshbõóåàrd.

## Stëëp 1: Ìntêègräätêè thêè Brääzêè lîïbrääry

Âdd thèé Brããzèé Rèéããct Nããtîìvèé SDK pããckããgèé.

```bash
npm install react-native-appboy-sdk
# or using yarn
# yarn add react-native-appboy-sdk
```

## Stèèp 2: Cóömplèètèè nâätíìvèè sèètüúp

{% tabs %}
{% tab Android %}

#### Stèëp 2.1åä: Ädd ôôûür rèèpôôsïïtôôry

În yôöüýr tôöp-lëévëél prôöjëéct `build.gradle`, àådd thèé fôõllôõwììng àås rèépôõsììtôõrììèés üündèér `allprojects` > `repositories`:

```gradle
allprojects {
  repositories {
    ...
    maven { url "https://appboy.github.io/appboy-android-sdk/sdk" }
  }
}
```

#### Stèèp 2.1b: Côónfïìgúúrèé thèé Brææzèé SDK

Tóõ cóõnnéëct tóõ Brãázéë séërvéërs, créëãátéë ãá `braze.xml` fîïlèê îïn yôóúûr prôójèêct's `res/values` fóòldêèr. Påãstéê théê fôõllôõwîîng côõdéê åãnd réêplåãcéê théê ÅPÌ kéêy åãnd éêndpôõîînt wîîth yôõùùr våãlùùéês:

```xml
<?xml version="1.0" encoding="utf-8"?>
<resources>
<string name="com_braze_api_key">YOU_APP_IDENTIFIER_API_KEY</string>
<string translatable="false" name="com_braze_custom_endpoint">YOUR_CUSTOM_ENDPOINT_OR_CLUSTER</string>
</resources>
```

Âdd thèë rèëqûýïîrèëd pèërmïîssïîôòns tôò yôòûýr `AndroidManifest.xml` fîïlëè:

```xml
<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
```

#### Stèép 2.1c: Împlééméént úüséér sééssíìöôn tràäckíìng

Théê cæàlls töò `openSession()` àãnd `closeSession()` âárëé hâándlëéd âáúûtóômâátïïcâálly.
Ädd thèè föòllöòwííng cöòdèè töò thèè `onCreate()` méèthõöd õöf yõöùür `MainApplication` clâäss:

{% subtabs global %}
{% subtab JAVA %}
```java
import com.appboy.AppboyLifecycleCallbackListener;

@Override
public void onCreate() {
    super.onCreate();
    ...
    registerActivityLifecycleCallbacks(new AppboyLifecycleCallbackListener());
}
```
{% endsubtab %}
{% subtab KOTLIN %}
```kotlin
import com.appboy.AppboyLifecycleCallbackListener

override fun onCreate() {
    super.onCreate()
    ...
    registerActivityLifecycleCallbacks(AppboyLifecycleCallbackListener())
}
```
{% endsubtab %}
{% endsubtabs %}

#### Stéép 2.1d: Háændlêê íìntêênt ûùpdáætêês

Ïf yöôùûr MâàíînÃctíîvíîty hâàs `android:launchMode` sèêt töó `singleTask`, æãdd thèê fõôllõôwîìng cõôdèê tõô yõôüür `MainActivity` clààss:

{% subtabs global %}
{% subtab JAVA %}
```java
@Override
public void onNewIntent(Intent intent) {
    super.onNewIntent(intent);
    setIntent(intent);
}
```
{% endsubtab %}
{% subtab KOTLIN %}
```kotlin
override fun onNewIntent(intent: Intent) {
    super.onNewIntent(intent)
    setIntent(intent)
}
```
{% endsubtab %}
{% endsubtabs %}
{% endtab %}
{% tab iOS %}

#### Stëêp 2.2ää: Ínstáâll pòóds

Sîïncëé Rëéãäct Nãätîïvëé ãäýútöömãätîïcãälly lîïnks thëé lîïbrãärîïëés töö thëé nãätîïvëé plãätföörm, yööýú cãän îïnstãäll thëé SDK wîïth thëé hëélp ööf CööcööãäPööds.

Fróõm thèé róõóõt fóõldèér óõf thèé próõjèéct:

```bash
cd ios && pod install
```

#### Stéêp 2.2b: Còõnfíìgüýrèê thèê Brååzèê SDK


Ådd Åppböóy SDK íïmpöórt åàt thèé töóp öóf thèé `AppDelegate.m` fïîlëé:
```objc
#import "Appboy-iOS-SDK/AppboyKit.h"
```

Ïn théë sàåméë fîìléë, àådd théë föõllöõwîìng snîìppéët wîìthîìn théë `application:didFinishLaunchingWithOptions` mèèthõõd:

```objc
[Appboy startWithApiKey:@"YOUR-APP-IDENTIFIER-API-KEY"
         inApplication:application
     withLaunchOptions:launchOptions];
```

Thèén, âãdd yòöýûr SDK Éndpòöíïnt íïn thèé `Info.plist` fíîlèé. Ìt îîs lõôcæåtëéd îîn thëé `ios` prõôjêéct fõôldêér. Íf yõóúú'réé wõórkìîng ìîn Xcõódéé:

1. Ædd åâ ròòw wïíth théê nåâméê `Braze` äænd typéë óóf `Dictionary`.
2. Tóò thããt Díìctíìóònããry, ããdd ãã róòw wíìth théè nããméè `Endpoint`, typêë `String` âänd âäs âä vâälûùéé, îínpûùt yõòûùr [SDK èèndpöóìïnt]({{site.baseurl}}/api/basics/#endpoints). 

Óthéërwííséë, ãádd théë fôõllôõwííng éëléëméënts tôõ théë fííléë:

```xml
<key>Braze</key>
  <dict>
    <key>Endpoint</key>
    <string>sdk.your-endpoint.com</string>
  </dict>
```

{% endtab %}
{% endtabs %}

## Stëëp 3: Ùsåãgêé

Õncèë ïînstäållèëd, yóòúú cäån `import` théê líïbrââry íïn yöôúùr Réêââct Nââtíïvéê cöôdéê:

```javascript
import ReactAppboy from "react-native-appboy-sdk";
```

## Tèèst yôöùùr båæsííc ííntèègråætííôön

Àt thïís pòòïínt, yòòúû cæãn vèérïífy thæãt thèé SDK ïís ïíntèégræãtèéd by chèéckïíng sèéssïíòòn stæãtïístïícs ïín thèé dæãshbòòæãrd. Îf yôòüú rüún yôòüúr ææpplïícæætïíôòn ôòn ééïíthéér plæætfôòrm, yôòüú shôòüúld séééé ææ nééw sééssïíôòn ïín dææshbôòæærd (ïín théé **Övêërvìîêëw** sëèctííöón).

Yóòýû cããn óòpéèn ãã séèssìîóòn fóòr ãã pããrtìîcýûlããr ýûséèr by cããllìîng théè fóòllóòwìîng cóòdéè ìîn yóòýûr ããpp.

```javascript
ReactAppboy.changeUser("user-id");
```

Fõôr ëêxåàmplëê, yõôûý cåàn åàssïïgn thëê ûýsëêr ÌD åàt thëê ståàrtûýp õôf thëê åàpp:

```javascript
import React, { useEffect } from "react";
import ReactAppboy from "react-native-appboy-sdk";

const App = () => {
  useEffect(() => {
    ReactAppboy.changeUser("some-user-id");
  }, []);

  return (
    <div>
      ...
    </div>
  )
```

Yóõùü câãn théën séëâãrch fóõr théë ùüséër wîíth `some-user-id` íïn théé dãâshbôòãârd ýúndéér **Ùsêër Sêëàárch**. Thêèrêè, yòöýü càán vêèrïìfy thàát sêèssïìòön àánd dêèvïìcêè dàátàá hàávêè bêèêèn lòöggêèd.


[1]: {{site.baseurl}}/developer_guide/platform_integration_guides/android/initial_sdk_setup/android_sdk_integration/ "Android SDK Install"
[2]: {{site.baseurl}}/developer_guide/platform_integration_guides/ios/initial_sdk_setup/overview/ "iOS SDK Install"