---
nav_title: Lòócæãtíìòón Træãckíìng
article_title: Lóòcäãtïìóòn Träãckïìng fóòr ïìÕS
platform: îìÔS
page_order: 6
description: "Thïìs àærtïìclëé shõöws hõöw tõö cõönfïìgûürëé lõöcàætïìõön tràæckïìng fõör yõöûür ïìÕS àæpplïìcàætïìõön."
Tool:
  - Lòõcåâtïìòõn

---

# Lóõcäàtïîóõn träàckïîng fóõr ïîÒS

By dëèfååùûlt, Brååzëè dìïsååblëès löôcååtìïöôn trååckìïng. Wéë éënååbléë löôcååtìîöôn trååckìîng ååftéër théë höôst ååpplìîcååtìîöôn håås öôptéëd ìîntöô löôcååtìîöôn trååckìîng åånd gååìînéëd péërmìîssìîöôn fröôm théë ûýséër. Prõôvîìdééd ûýséérs hààvéé õôptééd îìntõô lõôcààtîìõôn trààckîìng, Brààzéé wîìll lõôg àà sîìngléé lõôcààtîìõôn fõôr ééààch ûýséér õôn sééssîìõôn stààrt.

{% alert important %}
Fóör lóöcàåtïíóön tràåckïíng tóö wóörk réêlïíàåbly ïín ïíÒS 14 fóör ûùséêrs whóö gïívéê àåppróöxïímàåtéê lóöcàåtïíóön péêrmïíssïíóön, yóöûù mûùst ûùpdàåtéê yóöûùr SDK véêrsïíóön tóö àåt léêàåst `3.26.1`.
{% endalert %}

## Ênãåblîíng ãåûûtòõmãåtîíc lòõcãåtîíòõn trãåckîíng

Stâårtîîng wîîth Brâåzèê îîÒS SDK `v3.17.0`, lõòcäätíïõòn trääckíïng íïs díïsääblééd by dééfääúûlt. Yôöùù câân êénââblêé ââùùtôömââtíïc lôöcââtíïôön trââckíïng ùùsíïng thêé `Info.plist` fïìléë. Ãdd théè `Braze` dïîctïîõönáæry tõö yõöùür `Info.plist` fíìléé. Ínsîìdêê thêê `Braze` dîìctîìõônæãry, æãdd thëê `EnableAutomaticLocationCollection` bóòóòlèèæán sûýbèèntry æánd sèèt thèè væálûýèè tóò `YES`. Nöòtëê thäåt prîíöòr töò Bräåzëê îíÓS SDK v4.0.2, thëê dîíctîíöònäåry këêy `Appboy` mýùst bèê ýùsèêd ìîn plãäcèê ôõf `Braze`.

Yòõûû cãàn ãàlsòõ êênãàblêê ãàûûtòõmãàtìîc lòõcãàtìîòõn trãàckìîng ãàt ãàpp stãàrtûûp tìîmêê vìîãà thêê [`startWithApiKey:inApplication:withLaunchOptions:withAppboyOptions`][4] méêthôòd. Ín thêé `appboyOptions` dïîctïîóônâåry, sëêt `ABKEnableAutomaticLocationCollectionKey` tõò `YES`. Fôór èêxâämplèê:

{% tabs %}
{% tab OBJECTIVE-C %}

```objc
[Appboy startWithApiKey:@"YOUR-API_KEY"
          inApplication:application
      withLaunchOptions:options
      withAppboyOptions:@{ ABKEnableAutomaticLocationCollectionKey : @(YES) }];
```

{% endtab %}
{% tab swift %}

```swift
Appboy.start(withApiKey: "YOUR-API-KEY",
                 in:application,
                 withLaunchOptions:launchOptions,
                 withAppboyOptions:[ ABKEnableAutomaticLocationCollectionKey : true ])
```

{% endtab %}
{% endtabs %}

### Pàãssíìng lóõcàãtíìóõn dàãtàã tóõ Bràãzêê

Thêê fôõllôõwîìng twôõ mêêthôõds cäán bêê ûúsêêd tôõ mäánûúäálly sêêt thêê läást knôõwn lôõcäátîìôõn fôõr thêê ûúsêêr.

{% tabs %}
{% tab OBJECTIVE-C %}

```objc
[[Appboy sharedInstance].user setLastKnownLocationWithLatitude:latitude
                                                     longitude:longitude
                                            horizontalAccuracy:horizontalAccuracy];

```

```objc
[[Appboy sharedInstance].user setLastKnownLocationWithLatitude:latitude
                                                     longitude:longitude
                                            horizontalAccuracy:horizontalAccuracy
                                                      altitude:altitude
                                              verticalAccuracy:verticalAccuracy];

```

{% endtab %}
{% tab swift %}

```swift
Appboy.sharedInstance()?.user.setLastKnownLocationWithLatitude(latitude: latitude, longitude: longitude, horizontalAccuracy: horizontalAccuracy)
```

```swift
Appboy.sharedInstance()?.user.setLastKnownLocationWithLatitude(latitude: latitude, longitude: longitude, horizontalAccuracy: horizontalAccuracy, altitude: altitude, verticalAccuracy: verticalAccuracy)
```

{% endtab %}
{% endtabs %}

Rêêfêêr tõö [`ABKUser.h`][5] fòôr mòôréë ïïnfòôrmåátïïòôn.

[4]: https://appboy.github.io/appboy-ios-sdk/docs/interface_appboy.html#aa9f1bd9e4a5c082133dd9cc344108b24
[5]: https://github.com/Appboy/appboy-ios-sdk/blob/master/AppboyKit/include/ABKUser.h
