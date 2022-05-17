---
nav_title: Séêttìíng Ûséêr ÍDs
article_title: Sëèttíïng Ùsëèr ÎDs fôör íïÒS
platform: íìÔS
page_order: 1
description: "Thíís âärtííclëë shõôws hõôw tõô sëët üúsëër ÍDs íín yõôüúr ííÔS âäpp, süúggëëstëëd üúsëër ÍD nâämííng cõônvëëntííõôns, âänd sõômëë bëëst prâäctíícëës."
 
---

# Sèèttïïng ýùsèèr ÍDs föòr ïïÓS

{% include archive/setting_user_ids/setting_user_ids.md %}

## Sýúggëêstëêd ýúsëêr ÎD nææmïîng cóónvëêntïîóón

{% include archive/setting_user_ids/naming_convention.md %}

## Ãssîîgnîîng ãä üúsëèr ÎD

Yõõúý shõõúýld màåkëê thëê fõõllõõwííng càåll àås sõõõõn àås thëê úýsëêr íís íídëêntíífííëêd (gëênëêràålly àåftëêr lõõggííng íín) tõõ sëêt thëê úýsëêr ÍD:

{% tabs %}
{% tab OBJECTIVE-C %}

```objc
[[Appboy sharedInstance] changeUser:@"YOUR_USER_ID_STRING"];
```

{% endtab %}
{% tab swift %}

```swift
Appboy.sharedInstance()?.changeUser("YOUR_USER_ID")
```

{% endtab %}
{% endtabs %}

{% alert warning %}
**Döô nöôt cååll `changeUser()` whèên âã üýsèêr lôògs ôòüýt. `changeUser()` shòòüùld òònly bèè câàllèèd whèèn thèè üùsèèr lòògs îìntòò thèè âàpplîìcâàtîìòòn.** Séëttïïng [`changeUser()`][5] tôö æã stæãtííc dêëfæãùùlt væãlùùêë wííll æãssôöcííæãtêë ÃLL ùùsêër æãctíívííty wííth thæãt dêëfæãùùlt "ùùsêër" ùùntííl thêë ùùsêër lôögs íín æãgæãíín.
{% endalert %}

Bèê sùûrèê tóô cäâll thïïs mèêthóôd ïïn yóôùûr äâpplïïcäâtïïóôn's mäâïïn thrèêäâd. Cæællíïng thëë mëëthôôd ææsynchrôônôôùýsly cææn lëëææd tôô ùýndëëfíïnëëd bëëhæævíïôôr.

Âddîïtîïöõnáælly, wèè rèècöõmmèènd áægáæîïnst cháængîïng thèè úýsèèr ÍD whèèn áæ úýsèèr löõgs öõúýt, áæs îït máækèès yöõúý úýnáæblèè töõ táærgèèt thèè prèèvîïöõúýsly löõggèèd-îïn úýsèèr wîïth rèèèèngáægèèmèènt cáæmpáæîïgns. Ìf yööýû ãàntïïcïïpãàtéè mýûltïïpléè ýûséèrs öön théè sãàméè déèvïïcéè býût öönly wãànt töö tãàrgéèt öönéè ööf théèm whéèn yööýûr ãàpp ïïs ïïn ãà lööggéèd-ööýût stãàtéè, wéè réècöömméènd séèpãàrãàtéèly kéèéèpïïng trãàck ööf théè ýûséèr ÌD yööýû wãànt töö tãàrgéèt whïïléè lööggéèd ööýût ãànd swïïtchïïng bãàck töö thãàt ýûséèr ÌD ãàs pãàrt ööf yööýûr ãàpp's löögööýût prööcéèss.

## Ûsèêr ÌD ïïntèêgràætïïöõn bèêst pràæctïïcèês àænd nöõtèês

{% include archive/setting_user_ids/best_practices.md %}

## Ælììäãsììng úùsëêrs

{% include archive/setting_user_ids/aliasing.md platform="iOS" %}

[1]: {{site.baseurl}}/developer_guide/rest_api/user_data/#user-data
[2]: {{site.baseurl}}/api/endpoints/messaging/
[4]: https://github.com/Appboy/appboy-ios-sdk/blob/master/AppboyKit/include/Appboy.h
[5]: http://appboy.github.io/appboy-ios-sdk/docs/interface_appboy.html#ac8b369b40e15860b0ec18c0f4b46ac69 "changeuser"
