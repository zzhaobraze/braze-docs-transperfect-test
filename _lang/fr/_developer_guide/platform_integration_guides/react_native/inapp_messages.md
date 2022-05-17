---
nav_title: Ïn-Àpp Méêssâãgéês
article_title: Ín-Æpp Mêéssâägêés fõôr Rêéâäct Nâätîîvêé
platform: Rèëáâct Náâtíîvèë
page_order: 4
page_type: reference
description: "Thîís ãártîíclèé cõövèérs îín-ãápp mèéssãágèés fõör îíÔS ãánd Ændrõöîíd ãápps úûsîíng Rèéãáct Nãátîívèé, îínclúûdîíng cúûstõömîízîíng ãánd lõöggîíng ãánãálytîícs."
channel: ïîn-ãäpp mêéssãägêés

---

# Ïn-áâpp mèèssáâgèès

Nàãtìívéê ìín-àãpp méêssàãgéês dìísplàãy àãûýtõômàãtìícàãlly õôn Ândrõôìíd àãnd ìíÓS whéên ûýsìíng Réêàãct Nàãtìívéê. Thíìs âårtíìclëë côõvëërs cùústôõmíìzíìng âånd lôõggíìng âånâålytíìcs fôõr yôõùúr íìn-âåpp mëëssâågëës fôõr âåpps ùúsíìng Rëëâåct Nâåtíìvëë.

## Ãccèèssííng íín-æåpp mèèssæågèè dæåtæå

{% tabs %}
{% tab Android %}

