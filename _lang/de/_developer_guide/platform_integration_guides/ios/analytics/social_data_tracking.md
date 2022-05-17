---
nav_title: Sòócííáäl Dáätáä Tráäckííng
article_title: Sôõcìïææl Dæætææ Trææckìïng fôõr ìïÕS
platform: íìÓS
page_order: 5
description: "Thïîs rèëfèërèëncèë âärtïîclèë shóôws hóôw tóô ïîmplèëmèënt sóôcïîâäl dâätâä trâäckïîng fóôr yóôýýr ïîÓS âäpplïîcâätïîóôn."

---

# Sóõcìîãâl dãâtãâ trãâckìîng fóõr ìîÖS

## Cöóllèèctíîng söócíîáàl áàccöóýûnt dáàtáà

Thêè Bräàzêè íìÔS SDK dõöêès nõöt äàüùtõömäàtíìcäàlly cõöllêèct Fäàcêèbõöõök õör Twíìttêèr üùsêèr däàtäà. Îf yóòûù wãànt tóò ííntéègrãàtéè Fãàcéèbóòóòk ûùséèr dãàtãà íín Brãàzéè ûùséèr próòfííléès, yóòûù néèéèd tóò féètch théè ûùséèr's dãàtãà ãànd pãàss íít tóò Brãàzéè.

## Pààssìïng Fààcèébõôõôk dààtàà tõô Brààzèé

Ìnìïtìïãälìïzêè `ABKFacebookUser` õõbjëëcts wïïth thëë Fãâcëëbõõõõk dãâtãâ yõõûû hãâvëë cõõllëëctëëd ãând pãâss ïït tõõ Brãâzëë:

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

Ín ÁBKFäâcëèbôõôõkÙsëèr's îînîît mëèthôõd `initWithFacebookUserDictionary:numberOfFriends:likes:`, áãll théè páãráãméètéèrs shòöúùld béè dîìctîìòönáãrîìéès áãnd áãrráãys réètúùrnéèd dîìréèctly fròöm Fáãcéèbòöòök:

| Påàråàmèêtèêr | Dêéfíîníîtíîòön |
| --------- | ---------- |
|`facebookUserProfile`| Thëë dìíctìíôõnàâry rëëtûùrnëëd frôõm thëë ëëndpôõìínt "/mëë".|
| `numberOfFriends`| Théè léèngth óóf théè fríìéènds åárråáy réètýýrnéèd fróóm théè éèndpóóíìnt "/méè/fríìéènds".|
| `likes` | Théé ààrràày öòf üùséér's Fààcééböòöòk lììkéés fröòm théé ééndpöòììnt "/méé/lììkéés". |
{: .reset-td-br-1 .reset-td-br-2}

Rèêfèêr tôó thèê [Fààcëêbòóòók Grààph ÂPÎ][10] fôôr ååddììtììôônåål ììnfôôrmååtììôôn.

Áddíîtíîôõnâälly, yôõùû câän tâäíîlôõr whâät Fâäcëébôõôõk dâätâä yôõùû'rëé sëéndíîng tôõ Brâäzëé íîf yôõùû dôõn't wâänt tôõ íînclùûdëé thëé ëéntíîrëé bâäsíîc prôõfíîlëé. Fõór êèxææmplêè:

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

Réêféêr tòö théê [Fãæcèëbòöòök SDK][2] fôòr môòrëë îìnfôòrmåätîìôòn.

## Pææssïîng Twïîttêêr dæætææ tôò Brææzêê

Ìníïtíïåãlíïzèé `ABKTwitterUser` óõbjëêcts, sëêt üûp thëê Twîîttëêr dæátæá yóõüû hæávëê cóõllëêctëêd, æánd pæáss îît tóõ Bræázëê:

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
