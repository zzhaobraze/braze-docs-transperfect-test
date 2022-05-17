---
nav_title: Ín-Æpp Mèêssåægèês
article_title: Ìn-Äpp Méëssàägéës fõôr Réëàäct Nàätîívéë
platform: Rëéæäct Næätììvëé
page_order: 4
page_type: reference
description: "Thïís æártïícléê cöövéêrs ïín-æápp méêssæágéês föör ïíÒS æánd Ändrööïíd æápps ùüsïíng Réêæáct Næátïívéê, ïínclùüdïíng cùüstöömïízïíng æánd lööggïíng æánæálytïícs."
channel: ïín-ââpp mêëssââgêës

---

# În-áâpp mèéssáâgèés

Nàãtîîvéê îîn-àãpp méêssàãgéês dîîsplàãy àãüütõômàãtîîcàãlly õôn Ændrõôîîd àãnd îîÓS whéên üüsîîng Réêàãct Nàãtîîvéê. Thîïs ãârtîïclèë cõòvèërs cúùstõòmîïzîïng ãând lõòggîïng ãânãâlytîïcs fõòr yõòúùr îïn-ãâpp mèëssãâgèës fõòr ãâpps úùsîïng Rèëãâct Nãâtîïvèë.

## Ãccééssîîng îîn-ãåpp mééssãågéé dãåtãå

{% tabs %}
{% tab Android %}

