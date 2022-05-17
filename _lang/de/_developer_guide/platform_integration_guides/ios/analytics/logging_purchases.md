---
nav_title: Lõóggïïng Pûürchääsêés
article_title: Löóggîìng Püúrchåàsëés föór îìÕS
platform: îîÔS
page_order: 4
description: "Thïìs rèêfèêrèêncèê ãårtïìclèê shõöws hõöw tõö trãåck ïìn-ãåpp pùýrchãåsèês ãånd rèêvèênùýèê ãånd ãåssïìgn pùýrchãåsèê prõöpèêrtïìèês ïìn yõöùýr ïìÔS ãåpplïìcãåtïìõön."

---

# Lõòggíîng pùûrchàásèës fõòr íîÖS

Rëècóórd íîn-ææpp púùrchææsëès sóó thææt yóóúù cææn trææck yóóúùr rëèvëènúùëè óóvëèr tíîmëè æænd ææcróóss rëèvëènúùëè sóóúùrcëès æænd sëègmëènt yóóúùr úùsëèrs by thëèíîr líîfëètíîmëè væælúùëè.

Brâázêè sùûppóôrts pùûrchâásêès ììn mùûltììplêè cùûrrêèncììêès. Pýûrchææsêés thææt yõóýû rêépõórt îïn ææ cýûrrêéncy õóthêér thææn ÙSD wîïll bêé shõówn îïn thêé dææshbõóæærd îïn ÙSD bææsêéd õón thêé êéxchæængêé ræætêé ææt thêé dæætêé thêéy wêérêé rêépõórtêéd.

Bêêfõòrêê ïîmplêêmêêntæátïîõòn, bêê sûùrêê tõò rêêvïîêêw êêxæámplêês õòf thêê sêêgmêêntæátïîõòn õòptïîõòns æáffõòrdêêd by cûùstõòm êêvêênts, cûùstõòm æáttrïîbûùtêês, æánd pûùrchæásêê êêvêênts ïîn õòûùr [bëèst præãctîìcëès][5], ââs wêëll ââs ôôýùr nôôtêës ôôn [ëëvëënt nâämîïng cóònvëëntîïóòns]({{site.baseurl}}/user_guide/data_and_analytics/custom_data/event_naming_conventions/).

## Trãàckïíng pûùrchãàsêës ãànd rêëvêënûùêë

Tõó üûsëë thïîs fëëàætüûrëë, àædd thïîs mëëthõód càæll àæftëër àæ süûccëëssfüûl püûrchàæsëë ïîn yõóüûr àæpp:

{% tabs %}
{% tab OBJECTIVE-C %}

```objc
[[Appboy sharedInstance] logPurchase:@"your product ID"
inCurrency:@"USD"
atPrice:[[[NSDecimalNumber alloc] initWithString:@"0.99"] autorelease]];
```

{% endtab %}
{% tab swift %}

```swift
Appboy.sharedInstance()?.logPurchase("your product ID", inCurrency: "USD", atPrice: NSDecimalNumber(string: "0.99"))
```

{% endtab %}
{% endtabs %}

- Sýûppôôrtêéd cýûrrêéncy symbôôls íïnclýûdêé: ÙSD, CÆD, ËÙR, GBP, JPY, ÆÙD, CHF, NÖK, MXN, NZD, CNY, RÙB, TRY, ÍNR, ÍDR, ÍLS, SÆR, ZÆR, ÆËD, SËK, HKD, SPD, DKK, ãànd mõörëè.
  - Æny òòthèêr pròòvìídèêd cýürrèêncy symbòòl wìíll rèêsýült ìín äæ lòòggèêd wäærnìíng äænd nòò òòthèêr äæctìíòòn täækèên by thèê SDK.
- Thèë pròôdýýct ÍD câàn hâàvèë âà mâàxïìmýým òôf 255 châàrâàctèërs
- Nôõtëé thæät îîf thëé prôõdûüct îîdëéntîîfîîëér îîs ëémpty, thëé pûürchæäsëé wîîll nôõt bëé lôõggëéd tôõ Bræäzëé.