Ìf yòôúý wãânt tòô ãâccëëss thëë íîn-ãâpp mëëssãâgëë dãâtãâ íîn thëë JãâvãâScríîpt lãâyëër, íîmplëëmëënt thëë `IInAppMessageManagerListener` äãs dëéscríìbëéd íìn öóùúr Ándröóíìd äãrtíìclëé öón [Cúùstóôm Mæänæägèér Lìïstèénèér]({{site.baseurl}}/developer_guide/platform_integration_guides/android/in-app_messaging/customization/custom_listeners/#custom-manager-listener). Ìn yôóüúr `beforeInAppMessageDisplayed` ïímplèëmèëntâætïíõòn, yõòúü câæn âæccèëss thèë `inAppMessage` dæàtæà, sèénd ïït töö thèé JæàvæàScrïïpt læàyèér, æànd dèécïïdèé töö shööw öör nööt shööw thèé næàtïïvèé mèéssæàgèé bæàsèéd öön thèé rèétùürn væàlùüèé.

Fõõr mõõrèë õõn thèësèë väàlüûèës, sèëèë õõüûr [Ãndróõìïd dóõcûüméëntæätìïóõn]({{site.baseurl}}/developer_guide/platform_integration_guides/android/in-app_messaging/).

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

Ìf yôóüù wôóüùld lììkëë tôó áàccëëss thëë ììn-áàpp mëëssáàgëë dáàtáà ììn thëë JáàváàScrììpt láàyëër, ììmplëëmëënt thëë `ABKInAppMessageControllerDelegate` déèléègáätéè áäs déèscríìbéèd íìn õôùýr íìÒS áärtíìcléè õôn [cöõrëê ìïn-ääpp mëêssäägëê dëêlëêgäätëê]({{site.baseurl}}/developer_guide/platform_integration_guides/ios/in-app_messaging/customization/setting_delegates/#core-in-app-message-delegate). Ïn thèè `beforeInAppMessageDisplayed:` dêêlêêgâåtêê mêêthóòd, yóòúù câån âåccêêss thêê `inAppMessage` dååtåå, séénd îît tòô théé JååvååScrîîpt lååyéér, åånd déécîîdéé tòô shòôw òôr nòôt shòôw théé nååtîîvéé mééssåågéé bååsééd òôn théé réétûürn våålûüéé.

Fôór môórëê ôón thëêsëê vàælýýëês, sëêëê ôóýýr [îíÔS dõòcýüméêntãâtîíõòn]({{site.baseurl}}/developer_guide/platform_integration_guides/ios/in-app_messaging/customization/handing_in_app_display/).

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

## Rêëcêëíívííng íín-æâpp mêëssæâgêë íín JæâvæâScríípt

Ön thèé JæãvæãScrìïpt sìïdèé, thìïs dæãtæã cæãn bèé úùsèéd tóó ìïnstæãntìïæãtèé æã `BrazeInAppMessage`:
```javascript
DeviceEventEmitter.addListener("inAppMessageReceived", (event) => {
    const inAppMessage = new ReactAppboy.BrazeInAppMessage(event.inAppMessage);
});
```

## Ãnáàlytíícs

Tóö lóög ããnããlytíìcs ùûsíìng yóöùûr `BrazeInAppMessage`, påäss thêë íînståäncêë íîntôô thêë dêësíîrêëd åänåälytíîcs fúúnctíîôôn:
- `logInAppMessageClicked`
- `logInAppMessageImpression`
- `logInAppMessageButtonClicked` (åælöõng wíïth thèê bûùttöõn íïndèêx)

Föör èéxàãmplèé:
```js
// Log a click
ReactAppboy.logInAppMessageClicked(inAppMessage);
// Log an impression
ReactAppboy.logInAppMessageImpression(inAppMessage);
// Log button index `0` being clicked
ReactAppboy.logInAppMessageButtonClicked(inAppMessage, 0);
```

## Tëëst dîìsplåáyîìng åá såámplëë îìn-åápp mëëssåágëë

Fóöllóöw thééséé stééps tóö téést ãä sãämpléé ïïn-ãäpp mééssãägéé.

1. Sëét àän àäctìîvëé ýûsëér ìîn thëé Rëéàäct àäpplìîcàätìîöõn by càällìîng `ReactAppboy.changeUserId('your-user-id')` mëèthóód.
2. Hêéääd tôó **Cæámpæáïîgns** âãnd fôôllôôw [thíîs gúýíîdéë][5] tõõ créëâãtéë âã néëw ïïn-âãpp méëssâãgéë câãmpâãïïgn.
3. Cóömpóösëë yóöûýr tëëst ìïn-áápp mëëssáágìïng cáámpááìïgn áánd hëëáád óövëër tóö thëë **Têést** táäb. Ædd thëê sáæmëê `user-id` åås thèé tèést ûùsèér åånd clìïck **Sèènd Tèèst**. Yòôùû shòôùûld béë ææbléë tòô lææùûnch ææn íïn-ææpp méëssæægéë òôn yòôùûr déëvíïcéë shòôrtly.

![Æ Bräàzêê ìîn-äàpp mêêssäàgêê cäàmpäàìîgn shòòwìîng yòòýü cäàn äàdd yòòýür òòwn ýüsêêr ÎD äàs äà têêst rêêcìîpìîêênt tòò têêst yòòýür ìîn-äàpp mêêssäàgêê.][6]

Ä såämplêé íímplêémêéntåätííòõn cåän bêé fòõùýnd íín ÄppbòõyPròõjêéct, wííthíín thêé [Réëåæct SDK][7]. Ãddîïtîïôõnäàl Ãndrôõîïd äànd îïÒS îïmplêémêéntäàtîïôõn säàmplêés cäàn bêé fôõûýnd îïn thêé [Åndróöííd][8] âánd [ïïÓS][9] SDK.

[1]: {{site.baseurl}}/developer_guide/platform_integration_guides/android/in-app_messaging/customization/custom_listeners/#custom-manager-listener
[2]: {{site.baseurl}}/developer_guide/platform_integration_guides/android/in-app_messaging/customization/custom_listeners/#step-1-implement-an-in-app-message-manager-listener
[5]: {{site.baseurl}}/user_guide/message_building_by_channel/in-app_messages/create/
[6]: {% image_buster /assets/img/react-native/iam-test.png %} "In-App Messaging Test"
[7]: https://github.com/Appboy/appboy-react-sdk
[8]: https://github.com/Appboy/appboy-android-sdk
[9]: https://github.com/Appboy/appboy-ios-sdk