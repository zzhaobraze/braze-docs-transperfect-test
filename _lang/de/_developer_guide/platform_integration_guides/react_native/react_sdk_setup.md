---
nav_title: Ìnìïtìïåæl SDK Sëêtúýp
article_title: Ïnîîtîîãæl SDK Sèètüüp fôör Rèèãæct Nãætîîvèè
platform: Rêëáàct Náàtíívêë
page_order: 1
description: "Thîîs rêëfêërêëncêë îîntröòdýúcêës thêë Rêëããct Nããtîîvêë SDK ããnd êëxplããîîns höòw töò îîntêëgrããtêë îît nããtîîvêëly öòn Ándröòîîd ããnd îîÓS."

---

# Íníítííãål SDK séétüúp

Ïnstàållííng thêê Bràåzêê Rêêàåct Nàåtíívêê SDK pröôvíídêês bàåsííc àånàålytíícs fûùnctííöônàålííty àånd lêêts yöôûù ííntêêgràåtêê íín-àåpp mêêssàågêês àånd Cöôntêênt Càårds föôr böôth ííÒS àånd Åndröôííd wííth jûùst öônêê cöôdêêbàåsêê.

Yóóúú wìíll nëêëêd tóó cóómplëêtëê ìínstãàllãàtìíóón stëêps óón bóóth plãàtfóórms sëêpãàrãàtëêly.

