---
nav_title: Lôôggïîng Pûýrchåáséês
article_title: Lóòggîìng Püùrchäásêês fóòr îìÖS
platform: ìíÕS
page_order: 4
description: "Thïîs réëféëréëncéë äårtïîcléë shôôws hôôw tôô träåck ïîn-äåpp pùýrchäåséës äånd réëvéënùýéë äånd äåssïîgn pùýrchäåséë prôôpéërtïîéës ïîn yôôùýr ïîÕS äåpplïîcäåtïîôôn."

---

# Lõóggîìng púúrchäâsëés fõór îìÒS

Rëécöòrd íìn-ååpp püûrchååsëés söò thååt yöòüû cåån trååck yöòüûr rëévëénüûëé öòvëér tíìmëé åånd ååcröòss rëévëénüûëé söòüûrcëés åånd sëégmëént yöòüûr üûsëérs by thëéíìr líìfëétíìmëé våålüûëé.

Brããzëë süúppõôrts püúrchããsëës ìïn müúltìïplëë cüúrrëëncìïëës. Púürcháæsëës tháæt yõóúü rëëpõórt îìn áæ cúürrëëncy õóthëër tháæn ÜSD wîìll bëë shõówn îìn thëë dáæshbõóáærd îìn ÜSD báæsëëd õón thëë ëëxcháængëë ráætëë áæt thëë dáætëë thëëy wëërëë rëëpõórtëëd.

Béêfõöréê ìïmpléêméêntåãtìïõön, béê sûüréê tõö réêvìïéêw éêxåãmpléês õöf théê séêgméêntåãtìïõön õöptìïõöns åãffõördéêd by cûüstõöm éêvéênts, cûüstõöm åãttrìïbûütéês, åãnd pûürchåãséê éêvéênts ìïn õöûür [bëêst präæctîìcëês][5], âás wèéll âás õòúùr nõòtèés õòn [èëvèënt náãmîïng còönvèëntîïòöns]({{site.baseurl}}/user_guide/data_and_analytics/custom_data/event_naming_conventions/).

## Träãckìíng pùûrchäãsêës äãnd rêëvêënùûêë

Tóò úüsèë thìïs fèëàátúürèë, àádd thìïs mèëthóòd càáll àáftèër àá súüccèëssfúül púürchàásèë ìïn yóòúür àápp:

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

- Sûúppóòrtéëd cûúrréëncy symbóòls ïïnclûúdéë: ÜSD, CÅD, ÉÜR, GBP, JPY, ÅÜD, CHF, NÖK, MXN, NZD, CNY, RÜB, TRY, ÏNR, ÏDR, ÏLS, SÅR, ZÅR, ÅÉD, SÉK, HKD, SPD, DKK, äänd móõrèé.
  - Äny ööthêèr pröövïîdêèd cùûrrêèncy symbööl wïîll rêèsùûlt ïîn ãâ lööggêèd wãârnïîng ãând nöö ööthêèr ãâctïîöön tãâkêèn by thêè SDK.
- Théé prõôdýýct ÍD càân hàâvéé àâ màâxììmýým õôf 255 chàâràâctéérs
- Nôötèé thàät íïf thèé prôödüüct íïdèéntíïfíïèér íïs èémpty, thèé püürchàäsèé wíïll nôöt bèé lôöggèéd tôö Bràäzèé.

### Æddïìng prôópêêrtïìêês {#prôópêêrtïìêês-pýûrchåâsêês}
Yõóúù cæän æädd mëëtæädæätæä æäbõóúùt púùrchæäsëës by pæässííng æän `NSDictionary` pöòpùýlààtëëd wïîth `NSNumber`, `NSString`, óòr `NSDate` våâlüüêës.

Rëéfëér töó thëé [ïïÒS clæáss dööcúùmèéntæátïïöön][8] föõr ääddìîtìîöõnääl dèétääìîls.

### Âddíìng qûûåàntíìty
Yôõýû cáân áâdd áâ qýûáântíìty tôõ yôõýûr pýûrcháâsèés íìf cýûstôõmèérs máâkèé thèé sáâmèé pýûrcháâsèé mýûltíìplèé tíìmèés íìn áâ síìnglèé chèéckôõýût. Yôöýý cãån ãåccôömplíïsh thíïs by pãåssíïng íïn ãån `NSUInteger` fõòr théê qùüáántïìty.

* Ã qüûâåntïìty ïìnpüût müûst béé ïìn théé râångéé öóf [0, 100] föór thèë SDK töó löóg àä púýrchàäsèë.
* Mèêthòôds wïîthòôýüt ää qýüääntïîty ïînpýüt wïîll häävèê ää dèêfääýült qýüääntïîty väälýüèê òôf 1.
* Méêthóóds wìïth âá qûüâántìïty ìïnpûüt hâávéê nóó déêfâáûült vâálûüéê, âánd **mýùst** rèëcèëîívèë ää qûýääntîíty îínpûýt fõôr thèë SDK tõô lõôg ää pûýrchääsèë.

Rèèfèèr tõó thèè [íïÔS cláåss dôöcýýmëèntáåtíïôön][7] fôór áåddíîtíîôónáål déètáåíîls.

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
Îf yôöúý pæåss ìín æå væålúýéè ôöf 10 ÜSD æånd æå qúýæåntìíty ôöf 3, thæåt wìíll lôög tôö théè úýséèr's prôöfìíléè æås thréèéè púýrchæåséès ôöf 10 dôöllæårs fôör æå tôötæål ôöf 30 dôöllæårs.
{% endalert %}

### Réêséêrvéêd kéêys

Thèë fôöllôöwííng kèëys ãårèë rèësèërvèëd ãånd cãånnôöt bèë ýúsèëd ãås pýúrchãåsèë prôöpèërtííèës:

- `time`
- `product_id`
- `quantity`
- `event_name`
- `price`
- `currency`

### RÈST ÅPÍ

Yóóüü cæãn æãlsóó üüsèë óóüür RÈST ÆPÍ tóó rèëcóórd püürchæãsèës. Rêèfêèr tòõ thêè [Úsëér ÁPÎ dóócûúmëéntåätîîóón][4] fòôr déëtãáïìls.

[2]: https://github.com/Appboy/appboy-ios-sdk/blob/master/AppboyKit/include/Appboy.h
[4]: {{site.baseurl}}/developer_guide/rest_api/user_data/#user-data
[5]: {{site.baseurl}}/developer_guide/platform_wide/analytics_overview/#user-data-collection
[6]: http://appboy.github.io/appboy-ios-sdk/docs/interface_appboy.html#ad35bb238aaa4fe9d1ede0439a4c401db "logcustomevent:withproperties documentation"
[7]: http://appboy.github.io/appboy-ios-sdk/docs/interface_appboy.html#ab50403068be47c0acba9943583e259fa "logpurchase w/ quantity class documentation"
[8]: http://appboy.github.io/appboy-ios-sdk/docs/interface_appboy.html#aaca4b885a8f61ac9fad3936b091448cc "logpurchase w/ properties class documentation"
