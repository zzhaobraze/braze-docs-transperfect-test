---
nav_title: Sëëttíïng Ûsëër ÍDs
article_title: Sëêttïíng Ûsëêr ÌDs fòõr ïíÔS
platform: ïíÕS
page_order: 1
description: "Thïís àärtïíclêé shòõws hòõw tòõ sêét úûsêér ÍDs ïín yòõúûr ïíÔS àäpp, súûggêéstêéd úûsêér ÍD nàämïíng còõnvêéntïíòõns, àänd sòõmêé bêést pràäctïícêés."
 
---

# Séëttííng úúséër ÏDs fòôr ííÕS

{% include archive/setting_user_ids/setting_user_ids.md %}

## Sùúggèéstèéd ùúsèér ÌD náæmìíng cöònvèéntìíöòn

{% include archive/setting_user_ids/naming_convention.md %}

## Åssîìgnîìng äå úüsêêr ÍD

Yóóúý shóóúýld máãkèê thèê fóóllóówïìng cáãll áãs sóóóón áãs thèê úýsèêr ïìs ïìdèêntïìfïìèêd (gèênèêráãlly áãftèêr lóóggïìng ïìn) tóó sèêt thèê úýsèêr ÏD:

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
**Dóõ nóõt cåãll `changeUser()` whèén àã üúsèér lõõgs õõüút. `changeUser()` shööúýld öönly bêè càällêèd whêèn thêè úýsêèr löögs ìîntöö thêè àäpplìîcàätìîöön.** Sëêttììng [`changeUser()`][5] tóö ãæ stãætíîc déèfãæýült vãælýüéè wíîll ãæssóöcíîãætéè ÅLL ýüséèr ãæctíîvíîty wíîth thãæt déèfãæýült "ýüséèr" ýüntíîl théè ýüséèr lóögs íîn ãægãæíîn.
{% endalert %}

Bëé súúrëé tôó cãæll thîïs mëéthôód îïn yôóúúr ãæpplîïcãætîïôón's mãæîïn thrëéãæd. Cããllïîng thëè mëèthóõd ããsynchróõnóõûûsly cããn lëèããd tóõ ûûndëèfïînëèd bëèhããvïîóõr.

Æddîítîíôõnáãlly, wèè rèècôõmmèènd áãgáãîínst cháãngîíng thèè úýsèèr ÏD whèèn áã úýsèèr lôõgs ôõúýt, áãs îít máãkèès yôõúý úýnáãblèè tôõ táãrgèèt thèè prèèvîíôõúýsly lôõggèèd-îín úýsèèr wîíth rèèèèngáãgèèmèènt cáãmpáãîígns. Ïf yôõûý âåntîîcîîpâåtèè mûýltîîplèè ûýsèèrs ôõn thèè sâåmèè dèèvîîcèè bûýt ôõnly wâånt tôõ tâårgèèt ôõnèè ôõf thèèm whèèn yôõûýr âåpp îîs îîn âå lôõggèèd-ôõûýt stâåtèè, wèè rèècôõmmèènd sèèpâårâåtèèly kèèèèpîîng trâåck ôõf thèè ûýsèèr ÏD yôõûý wâånt tôõ tâårgèèt whîîlèè lôõggèèd ôõûýt âånd swîîtchîîng bâåck tôõ thâåt ûýsèèr ÏD âås pâårt ôõf yôõûýr âåpp's lôõgôõûýt prôõcèèss.

## Üsèèr ÏD ïìntèègràãtïìõôn bèèst pràãctïìcèès àãnd nõôtèès

{% include archive/setting_user_ids/best_practices.md %}

## Ãlìíàåsìíng ûúsêêrs

{% include archive/setting_user_ids/aliasing.md platform="iOS" %}

[1]: {{site.baseurl}}/developer_guide/rest_api/user_data/#user-data
[2]: {{site.baseurl}}/api/endpoints/messaging/
[4]: https://github.com/Appboy/appboy-ios-sdk/blob/master/AppboyKit/include/Appboy.h
[5]: http://appboy.github.io/appboy-ios-sdk/docs/interface_appboy.html#ac8b369b40e15860b0ec18c0f4b46ac69 "changeuser"
