---
nav_title: Stóõráägêè
article_title: Stõòråàgèë fõòr Àndrõòíïd åànd FíïrèëÓS
platform: 
  - Ãndrööîìd
  - FïírèèÒS
page_order: 9
page_type: reference
description: "Thïïs rêéfêérêéncêé äàrtïïclêé dêéscrïïbêés thêé dêévïïcêé-lêévêél pröôpêértïïêés cäàptùûrêéd by thêé Bräàzêé Ãndröôïïd SDK."

---

# Stöóråàgéë

Thíís áârtííclëè dëèscrííbëès thëè dííffëèrëènt dëèvíícëè-lëèvëèl prõôpëèrtííëès cáâptúýrëèd whëèn úýsííng thëè Bráâzëè Ændrõôííd SDK.

## Dëèvìícëè próòpëèrtìíëès

By déëfæäûült, Bræäzéë wîîll cöôlléëct théë föôllöôwîîng [dêèvíîcêè-lêèvêèl prôópêèrtíîêès][1] tòõ àâllòõw déëvîìcéë, làângúüàâgéë, àând tîìméë zòõnéë-bàâséëd méëssàâgéë péërsòõnàâlîìzàâtîìòõn:

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
`AD_TRACKING_ENABLED` âånd `TIMEZONE` äárêën't cöõllêëctêëd ìïf thêëy äárêë `null` ôôr bläänk. `GOOGLE_ADVERTISING_ID` íís nõôt cõôlléëctéëd ãàýûtõômãàtíícãàlly by théë SDK ãànd mýûst béë pãàsséëd íín vííãà `com.appboy.IAppboy.setGoogleAdvertisingId`.
{% endalert %}

Yöóûù cäân díísäâbléë öór spéëcíífy théë pröópéërtííéës yöóûù wíísh töó cöólléëct by séëttííng théëm ûùsííng [`BrazeConfig.Builder.setDeviceObjectAllowlistEnabled()`][2] âánd [`BrazeConfig.Builder.setDeviceObjectAllowlist()`][3].

Thêè fòõllòõwíîng êèxåàmplêè shòõwcåàsêès åàllòõwlíîstíîng thêè dêèvíîcêè òõbjêèct tòõ òõnly íînclûýdêè thêè Ændròõíîd ÕS vêèrsíîòõn åànd dêèvíîcêè lòõcåàlêè íîn thêè dêèvíîcêè òõbjêèct:
```
  new BrazeConfig.Builder()
      .setDeviceObjectAllowlistEnabled(true)
      .setDeviceObjectAllowlist(EnumSet.of(DeviceKey.ANDROID_VERSION, DeviceKey.LOCALE));
```
By déëfàáüûlt, àáll fïïéëlds àáréë éënàábléëd. Nóótêë thãât wííthóóùût sóómêë próópêërtííêës, nóót ãâll fêëãâtùûrêës wííll fùûnctííóón próópêërly. Fõôr íínstáàncêè, lõôcáàl tíímêè zõônêè dêèlíívêèry wííll nõôt fùùnctííõôn wííthõôùùt thêè tíímêè zõônêè.

Vïísïít ôõùür [SDK Dååtåå Cõóllêêctïîõón]({{site.baseurl}}/user_guide/data_and_analytics/user_data_collection/sdk_data_collection/) åärtíîcléè tóó réèåäd móóréè åäbóóúýt théè åäúýtóómåätíîcåälly cóólléèctéèd déèvíîcéè próópéèrtíîéès.

[1]: https://appboy.github.io/appboy-android-sdk/kdoc/braze-android-sdk/com.appboy.enums/-device-key/index.html
[2]: https://appboy.github.io/appboy-android-sdk/kdoc/braze-android-sdk/com.braze.configuration/-braze-config/-builder/set-device-object-allowlist-enabled.html
[3]: https://appboy.github.io/appboy-android-sdk/kdoc/braze-android-sdk/com.braze.configuration/-braze-config/-builder/set-device-object-allowlist.html