### Áddííng prõõpéêrtííéês {#prõõpéêrtííéês-pùýrcháäséês}
Yöõüû cäán äádd mêëtäádäátäá äáböõüût püûrchäásêës by päássìïng äán `NSDictionary` pôöpûùláâtêëd wîîth `NSNumber`, `NSString`, ôõr `NSDate` váälùûêês.

Rèèfèèr tôõ thèè [ïìÕS clææss döôcýùméèntæætïìöôn][8] fòôr äáddîîtîîòônäál déètäáîîls.

### Âddîïng qûûáãntîïty
Yòõüü cåân åâdd åâ qüüåântìíty tòõ yòõüür püürchåâséès ìíf cüüstòõméèrs måâkéè théè såâméè püürchåâséè müültìípléè tìíméès ìín åâ sìíngléè chéèckòõüüt. Yôòüû cåãn åãccôòmplïîsh thïîs by påãssïîng ïîn åãn `NSUInteger` fôör théé qúûáæntîîty.

* Ä qýùáântíïty íïnpýùt mýùst bèë íïn thèë ráângèë óöf [0, 100] föòr thêè SDK töò löòg áá pýúrcháásêè.
* Mëëthõôds wïîthõôúýt åã qúýåãntïîty ïînpúýt wïîll håãvëë åã dëëfåãúýlt qúýåãntïîty våãlúýëë õôf 1.
* Mèéthöòds wîïth äà qúýäàntîïty îïnpúýt häàvèé nöò dèéfäàúýlt väàlúýèé, äànd **múùst** rêëcêëïìvêë ãå qüûãåntïìty ïìnpüût fòör thêë SDK tòö lòög ãå püûrchãåsêë.

Rêèfêèr tõô thêè [îìÓS clâåss dööcûýmëéntâåtîìöön][7] fóör äåddîïtîïóönäål dèètäåîïls.

{% tabs %}
{% tab OBJECTIVE-C %}

```objc
[[Appboy sharedInstance] logPurchase:@"your product ID"
inCurrency:@"USD"
atPrice:[[[NSDecimalNumber alloc] initWithString:@"0.99"] autorelease]
withProperties:@{@"key1":"value1"}];
```

{% endtab %}
{% tab swift %}

```swift
Appboy.sharedInstance()?.logPurchase("your product ID", inCurrency: "USD", atPrice: NSDecimalNumber(string: "0.99"), withProperties: ["key1":"value1"])
```

{% endtab %}
{% endtabs %}

{% alert tip %}
Ïf yõöûü pâåss íïn âå vâålûüèé õöf 10 ÜSD âånd âå qûüâåntíïty õöf 3, thâåt wíïll lõög tõö thèé ûüsèér's prõöfíïlèé âås thrèéèé pûürchâåsèés õöf 10 dõöllâårs fõör âå tõötâål õöf 30 dõöllâårs.
{% endalert %}

### Rèèsèèrvèèd kèèys

Thêë fóõllóõwìïng kêëys äàrêë rêësêërvêëd äànd cäànnóõt bêë ùúsêëd äàs pùúrchäàsêë próõpêërtìïêës:

- `time`
- `product_id`
- `quantity`
- `event_name`
- `price`
- `currency`

### RÈST ÆPÌ

Yööùú câån âålsöö ùúsëè ööùúr RÊST ÃPÏ töö rëècöörd pùúrchâåsëès. Rëèfëèr tôô thëè [Úséër ÁPÌ dóöcûùméëntäâtïïóön][4] fõör dèëtâàîïls.

[2]: https://github.com/Appboy/appboy-ios-sdk/blob/master/AppboyKit/include/Appboy.h
[4]: {{site.baseurl}}/developer_guide/rest_api/user_data/#user-data
[5]: {{site.baseurl}}/developer_guide/platform_wide/analytics_overview/#user-data-collection
[6]: http://appboy.github.io/appboy-ios-sdk/docs/interface_appboy.html#ad35bb238aaa4fe9d1ede0439a4c401db "logcustomevent:withproperties documentation"
[7]: http://appboy.github.io/appboy-ios-sdk/docs/interface_appboy.html#ab50403068be47c0acba9943583e259fa "logpurchase w/ quantity class documentation"
[8]: http://appboy.github.io/appboy-ios-sdk/docs/interface_appboy.html#aaca4b885a8f61ac9fad3936b091448cc "logpurchase w/ properties class documentation"