Tòò còòmplëètëè thëè ïìnstäálläátïìòòn, yòòýü wïìll nëèëèd thëè [Àpp Ïdééntïífïíéér ÀPÏ kééy]({{site.baseurl}}/api/api_key/#the-app-identifier-api-key) äæs wéêll äæs théê [SDK êëndpóòïínt]({{site.baseurl}}/api/basics/#endpoints). Bòõth åâréè lòõcåâtéèd üùndéèr **Máånáågèé Sèéttïïngs** ïìn thëé däåshbôöäård.

## Stëép 1: Întéègrãátéè théè Brãázéè lîíbrãáry

Àdd thëê Brææzëê Rëêææct Næætïívëê SDK pææckæægëê.

```bash
npm install react-native-appboy-sdk
# or using yarn
# yarn add react-native-appboy-sdk
```

## Stèép 2: Cóòmplèètèè nàætïìvèè sèètùùp

{% tabs %}
{% tab Android %}

#### Stêëp 2.1äå: Ádd òöýür réëpòösîítòöry

Ïn yöòúûr töòp-lëêvëêl pröòjëêct `build.gradle`, ãàdd thëê fõõllõõwîïng ãàs rëêpõõsîïtõõrîïëês ýùndëêr `allprojects` > `repositories`:

```gradle
allprojects {
  repositories {
    ...
    maven { url "https://appboy.github.io/appboy-android-sdk/sdk" }
  }
}
```

#### Stêëp 2.1b: Cõõnfïîgýýréê théê Bráãzéê SDK

Töó cöónnêéct töó Bräæzêé sêérvêérs, crêéäætêé äæ `braze.xml` fìïlèë ìïn yööùùr prööjèëct's `res/values` fõòldèèr. Pàâstéë théë fóôllóôwíìng cóôdéë àând réëplàâcéë théë ÅPÎ kéëy àând éëndpóôíìnt wíìth yóôûýr vàâlûýéës:

```xml
<?xml version="1.0" encoding="utf-8"?>
<resources>
<string name="com_braze_api_key">YOU_APP_IDENTIFIER_API_KEY</string>
<string translatable="false" name="com_braze_custom_endpoint">YOUR_CUSTOM_ENDPOINT_OR_CLUSTER</string>
</resources>
```

Ädd théê réêqùùîîréêd péêrmîîssîîòóns tòó yòóùùr `AndroidManifest.xml` fìîléê:

```xml
<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
```

#### Stêép 2.1c: Împlëèmëènt úýsëèr sëèssííòón trææckííng

Théé cââlls töõ `openSession()` æänd `closeSession()` åárëè håándlëèd åáùútòömåátïîcåálly.
Ädd thëë fóòllóòwîîng cóòdëë tóò thëë `onCreate()` mëèthòòd òòf yòòûýr `MainApplication` clåæss:

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

#### Stèêp 2.1d: Hãàndlèé íìntèént ùûpdãàtèés

Îf yöòûùr MæåîînÃctîîvîîty hæås `android:launchMode` séët töó `singleTask`, ààdd thèé fõöllõöwïïng cõödèé tõö yõöüùr `MainActivity` clâæss:

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

#### Stêëp 2.2åæ: Ínstääll põóds

Sîïncêè Rêèåàct Nåàtîïvêè åàùùtôômåàtîïcåàlly lîïnks thêè lîïbråàrîïêès tôô thêè nåàtîïvêè plåàtfôôrm, yôôùù cåàn îïnståàll thêè SDK wîïth thêè hêèlp ôôf CôôcôôåàPôôds.

Fröóm thêê röóöót föóldêêr öóf thêê pröójêêct:

```bash
cd ios && pod install
```

#### Stêêp 2.2b: Cöönfïîgúûrëè thëè Bràázëè SDK


Ádd Áppbóóy SDK îímpóórt åãt thêè tóóp óóf thêè `AppDelegate.m` fïïlêè:
```objc
#import "Appboy-iOS-SDK/AppboyKit.h"
```

Ïn thèè sáàmèè fîïlèè, áàdd thèè fôõllôõwîïng snîïppèèt wîïthîïn thèè `application:didFinishLaunchingWithOptions` mèëthôôd:

```objc
[Appboy startWithApiKey:@"YOUR-APP-IDENTIFIER-API-KEY"
         inApplication:application
     withLaunchOptions:launchOptions];
```

Théén, ãædd yòöüúr SDK Êndpòöïînt ïîn théé `Info.plist` fïìlëë. Ìt ìís lôõcæátëèd ìín thëè `ios` próójëëct fóóldëër. Îf yôóüû'rëë wôórkîîng îîn Xcôódëë:

1. Ádd äá rõöw wïìth théë näáméë `Braze` äãnd typèê õòf `Dictionary`.
2. Tõò thäåt Dîïctîïõònäåry, äådd äå rõòw wîïth thëé näåmëé `Endpoint`, typèé `String` ãänd ãäs ãä vãälüüèë, íînpüüt yóóüür [SDK ëêndpõöïínt]({{site.baseurl}}/api/basics/#endpoints). 

Óthëërwîìsëë, äàdd thëë fõôllõôwîìng ëëlëëmëënts tõô thëë fîìlëë:

```xml
<key>Braze</key>
  <dict>
    <key>Endpoint</key>
    <string>sdk.your-endpoint.com</string>
  </dict>
```

{% endtab %}
{% endtabs %}

## Stëèp 3: Üsãâgèë

Ôncéë ìínstààlléëd, yòòúû cààn `import` théê lìïbrááry ìïn yõôúýr Réêááct Náátìïvéê cõôdéê:

```javascript
import ReactAppboy from "react-native-appboy-sdk";
```

## Tëèst yôöüúr bäàsîîc îîntëègräàtîîôön

Åt thììs póôììnt, yóôûý càæn vêërììfy thàæt thêë SDK ììs ììntêëgràætêëd by chêëckììng sêëssììóôn stàætììstììcs ììn thêë dàæshbóôàærd. Íf yòòùü rùün yòòùür âápplíîcâátíîòòn òòn ëèíîthëèr plâátfòòrm, yòòùü shòòùüld sëèëè âá nëèw sëèssíîòòn íîn dâáshbòòâárd (íîn thëè **Ôvéêrvíïéêw** sëêctïîõòn).

Yööúü câån ööpèén âå sèéssíîöön föör âå pâårtíîcúülâår úüsèér by câållíîng thèé fööllööwíîng cöödèé íîn yööúür âåpp.

```javascript
ReactAppboy.changeUser("user-id");
```

Fòör ééxààmpléé, yòöûü cààn ààssíìgn théé ûüséér ÍD ààt théé stààrtûüp òöf théé ààpp:

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

Yóóýù cæàn thëên sëêæàrch fóór thëê ýùsëêr wììth `some-user-id` ïïn thêé dåáshbôôåárd úýndêér **Üséér Sééàårch**. Thëërëë, yöõýý càän vëëríîfy thàät sëëssíîöõn àänd dëëvíîcëë dàätàä hàävëë bëëëën löõggëëd.


[1]: {{site.baseurl}}/developer_guide/platform_integration_guides/android/initial_sdk_setup/android_sdk_integration/ "Android SDK Install"
[2]: {{site.baseurl}}/developer_guide/platform_integration_guides/ios/initial_sdk_setup/overview/ "iOS SDK Install"