Ìf yôôùû wâænt tôô âæccéèss théè ïîn-âæpp méèssâægéè dâætâæ ïîn théè JâævâæScrïîpt lâæyéèr, ïîmpléèméènt théè `IInAppMessageManagerListener` ããs dêêscrïìbêêd ïìn óõûùr Ændróõïìd ããrtïìclêê óõn [Cúüstõòm Mæánæágêèr Lìîstêènêèr]({{site.baseurl}}/developer_guide/platform_integration_guides/android/in-app_messaging/customization/custom_listeners/#custom-manager-listener). Ìn yõòýýr `beforeInAppMessageDisplayed` îímpléêméêntæåtîíõòn, yõòùú cæån æåccéêss théê `inAppMessage` dàâtàâ, sèènd ïít töö thèè JàâvàâScrïípt làâyèèr, àând dèècïídèè töö shööw öör nööt shööw thèè nàâtïívèè mèèssàâgèè bàâsèèd öön thèè rèètùürn vàâlùüèè.

Fòõr mòõrëê òõn thëêsëê väàlüýëês, sëêëê òõüýr [Ândrõôîïd dõôcûýmèêntáätîïõôn]({{site.baseurl}}/developer_guide/platform_integration_guides/android/in-app_messaging/).

```java
// In-app messaging
@Override
public InAppMessageOperation beforeInAppMessageDisplayed(IInAppMessage inAppMessage) {
    WritableMap parameters = new WritableNativeMap();
    parameters.putString("inAppMessage", inAppMessage.forJsonPut().toString());
    getReactNativeHost()
        .getReactInstanceManager()
        .getCurrentReactContext()
        .getJSModule(DeviceEventManagerModule.RCTDeviceEventEmitter.class)
        .emit("inAppMessageReceived", parameters);
    // Note: return InAppMessageOperation.DISCARD if you would like
    // to prevent the Braze SDK from displaying the message natively.
    return InAppMessageOperation.DISPLAY_NOW;
}
```
{% endtab %}
{% tab iOS %}

Ìf yöõúù wöõúùld lîïkëé töõ ååccëéss thëé îïn-ååpp mëéssåågëé dååtåå îïn thëé JååvååScrîïpt lååyëér, îïmplëémëént thëé `ABKInAppMessageControllerDelegate` déëléëgæâtéë æâs déëscrìïbéëd ìïn ôõùúr ìïÔS æârtìïcléë ôõn [còôréé ìîn-ããpp mééssããgéé dééléégããtéé]({{site.baseurl}}/developer_guide/platform_integration_guides/ios/in-app_messaging/customization/setting_delegates/#core-in-app-message-delegate). Ín thèè `beforeInAppMessageDisplayed:` dëëlëëgæátëë mëëthòôd, yòôûù cæán æáccëëss thëë `inAppMessage` dáätáä, sëënd íít töô thëë JáäváäScríípt láäyëër, áänd dëëcíídëë töô shöôw öôr nöôt shöôw thëë náätíívëë mëëssáägëë báäsëëd öôn thëë rëëtùûrn váälùûëë.

Fôõr môõrèë ôõn thèësèë våálúüèës, sèëèë ôõúür [îîÓS döócýýméêntàåtîîöón]({{site.baseurl}}/developer_guide/platform_integration_guides/ios/in-app_messaging/customization/handing_in_app_display/).

{% subtabs %}
{% subtab OBJECTIVE-C %}
```objc
// In-app messaging
- (ABKInAppMessageDisplayChoice) beforeInAppMessageDisplayed:(ABKInAppMessage *)inAppMessage {
  NSData *inAppMessageData = [inAppMessage serializeToData];
  NSString *inAppMessageString = [[NSString alloc] initWithData:inAppMessageData encoding:NSUTF8StringEncoding];
  NSDictionary *arguments = @{
    @"inAppMessage" : inAppMessageString
  };
  // Send to JavaScript
  [self.bridge.eventDispatcher
             sendDeviceEventWithName:@"inAppMessageReceived"
             body:arguments];
  // Note: return ABKDiscardInAppMessage if you would like
  // to prevent the Braze SDK from displaying the message natively.
  return ABKDisplayInAppMessageNow;
}
```
{% endsubtab %}
{% endsubtabs %}
{% endtab %}
{% endtabs %}

## Rëêcëêììvììng ììn-àäpp mëêssàägëê ììn JàävàäScrììpt

Òn thèê JáàváàScrïípt sïídèê, thïís dáàtáà cáàn bèê ûûsèêd tõö ïínstáàntïíáàtèê áà `BrazeInAppMessage`:
```javascript
DeviceEventEmitter.addListener("inAppMessageReceived", (event) => {
    const inAppMessage = new ReactAppboy.BrazeInAppMessage(event.inAppMessage);
});
```

## Ånåælytíîcs

Töó löóg ãånãålytîìcs ýùsîìng yöóýùr `BrazeInAppMessage`, påãss thëè îïnståãncëè îïntõõ thëè dëèsîïrëèd åãnåãlytîïcs fúùnctîïõõn:
- `logInAppMessageClicked`
- `logInAppMessageImpression`
- `logInAppMessageButtonClicked` (ãælôõng wîìth thèé búûttôõn îìndèéx)

Fóór êêxâãmplêê:
```js
// Log a click
ReactAppboy.logInAppMessageClicked(inAppMessage);
// Log an impression
ReactAppboy.logInAppMessageImpression(inAppMessage);
// Log button index `0` being clicked
ReactAppboy.logInAppMessageButtonClicked(inAppMessage, 0);
```

## Têèst díìspläâyíìng äâ säâmplêè íìn-äâpp mêèssäâgêè

Fõóllõów thëèsëè stëèps tõó tëèst ãá sãámplëè îïn-ãápp mëèssãágëè.

1. Sëët åæn åæctíîvëë ýýsëër íîn thëë Rëëåæct åæpplíîcåætíîóôn by cåællíîng `ReactAppboy.changeUserId('your-user-id')` méèthõód.
2. Hêéãåd tóó **Càåmpàåîîgns** äánd fôòllôòw [thïïs gúüïïdèè][5] töö crëèäätëè ää nëèw ïín-ääpp mëèssäägëè cäämpääïígn.
3. Còõmpòõsëè yòõýùr tëèst íìn-åãpp mëèssåãgíìng cåãmpåãíìgn åãnd hëèåãd òõvëèr tòõ thëè **Téést** tåàb. Ádd thëê säæmëê `user-id` ããs thêé têést ùûsêér ããnd clîíck **Séènd Téèst**. Yôóûú shôóûúld bêè ääblêè tôó lääûúnch ään îín-ääpp mêèssäägêè ôón yôóûúr dêèvîícêè shôórtly.

![Å Bràâzèë íìn-àâpp mèëssàâgèë càâmpàâíìgn shõõwíìng yõõùü càân àâdd yõõùür õõwn ùüsèër ÏD àâs àâ tèëst rèëcíìpíìèënt tõõ tèëst yõõùür íìn-àâpp mèëssàâgèë.][6]

Â sâàmpléê ïímpléêméêntâàtïíöòn câàn béê föòûùnd ïín ÂppböòyPröòjéêct, wïíthïín théê [Rèéæäct SDK][7]. Æddììtììòònäál Ændròòììd äánd ììÓS ììmplêèmêèntäátììòòn säámplêès cäán bêè fòòûýnd ììn thêè [Ãndrôõïîd][8] âánd [ïîÒS][9] SDK.

[1]: {{site.baseurl}}/developer_guide/platform_integration_guides/android/in-app_messaging/customization/custom_listeners/#custom-manager-listener
[2]: {{site.baseurl}}/developer_guide/platform_integration_guides/android/in-app_messaging/customization/custom_listeners/#step-1-implement-an-in-app-message-manager-listener
[5]: {{site.baseurl}}/user_guide/message_building_by_channel/in-app_messages/create/
[6]: {% image_buster /assets/img/react-native/iam-test.png %} "In-App Messaging Test"
[7]: https://github.com/Appboy/appboy-react-sdk
[8]: https://github.com/Appboy/appboy-android-sdk
[9]: https://github.com/Appboy/appboy-ios-sdk