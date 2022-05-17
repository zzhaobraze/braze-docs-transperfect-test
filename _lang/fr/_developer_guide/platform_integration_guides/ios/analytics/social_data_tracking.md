---
nav_title: Sööcîïäål Däåtäå Träåckîïng
article_title: Sôòcíîåàl Dåàtåà Tråàckíîng fôòr íîÕS
platform: ìîÒS
page_order: 5
description: "Thîís rêèfêèrêèncêè âártîíclêè shõôws hõôw tõô îímplêèmêènt sõôcîíâál dâátâá trâáckîíng fõôr yõôúýr îíÒS âápplîícâátîíõôn."

---

# Sòôcíïåàl dåàtåà tråàckíïng fòôr íïÖS

## Cööllééctííng sööcííáâl áâccööûýnt dáâtáâ

Théê Bräâzéê ìïÔS SDK dóõéês nóõt äâüûtóõmäâtìïcäâlly cóõlléêct Fäâcéêbóõóõk óõr Twìïttéêr üûséêr däâtäâ. Íf yôõùù wàänt tôõ íîntéëgràätéë Fàäcéëbôõôõk ùùséër dàätàä íîn Bràäzéë ùùséër prôõfíîléës, yôõùù néëéëd tôõ féëtch théë ùùséër's dàätàä àänd pàäss íît tôõ Bràäzéë.

## Pæässìíng Fæäcêébõöõök dæätæä tõö Bræäzêé

Ínîîtîîãälîîzéè `ABKFacebookUser` ôòbjêëcts wîîth thêë Fääcêëbôòôòk däätää yôòúú häävêë côòllêëctêëd äänd pääss îît tôò Brääzêë:

{% tabs %}
{% tab OBJECTIVE-C %}

```objc
ABKFacebookUser *facebookUser = [[ABKFacebookUser alloc] initWithFacebookUserDictionary:self.facebookUserProfile numberOfFriends:self.numberOfFacebookFriends likes:self.facebookLikes];
[Appboy sharedInstance].user.facebookUser = facebookUser;
```

{% endtab %}
{% tab SWIFT %}

```swift
let facebookUser = ABKFacebookUser(facebookUserDictionary: facebookUserDictionary, numberOfFriends: numberOfFriends, likes: likes)
Appboy.sharedInstance()?.user.facebookUser = facebookUser
```

{% endtab %}
{% endtabs %}

În ÄBKFæåcèëbòòòòkÜsèër's ïïnïït mèëthòòd `initWithFacebookUserDictionary:numberOfFriends:likes:`, ääll thêê pääräämêêtêêrs shõóùùld bêê díïctíïõónääríïêês äänd äärrääys rêêtùùrnêêd díïrêêctly frõóm Fääcêêbõóõók:

| Páåráåmëètëèr | Déëfîînîîtîîôòn |
| --------- | ---------- |
|`facebookUserProfile`| Théê dïìctïìõönáåry réêtýûrnéêd frõöm théê éêndpõöïìnt "/méê".|
| `numberOfFriends`| Thëë lëëngth óòf thëë fríîëënds àãrràãy rëëtùùrnëëd fróòm thëë ëëndpóòíînt "/mëë/fríîëënds".|
| `likes` | Thêè âærrâæy ôôf ýùsêèr's Fâæcêèbôôôôk lìîkêès frôôm thêè êèndpôôìînt "/mêè/lìîkêès". |
{: .reset-td-br-1 .reset-td-br-2}

Réêféêr tóõ théê [Fáâcëëbôóôók Gráâph ÄPÎ][10] fõõr àâddìítìíõõnàâl ìínfõõrmàâtìíõõn.

Áddïïtïïõönäàlly, yõöüý cäàn täàïïlõör whäàt Fäàcèëbõöõök däàtäà yõöüý'rèë sèëndïïng tõö Bräàzèë ïïf yõöüý dõön't wäànt tõö ïïnclüýdèë thèë èëntïïrèë bäàsïïc prõöfïïlèë. Fôõr ééxããmpléé:

{% tabs %}
{% tab OBJECTIVE-C %}

```objc
ABKFacebookUser *facebookUser = [[ABKFacebookUser alloc] initWithFacebookUserDictionary:facebookUserPublicProfile numberOfFriends:-1 likes:nil];  
```

{% endtab %}
{% tab SWIFT %}

```swift
let facebookUser = ABKFacebookUser(facebookUserDictionary: facebookUserDictionary, numberOfFriends: -1, likes:nil)
```

{% endtab %}
{% endtabs %}

Rêéfêér töô thêé [Fàâcèêbõóõók SDK][2] fõór mõórêë ìînfõórmàätìîõón.

## Pààssíïng Twíïttèér dààtàà tòó Brààzèé

Ínìïtìïäãlìïzêé `ABKTwitterUser` ôôbjèêcts, sèêt ýúp thèê Twïíttèêr däætäæ yôôýú häævèê côôllèêctèêd, äænd päæss ïít tôô Bräæzèê:

{% tabs %}
{% tab OBJECTIVE-C %}

```objc
ABKTwitterUser *twitterUser = [[ABKTwitterUser alloc] init];
twitterUser.userDescription = self.userDescription;
twitterUser.twitterID = self.twitterID;
[Appboy sharedInstance].user.twitterUser = twitterUser;
```

{% endtab %}
{% tab SWIFT %}

```swift
let twitterUser = ABKTwitterUser()
twitterUser.userDescription = twitterDserDescription
twitterUser.twitterID = twitterID
Appboy.sharedInstance()?.user.twitterUser = twitterUser
```

{% endtab %}
{% endtabs %}

[2]: https://developers.facebook.com/docs/ios "facebook iOS sdk docs"
[10]: https://developers.facebook.com/docs/graph-api/reference/v4.0/user "facebook graph api docs"
