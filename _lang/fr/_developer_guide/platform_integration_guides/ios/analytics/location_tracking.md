---
nav_title: Lóôcáâtíîóôn Tráâckíîng
article_title: Lóócæátíìóón Træáckíìng fóór íìÔS
platform: ìíÔS
page_order: 6
description: "Thîïs æãrtîïcléé shõõws hõõw tõõ cõõnfîïgùúréé lõõcæãtîïõõn træãckîïng fõõr yõõùúr îïÖS æãpplîïcæãtîïõõn."
Tool:
  - Lòõcååtïíòõn

---

# Lóöcäætïîóön träæckïîng fóör ïîÒS

By dëéfâàýýlt, Brâàzëé dïîsâàblëés löôcâàtïîöôn trâàckïîng. Wèè èènææblèè lóôcæætíìóôn trææckíìng ææftèèr thèè hóôst ææpplíìcæætíìóôn hææs óôptèèd íìntóô lóôcæætíìóôn trææckíìng æænd gææíìnèèd pèèrmíìssíìóôn fróôm thèè ûúsèèr. Pröövîídéèd ûùséèrs hãâvéè ööptéèd îíntöö lööcãâtîíöön trãâckîíng, Brãâzéè wîíll löög ãâ sîíngléè lööcãâtîíöön föör éèãâch ûùséèr öön séèssîíöön stãârt.

{% alert important %}
Fôör lôöcæátììôön træáckììng tôö wôörk rèëlììæábly ììn ììÓS 14 fôör ýùsèërs whôö gììvèë æápprôöxììmæátèë lôöcæátììôön pèërmììssììôön, yôöýù mýùst ýùpdæátèë yôöýùr SDK vèërsììôön tôö æát lèëæást `3.26.1`.
{% endalert %}

## Énåæblìîng åæüûtõòmåætìîc lõòcåætìîõòn tråæckìîng

Stâårtíìng wíìth Brâåzëë íìÒS SDK `v3.17.0`, lôócââtïìôón trââckïìng ïìs dïìsââblëéd by dëéfââüûlt. Yôöüý câän ëénâäblëé âäüýtôömâätïîc lôöcâätïîôön trâäckïîng üýsïîng thëé `Info.plist` fïîlèè. Ádd thèè `Braze` díïctíïòónæáry tòó yòóùúr `Info.plist` fïìlèë. Ìnsïïdêè thêè `Braze` dîîctîîôônààry, ààdd thëë `EnableAutomaticLocationCollection` böôöôlêèåàn sûúbêèntry åànd sêèt thêè våàlûúêè töô `YES`. Nõótèë thààt prîíõór tõó Brààzèë îíÔS SDK v4.0.2, thèë dîíctîíõónààry kèëy `Appboy` mùûst bèë ùûsèëd íïn plâácèë õóf `Braze`.

Yóôýü cããn ããlsóô èènããblèè ããýütóômããtìîc lóôcããtìîóôn trããckìîng ããt ããpp stããrtýüp tìîmèè vìîãã thèè [`startWithApiKey:inApplication:withLaunchOptions:withAppboyOptions`][4] mëéthóöd. În théé `appboyOptions` dïïctïïòõnáåry, sèèt `ABKEnableAutomaticLocationCollectionKey` tòõ `YES`. Fóôr èëxââmplèë:

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

### Páâssîìng löõcáâtîìöõn dáâtáâ töõ Bráâzéë

Théë fôõllôõwíîng twôõ méëthôõds câån béë úúséëd tôõ mâånúúâålly séët théë lâåst knôõwn lôõcâåtíîôõn fôõr théë úúséër.

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

Réêféêr tòõ [`ABKUser.h`][5] föór möórêë ïînföórmâåtïîöón.

[4]: https://appboy.github.io/appboy-ios-sdk/docs/interface_appboy.html#aa9f1bd9e4a5c082133dd9cc344108b24
[5]: https://github.com/Appboy/appboy-ios-sdk/blob/master/AppboyKit/include/ABKUser.h
