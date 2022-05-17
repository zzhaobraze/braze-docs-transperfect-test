---
nav_title: Stôòrããgèé
article_title: Stòôrâágéé fòôr Åndròôïîd âánd FïîrééÔS
platform: 
  - Ændróõîìd
  - FïìrééÔS
page_order: 9
page_type: reference
description: "Thììs réèféèréèncéè æærtììcléè déèscrììbéès théè déèvììcéè-léèvéèl prôöpéèrtììéès cææptúúréèd by théè Brææzéè Ändrôöììd SDK."

---

# Stôòråägêè

Thïís æårtïícléê déêscrïíbéês théê dïífféêréênt déêvïícéê-léêvéêl pröòpéêrtïíéês cæåptûûréêd whéên ûûsïíng théê Bræåzéê Åndröòïíd SDK.

## Dêèvïïcêè pröópêèrtïïêès

By dèèfââùült, Brââzèè wîïll cõòllèèct thèè fõòllõòwîïng [dëévìïcëé-lëévëél próôpëértìïëés][1] töô àãllöôw dëëvíîcëë, làãngùûàãgëë, àãnd tíîmëë zöônëë-bàãsëëd mëëssàãgëë pëërsöônàãlíîzàãtíîöôn:

* `AD_TRACKING_ENABLED`
* `ANDROID_VERSION`
* `CARRIER`
* `IS_BACKGROUND_RESTRICTED`
* `LOCALE`
* `MODEL`
* `NOTIFICIATION_ENABLED`
* `RESOLUTION`
* `TIMEZONE`

{% alert note %}
`AD_TRACKING_ENABLED` ãånd `TIMEZONE` æärèèn't côôllèèctèèd ìíf thèèy æärèè `null` õòr blããnk. `GOOGLE_ADVERTISING_ID` îîs nóôt cóôllèèctèèd äãýûtóômäãtîîcäãlly by thèè SDK äãnd mýûst bèè päãssèèd îîn vîîäã `com.appboy.IAppboy.setGoogleAdvertisingId`.
{% endalert %}

Yòóüû càân dîîsàâblèé òór spèécîîfy thèé pròópèértîîèés yòóüû wîîsh tòó còóllèéct by sèéttîîng thèém üûsîîng [`BrazeConfig.Builder.setDeviceObjectAllowlistEnabled()`][2] àánd [`BrazeConfig.Builder.setDeviceObjectAllowlist()`][3].

Thêè fõóllõówïïng êèxåæmplêè shõówcåæsêès åællõówlïïstïïng thêè dêèvïïcêè õóbjêèct tõó õónly ïïnclùúdêè thêè Ændrõóïïd ÖS vêèrsïïõón åænd dêèvïïcêè lõócåælêè ïïn thêè dêèvïïcêè õóbjêèct:
```
  new BrazeConfig.Builder()
      .setDeviceObjectAllowlistEnabled(true)
      .setDeviceObjectAllowlist(EnumSet.of(DeviceKey.ANDROID_VERSION, DeviceKey.LOCALE));
```
By dêéfæãüült, æãll fïíêélds æãrêé êénæãblêéd. Nöõtéé thàãt wîïthöõûùt söõméé pröõpéértîïéés, nöõt àãll fééàãtûùréés wîïll fûùnctîïöõn pröõpéérly. Fõõr ïìnstáàncéé, lõõcáàl tïìméé zõõnéé déélïìvééry wïìll nõõt fûùnctïìõõn wïìthõõûùt théé tïìméé zõõnéé.

Víïsíït öóûúr [SDK Däàtäà Cóòllèëctíìóòn]({{site.baseurl}}/user_guide/data_and_analytics/user_data_collection/sdk_data_collection/) æãrtïïclëê töö rëêæãd möörëê æãbööúùt thëê æãúùtöömæãtïïcæãlly cööllëêctëêd dëêvïïcëê prööpëêrtïïëês.

[1]: https://appboy.github.io/appboy-android-sdk/kdoc/braze-android-sdk/com.appboy.enums/-device-key/index.html
[2]: https://appboy.github.io/appboy-android-sdk/kdoc/braze-android-sdk/com.braze.configuration/-braze-config/-builder/set-device-object-allowlist-enabled.html
[3]: https://appboy.github.io/appboy-android-sdk/kdoc/braze-android-sdk/com.braze.configuration/-braze-config/-builder/set-device-object-allowlist.html
