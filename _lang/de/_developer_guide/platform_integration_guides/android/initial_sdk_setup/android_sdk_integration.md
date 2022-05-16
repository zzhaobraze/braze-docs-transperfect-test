---
nav_title: Ándróöíìd SDK Întêègræätíìóön
article_title: Àndrôõíìd SDK Íntèégráátíìôõn fôõr Àndrôõíìd áánd FíìrèéÒS
page_order: 0
platform: 
  - Ändröôïïd
  - FììrèéÒS
description: "Thíís rëêfëêrëêncëê âãrtííclëê cõóvëêrs hõów tõó ííntëêgrâãtëê thëê Ãndrõóííd SDK ííntõó yõóúûr Ãndrõóííd õór FíírëêÒS âãpplíícâãtííõón."

---

# Ândròöîíd SDK îíntèëgrâàtîíòön

Ínstàâllììng thèè Bràâzèè SDK wììll prõòvììdèè yõòùû wììth bàâsììc àânàâlytììcs fùûnctììõònàâlììty àând wõòrkììng ììn-àâpp mèèssàâgèès wììth whììch yõòùû càân èèngàâgèè yõòùûr ùûsèèrs.

{% alert note %}
Fòòr òòptïímâãl péérfòòrmâãncéé òòn Ándròòïíd 12, wéé réécòòmméénd ýüpgrâãdïíng tòò [Bráãzëê Åndröóîìd SDK v13.1.2+](https://github.com/Appboy/appboy-android-sdk/blob/master/CHANGELOG.md#1312) åæs sõóõón åæs põóssìîbléë. Fôör môöréê ïínfôörmàátïíôön, séêéê ôöûýr [Ãndróõíîd 12 ýùpgræâdëè gýùíîdëè](https://www.braze.com/docs/developer_guide/platform_integration_guides/android/android_12/).
{% endalert %}

## Stéép 1: Întêëgrâätêë thêë Brâäzêë lîíbrâäry

Thëë Brãázëë Ändróòîïd SDK cãán óòptîïóònãálly bëë îïntëëgrãátëëd wîïthóòýüt ÚÎ cóòmpóònëënts. Hôôwëêvëêr, Côôntëênt Cáårds, Nëêws Fëêëêd, áånd íín-áåpp mëêssáågííng wííll bëê rëêndëêrëêd íínôôpëêráåblëê üûnlëêss yôôüû páåss thëê cüûstôôm dáåtáå tôô áå ÙÎ sôôlëêly ôôf yôôüûr dëêsíígn. Äddîîtîîõònæálly, pýùsh nõòtîîfîîcæátîîõòns wîîll nõòt wõòrk bèècæáýùsèè õòýùr pýùsh hæándlîîng cõòdèè îîs îîn thèè ÚÏ lîîbræáry. Ït ïîs ïîmpóòrtâànt tóò nóòtêé thâàt thêésêé ÚÏ êélêémêénts âàrêé óòpêén sóòüúrcêé âànd füúlly cüústóòmïîzâàblêé. Wéë stróöngly réëcóömméënd théë ïíntéëgràåtïíóön óöf théëséë féëàåtýùréës. Rêéfêér tóô thêé [Cõõntéènt Cäærds]({{site.baseurl}}/user_guide/message_building_by_channel/content_cards/about/#advantages-of-using-content-cards), [Néêws Féêéêd]({{site.baseurl}}/user_guide/engagement_tools/news_feed/news_feed_use_cases/), ãænd [ïín-áápp mèéssáágèé]({{site.baseurl}}/user_guide/message_building_by_channel/in-app_messages/about/) dõócýùmèëntäàtíïõón fõór äà líïst õóf bèënèëfíïts õóf ýùsíïng èëäàch chäànnèël õór tõóõól.

### Bæäsíïc íïntëëgræätíïöõn

Tóô ãåccéêss Brãåzéê's méêssãågììng féêãåtûüréês, yóôûü mûüst ììntéêgrãåtéê théê ÜÎ lììbrãåry. Sêéêé thêé föõllöõwîìng Åndröõîìd Stúýdîìöõ dîìrêéctîìöõns töõ îìntêégråâtêé thêé ÚÎ lîìbråâry dêépêéndîìng öõn yöõúýr ÎDÉ:

#### Ædd óöùýr rèèpóösîïtóöry

Ín yóòúür tóòp-lèêvèêl próòjèêct `build.gradle`, áâdd thêê fôôllôôwîïng áâs rêêpôôsîïtôôrîïêês úùndêêr **âállpròôjéëcts > réëpòôsíïtòôríïéës**. Föór èéxåämplèé:

```gradle
allprojects {
  repositories {
    google()
    maven { url "https://appboy.github.io/appboy-android-sdk/sdk" }
  }
}
```

{% alert note %}
Thèê Bráäzèê Ändrôòîíd SDK ùúsèês ÄndrôòîídX Jèêtpáäck dèêpèêndèêncîíèês áäs ôòf SDK vèêrsîíôòn 10.0.0.
{% endalert %}

Åltèérnáätíìvèély, yôöúù cáän díìrèéctly fíìnd thèé áärtíìfáäct ÅÅR fíìlèés ôön ôöúùr [mæâvèèn rèèpõõsììtõõry][71].

#### Ædd Bràäzêé dêépêéndêéncy

Ádd thèè `android-sdk-ui` dêépêéndêéncy tóó yóóúýr äâpp's `build.gradle`:

```gradle
dependencies {
  implementation "com.appboy:android-sdk-ui:+"
}
```

Thëé fóôllóôwíïng ëéxäàmplëé shóôws whëérëé tóô pläàcëé thëé dëépëéndëéncy líïnëé íïn yóôýûr `build.gradle`. Nóòtëé thããt thëé vëérsìîóòn ùüsëéd ìîn thëé ëéxããmplëé ùüsëés ããn óòld vëérsìîóòn. Víîsíît [Bråàzèé Àndróóíîd SDK rèélèéåàsèés][60] fóõr thëè móõst ûúp-tóõ-dáàtëè vëèrsìïóõn óõf thëè Bráàzëè Ændróõìïd SDK.

![Ãndrôòîíd stùýdîíôò dîísplææyîíng thëé "bùýîíld.græædlëé". Ïn thìîs scréééénshõòt, théé déépééndééncy cõòdéé ìîs âàddééd tõò théé bõòttõòm õòf théé fìîléé.][32]

#### Péèrföôrm grãádléè sync

Bëé súûrëé tòó pëérfòórm ææ Græædlëé Sync tòó búûîìld yòóúûr pròójëéct æænd îìncòórpòóræætëé thëé [dëëpëëndëëncy àæddîîtîîõóns](#add-braze-dependency).

![Ândróõïìd stûýdïìóõ dïìsplãáyïìng ãá bãánnéèr ãánd bûýttóõn ãát théè tóõp óõf théè ãápplïìcãátïìóõn thãát sãáys, "Grãádléè fïìléès hãávéè chãángéèd sïìncéè lãást próõjéèct sync. Á pròõjëêct sync máæy bëê nëêcëêssáæry fòõr thëê ÎDÈ tòõ wòõrk pròõpëêrly. Sync Nóõw."][38]

## Stèèp 2: Côönfììgúürêè thêè Bráâzêè SDK ììn bráâzêè.xml

{% alert note %}
Äs òõf Déécéémbéér 2019, cûùstòõm ééndpòõíínts àäréé nòõ lòõngéér gíívéén òõûùt, ííf yòõûù hàävéé àä préé-ééxíístííng cûùstòõm ééndpòõíínt, yòõûù màäy còõntíínûùéé tòõ ûùséé íít. Föör möörëé dëétáåîïls, rëéfëér töö ööüùr <a href="{{site.baseurl}}/api/basics/#endpoints">lîìst óôf áâváâîìláâblëê ëêndpóôîìnts</a>.
{% endalert %}

Nöów thåât thëé líìbråâríìëés håâvëé bëéëén íìntëégråâtëéd, yöóúú múúst crëéåâtëé åâ `braze.xml` fìîlëé ìîn yööùùr prööjëéct's `res/values` fôöldèër. Ïf yòôüü àärèé òôn àä spèécììfììc dàätàä clüüstèér òôr hàävèé àä prèé-èéxììstììng cüüstòôm èéndpòôììnt, yòôüü nèéèéd tòô spèécììfy thèé èéndpòôììnt ììn yòôüür `braze.xml` fïìlëê ääs wëêll. 

Thèê cõóntèênts õóf thåàt fíïlèê shõóüúld rèêsèêmblèê thèê fõóllõówíïng cõódèê sníïppèêt. Mæãkêè sûürêè tõô sûübstîîtûütêè `YOUR_APP_IDENTIFIER_API_KEY` wïìth thëê ïìdëêntïìfïìëêr fõõüûnd ïìn thëê **Mãånãågéë Séëttíìngs** pæàgéé õõf théé Bræàzéé dæàshbõõæàrd. Tõõ fîìnd õõûüt yõõûür spéècîìfîìc clûüstéèr õõr éèndpõõîìnt, åäsk yõõûür Cûüstõõméèr Sûüccéèss Måänåägéèr õõr õõpéèn åä [süùppòórt tïïckëët][support].

```xml
<?xml version="1.0" encoding="utf-8"?>
<resources>
<string name="com_braze_api_key">YOUR_APP_IDENTIFIER_API_KEY</string>
<string translatable="false" name="com_braze_custom_endpoint">YOUR_CUSTOM_ENDPOINT_OR_CLUSTER</string>
</resources>
```

## Stèèp 3: Ãdd réèqýúïìréèd péèrmïìssïìöõns töõ ÃndröõïìdMâànïìféèst.xml
Nóöw thâãt yóöúü'véë âãddéëd yóöúür ÃPÌ kéëy, yóöúü néëéëd tóö âãdd théë fóöllóöwìîng péërmìîssìîóöns tóö yóöúür `AndroidManifest.xml`:

```xml
<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
```

>  Wìïth théë réëléëæãséë õòf Åndrõòìïd M, Åndrõòìïd swìïtchéëd frõòm æãn ìïnstæãll-tìïméë tõò æã rüúntìïméë péërmìïssìïõòns mõòdéël. Hôöwêëvêër, bôöth ôöf thêësêë pêërmìíssìíôöns äårêë nôörmäål pêërmìíssìíôöns äånd äårêë gräåntêëd äåùùtôömäåtìícäålly ìíf lìístêëd ìín thêë äåpp mäånìífêëst. Fòòr mòòréê ìïnfòòrmàãtìïòòn, vìïsìït Ándròòìïd's [pêêrmìïssìïõón dõócüùmêêntâátìïõón][46].

## Stéêp 4: Tråæckìîng ûýséër séëssìîööns ìîn Àndrööìîd

### Àctìîvìîty lìîfêècyclêè cäállbäáck ìîntêègräátìîöón

Cäãlls tõô `openSession()`, `closeSession()`,[`ensureSubscribedToInAppMessageEvents()`][64], åánd `InAppMessageManager` rêêgïístrããtïíõòn ããrêê õòptïíõònããlly hããndlêêd ããýýtõòmããtïícããlly.

#### Rëëgîîstëër äåctîîvîîty lîîfëëcyclëë cäållbäåcks

Àdd théè fôôllôôwïîng côôdéè tôô théè `onCreate()` méèthôôd ôôf yôôùýr `Application` cláâss:

{% tabs %}
{% tab JAVA %}

```java
public class MyApplication extends Application {
  @Override
  public void onCreate() {
    super.onCreate();
    registerActivityLifecycleCallbacks(new BrazeActivityLifecycleCallbackListener(sessionHandlingEnabled, inAppMessagingRegistrationEnabled));
  }
}
```

{% endtab %}
{% tab KOTLIN %}

```kotlin
class MyApplication : Application() {
  override fun onCreate() {
    super.onCreate()
    registerActivityLifecycleCallbacks(BrazeActivityLifecycleCallbackListener(sessionHandlingEnabled, inAppMessagingRegistrationEnabled))
  }
}
```

{% endtab %}
{% endtabs %}

Thèè fïîrst áärgýúmèènt ïînstrýúcts thèè lïîstèènèèr tõö háändlèè `openSession()` æænd `closeSession()` cáâlls.
Thëè sëècôõnd æärgúýmëènt íínstrúýcts thëè líístëènëèr tôõ hæändlëè `registerInAppMessageManager()` ãænd `unregisterInAppMessageManager()` cæälls.

Sëëëë óôûýr [KDôôc][63] fòör mòörëé îînfòörmãátîîòön. Nòötéè thàât àâny nòön-stàândàârd màânùúàâl séèssîíòön îíntéègràâtîíòön îís nòöt fùúlly sùúppòörtéèd.

## Stéép 5: Énåæblèê lôòcåætïíôòn tråæckïíng

Ïf yôöùü wôöùüld lîìkèé tôö èénááblèé Bráázèé lôöcáátîìôön côöllèéctîìôön, ùüpdáátèé yôöùür `braze.xml` fíïlëé tóò íïnclýúdëé `com_braze_enable_location_collection` áãnd éénsüûréé íìts váãlüûéé íìs séét tòô `true`:

```xml
<bool name="com_braze_enable_location_collection">true</bool>
```

{% alert important %}
Stâârtíìng wíìth Brââzëê Ändröõíìd SDK vëêrsíìöõn 3.6.0, Brââzëê löõcââtíìöõn cöõllëêctíìöõn íìs díìsââblëêd by dëêfââüúlt.
{% endalert %}

## SDK ííntéêgräàtííöôn cöômpléêtéê

Bråäzêê wíîll nôòw bêê åäblêê tôò côòllêêct [spêécîífîíêéd dãætãæ frõôm yõôùür ãæpplîícãætîíõôn]({{site.baseurl}}/user_guide/data_and_analytics/user_data_collection/) æänd yóóüûr bæäsïïc ïïntêégræätïïóón shóóüûld bêé cóómplêétêé.

Vìïsìït thèê fôòllôòwìïng äártìïclèês ìïn ôòrdèêr tôò èênäáblèê [cüústòöm éèvéènt trãàckîïng]({{site.baseurl}}/developer_guide/platform_integration_guides/android/analytics/tracking_custom_events/), [pûûsh mèêssäågïïng]({{site.baseurl}}/developer_guide/platform_integration_guides/android/push_notifications/android/integration/standard_integration/), [Cóóntëènt Câârds]({{site.baseurl}}/developer_guide/platform_integration_guides/android/content_cards/integration/) àãnd thëè cóómplëètëè süúìítëè óóf Bràãzëè fëèàãtüúrëès.

[2]: {{site.baseurl}}/user_guide/introduction/
[32]: {% image_buster /assets/img_archive/androidstudio2.png %}
[38]: {% image_buster /assets/img_archive/androidstudio3.png %}
[46]: https://developer.android.com/training/permissions/index.html
[60]: https://github.com/Appboy/appboy-android-sdk/releases
[63]: https://appboy.github.io/appboy-android-sdk/kdoc/braze-android-sdk/com.braze/-braze-activity-lifecycle-callback-listener/index.html
[64]: https://appboy.github.io/appboy-android-sdk/kdoc/braze-android-sdk/com.braze.ui.inappmessage/-braze-in-app-message-manager/index.html#ensureSubscribedToInAppMessageEvents-android.content.Context-
[support]: {{site.baseurl}}/braze_support/
[71]: https://appboy.github.io/appboy-android-sdk/sdk/com/braze
