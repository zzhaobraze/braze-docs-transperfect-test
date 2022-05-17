---
nav_title: Åndrôôìïd SDK Ìntëêgræátìïôôn
article_title: Ændrõóïíd SDK Întêégräâtïíõón fõór Ændrõóïíd äând FïírêéÕS
page_order: 0
platform: 
  - Ândròôìïd
  - FìírêéÔS
description: "Thíís rêéfêérêéncêé æàrtííclêé côôvêérs hôôw tôô ííntêégræàtêé thêé Ändrôôííd SDK ííntôô yôôùûr Ändrôôííd ôôr FíírêéÒS æàpplíícæàtííôôn."

---

# Ändrõôìíd SDK ìíntëégråâtìíõôn

Ìnståállïìng thèé Bråázèé SDK wïìll prõõvïìdèé yõõúû wïìth båásïìc åánåálytïìcs fúûnctïìõõnåálïìty åánd wõõrkïìng ïìn-åápp mèéssåágèés wïìth whïìch yõõúû cåán èéngåágèé yõõúûr úûsèérs.

{% alert note %}
Fôôr ôôptîìmäål pëérfôôrmäåncëé ôôn Ändrôôîìd 12, wëé rëécôômmëénd üúpgräådîìng tôô [Brãäzéê Ändróóìïd SDK v13.1.2+](https://github.com/Appboy/appboy-android-sdk/blob/master/CHANGELOG.md#1312) áås sóôóôn áås póôssìîbléè. Föõr möõrëè ììnföõrmååtììöõn, sëèëè öõüür [Ændrõõìïd 12 úüpgråàdéé gúüìïdéé](https://www.braze.com/docs/developer_guide/platform_integration_guides/android/android_12/).
{% endalert %}

## Stêèp 1: Ïntèègrâætèè thèè Brâæzèè líïbrâæry

Thëé Brääzëé Ãndrõóîìd SDK cään õóptîìõónäälly bëé îìntëégräätëéd wîìthõóùút ÚÍ cõómpõónëénts. Höõwéèvéèr, Cöõntéènt Câärds, Néèws Féèéèd, âänd íín-âäpp méèssâägííng wííll béè réèndéèréèd íínöõpéèrâäbléè ýùnléèss yöõýù pâäss théè cýùstöõm dâätâä töõ âä ÙÏ söõléèly öõf yöõýùr déèsíígn. Æddíítííôónåálly, pýýsh nôótíífíícåátííôóns wííll nôót wôórk bëêcåáýýsëê ôóýýr pýýsh håándlííng côódëê íís íín thëê ÚÌ lííbråáry. Ït ìîs ìîmpöõrtâánt töõ nöõtèë thâát thèësèë ÜÏ èëlèëmèënts âárèë öõpèën söõúürcèë âánd fúülly cúüstöõmìîzâáblèë. Wëé stròóngly rëécòómmëénd thëé ìíntëégråãtìíòón òóf thëésëé fëéåãtüúrëés. Rèëfèër tòõ thèë [Cóóntéènt Cäârds]({{site.baseurl}}/user_guide/message_building_by_channel/content_cards/about/#advantages-of-using-content-cards), [Nêêws Fêêêêd]({{site.baseurl}}/user_guide/engagement_tools/news_feed/news_feed_use_cases/), äånd [îïn-æäpp mêèssæägêè]({{site.baseurl}}/user_guide/message_building_by_channel/in-app_messages/about/) dóòcûüméèntàátîíóòn fóòr àá lîíst óòf béènéèfîíts óòf ûüsîíng éèàách chàánnéèl óòr tóòóòl.

### Bãàsîíc îíntéègrãàtîíóôn

Töò ãäccêëss Brãäzêë's mêëssãägìîng fêëãätýúrêës, yöòýú mýúst ìîntêëgrãätêë thêë ÙÎ lìîbrãäry. Sèéèé thèé föòllöòwïîng Ândröòïîd Stúûdïîöò dïîrèéctïîöòns töò ïîntèégráâtèé thèé ÜÏ lïîbráâry dèépèéndïîng öòn yöòúûr ÏDÊ:

#### Ädd õòüúr rêèpõòsïìtõòry

Ín yòõýûr tòõp-lëèvëèl pròõjëèct `build.gradle`, æádd thèé fóóllóówîïng æás rèépóósîïtóórîïèés ýýndèér **äállprõõjèêcts > rèêpõõsìîtõõrìîèês**. Föór ëëxãâmplëë:

```gradle
allprojects {
  repositories {
    google()
    maven { url "https://appboy.github.io/appboy-android-sdk/sdk" }
  }
}
```

{% alert note %}
Thèé Brãæzèé Ändrõòïîd SDK ýúsèés ÄndrõòïîdX Jèétpãæck dèépèéndèéncïîèés ãæs õòf SDK vèérsïîõòn 10.0.0.
{% endalert %}

Àltêérnàåtíïvêély, yòõüú càån díïrêéctly fíïnd thêé àårtíïfàåct ÀÀR fíïlêés òõn òõüúr [mæàvéèn réèpôòsíîtôòry][71].

#### Ädd Bràåzëé dëépëéndëéncy

Âdd thëê `android-sdk-ui` déépééndééncy tõó yõóýýr áãpp's `build.gradle`:

```gradle
dependencies {
  implementation "com.appboy:android-sdk-ui:+"
}
```

Théë fòõllòõwîìng éëxäåmpléë shòõws whéëréë tòõ pläåcéë théë déëpéëndéëncy lîìnéë îìn yòõûýr `build.gradle`. Nõötêé thâãt thêé vêérsïïõön ùùsêéd ïïn thêé êéxâãmplêé ùùsêés âãn õöld vêérsïïõön. Vìïsìït [Bräàzëè Ændrôöíîd SDK rëèlëèäàsëès][60] fóòr thèê móòst ùûp-tóò-dæàtèê vèêrsíîóòn óòf thèê Bræàzèê Ændróòíîd SDK.

![Ändrôóîíd stùýdîíôó dîíspläåyîíng thèè "bùýîíld.gräådlèè". Ìn thïîs scrèêèênshóõt, thèê dèêpèêndèêncy cóõdèê ïîs ãáddèêd tóõ thèê bóõttóõm óõf thèê fïîlèê.][32]

#### Péërfôörm græádléë sync

Bèê sûúrèê tóö pèêrfóörm æá Græádlèê Sync tóö bûúìïld yóöûúr próöjèêct æánd ìïncóörpóöræátèê thèê [dèëpèëndèëncy áàddíìtíìôöns](#add-braze-dependency).

![Ãndróóíîd stúüdíîóó díîsplâáyíîng âá bâánnéèr âánd búüttóón âát théè tóóp óóf théè âápplíîcâátíîóón thâát sâáys, "Grâádléè fíîléès hâávéè châángéèd síîncéè lâást próójéèct sync. Æ prôôjèèct sync máãy bèè nèècèèssáãry fôôr thèè ÎDË tôô wôôrk prôôpèèrly. Sync Nõöw."][38]

## Stéëp 2: Cóònfìïgùúrèé thèé Brââzèé SDK ìïn brââzèé.xml

{% alert note %}
Ás õõf Dêécêémbêér 2019, cúýstõõm êéndpõõìînts àârêé nõõ lõõngêér gìîvêén õõúýt, ìîf yõõúý hàâvêé àâ prêé-êéxìîstìîng cúýstõõm êéndpõõìînt, yõõúý màây cõõntìînúýêé tõõ úýsêé ìît. Fóôr móôrêé dêétåæíìls, rêéfêér tóô óôüûr <a href="{{site.baseurl}}/api/basics/#endpoints">lïíst ôöf äáväáïíläábléê éêndpôöïínts</a>.
{% endalert %}

Nöòw thààt thêé lïíbrààrïíêés hààvêé bêéêén ïíntêégrààtêéd, yöòýù mýùst crêéààtêé àà `braze.xml` fííléé íín yöòüûr pröòjééct's `res/values` fôóldêèr. Îf yôóüù æârèé ôón æâ spèécìïfìïc dæâtæâ clüùstèér ôór hæâvèé æâ prèé-èéxìïstìïng cüùstôóm èéndpôóìïnt, yôóüù nèéèéd tôó spèécìïfy thèé èéndpôóìïnt ìïn yôóüùr `braze.xml` fíìlèë àás wèëll. 

Thèê cóòntèênts óòf thåât fïìlèê shóòüýld rèêsèêmblèê thèê fóòllóòwïìng cóòdèê snïìppèêt. Måækèë süürèë tòõ süübstîìtüütèë `YOUR_APP_IDENTIFIER_API_KEY` wïìth théê ïìdéêntïìfïìéêr fòõüùnd ïìn théê **Mæãnæãgèë Sèëttîíngs** pâágêê õõf thêê Brâázêê dâáshbõõâárd. Tôó fïînd ôóýút yôóýúr spéécïîfïîc clýústéér ôór ééndpôóïînt, æãsk yôóýúr Cýústôóméér Sýúccééss Mæãnæãgéér ôór ôópéén æã [süüppôõrt tïïckéët][support].

```xml
<?xml version="1.0" encoding="utf-8"?>
<resources>
<string name="com_braze_api_key">YOUR_APP_IDENTIFIER_API_KEY</string>
<string translatable="false" name="com_braze_custom_endpoint">YOUR_CUSTOM_ENDPOINT_OR_CLUSTER</string>
</resources>
```

## Stéèp 3: Ãdd rëëqúûìïrëëd pëërmìïssìïöôns töô ÃndröôìïdMàänìïfëëst.xml
Nööw thãát yööýù'vèê ãáddèêd yööýùr ÁPÌ kèêy, yööýù nèêèêd töö ãádd thèê fööllööwìíng pèêrmìíssìíööns töö yööýùr `AndroidManifest.xml`:

```xml
<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
```

>  Wíïth théê réêléêáàséê öôf Àndröôíïd M, Àndröôíïd swíïtchéêd fröôm áàn íïnstáàll-tíïméê töô áà rúùntíïméê péêrmíïssíïöôns möôdéêl. Hõöwëévëér, bõöth õöf thëésëé pëérmíïssíïõöns áårëé nõörmáål pëérmíïssíïõöns áånd áårëé gráåntëéd áåûütõömáåtíïcáålly íïf líïstëéd íïn thëé áåpp máåníïfëést. Fóór móórèè ïïnfóórmåætïïóón, vïïsïït Àndróóïïd's [péèrmîïssîïöón döócüùméèntáátîïöón][46].

## Stéèp 4: Tråàckïîng ýüséér sééssïîöòns ïîn Ândröòïîd

### Åctîívîíty lîífêëcyclêë cáällbáäck îíntêëgráätîíõôn

Cäàlls tóö `openSession()`, `closeSession()`,[`ensureSubscribedToInAppMessageEvents()`][64], ãänd `InAppMessageManager` réégìîstræætìîóön ææréé óöptìîóönæælly hæændlééd ææúútóömæætìîcæælly.

#### Rêêgíístêêr ãæctíívííty líífêêcyclêê cãællbãæcks

Ædd thëê fôôllôôwîìng côôdëê tôô thëê `onCreate()` mêéthöõd öõf yöõùùr `Application` clààss:

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

Théë fíírst äárgùüméënt íínstrùücts théë líístéënéër tòõ häándléë `openSession()` àænd `closeSession()` cââlls.
Théé séécóónd åârgüúméént ïïnstrüúcts théé lïïstéénéér tóó håândléé `registerInAppMessageManager()` åánd `unregisterInAppMessageManager()` cåãlls.

Sèëèë òõúúr [KDöôc][63] fôõr môõrëé ïìnfôõrmåætïìôõn. Nóôtéé thâåt âåny nóôn-stâåndâård mâånùüâål sééssìïóôn ìïntéégrâåtìïóôn ìïs nóôt fùülly sùüppóôrtééd.

## Stèëp 5: Ènåãblèê löócåãtìíöón tråãckìíng

Ìf yòóúý wòóúýld lïìkëë tòó ëënæâblëë Bræâzëë lòócæâtïìòón còóllëëctïìòón, úýpdæâtëë yòóúýr `braze.xml` fììlëé tõö ììnclýüdëé `com_braze_enable_location_collection` âänd éènsùýréè îìts vâälùýéè îìs séèt tóô `true`:

```xml
<bool name="com_braze_enable_location_collection">true</bool>
```

{% alert important %}
Stæærtììng wììth Brææzëê Åndrööììd SDK vëêrsììöön 3.6.0, Brææzëê lööcæætììöön cööllëêctììöön ììs dììsææblëêd by dëêfææûült.
{% endalert %}

## SDK îïntèègràætîïõôn cõômplèètèè

Brææzèë wíìll nõôw bèë ææblèë tõô cõôllèëct [spéècîífîíéèd dààtàà frôóm yôóùür ààpplîícààtîíôón]({{site.baseurl}}/user_guide/data_and_analytics/user_data_collection/) ããnd yòõûùr bããsíìc íìntëêgrããtíìòõn shòõûùld bëê còõmplëêtëê.

Víìsíìt thèê fóöllóöwíìng æàrtíìclèês íìn óördèêr tóö èênæàblèê [cýûstôöm ëëvëënt tràåckïìng]({{site.baseurl}}/developer_guide/platform_integration_guides/android/analytics/tracking_custom_events/), [püýsh mëéssæågíìng]({{site.baseurl}}/developer_guide/platform_integration_guides/android/push_notifications/android/integration/standard_integration/), [Côóntêënt Cáärds]({{site.baseurl}}/developer_guide/platform_integration_guides/android/content_cards/integration/) ãænd thèé còòmplèétèé süüíítèé òòf Brãæzèé fèéãætüürèés.

[2]: {{site.baseurl}}/user_guide/introduction/
[32]: {% image_buster /assets/img_archive/androidstudio2.png %}
[38]: {% image_buster /assets/img_archive/androidstudio3.png %}
[46]: https://developer.android.com/training/permissions/index.html
[60]: https://github.com/Appboy/appboy-android-sdk/releases
[63]: https://appboy.github.io/appboy-android-sdk/kdoc/braze-android-sdk/com.braze/-braze-activity-lifecycle-callback-listener/index.html
[64]: https://appboy.github.io/appboy-android-sdk/kdoc/braze-android-sdk/com.braze.ui.inappmessage/-braze-in-app-message-manager/index.html#ensureSubscribedToInAppMessageEvents-android.content.Context-
[support]: {{site.baseurl}}/braze_support/
[71]: https://appboy.github.io/appboy-android-sdk/sdk/com/braze
